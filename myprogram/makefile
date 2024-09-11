# Makefile

protoc:
	cd proto && protoc --go_out=../protogen/golang --go_opt=paths=source_relative \
	./**/*.proto
	make protoc

# Makefile

# Variables para los plugins de Go
PROTOC_GEN_GO = protoc-gen-go
PROTOC_GEN_GO_GRPC = protoc-gen-go-grpc

# Directorios
PROTO_DIR = ./proto
OUT_DIR = ./protogen

# Regla para ejecutar el comando protoc
protoc:
	@echo "Generando código Go a partir de archivos .proto..."
	protoc -I=$(PROTO_DIR) --go_out=$(OUT_DIR) --go-grpc_out=$(OUT_DIR) $(PROTO_DIR)/*.proto
	@echo "Generación de código Protobuf completada."
