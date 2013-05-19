# CampBX-Ruby

## About
Provides a Ruby module to access the CampBX API.  For a full list of available API calls and their parameters, read the source, or see: [https://campbx.com/api.php](https://campbx.com/api.php).

## Usage
Each method returns a Hash with JSON data from the API. Requests are rate-limited to a maximum of once per 500ms.

### Initialize
  ```Ruby
  require 'campbx.rb'
  cbx = CampBX::API.new
  # Optionally CampBX::API.new('user','pass')
  # if you wish to use endpoints that require authentication
  ```
### Get Ticker Data
  ```Ruby
  cbx.xticker

  {"Last Trade"=>"117.70", "Best Bid"=>"117.54", "Best Ask"=>"117.70"}
  ```
### Check Account Data
  ```Ruby
  cbx.my_funds # Credentials provided upon initialization are included

  # will update w/test info once my API access is approved
  ```
### Send BTC
  ```Ruby
  cbx.send_btc( 'bitcoinaddresshere', 43.30 )

  ###
  ```
