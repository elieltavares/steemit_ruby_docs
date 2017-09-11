```ruby
 api = Radiator::Api.new
```

- [get_block_header](https://github.com/elieltavares/radiator/wiki/Block-Api#get_block_header)
- [get_block](https://github.com/elieltavares/radiator/wiki/Block-Api#get_block)
- [get_ops_in_block](https://github.com/elieltavares/radiator/wiki/Block-Api#get_ops_in_block)
- [get_state](https://github.com/elieltavares/radiator/wiki/Block-Api#get_state)


## get_block_header
```ruby
response = api.get_block_header(block_num)
response = api.get_block_header(13921760)
```
 
## get_block
```ruby
response = api.get_block(block_num)
response = api.get_block(13921760)
```

## get_ops_in_block
```ruby
response = api.get_ops_in_block(block_num, 'onlyVirtual')
response = api.get_ops_in_block(13921760, 'false')
```

## get_state
```ruby
response = api.get_state("path")
response = api.get_state("/trends/funny")
```


```ruby
 api = Radiator::FollowApi.new
```

- [get_followers](https://github.com/elieltavares/radiator/wiki/Follower-API#get_followers)
- [get_following](https://github.com/elieltavares/radiator/wiki/Follower-API#get_following)
- [get_follow_count](https://github.com/elieltavares/radiator/wiki/Follower-API#get_follow_count)
- [get_feed_entries](https://github.com/elieltavares/radiator/wiki/Follower-API#get_feed_entries)
- [get_feed](https://github.com/elieltavares/radiator/wiki/Follower-API#get_feed-show-all-detail)
- [get_blog_entries](https://github.com/elieltavares/radiator/wiki/Follower-API#get_blog_entries-show-you-blog-feed)
- [get_blog](https://github.com/elieltavares/radiator/wiki/Follower-API#get_blog-show-you-blog-with-textimage)
- [get_account_reputations](https://github.com/elieltavares/radiator/wiki/Follower-API#get_account_reputations-get-all-account-with-same-name-and-reputation-thats-accounts-)
- [get_reblogged_by](https://github.com/elieltavares/radiator/wiki/Follower-API#get_reblogged_by)
- [get_blog_authors](https://github.com/elieltavares/radiator/wiki/Follower-API#get_blog_authors-get-all-authors-of-your-blog-reesteem-posting)

## get_followers
```ruby
response = api.get_followers("account", "startNumberFollower", "followType", "MaxNumberOfFollow")
response = api.get_followers("eliel", "0", "blog", "10")
response.result[0].follower
response.result[0].following
response.result[0].what[0]
```
               
## get_following
```ruby
response = api.get_following("account", "startFollowing", "followType", "limit")
response = api.get_following("eliel", "0", "blog", "10")
response.result[0].follower
response.result[0].following
response.result[0].what[0]
```

## get_follow_count
```ruby
response = api.get_follow_count("account")
response = api.get_follow_count("eliel")
response.result.account
response.result.follower_count
response.result.following_count
```

## get_feed_entries
```ruby
response = api.get_feed_entries("account", "entryId", "MaxPostShow")
response = api.get_feed_entries("eliel", "0", "7")
response.result[0].author
response.result[0].entry_id
response.result[0].permlink
response.result[0].reblog_on
```

## get_feed (Show all detail)
```ruby
response = api.get_feed("account", "entryId", "MaxPostShow")
response = api.get_feed("eliel", "0", "7")
response.result[0].comment
response.result[0].comment.abs_rshares
response.result[0].comment.active
response.result[0].comment.allow_curation_rewards
response.result[0].comment.allow_replies
response.result[0].comment.allow_votes
response.result[0].comment.author
response.result[0].comment.author_rewards
response.result[0].comment.beneficiaries
response.result[0].comment.body
response.result[0].comment.cashout_time
response.result[0].comment.category
response.result[0].comment.children
response.result[0].comment.children_abs_rshares
response.result[0].comment.created
response.result[0].comment.curator_payout_value 
response.result[0].comment.depth 
response.result[0].comment.id
response.result[0].comment.json_metadata
response.result[0].comment.last_payout
response.result[0].comment.last_update
response.result[0].comment.max_accepted_payout
response.result[0].comment.max_cashout_time
response.result[0].comment.net_rshares
response.result[0].comment.net_votes
response.result[0].comment.parent_author
response.result[0].comment.parent_permlink
response.result[0].comment.percent_steem_dollars
response.result[0].comment.permlink
response.result[0].comment.reward_weight
response.result[0].comment.root_comment
response.result[0].comment.title
response.result[0].comment.total_payout_value
response.result[0].comment.total_vote_weight
response.result[0].comment.vote_rshares
response.result[0].comment.entry_id
response.result[0].comment.reblog_by
response.result[0].comment.reblog_on
```

## get_blog_entries (Show you blog)
```ruby
response = api.get_blog_entries("account", "entryId", "MaxPostShow")
response = api.get_blog_entries("eliel", "15", "1")
response.result[0]
response.result[0].author
response.result[0].blog
response.result[0].entry_id
response.result[0].permlink
response.result[0].reblog_on
```

## get_blog (Show you blog with text,image...)
```ruby
response = api.get_blog_entries("account", "entryId", "MaxPostShow")
response = api.get_blog_entries("eliel", "15", "7")
response.result[0].author
response.result[0].blog
response.result[0].entry_id
response.result[0].permlink
response.result[0].reblog_on
```

## get_account_reputations (Get your account, and other too with same name and reputation thats accounts )
```ruby
response = api.get_account_reputations("account", "limit")
response = api.get_account_reputations("eliel", "1")
response.result[0].account
response.result[0].reputation
```

## get_reblogged_by
```ruby
response = api.get_reblogged_by("author", "permlink")
response = api.get_reblogged_by("teamsteem", "cooperation-is-humanity-s-greatest-asset")
response.result[0]
response.result[1]
```

## get_blog_authors (Get all reesteem)
```ruby
response = api.get_blog_authors("BlogAuthor")
response = api.get_blog_authors("eliel")
```



```ruby
api = Radiator::Api.new
```

```ruby
response = api.get_accounts(['name'])
response = api.get_accounts(['eliel'])
```


```ruby
 api = Radiator::Api.new
```

-  [get_config]()
-  [get_dynamic_global_properties]()
-  [get_chain_properties]()
-  [get_feed_history]()
-  [get_current_median_history_price]()
-  [get_witness_schedule]()
-  [get_hardfork_version]()
-  [get_next_scheduled_hardfork]()
-  [get_reward_fund]()

## get_config
```ruby
response = api.get_config
```

## get_dynamic_global_properties
```ruby
response = api.get_dynamic_global_properties
```

## get_chain_properties
```ruby
response = api.get_chain_properties
```

## get_feed_history
```ruby
response = api.get_feed_history
```

## get_current_median_history_price
```ruby
response = api.get_current_median_history_price
```

## get_witness_schedule
```ruby
response = api.get_witness_schedule
```

## get_hardfork_version
```ruby
response = api.get_hardfork_version
```

## get_next_scheduled_hardfork
```ruby
response = api.get_next_scheduled_hardfork
```

## get_reward_fund
```ruby
response = api.get_reward_fund(name)
response = api.get_reward_fund('post')
```


```ruby
api = Radiator::MarketHistoryApi.new
```
- [get_market_history](https://github.com/elieltavares/radiator/wiki/MarketHistory-Api#get_market_history-dont-work)
- [get_market_history_buckets](https://github.com/elieltavares/radiator/wiki/MarketHistory-Api#get_market_history_buckets)
- [get_order_book](https://github.com/elieltavares/radiator/wiki/MarketHistory-Api#get_order_book)
- [get_recent_trades](https://github.com/elieltavares/radiator/wiki/MarketHistory-Api#get_recent_trades-current_pays-date-open_pays)
- [get_ticker](https://github.com/elieltavares/radiator/wiki/MarketHistory-Api#get_ticker-highest_bid-latest-lowest_ask-sbd_volume-steem_volume)
- [get_trade_history](https://github.com/elieltavares/radiator/wiki/MarketHistory-Api#get_trade_history-dont-work)
- [get_volume](https://github.com/elieltavares/radiator/wiki/MarketHistory-Api#get_volume-last-24-hours-sbd_volume-steem_volume)

## get_market_history (Don't work)
```ruby
response = api.get_market_history (uint32_t bucket_seconds, time_point_sec start, time_point_sec end)
```
## get_market_history_buckets
```ruby
response = api.get_market_history_buckets
```
## get_order_book
```ruby
response = api.get_order_book(limit=500)
response = api.get_order_book(500)
response.result.asks[1].price
response.result.asks[1].sbd
response.result.asks[1].steem
response.result.bids[2].price
response.result.bids[2].sbd
response.result.bids[2].steem
```
## get_recent_trades (current_pays, date, open_pays)
```ruby
response = api.get_recent_trades(limit=1000)
response = api.get_recent_trades(7)
response.result[1].current_pays
response.result[1].date
response.result[1].open_pays
```
## get_ticker (highest_bid, latest, lowest_ask, sbd_volume, steem_volume)
```ruby
response = api.get_ticker
response.result.highest_bid
response.result.latest
response.result.lowest_ask
response.result.percent_change
response.result.sbd_volume
response.result.steem_volume
```
## get_trade_history (Don't work)
```ruby
response = api.get_trade_history (start, end, limit=1000)
```
## get_volume (Last 24 hours, sbd_volume, steem_volume)
```ruby
response = api.get_volume
response.result.sbd_volume
response.result.steem_volume
```

```ruby
stream = Radiator::Stream.new
```
## Method List
```ruby
head_block_number
head_block_id
time
current_witness
total_pow
num_pow_witnesses
virtual_supply
current_supply
confidential_supply
current_sbd_supply
confidential_sbd_supply
total_vesting_fund_steem
total_vesting_shares
total_reward_fund_steem
total_reward_shares2
total_activity_fund_steem
total_activity_fund_shares
sbd_interest_rate
average_block_size
maximum_block_size
current_aslot
recent_slots_filled
participation_count
last_irreversible_block_num
max_virtual_bandwidth
current_reserve_ratio
block_numbers
blocks
```
## Example
```ruby
stream.head_block_number do |block|
    puts "Block Numer: #{block}"
end
```

## Operation Method
```ruby
stream.operations(:Method_name)
```
```ruby
transfer_to_vesting
withdraw_vesting
interest
transfer
liquidity_reward
author_reward
curation_reward
transfer_to_savings
transfer_from_savings
cancel_transfer_from_savings
escrow_transfer
escrow_approve
escrow_dispute
escrow_release
comment
limit_order_create
limit_order_cancel
fill_convert_request
fill_order
vote
account_witness_vote
account_witness_proxy
account_create
account_update
witness_update
pow
custom
```
## Example
```ruby
stream.operations(:vote) do |op|
  print "#{op.voter} voted for #{op.author}"
  puts " (weight: #{op.weight / 100.0}%)"
end
```
## Or all Operations
```ruby
stream.operations do |op|
  puts op.to_json
end
```

```ruby
 api = Radiator::DatabaseApi.new
```

- [get_trending_tags](https://github.com/elieltavares/radiator/wiki/Tags#get_trending_tags)
- [get_discussions_by_trending](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_trending)
- [get_tags_used_by_author](https://github.com/elieltavares/radiator/wiki/Tags#get_tags_used_by_author)
- [get_discussions_by_payout](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_payout)
- [get_post_discussions_by_payout](https://github.com/elieltavares/radiator/wiki/Tags#get_post_discussions_by_payout)
- [get_comment_discussions_by_payout](https://github.com/elieltavares/radiator/wiki/Tags#get_comment_discussions_by_payout)
- [get_discussions_by_created](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_created)
- [get_discussions_by_active](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_active)
- [get_discussions_by_cashout](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_cashout)
- [get_discussions_by_votes](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_votes)
- [get_discussions_by_children](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_children)
- [get_discussions_by_hot](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_hot)
- [get_discussions_by_feed](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_feed)
- [get_discussions_by_blog](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_blog)
- [get_discussions_by_comments](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_comments)
- [get_discussions_by_promoted](https://github.com/elieltavares/radiator/wiki/Tags#get_discussions_by_promoted)


## get_trending_tags
```ruby
response = api.get_trending_tags("TagName or for All empty","limit")
response = api.get_trending_tags("",10)
response.result[0]
response.result[0].comments
response.result[0].name
response.result[0].net_votes
response.result[0].top_posts
response.result[0].total_payouts
response.result[0].trending
```
               
## get_discussions_by_trending
```ruby
api.get_discussions_by_trending("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_trending("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
api.get_discussions_by_trending('tag':'brasil' ,'limit': '10',"filter_tags": [])
response.result[0].abs_rshares
response.result[0].active
response.result[0].active_votes
response.result[0].active_votes[0].percent
response.result[0].active_votes[0].reputation
response.result[0].active_votes[0].rshares
response.result[0].active_votes[0].time 
response.result[0].active_votes[0].voter 
response.result[0].active_votes[0].weight
response.result[0].allow_curation_rewards
response.result[0].allow_replies
response.result[0].allow_votes
response.result[0].author
response.result[0].author_reputation
response.result[0].author_rewards
response.result[0].beneficiaries
response.result[0].body
response.result[0].body_length
response.result[0].cashout_time
response.result[0].category
response.result[0].children
response.result[0].children_abs_rshares
response.result[0].created
response.result[0].curator_payout_value
response.result[0].depth
response.result[0].id
response.result[0].json_metadata 
response.result[0].last_payout
response.result[0].last_update
response.result[0].max_accepted_payout
response.result[0].max_cashout_time
response.result[0].net_rshares
response.result[0].net_votes
response.result[0].parent_author
response.result[0].parent_permlink
response.result[0].pending_payout_value
response.result[0].percent_steem_dollars
response.result[0].permlink
response.result[0].promoted
response.result[0].reblogged_by
response.result[0].replies
response.result[0].reward_weight
response.result[0].root_comment
response.result[0].root_title
response.result[0].title
response.result[0].total_payout_value
response.result[0].total_pending_payout_value
response.result[0].total_vote_weight
response.result[0].url
response.result[0].vote_rshares
```
## get_tags_used_by_author
```ruby
api.get_tags_used_by_author("Author")
api.get_tags_used_by_author("eliel")
```

## get_discussions_by_payout
```ruby
api.get_discussions_by_payout("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_payout("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_post_discussions_by_payout
```ruby
api.get_post_discussions_by_payout("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_post_discussions_by_payout("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_comment_discussions_by_payout
```ruby
api.get_comment_discussions_by_payout("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_comment_discussions_by_payout("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_discussions_by_created
```ruby
api.get_discussions_by_created("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_created("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_discussions_by_active
```ruby
api.get_discussions_by_active("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_active("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_discussions_by_cashout
```ruby
api.get_discussions_by_cashout("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_cashout("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_discussions_by_votes
```ruby
api.get_discussions_by_votes("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_votes("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_discussions_by_children
```ruby
api.get_discussions_by_children("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_children("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_discussions_by_hot
```ruby
api.get_discussions_by_hot("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_hot("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```

## get_discussions_by_feed
```ruby
response = api.get_discussions_by_feed('tag': 'eliel', 'limit': 10)
```

## get_discussions_by_blog
```ruby
response = api.get_discussions_by_blog('tag': 'eliel', 'limit': 10)
```

## get_discussions_by_comments
```ruby
response = api.get_discussions_by_comments("start_author":"smooth","start_permlink":"test","limit":"10")
```

## get_discussions_by_promoted
```ruby
api.get_discussions_by_promoted("select_tags": [], "filter_tags": [], "select_authors": [], "truncate_body": 0, "start_author": '', "start_permlink": '', "parent_author": '', "parent_permlink": '', "limit": 1)
api.get_discussions_by_promoted("select_tags": ["brasil"], "filter_tags": [], "select_authors": [],"limit": 1)
```
