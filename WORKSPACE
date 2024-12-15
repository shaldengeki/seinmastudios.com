workspace(
    name = "com_github_shaldengeki_seinmastudios_com",
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_HUGO_COMMIT = "54fa9d05e93a5a28f835e297949c1f8544042ec1"
RULES_HUGO_SHA256 = "690fdb46a4baac5e1b817ff3de24c20da72573ea3cf331d30bc046ac99345e6e"

http_archive(
    name = "rules_hugo",
    url = "https://github.com/shaldengeki/rules_hugo/archive/%s.zip" % RULES_HUGO_COMMIT,
    sha256 = RULES_HUGO_SHA256,
    strip_prefix = "rules_hugo-%s" % RULES_HUGO_COMMIT
)

load("@rules_hugo//hugo:rules.bzl", "hugo_repository")

#
# Load hugo binary itself
#
# Optionally, load a specific version of Hugo, with the 'version' argument
hugo_repository(
    name = "hugo",
    version = "0.127.0",
    sha256 = "3cf961de9831c0f2ac0e67eabc83251916ae8729292fa85ffa140e59bcbea8c0",
)
