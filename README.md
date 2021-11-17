# actions-terraform
GitHub Action for running Terraform

## Usage
```yaml
- uses: stordco/actions-terraform@v0.0
  with:
    command: apply
    tfe_token: ${{ secrets.TFE_TOKEN }}
```

### Inputs
- `args` - Terraform command arguments (optional)
- `command` - Terraform command (ie: apply, plan)
- `enable_init` - Init before running (use false for successive runs)
- `enable_setup` - Use hashicorp/setup-terraform
- `log` - Terraform detailed log level
- `tfe_token` - Terraform Cloud Token
- `version` - Terraform Version
- `workspace` - Terraform environment/workspace

### Outputs
- `exitcode` - Terraform command exit code
- `stderr` - Terraform output (STDERR)
- `stdout` - Terraform output (STDOUT)
