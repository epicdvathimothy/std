if [[ -n "${INPUT_GITHUB_ACCESS_TOKEN:-}" ]]; then
  add_config "access-tokens = github.com=$INPUT_GITHUB_ACCESS_TOKEN"
elif [[ -n "${GITHUB_TOKEN:-}" && $GITHUB_SERVER_URL == "https://github.com" ]]; then
  add_config "access-tokens = github.com=$GITHUB_TOKEN"
fi