##############################
Change Extbase Backend Modules
##############################

************************************************************
This is an example on how to change extbase backend modules.
************************************************************

:Author: Philipp Gampe <philipp.gampe@typo3.org>
:Date: 2013-05-24
:Manual section: 1

DESCRIPTION
===========

Changing an extbase based backend module is really easy. All you need is to adjust the fluid template.

In particular you will need to add the following TypoScript to the global TypoScript configuration.
You can do so either via an extension (like done here) or by using the Install Tool.

.. code::

	module.tx_beuser {
		view {
			partialRootPath = EXT:extendBeModules/Resources/Private/Partials/
			templateRootPath = EXT:extendBeModules/Resources/Private/Templates/
		}
	}


What does it do
===============

This example extension adds a new column to the backend users module. The new column renders
a nested list of backend user groups for each user.
To support infinite nesting, a new partial is introduced that renders the actual group and any subgroups.

LICENSE
=======

.. code::

	To the extent possible under law, Philipp Gampe has waived all copyright and related or neighboring rights to "Change Extbase Backend Modules". This work is published from: Germany

	http://creativecommons.org/publicdomain/zero/1.0/
