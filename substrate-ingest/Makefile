DB="postgres://postgres:postgres@localhost:29387/archive"


kusama:
	@node lib/main.js --out $(DB) \
		-e wss://kusama-rpc.polkadot.io \
		-c 10 \
		-e wss://kusama-rpc.dwellir.com \
		-c 10 \
		-e wss://kusama.api.onfinality.io/public-ws \
		-c 10 \
		--prom-port 0 \
		--write-batch-size 30 \
		--start-block 3876


moonriver:
	@node lib/main.js --out $(DB) \
		-e wss://moonriver.api.onfinality.io/public-ws \
		-e wss://moonriver-rpc.dwellir.com \
		-e wss://wss.api.moonriver.moonbeam.network/ \
		--write-batch-size 20 \
		--start-block 600000


moonbeam:
	@node lib/main.js --out $(DB) \
		-e wss://moonbeam.api.onfinality.io/public-ws \
		--write-batch-size 20 \
		--start-block 610238


karura:
	@node lib/main.js --out $(DB) \
		-e wss://karura.api.onfinality.io/public-ws \
		-e wss://karura-rpc.dwellir.com \
		-e wss://karura.polkawallet.io \
		--write-batch-size 20


astar:
	@node lib/main.js --out $(DB) \
		-e wss://astar.api.onfinality.io/public-ws \
		-e wss://astar-rpc.dwellir.com \
		--write-batch-size 20 \
		--start-block 214823


shibuya:
	@node lib/main.js --out $(DB) \
		-e wss://rpc.shibuya.astar.network/ \
		-e wss://shibuya-rpc.dwellir.com/ \
		--write-batch-size 20 \
		--start-block 816402


up:
	@docker-compose up -d


down:
	@docker-compose down


.PHONY: up down kusama moonriver moonbeam karura astar shibuya
