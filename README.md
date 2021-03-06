# MINIMUM NAME LENGTH EXTENSION
Version 1.0

Copyright © 2007 Rob Church.
All rights reserved.
Please see the LICENCE file for terms of use and redistribution

## Introduction

This extension introduces a new configuration variable,
$wgMinimumNameLength, which can be used to enforce a minimum
username length during user account creation.

This is often helpful in conjunction with other anti-spam
measures.

## Requirements

This extension requires:

* PHP 5.0.x (5.1.x *strongly recommended*) or above
* MediaWiki 1.11.0 or above

## Installation

To install the extension, please download or check out all files from
the Subversion repository, and place them in a "MinimumNameLength" directory
within your MediaWiki extensions directory.

You then need to edit your LocalSettings.php file, and add the following
line, somewhere near the bottom:

	require_once( "{$IP}/extensions/MinimumNameLength/MinimumNameLength.php" );
	
Access the Special:Version page on your wiki to confirm the installation.

## Configuration

To configure the minimum name length, set $wgMinimumNameLength in LocalSettings.php,
*after* the call to include the extension, e.g.

	require_once( "{$IP}/extensions/MinimumNameLength/MinimumNameLength.php" );
	$wgMinimumNameLength = 10;
	
## Change log
11/01/2008
1.1
	Uses wfLoadExtensionMessages now
29/03/2007
1.0
	Initial release
