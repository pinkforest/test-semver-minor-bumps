# Minor SemVer Bumps

curve25519-dalek has 4.0 and 4.1

curve25519-dalek may bump MSRV SemVer-exempt as minor version bump

This means in order to control SemVer bumps manifest needs 

Using default resolver via workspace (that uses "2")

| Test    | Manifest                                   |
| :---    | :---                                       |
| bin_400 | `curve25519-dalek = { version = "4.0.0" }` |
| bin_410 | `curve25519-dalek = { version = "4.1.0" }` |


## dep_410

$ cargo tree
    Updating crates.io index
bin_curve_410 v4.1.0 (/home/foobar/code/version-test/dep_410)
└── curve25519-dalek v4.1.2
    ├── cfg-if v1.0.0
    ├── cpufeatures v0.2.12
    ├── curve25519-dalek-derive v0.1.1 (proc-macro)
    │   ├── proc-macro2 v1.0.79
    │   │   └── unicode-ident v1.0.12
    │   ├── quote v1.0.35
    │   │   └── proc-macro2 v1.0.79 (*)
    │   └── syn v2.0.52
    │       ├── proc-macro2 v1.0.79 (*)
    │       ├── quote v1.0.35 (*)
    │       └── unicode-ident v1.0.12
    ├── subtle v2.5.0
    └── zeroize v1.7.0
    [build-dependencies]
    ├── platforms v3.3.0
    └── rustc_version v0.4.0
        └── semver v1.0.22

## dep_400

$ cargo tree
bin_400 v4.0.0 (/home/foobar/code/version-test/dep_400)
└── curve25519-dalek v4.1.2
    ├── cfg-if v1.0.0
    ├── cpufeatures v0.2.12
    ├── curve25519-dalek-derive v0.1.1 (proc-macro)
    │   ├── proc-macro2 v1.0.79
    │   │   └── unicode-ident v1.0.12
    │   ├── quote v1.0.35
    │   │   └── proc-macro2 v1.0.79 (*)
    │   └── syn v2.0.52
    │       ├── proc-macro2 v1.0.79 (*)
    │       ├── quote v1.0.35 (*)
    │       └── unicode-ident v1.0.12
    ├── subtle v2.5.0
    └── zeroize v1.7.0
    [build-dependencies]
    ├── platforms v3.3.0
    └── rustc_version v0.4.0
        └── semver v1.0.22
