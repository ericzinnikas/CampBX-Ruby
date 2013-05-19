# CampBX-Ruby

## About
Provides a Ruby module to access the CampBX API.

## Usage
### Initialize
  ```Ruby
  require 'campbx.rb'
  cbx = CampBX::API.new
  # Optionally CampBX::API.new('user','pass')
  # if you wish to use endpoints that require authentication
  ```
### Get Ticker Data
  Requests are rate-limited to a maximum of one per 500ms.
  ```Ruby
  cbx.xticker

  {"Last Trade"=>"117.70", "Best Bid"=>"117.54", "Best Ask"=>"117.70"}
  ```
### Check Account Data
  ```Ruby
  cbx.my_funds

  # will update w/test info once my API access is approved
  ```
