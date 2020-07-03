# gridpane-updates
This page is simply a page to track changes from the GridPane video updates. It's not set in stone, only a transcription.

# July 3rd 2020
* System users will be automatically be generated for new sites, this is a default.
	* This is for security.
	* This is also for resource monitoring.
* Developers will have the option of building MariaDB 10.5 option during server provisioning.
* Added in OAuth, available with Gitlab and Github.
	* No Twitter or Facebook.
* Site Migrations/Clones/Failover Change
	* System users will be copied over.
	* Routing for www or non-www will be copied over.
* Reduced payload for server creation for API users.
* Various bug fixes
	* Team bug fixes, admins couldn't delete own team members.
	* Auto SSL with alias domains, were showing on even if the primary domain failed.
	* Domain routing, in certain instances if you switched to www or root and you made other changes, would revert to not set.
	* Unverified users not being able to login.
	* Console errors when deleting servers fixed.
* All new servers are being build monit 5.2.6
	* Slew of new notifications and system utilization checks.
	* Anywhere near 70% or more utilization on ram, disk, cpu will result in notifications in slack and in-app notifications.
* PHP Workers are now set dynamic based on core count.
	* Low end 2x core count at most 4x core count.
	* Documentation on default standards based upon your specific use case.
* New re-writes within robots.txt virtual re-writes that SEO Press does.
* Enhanced certbot renewal checks and built in some self healing for the acme SSL configs.
* Migrations/Clones/Backups/Restores/Staging 
	* If you've had any bugs with these functions and manually done non-standard changes to wp-config.php. We've put in traps, locks and checks so that these issues shouldn't happen going forward.
* Fix for Failover Sites. 
	* Not showing up correctly, and sites that weren't failover sites showing as failover sites are now fixed.
* Lots of fixes, monitoring and MariaDB.
* Critical support over holidays until Monday.

*
# June 19th 2020
* Cloudflare fix, you can now set the TTL to auto and enable/disable proxy.
* Failover Icons added.
* Heartbeat icons adjusted.
* Many console bugs fixed.
* Affiliate codes fixed.
* Changes to support.
	* Extended use documented articles will no longer be actioned for free by support.
		* Example: 
			* 6G firewall is conflictin with a plugin, resolution is in the knowledge base.
			* Customer asks for the fix/change to be implemented on their server.
			* Usually this is done by a GridPane support staff member
			* Going forward this will cease.
	* DevOps as a service option.
		* A paid option for customers to have extended use documentation articles implemented.
		* If a uniquie use case and is reasonable within the scope of serious production WordPress and we don't have documentation for it.
			* We will be creating the document and solving it for free that first time.
			* We will be using that ticket/situation to create the foundation of the documentation.
			* First one is always free, and is brand new and not seen before.
		* Working with GridPane engineers.
		* Early as Monday/Tuesday next week.
	* If someting is baked into the platform, and is broke; we will fix it.
* Load Balancers of Apollo
	* We default to GCP for Apollo instances.
	* For nordics, it would be upcloud as that's what's available.
	* Signal Review used Cloudflare LB and GCP LB
* Apollo
	* Pricing starts at $1000 up to 10 sites.
	* Goal for Apolo is high-concurrency and high-volume.
	* If you need more sites, contact.
	* Each Apollo build out is a bespoke setup.
