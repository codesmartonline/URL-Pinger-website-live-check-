=== URL Pinger (website live check) ===
Contributors: CodeSmart
Tags: uptime, website monitor, ping, site monitor, down alert, admin, csv, cron
Requires at least: 4.6
Tested up to: 6.8
Requires PHP: 5.6
Stable tag: 1.20
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

Check live/down status of URLs or Websites by pinging them on set intervals. Get notified if any site goes down. Import/export URLs via CSV. Easy admin interface.

== Description ==

**URL Pinger (website live check)** is an easy-to-use WordPress admin plugin to monitor the status of any number of websites or URLs. It pings your chosen URLs at set intervals and keeps a log of the results. If any are down, you'll receive an email notification.

**Key Features:**
- Add, edit, or remove URLs to monitor.
- Set custom check intervals (in hours) for each URL.
- Results table with status, last checked time, and more.
- "Check Now" button: instantly ping all URLs.
- Import/export URLs list via CSV (with interval).
- Download a CSV of failed URLs.
- Search/filter your URL list.
- Pagination for large lists (15 URLs per page).
- Custom User-Agent sent with pings.
- Admin notification email if any site is down.
- Fully cleans up after uninstall.

**Please note:** Some hosting providers may block incoming pings, leading to false "Fail" results even if the site is working.

== Installation ==

1. Upload the plugin files to the `/wp-content/plugins/url-pinger/` directory, or install via the WordPress plugins screen directly.
2. Activate the plugin through the 'Plugins' screen in WordPress.
3. Go to **URL Pinger** in your WordPress admin menu to configure.

== Frequently Asked Questions ==

= Does this plugin use an external service? =

No, all pings are performed from your own server using WordPress's HTTP API.

= How often are URLs checked? =

Each URL is checked based on the interval (hours) you set for it. The plugin checks which URLs are due every 5 minutes using WordPress cron, but each URL is only pinged when its interval has elapsed.

= What happens if a ping fails? =

If a ping fails, the plugin automatically retries once after a short delay. Only if both attempts fail is the status marked as "Fail".

= Can I check all URLs immediately? =

Yes, use the "Check Now" button to ping all URLs instantly, regardless of their interval.

= Can I import/export URLs? =

Yes! Use the CSV import/export features. The CSV file should include URL and interval columns.

= Does the plugin send notifications? =

Yes, if any URLs are detected as "down", an email alert is sent to the configured admin email.

= Will it affect website performance? =

Pings are staggered and run in the background via cron, with throttling and retry logic to avoid server overload.

= What happens on uninstall? =

All plugin data and settings are removed from the database.

== Screenshots ==

1. URL list table with status, search, and actions.
2. Add URLs and set ping intervals.
3. Import/export URLs via CSV.
4. Notification email settings.

== Changelog ==

= 1.20 =
* Bug fixes

= 1.18 =
* Retry ping once if a URL fails before marking as Fail.
* Added info message for potential false positives due to hosting.
* Improved UI styles, red "Delete All" button, and search/pagination.
* Code and compatibility improvements.

= 1.17 =
* Added "Download failed URLs list" CSV.
* Optimized admin UI and paging.
* Improved CSV import/normalization.
* Enhanced notification and cron handling.

= 1.15 =
* Remove all data on uninstall.
* Reduce ping throttling interval to 3 seconds.
* Remove all data (DB table and options) on uninstall.
* Use a short table name if the table prefix is very long.

= 1.14 =
* Search bar for URLs in admin.
* CSV export for failed URLs.
* UI improvements and code clean-up.

= 1.13 =
* Added support for browser-like User-Agent in ping requests.
* Minor bug fixes.

= 1.12 =
* Pagination and sorting improvements.
* Manual "Check Now" runs in background via cron.
* Enhanced dashboard notices.

= 1.0 =
* Initial release.

== Upgrade Notice ==

= 1.20 =
Highly recommended: improved reliability, UI, and notification features.

== License ==

This plugin is free software, distributed under the terms of the GNU General Public License v2 or later. See [GPLv2](https://www.gnu.org/licenses/gpl-2.0.html) for details.
