# sharethis-reactjs 

![alt text][logo]

[logo]: https://s18955.pcdn.co/wp-content/uploads/2016/12/ShareThisLogo2x.png "ShareThis"

ShareThis official social media share buttons for React.
Visit www.sharethis.com for more technical support.


## Products

 - Inline Share Buttons
 - Sticky Share Buttons
 - Inline Reaction Buttons
 - Inline Follow Buttons

## How to use the buttons

```Javascript
import React from "react";
import {InlineReactionButtons} from 'sharethis-reactjs';
import {InlineShareButtons} from 'sharethis-reactjs';
import {StickyShareButtons} from 'sharethis-reactjs';
import {InlineFollowButtons} from 'sharethis-reactjs';

class App extends React.Component {

  render () {
    return (
      <div>
        <style dangerouslySetInnerHTML={{__html: `
          html, body {
            margin: 0;
            padding: 0;
            text-align: center;
          }
          h1 {
            font-size: 24px;
            font-weight: bold;
          }
          hr {
            margin-bottom: 40px;
            margin-top: 40px;
            width: 50%;
          }
        `}} />

        <h1>Inline Share Buttons</h1>
        <InlineShareButtons
          config={{
            alignment: 'center',  // alignment of buttons (left, center, right)
            enabled: true,        // show/hide buttons (true, false)
            font_size: 16,        // font size for the buttons
            labels: 'cta',        // button labels (cta, counts, null)
            language: 'en',       // which language to use (see LANGUAGES)
            networks: [           // which networks to include (see NETWORKS)
              'whatsapp',
              'linkedin',
              'messenger',
              'facebook',
              'twitter'
            ],
            padding: 12,          // padding within buttons (INTEGER)
            radius: 4,            // the corner radius on each button (INTEGER)
            show_total: true,
            size: 40,             // the size of each button (INTEGER)

            // OPTIONAL PARAMETERS
            url: 'https://www.sharethis.com', // (defaults to current url)
            image: 'https://bit.ly/2CMhCMC',  // (defaults to og:image or twitter:image)
            description: 'custom text',       // (defaults to og:description or twitter:description)
            title: 'custom title',            // (defaults to og:title or twitter:title)
            message: 'custom email text',     // (only for email sharing)
            subject: 'custom email subject',  // (only for email sharing)
            username: 'custom twitter handle' // (only for twitter sharing)
          }}
        />
        <hr />

        <h1>Inline Reaction Buttons</h1>
        <InlineReactionButtons
          config={{
            alignment: 'center',  // alignment of buttons (left, center, right)
            enabled: true,        // show/hide buttons (true, false)
            language: 'en',       // which language to use (see LANGUAGES)
            min_count: 0,         // hide react counts less than min_count (INTEGER)
            padding: 12,          // padding within buttons (INTEGER)
            reactions: [          // which reactions to include (see REACTIONS)
              'slight_smile',
              'heart_eyes',
              'laughing',
              'astonished',
              'sob',
              'rage'
            ],
            size: 48,             // the size of each button (INTEGER)
            spacing: 8,           // the spacing between buttons (INTEGER)

            // OPTIONAL PARAMETERS
            url: 'https://www.sharethis.com' // (defaults to current url)
          }}
        />
        <hr />

        <h1>Inline Follow Buttons</h1>
        <InlineFollowButtons
          config={{
            action: 'Follow us:', // call to action (STRING)
            action_enable: true,  // show/hide call to action (true, false)
            action_pos: 'bottom', // position of call to action (left, top, right)
            alignment: 'center',  // alignment of buttons (left, center, right)
            enabled: true,        // show/hide buttons (true, false)
            networks: [           // which networks to include (see NETWORKS)
              'twitter',
              'facebook',
              'instagram',
              'youtube'
            ],
            padding: 8,           // padding within buttons (INTEGER)
            profiles: {           // social profile links for buttons
              twitter: 'sharethis',
              facebook: 'sharethis',
              instagram: 'sharethis',
              youtube: '/channel/UCbM93niCmdc2RD9RZbLMP6A?view_as=subscriber'
            },
            radius: 9,            // the corner radius on each button (INTEGER)
            size: 32,             // the size of each button (INTEGER)
            spacing: 8            // the spacing between buttons (INTEGER)
          }}
        />
        <hr />

        <StickyShareButtons
          config={{
            alignment: 'left',    // alignment of buttons (left, right)
            enabled: true,        // show/hide buttons (true, false)
            font_size: 16,        // font size for the buttons
            hide_desktop: false,  // hide buttons on desktop (true, false)
            labels: 'counts',     // button labels (cta, counts, null)
            language: 'en',       // which language to use (see LANGUAGES)
            min_count: 0,         // hide react counts less than min_count (INTEGER)
            networks: [           // which networks to include (see NETWORKS)
              'linkedin',
              'facebook',
              'twitter',
              'pinterest',
              'email'
            ],
            padding: 12,          // padding within buttons (INTEGER)
            radius: 4,            // the corner radius on each button (INTEGER)
            show_total: true,     // show/hide the total share count (true, false)
            show_mobile: true,    // show/hide the buttons on mobile (true, false)
            show_toggle: true,    // show/hide the toggle buttons (true, false)
            size: 48,             // the size of each button (INTEGER)
            top: 160,             // offset in pixels from the top of the page

            // OPTIONAL PARAMETERS
            url: 'https://www.sharethis.com', // (defaults to current url)
            image: 'https://bit.ly/2CMhCMC',  // (defaults to og:image or twitter:image)
            description: 'custom text',       // (defaults to og:description or twitter:description)
            title: 'custom title',            // (defaults to og:title or twitter:title)
            message: 'custom email text',     // (only for email sharing)
            subject: 'custom email subject',  // (only for email sharing)
            username: 'custom twitter handle' // (only for twitter sharing)

          }}
        />

      </div>
    );
  }
};

// export
export default App;
```

## Available Networks

| Network | Icon  |
| ------- | ----- |
| blogger | <img src="https://s18955.pcdn.co/wp-content/uploads/2017/05/Blogger.png" width="48" /> |
| delicious | ![](https://s18955.pcdn.co/wp-content/uploads/2017/05/Delicious.png | width=48)
| digg | ![](https://s18955.pcdn.co/wp-content/uploads/2017/05/Digg.png | width=48)
| email | ![](https://s18955.pcdn.co/wp-content/uploads/2017/05/Email.png | width=48)
| facebook | ![](https://s18955.pcdn.co/wp-content/uploads/2017/05/Facebook.png | width=48)
| flipboard | ![](https://s18955.pcdn.co/wp-content/uploads/2018/08/flipboard-logo.png | width=48)

| googleplus | linkedin |
| livejournal | mailru | meneame | messenger |
| odnoklassniki | pinterest | print | reddit |
| sharethis | sms | stumbleopon | tumblr |
| twitter | vk | wechat | weibo |
| whatsapp | xing | | |

## Available Reactions

| slight_smile | heart_eyes | laughing |
| astonished | sob | rage |

## Demo

```
 npm install
 npm run demo
```

  Open `localhost:5000`
  
