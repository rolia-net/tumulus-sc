
### External function list

```
	function isInState(address owner, uint8 bit) returns(bool) {
	function getAuthorizationsByOwner(address owner) returns(Authorization[] memory _rtn) {
	function getAuthorizationsByViewer(address viewer) returns(Authorization[] memory _rtn) {
	function getAuthorizationsFromIds(uint40[] memory ids, uint8 status, bool onBit, uint8 bit) returns(Authorization[] memory _rtn) {
	function getAssetData(uint40 id, address owner) returns(bytes memory _rtn) {
	function getAuthorizedAssetData(uint40 id, address viewer) returns(bytes memory _rtn) {
	function getAgreementsByOwner(address owner) returns(Agreement[] memory _rtn) {
	function getAgreementsByAnnouncer(address announcer) returns(Agreement[] memory _rtn) {
	function getAgreementsFromIds(uint40[] memory ids) returns(Agreement[] memory _rtn) {
	function getStates(address owner) returns(State[] memory _rtn) {
	function saveAsset(uint40 id, address owner, uint32 sno, bytes calldata data) adm alive(owner) valid(id, owner, AS) external {
	function createAuthorization(address owner, address viewer, uint8 bit, uint40 assetId, uint32 sno) adm alive(owner) external {
	function requestAgreement(address owner, address announcer, uint8 bit, uint32 sno) adm alive(owner) external {
	function agreeAgreement(uint40 id, address announcer) adm valid(id, announcer, AG) external  {
	function rejectAgreement(uint40 id, address announcer) adm valid(id, announcer, AG) external  {
	function deleteAgreement(uint40 id, address owner) adm alive(owner) valid(id, owner, AG|OW) external  {
	function announce(uint40 id, address announcer) adm valid(id, announcer, AG) external  {
	function activateOwnerState(address owner, uint8 bit) internal {
	function setThreshold(address owner, uint8 bit, uint8 value) adm alive(owner) external  {
	function removeState(address owner, uint8 bit) adm alive(owner) external  {
	function removeAuthorization(uint40 id, address owner) adm alive(owner) valid(id, owner, AU|OW) external  {
	function burnNonce() external {
```

	function isInState(owner, bit)
	function getAuthorizationsByOwner(owner)
	function getAuthorizationsByViewer(viewer)
	function getAssetData(id, owner)
	function getAuthorizedAssetData(id, viewer)
	function getStates(owner)
	function createAuthorization(owner, viewer, bit, assetId, sno)

	function getAgreementsByOwner(owner)
	function getAgreementsByAnnouncer(announcer)
	function requestAgreement(owner, announcer, bit, sno)
	function agreeAgreement(id, announcer)
	function rejectAgreement(id, announcer)
	function deleteAgreement(id, owner)
	function announce(id, announcer)

	function activateOwnerState(owner, bit)
	function setThreshold(owner, bit, value)
	function removeState(owner, bit)
	function removeAuthorization(id, owner)
	function burnNonce()
