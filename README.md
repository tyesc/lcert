# lcert
Automatic cp and Load new cert.pem to certificate trust store of applications using NSS

## Usage

```text
NAME

	lcert - load certificate

SYNOSIS

	lcert [OPTIONS]...

DESCRIPTION
	Automatic cp and Load new cert.pem to certificate trust store of applications using NSS

	-n	set name, with extention, of cert in /etc/ssl/certs/ , -n exemple.cert.pem

	-p (OPTIONAL)	set the path of the certificate to copy into /etc/ssl/certs/ , -p ./cert.pem

EXEMPLE
	lcert -n my-cert.pem
	> Do you want to load certificate in trust store of applications [y/n]? y
	> This process can take a long moment, please don't abort the task
	> Loaded !

	lcert -n my-cert.pem -p ./cert.pem
	> Do you want to copy ./cert.pem into /etc/ssl/certs/my-cert.pem [y/n]? y
	> ./cert.pem copied into /etc/ssl/certs/my-cert.pem
	> This process can take a long moment, please don't abort the task
	> Loaded !

```

## Requirement

```bash
$ apt install libnss3-tools
```
