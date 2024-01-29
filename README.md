# palestine
Palestine (Arabic: فلسطين, romanized: Filasṭīn[d]), officially the State of Palestine (دولة فلسطين, Dawlat Filasṭīn),[e] is a state in the Southern Levant region of West Asia. Founded on 15 November 1988 and officially governed by the Palestine Liberation Organization (PLO), it claims the West Bank (including East Jerusalem) and the Gaza Strip as its territory, all of which has been Israeli-occupied territories since the 1967 Six-Day War.[6][18] The West Bank contains 165 Palestinian enclaves that are under partial Palestinian rule, but the remainder, including 200 Israeli settlements, is under full Israeli control. The Gaza Strip was governed by Egypt but conquered by Israel in 1967. Israel governed the region until it withdrew in 2005; although it is still considered to occupy Gaza.[19][20][21] Hamas seized power after winning the 2006 Palestinian legislative election. The Gaza Strip has since been blockaded by Israel and Egypt.[c]

After World War II, in 1947, the United Nations (UN) adopted a Partition Plan for Mandatory Palestine, which recommended the creation of independent Arab and Jewish states and an internationalized Jerusalem.[30] Immediately after the United Nations General Assembly adopted the plan as Resolution 181, a civil war broke out in Palestine,[31] and the plan was not implemented.[32] The day after the establishment of the State of Israel on 14 May 1948,[33][34][35] neighboring Arab countries invaded the former British Mandate and engaged Israeli forces in the 1948 Arab–Israeli War.[36][37] Later, the All-Palestine Government was established by the Arab League on 22 September 1948 to govern the All-Palestine Protectorate in the Egyptian-occupied Gaza Strip. It was soon recognized by all Arab League members except Transjordan, which had occupied and later annexed the West Bank, including East Jerusalem. Palestine is currently recognized by 138 of the 193 United Nations (UN) member states. Though jurisdiction of the All-Palestine Government was declared to cover the whole of the former Mandatory Palestine, its effective jurisdiction was limited to the Gaza Strip.[38] During the Six-Day War in June 1967, Israel captured the Gaza Strip and the Sinai Peninsula from Egypt, the West Bank and East Jerusalem from Jordan, and the Golan Heights from Syria.

On 15 November 1988 in Algiers, Yasser Arafat, as Chairman of the PLO, issued the Palestinian Declaration of Independence, which established the State of Palestine. A year after the signing of the Oslo Accords in 1993, the Palestinian National Authority (PNA) was formed to govern (in varying degrees) areas A and B in the West Bank, comprising 165 enclaves, and the Gaza Strip. After Hamas became the PNA parliament's leading party in the most recent elections (2006), a conflict broke out between it and the Fatah party, leading to the Gaza Strip being taken over by Hamas in 2007 (two years after the Israeli disengagement).

The State of Palestine's mid-year population in 2021 was 5,227,193. Although Palestine claims Jerusalem as its capital, the city is under the control of Israel; both Palestinian and Israeli claims to the city are mostly unrecognized by the international community. Palestine is a member of the Arab League, the Organisation of Islamic Cooperation, the G77, the International Olympic Committee, as well as UNESCO, UNCTAD and the International Criminal Court.[39] Following a failed attempt in 2011 to secure full United Nations member state status, the United Nations General Assembly voted in 2012 to recognize Palestine as a non-member observer state.[40][41][42]

# build
```yaml
cargo build --release
```

# build on docker 🚀

```bash
docker build . -t palestine
docker run palestine
```

# kubernetes operator

```bash
helm repo add palestine https://palestine.github.io/helm-repo
helm install palestine/palestine-operator
```

## palestine cluster
```yaml
apiVersion: palestine.ps/v1
Kind: PalestineCluster
metadata:
  name: palestine-testing
spec:
  replicas: 3 # run redundant copies of palestine for HA
  forcedGore: true # forces users to watch gore on twitter

  xApi: # 𝕏 API keys to post the 𝕏emes
    secretName: x-api-key
    key: api_key
    
  leaderElection: true # NOT political leader, this is a raft cluster leader that runs the palestine program

  storageBackend: disk

  postgresql:
    endpoint: postgresql.postgresql.svc.cluster.local
    secret: idfk

  diskStorage: # store state on disk
    volumeClaimTemplate: # store palestine state on your hard drives today!
      storageClass: local-path # get your own storageclass
```
