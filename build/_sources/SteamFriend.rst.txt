************
Steam Friend Callbacks
************
GetFriendCallback
=====================
.. centered:: Get reference to Friend Callback Object to assign callback events.

.. image:: Images/Friend/GetFriendCallback.jpg
	:width: 600px
	:height: 350px
	:align: center

.. list-table:: Returns **PFFriendCallbacks**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Type
     - Description

   * - Return Value
     - PFFriendCallbacks
     - Pointer to friend callback handler.

SteamGameOverlayActivatedCallback
==================
.. centered:: When the steam overlay activates or deactivates. Can be used to pause or resume single player games.

.. image:: Images/Friend/SteamGameOverlayActivatedCallback.jpg
	:width: 600px
	:height: 350px
	:align: center


.. list-table:: Returns **bActive**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Type
     - Description

   * - bActive
     - bool
     - Returns true if steam overlay was activated, and returns false when steam overlay deactivated.


SteamPersonaStateChangeCallback
==================
.. centered:: Called when a friends' status changes.

.. image:: Images/Friend/SteamPersonaStateChangeCallback.jpg
  :width: 600px
  :height: 350px
  :align: center


.. list-table:: Returns **FLobbyCreatedStruct**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Type
     - Description

   * - SteamUserID
     - Integer 
     - Steam ID of user who changed.

   * - SteamPersonaChange
     - `ESteamPersonaChange <#esteampersonachange>`__
     - Steam persona change result.


ESteamPersonaChange
======================

.. image:: Images/Friend/ESteamPersonaChange.jpg
	:width: 600px
	:height: 350px
	:align: center

.. list-table:: **EChatMemberStateChange**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Value
     - Description

   * - EPersonaChangeName
     - ChangedName (1)
     - The user changed their persona name.

   * - EPersonaChangeStatus
     - ChangedStatus (2)
     - The user changed their account status (online, away, busy).

   * - EPersonaChangeComeOnline
     - ComeOnline (3)
     - The user has come online.

   * - EPersonaChangeGoneOffline
     - GoneOffline (4)
     - The user has gone offline.

   * - EPersonaChangeGamePlayed
     - ChangedGame (5)
     - The user has changed games.

   * - EPersonaChangeGameServer
     - ChangeServer (6)
     - The user has changed game servers.

   * - EPersonaChangeAvatar
     - ChangedAvatar (7)
     - The user has changed their steam avatar.

   * - EPersonaChangeJoinedSource
     - ChangedSource (8)
     - The user has changed source.

   * - EPersonaChangeLeftSource
     - LeftSource (9)
     - The user has left source.

   * - EPersonaChangeRelationshipChanged
     - ChangedRelationship (10)
     - The user has changed their relationship.

   * - EPersonaChangeNameFirstSet
     - ChangedFirstName (11)
     - The user has changed their first name.

   * - EPersonaChangeFacebookInfo
     - ChangedFacebookInfo (12)
     - The user has changed their facebook info.

   * - EPersonaChangeNickname
     - ChangedNickname (13)
     - The user's nickname has changed.

   * - EPersonaChangeSteamLevel
     - ChangedFacebookInfo (14)
     - The user's steam level has changed.

   * - EPersonaChangeErr
     - Error (15)
     - Result Error.


SteamSetPersonaNameCallback
==================
.. centered:: Result of entering a lobby.

.. image:: Images/Friend/SteamSetPersonaNameCallback.jpg
	:width: 600px
	:height: 350px
	:align: center

.. list-table:: Returns **FSteamSetPersonaName**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Type
     - Description

   * - bSuccess
     - bool
     - true if name change completed successfully.

   * - bLocalSuccess
     - bool
     - true if name changed was locally.

   * - SteamSetPersonaEResult
     - (Integer) `EResult`_.
     - result of the operation as an integer of EResult.

.. _EResult: https://partner.steamgames.com/doc/api/steam_api#EResult

