#![no_std]

use soroban_sdk::{contract, contractimpl, Env, Symbol, BytesN, Map};

#[contract]
pub struct ProofOfExistenceContract;

#[contractimpl]
impl ProofOfExistenceContract {

    // Store document hash with timestamp
    pub fn store_proof(env: Env, hash: BytesN<32>) {
        let timestamp = env.ledger().timestamp();
        env.storage().instance().set(&hash, &timestamp);
    }

    // Verify if proof exists
    pub fn verify_proof(env: Env, hash: BytesN<32>) -> bool {
        env.storage().instance().has(&hash)
    }

    // Get timestamp of stored proof
    pub fn get_proof(env: Env, hash: BytesN<32>) -> u64 {
        env.storage()
            .instance()
            .get(&hash)
            .unwrap_or(0)
    }
}
