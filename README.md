# Hello dear Scryptonaut
Supra isn't live yet and Religant has abondoned ship, so Stokenet is lacking an oracle.

Not wanting to do manual updates to my components, I made a small blueprint that can take an xrd price and save it. I have it instantiated, and set it up to be updated every 10 minutes using CoinGecko data, so not decentralized at all. Still, it's usable if you want to test your Stokenet creations. Beware, this was made super quick, so it's shitty ;)

# Requesting data
Component address: component_tdx_2_1cqeh8j4wgyezttn969kf0c7644m0cc33c0jpfsc9zf770rnpg69y4z

Call the get_prices method:

```rust
pub fn get_prices(&mut self) -> Vec<(ResourceAddress, Decimal)> {
            /*if let Some(xrd_price_info) = self.religant.get_price() {
                if xrd_price_info.price != self.prices[0].1 {
                    self.prices[0].1 = xrd_price_info.price;
                }
            }*/
            self.prices.clone()
        }
```

As you can see, it spits out a Vec<(ResourceAddress, Decimal)>, it contains only one element: (xrd_address, xrd_price). Why? Short story: I was lazy and used something I had laying around. Good luck.

# Help meeeeeee
Need help, contact me on tg: @octopusxrd
