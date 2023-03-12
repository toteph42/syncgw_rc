# syncgw-rc

With this Plugin you can specify in your [RoundCube](https://roundcube.net) installation which address books, calendars, task lists and notes you want to synchronize with your cell phone / smart phone. For address boks you can specify whether you want to synchronize only contacts with a phone number specified or if you want to synchronize all contacts within this address book.

**Requirements**

To use this plugin, you need

* A functional [RoundCube](https://roundcube.net) installation.
* [sync•gw](https://github.com/Toteph42/syncgw) installed and configured.

**Installation**
* Please install [sync•gw plugin](https://github.com/Toteph42/syncgw-rc).

   ```
  composer require toteph42/syncgw_rc
   ```

* If you want to synchronize address books, then you don't need any additional RoundCube plugin.
* If you want to use shared address books, then you need to install [globaladdressbook-Plugin](https://github.com/johndoh/roundcube-globaladdressbook).

   ```
   composer require johndoh/globaladdressbook
   ```
  
* If you want to synchronize calendar, then you need to install [calender plugin](https://packagist.org/packages/kolab/calendar).

   ```
  composer require kolab/calendar
   ```

* If you want to synchronize tasklis, then you need to install [tasklist plugin](https://plugins.roundcube.net/packages/kolab/tasklist).

   ```
  composer require kolab/tasklist
   ```
  
    **Caution:** If you use the plugin and receive a error message in RoundCube log file, then please check file `plugins/tasklist/config.inc.php`. There `$config['tasklist_driver'] = 'database';` should be specified.
  
* If you want to synchronize notes, then you need to install [ddnotes plugin](https://packagist.org/packages//dondominio/ddnotes).

   ```
  composer require dondominio/ddnotes 
   ```

* Activate our plugin by adding plugin name in file `config/config.inc.php`

   ```
  $config['plugins'] = array(
	...
	'syncgw_rc',
	[the other optional plugins]
	...
  );
   ```
	
**Usage**

* Go to menu `Settings` and configure synchronization settings by selecting `Synchronization settings`.
* Now you're ready to synchronize your selected data with your cell phone / smart phone.

Please enjoy!

## Donation ##
If you want to support my work, feel free to send me a donation.

<a href="https://www.paypal.com/donate/?hosted_button_id=DS6VK49NAFHEQ" target="_blank">
  <img src="https://www.paypalobjects.com/en_US/DK/i/btn/btn_donateCC_LG.gif" alt="Donate with PayPal"/>
</a>
