# ACM SSL Swap for AWS ELB's

### Usage

```
usage: sslswappa.py [-h] [-r REGION] [-p PORT] -a ACCOUNT_NUMBER -c CERT_ID
                       -e ELB_NAME
sslswappa.py: error: argument -a/--account_number is required
```

### Setup

1. Clone this
1. Create a virtualenv `virtualenv sslswappa`
1. Activate the virtualenv: `source sslswappa/bin/activate`
1. Install the requirements: `pip install -r requirements.txt`
1. Run script with your parameters

### Params
- `-r` - Region ie us-west-2, us-east-1, etc.
- `-p` - Port number, defaults to `443`
- `-a` - [REQUIRED] AWS Account Number
- `-c` - [REQUIRED] ACM Certificate ID, Just the ID not the full ARN
- `-e` - [REQUIRED] ELB Name, the actual NAME not the FQDN

### Example

```
./sslswappa.py -r us-west-2 -a xxxxxxxxxxxx -c xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx -e my-elb-test
```

Success Output:

```
[O] Success! ELB: the-real-cphillips'-test-elb SSL Cert was Updated
```

Failure Output:

```
[x] Something went wrong, please check your values again
```
