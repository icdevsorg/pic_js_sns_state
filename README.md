# pic_js_sns_stateS

NNS subnet : 6hddd-nszlm-yb7u4-wqfxt-btk2p-w2jgp-emsaz-ree4f-cmeth-y3gko-gae

Requires: Pic.js beta 0.9.0-b0

npm install -D @hadronous/pic@beta

dfx 0.20.1

Unzip the state to a directory: ie  "pic/sns_state2/node-100/state";

In your Jest test , when setting up pic:

```
const NNS_STATE_PATH = "pic/sns_state2/node-100/state";

pic = await PocketIc.create(process.env.PIC_URL,{
      processingTimeoutMs: 30000,
      nns: {
        state: {
          type: SubnetStateType.FromPath,
          path: NNS_STATE_PATH,
          subnetId: Principal.fromText(NNS_SUBNET_ID),
          
        },
      },
      
    });

    

    await pic.setTime(new Date(2024, 7, 10, 17, 55,33).getTime()); //this is required to make sure that the state is moved after the time the state was created
    ```
    
    Here is the json with all the canister IDs:

    ```
[
  {
    "index": 0,
    "canister_ids": {
      "root_canister_id": "be2us-64aaa-aaaaa-qaabq-cai",
      "governance_canister_id": "br5f7-7uaaa-aaaaa-qaaca-cai",
      "index_canister_id": "by6od-j4aaa-aaaaa-qaadq-cai",
      "swap_canister_id": "b77ix-eeaaa-aaaaa-qaada-cai",
      "ledger_canister_id": "bw4dl-smaaa-aaaaa-qaacq-cai"
    },
    "list_sns_canisters": {
      "root": "be2us-64aaa-aaaaa-qaabq-cai",
      "swap": "b77ix-eeaaa-aaaaa-qaada-cai",
      "ledger": "bw4dl-smaaa-aaaaa-qaacq-cai",
      "index": "by6od-j4aaa-aaaaa-qaadq-cai",
      "governance": "br5f7-7uaaa-aaaaa-qaaca-cai",
      "dapps": [
        "bkyz2-fmaaa-aaaaa-qaaaq-cai"
      ],
      "archives": []
    },
    "meta": {
      "url": "https://forum.dfinity.org/thread-where-this-sns-is-discussed",
      "name": "Rock Out",
      "description": "A poem co-written with ChatGPT\nIn a realm of code, a beacon forth surges, a wondrous app on the Internet Computer emerges. Born of inspiration divine, This marvel of technology brilliantly shines.\nWith each line of code, a world takes flight, A symphony of bits, a chorus of bytes. Built on chainkey cryptography, secure and true, An app that transcends, all we once knew...\n",
      "logo": "/v1/sns/root/be2us-64aaa-aaaaa-qaabq-cai/logo.png"
    },
    "parameters": {
      "reserved_ids": [],
      "functions": [
        {
          "id": 0,
          "name": "All non-critical topics",
          "description": "Catch-all w.r.t to following for non-critical proposals.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 1,
          "name": "Motion",
          "description": "Side-effect-less proposals to set general governance direction.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 2,
          "name": "Manage nervous system parameters",
          "description": "Proposal to change the core parameters of SNS governance.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 3,
          "name": "Upgrade SNS controlled canister",
          "description": "Proposal to upgrade the wasm of an SNS controlled canister.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 4,
          "name": "Add nervous system function",
          "description": "Proposal to add a new, user-defined, nervous system function:a canister call which can then be executed by proposal.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 5,
          "name": "Remove nervous system function",
          "description": "Proposal to remove a user-defined nervous system function,which will be no longer executable by proposal.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 6,
          "name": "Execute nervous system function",
          "description": "Proposal to execute a user-defined nervous system function,previously added by an AddNervousSystemFunction proposal. A canister call will be made when executed.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 7,
          "name": "Upgrade SNS to next version",
          "description": "Proposal to upgrade the WASM of a core SNS canister.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 8,
          "name": "Manage SNS metadata",
          "description": "Proposal to change the metadata associated with an SNS.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 9,
          "name": "Transfer SNS treasury funds",
          "description": "Proposal to transfer funds from an SNS Governance controlled treasury account",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 10,
          "name": "Register dapp canisters",
          "description": "Proposal to register a dapp canister with the SNS.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 11,
          "name": "Deregister Dapp Canisters",
          "description": "Proposal to deregister a previously-registered dapp canister from the SNS.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 12,
          "name": "Mint SNS Tokens",
          "description": "Proposal to mint SNS tokens to a specified recipient.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 13,
          "name": "Manage ledger parameters",
          "description": "Proposal to change some parameters in the ledger canister.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        },
        {
          "id": 14,
          "name": "Manage dapp canister settings",
          "description": "Proposal to change canister settings for some dapp canisters.",
          "function_type": {
            "NativeNervousSystemFunction": {}
          }
        }
      ]
    },
    "nervous_system_parameters": {
      "default_followees": {
        "followees": []
      },
      "max_dissolve_delay_seconds": 252460800,
      "max_dissolve_delay_bonus_percentage": 100,
      "max_followees_per_function": 15,
      "neuron_claimer_permissions": {
        "permissions": [
          0,
          1,
          2,
          3,
          4,
          5,
          6,
          7,
          8,
          9,
          10
        ]
      },
      "neuron_minimum_stake_e8s": 100000000,
      "max_neuron_age_for_age_bonus": 126230400,
      "initial_voting_period_seconds": 345600,
      "neuron_minimum_dissolve_delay_to_vote_seconds": 2630016,
      "reject_cost_e8s": 100000000,
      "max_proposals_to_keep_per_action": 100,
      "wait_for_quiet_deadline_increase_seconds": 86400,
      "max_number_of_neurons": 200000,
      "transaction_fee_e8s": 10000,
      "max_number_of_proposals_with_ballots": 700,
      "max_age_bonus_percentage": 25,
      "neuron_grantable_permissions": {
        "permissions": [
          0,
          1,
          2,
          3,
          4,
          5,
          6,
          7,
          8,
          9,
          10
        ]
      },
      "voting_rewards_parameters": {
        "final_reward_rate_basis_points": 225,
        "initial_reward_rate_basis_points": 1000,
        "reward_rate_transition_duration_seconds": 378691200,
        "round_duration_seconds": 86400
      },
      "maturity_modulation_disabled": false,
      "max_number_of_principals_per_neuron": 5
    },
    "swap_state": {
      "swap": {
        "lifecycle": 3,
        "init": {
          "nns_proposal_id": 10,
          "sns_root_canister_id": "be2us-64aaa-aaaaa-qaabq-cai",
          "neurons_fund_participation": true,
          "min_participant_icp_e8s": 1000000000,
          "neuron_basket_construction_parameters": {
            "dissolve_delay_interval_seconds": 2630016,
            "count": 3
          },
          "fallback_controller_principal_ids": [
            "a5oei-rvrhg-x5qx4-whi3a-fwxqy-odwgo-c5jfi-26jx2-fauk5-gmw2u-zqe"
          ],
          "max_icp_e8s": null,
          "neuron_minimum_stake_e8s": 100000000,
          "confirmation_text": null,
          "swap_start_timestamp_seconds": 1720630327,
          "swap_due_timestamp_seconds": 1721325600,
          "min_participants": 57,
          "sns_token_e8s": 50000000000000,
          "nns_governance_canister_id": "rrkah-fqaaa-aaaaa-aaaaq-cai",
          "transaction_fee_e8s": 10000,
          "icp_ledger_canister_id": "ryjl3-tyaaa-aaaaa-aaaba-cai",
          "sns_ledger_canister_id": "bw4dl-smaaa-aaaaa-qaacq-cai",
          "neurons_fund_participation_constraints": {
            "coefficient_intervals": [
              {
                "slope_numerator": 0,
                "intercept_icp_e8s": 0,
                "from_direct_participation_icp_e8s": 0,
                "slope_denominator": 999999000000000,
                "to_direct_participation_icp_e8s": 7753935657521
              },
              {
                "slope_numerator": 900000000000000,
                "intercept_icp_e8s": 0,
                "from_direct_participation_icp_e8s": 7753935657521,
                "slope_denominator": 999999000000000,
                "to_direct_participation_icp_e8s": 8277217552429
              },
              {
                "slope_numerator": 990000000000000,
                "intercept_icp_e8s": 0,
                "from_direct_participation_icp_e8s": 8277217552429,
                "slope_denominator": 999999000000000,
                "to_direct_participation_icp_e8s": 9763040095110
              },
              {
                "slope_numerator": 999000000000000,
                "intercept_icp_e8s": 0,
                "from_direct_participation_icp_e8s": 9763040095110,
                "slope_denominator": 999999000000000,
                "to_direct_participation_icp_e8s": 13570070475945
              },
              {
                "slope_numerator": 99900000000000,
                "intercept_icp_e8s": 1000000000000,
                "from_direct_participation_icp_e8s": 13570070475945,
                "slope_denominator": 999999000000000,
                "to_direct_participation_icp_e8s": 22430266717481
              },
              {
                "slope_numerator": 9990000000000,
                "intercept_icp_e8s": 2000000000000,
                "from_direct_participation_icp_e8s": 22430266717481,
                "slope_denominator": 999999000000000,
                "to_direct_participation_icp_e8s": 18446744073709552000
              }
            ],
            "max_neurons_fund_participation_icp_e8s": 2716361827473,
            "min_direct_participation_threshold_icp_e8s": 10000000000000,
            "ideal_matched_participation_function": {
              "serialized_representation": "{\"t_1\":\"75000.0\",\"t_2\":\"225000.0\",\"t_3\":\"375000.0\",\"t_4\":\"1500000.00\",\"cap\":\"750000.0\"}"
            }
          },
          "neurons_fund_participants": null,
          "should_auto_finalize": true,
          "max_participant_icp_e8s": 1000000000000,
          "sns_governance_canister_id": "br5f7-7uaaa-aaaaa-qaaca-cai",
          "min_direct_participation_icp_e8s": 10000000000000,
          "restricted_countries": {
            "iso_codes": [
              "AQ"
            ]
          },
          "min_icp_e8s": null,
          "max_direct_participation_icp_e8s": 100000000000000
        },
        "params": {
          "min_participant_icp_e8s": 1000000000,
          "neuron_basket_construction_parameters": {
            "dissolve_delay_interval_seconds": 2630016,
            "count": 3
          },
          "max_icp_e8s": 102716361827473,
          "swap_due_timestamp_seconds": 1721325600,
          "min_participants": 57,
          "sns_token_e8s": 50000000000000,
          "sale_delay_seconds": null,
          "max_participant_icp_e8s": 1000000000000,
          "min_direct_participation_icp_e8s": 10000000000000,
          "min_icp_e8s": 10000000000000,
          "max_direct_participation_icp_e8s": 100000000000000
        },
        "open_sns_token_swap_proposal_id": 10,
        "decentralization_sale_open_timestamp_seconds": 1720630327
      },
      "derived": {
        "buyer_total_icp_e8s": 102716361827472,
        "sns_tokens_per_icp": 0.48677737
      }
    },
    "icrc1_metadata": [
      [
        "icrc1:logo",
        {
          "Text": "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAIAAAD8GO2jAAABhmlDQ1BJQ0MgcHJvZmlsZQAAKJF9kT1Iw0AYht+mSlUqDnYQcchQfwYLoiKOWoUiVAi1QqsOJpf+CE0akhQXR8G14ODPYtXBxVlXB1dBEPwBcXVxUnSREr9LCi1ivOO4h/e+9+XuO0ColZhmtY0Bmm6bqURczGRXxNArBHTSHMaIzCxjVpKS8B1f9wjw/S7Gs/zr/hzdas5iQEAknmGGaROvE09t2gbnfeIIK8oq8TnxqEkXJH7kuuLxG+eCywLPjJjp1BxxhFgstLDSwqxoasSTxFFV0ylfyHisct7irJUqrHFP/sJwTl9e4jqtASSwgEVIEKGggg2UYCNGu06KhRSdx338/a5fIpdCrg0wcsyjDA2y6wf/g9+9tfIT415SOA60vzjOxyAQ2gXqVcf5Pnac+gkQfAau9Ka/XAOmP0mvNrXoEdCzDVxcNzVlD7jcAfqeDNmUXSlIS8jngfcz+qYs0HsLdK16fWuc4/QBSFOvkjfAwSEwVKDsNZ93d7T27d+aRv9+AGjDcqPmD3ruAAAACXBIWXMAAC4jAAAuIwF4pT92AAAAB3RJTUUH5wIJCSgDC9hZ7wAAABl0RVh0Q29tbWVudABDcmVhdGVkIHdpdGggR0lNUFeBDhcAAAAoSURBVEjH7c1BAQAABAQw9O98SvDbCqyT1KepZwKBQCAQCAQCgeDKAsfxAz1FI3Q3AAAAAElFTkSuQmCC"
        }
      ],
      [
        "icrc1:decimals",
        {
          "Nat": [
            8
          ]
        }
      ],
      [
        "icrc1:name",
        {
          "Text": "Rock Out Token"
        }
      ],
      [
        "icrc1:symbol",
        {
          "Text": "ROT"
        }
      ],
      [
        "icrc1:fee",
        {
          "Nat": [
            10000
          ]
        }
      ],
      [
        "icrc1:max_memo_length",
        {
          "Nat": [
            32
          ]
        }
      ]
    ],
    "icrc1_fee": [
      10000
    ],
    "icrc1_total_supply": 250099996850000,
    "swap_params": {
      "params": {
        "min_participant_icp_e8s": 1000000000,
        "neuron_basket_construction_parameters": {
          "dissolve_delay_interval_seconds": 2630016,
          "count": 3
        },
        "max_icp_e8s": 102716361827473,
        "swap_due_timestamp_seconds": 1721325600,
        "min_participants": 57,
        "sns_token_e8s": 50000000000000,
        "sale_delay_seconds": null,
        "max_participant_icp_e8s": 1000000000000,
        "min_direct_participation_icp_e8s": 10000000000000,
        "min_icp_e8s": 10000000000000,
        "max_direct_participation_icp_e8s": 100000000000000
      }
    },
    "init": {
      "init": {
        "nns_proposal_id": 10,
        "sns_root_canister_id": "be2us-64aaa-aaaaa-qaabq-cai",
        "neurons_fund_participation": true,
        "min_participant_icp_e8s": 1000000000,
        "neuron_basket_construction_parameters": {
          "dissolve_delay_interval_seconds": 2630016,
          "count": 3
        },
        "fallback_controller_principal_ids": [
          "a5oei-rvrhg-x5qx4-whi3a-fwxqy-odwgo-c5jfi-26jx2-fauk5-gmw2u-zqe"
        ],
        "max_icp_e8s": null,
        "neuron_minimum_stake_e8s": 100000000,
        "confirmation_text": null,
        "swap_start_timestamp_seconds": 1720630327,
        "swap_due_timestamp_seconds": 1721325600,
        "min_participants": 57,
        "sns_token_e8s": 50000000000000,
        "nns_governance_canister_id": "rrkah-fqaaa-aaaaa-aaaaq-cai",
        "transaction_fee_e8s": 10000,
        "icp_ledger_canister_id": "ryjl3-tyaaa-aaaaa-aaaba-cai",
        "sns_ledger_canister_id": "bw4dl-smaaa-aaaaa-qaacq-cai",
        "neurons_fund_participation_constraints": {
          "coefficient_intervals": [
            {
              "slope_numerator": 0,
              "intercept_icp_e8s": 0,
              "from_direct_participation_icp_e8s": 0,
              "slope_denominator": 999999000000000,
              "to_direct_participation_icp_e8s": 7753935657521
            },
            {
              "slope_numerator": 900000000000000,
              "intercept_icp_e8s": 0,
              "from_direct_participation_icp_e8s": 7753935657521,
              "slope_denominator": 999999000000000,
              "to_direct_participation_icp_e8s": 8277217552429
            },
            {
              "slope_numerator": 990000000000000,
              "intercept_icp_e8s": 0,
              "from_direct_participation_icp_e8s": 8277217552429,
              "slope_denominator": 999999000000000,
              "to_direct_participation_icp_e8s": 9763040095110
            },
            {
              "slope_numerator": 999000000000000,
              "intercept_icp_e8s": 0,
              "from_direct_participation_icp_e8s": 9763040095110,
              "slope_denominator": 999999000000000,
              "to_direct_participation_icp_e8s": 13570070475945
            },
            {
              "slope_numerator": 99900000000000,
              "intercept_icp_e8s": 1000000000000,
              "from_direct_participation_icp_e8s": 13570070475945,
              "slope_denominator": 999999000000000,
              "to_direct_participation_icp_e8s": 22430266717481
            },
            {
              "slope_numerator": 9990000000000,
              "intercept_icp_e8s": 2000000000000,
              "from_direct_participation_icp_e8s": 22430266717481,
              "slope_denominator": 999999000000000,
              "to_direct_participation_icp_e8s": 18446744073709552000
            }
          ],
          "max_neurons_fund_participation_icp_e8s": 2716361827473,
          "min_direct_participation_threshold_icp_e8s": 10000000000000,
          "ideal_matched_participation_function": {
            "serialized_representation": "{\"t_1\":\"75000.0\",\"t_2\":\"225000.0\",\"t_3\":\"375000.0\",\"t_4\":\"1500000.00\",\"cap\":\"750000.0\"}"
          }
        },
        "neurons_fund_participants": null,
        "should_auto_finalize": true,
        "max_participant_icp_e8s": 1000000000000,
        "sns_governance_canister_id": "br5f7-7uaaa-aaaaa-qaaca-cai",
        "min_direct_participation_icp_e8s": 10000000000000,
        "restricted_countries": {
          "iso_codes": [
            "AQ"
          ]
        },
        "min_icp_e8s": null,
        "max_direct_participation_icp_e8s": 100000000000000
      }
    },
    "derived_state": {
      "sns_tokens_per_icp": 0.4867773652076721,
      "buyer_total_icp_e8s": 102716361827472,
      "cf_participant_count": 5,
      "neurons_fund_participation_icp_e8s": 2716361827472,
      "direct_participation_icp_e8s": 100000000000000,
      "direct_participant_count": 100,
      "cf_neuron_count": 5
    },
    "lifecycle": {
      "decentralization_sale_open_timestamp_seconds": 1720630327,
      "lifecycle": 3,
      "decentralization_swap_termination_timestamp_seconds": 1720631128
    }
  }
]
    ```




