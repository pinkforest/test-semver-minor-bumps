# Minor SemVer Bumps

curve25519-dalek has 4.0 and 4.1

curve25519-dalek may bump MSRV SemVer-exempt as minor version bump

This means in order to control SemVer bumps is not possible w/o bounds

Someone  perhaps could think 4.0.0 restricts to >= 4.0.0, <= 4.1 ..

But this isn't the case ...

Using default resolver via workspace (that uses "2")

| Test    | Manifest                                   |
| :---    | :---                                       |
| dep_400 | `curve25519-dalek = { version = "4.0.0" }` |
| dep_410 | `curve25519-dalek = { version = "4.1.0" }` |
| dep_4   | `curve25519-dalek = { version = "4" }`     |
| dep_40  | `curve25519-dalek = { version = "4.0" }    |
| dep_41  | `curve25519-dalek = { version = "4.1" }    |

## dep_410 - Gets 4.1

"4.1.0" gets 4.1.LATEST
```
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
```

## dep_400 - Gets 4.1 :(

"4.0.0" gets 4.1.LATEST :(
```
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
```

## dep_4 - Gets 4.1

"4" gets 4.LATEST
```
$ cargo tree
bin_4 v4.0.0 (/home/foobar/code/version-test/dep_4)
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
```

## dep_40 - Gets 4.1 :(

"4.0" gets 4.1.LATEST
```
$ cargo tree
bin_curve_40 v4.1.0 (/home/foobar/code/version-test/dep_40)
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
```

## dep_41 - Gets 4.1

"4.1" gets 4.1.LATEST
```
$ cargo tree
bin_curve_41 v4.1.0 (/home/foobar/code/version-test/dep_41)
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
```