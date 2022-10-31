# import

1. Note: import resolution is stuck, try simplifying macro imports
   1. Description: 在`crago.toml` 里确实已经引入依赖，但在使用时依然标红报错
   2. Action required: `cargo.toml`里的依赖写在了`[dev-dependices]`下，将其移到`[dependices]`下即可解决



https://github.com/rust-lang/rust/issues/57966#issuecomment-1219732285