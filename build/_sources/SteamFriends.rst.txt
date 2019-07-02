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
.. centered:: When the steam ovberlay activates or deactivates. Can be used to pause or resume single player games.

.. image:: Images/Friend/SteamGameOverlayActivatedCallback.jpg
	:width: 600px
	:height: 350px
	:align: center


.. list-table:: Returns **FLobbyUpdatedStruct**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Type
     - Description

   * - bActive
     - bool
     - Returns true if steam overlay was activated, and returns false when steam overlay deactivated.

EChatMemberStateChange
======================

.. image:: Images/Matchmaking/EChatMemberStateChange.jpg
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

   * - ChatMemberStateChangeEntered
     - Entered (0x0001)
     - The User has joined or is joining the lobby.

   * - ChatMemberStateChangeLeft
     - Left (0x0002)
     - The User has left or is leaving the lobby.

   * - ChatMemberStateChangeDisconnected
     - Disconnected (0x0004)
     - The User has disconnected from the lobby.

   * - ChatMemberStateChangedKicked
     - Kicked (0x0008)
     - The User has been kicked.

   * - ChatMemberStateChangeBanned
     - Banned (0x0010)
     - The User has been kicked or banned.


SteamLobbyCreated
==================
.. centered:: Result of a request to create a Lobby. Lobby has been joined and is ready for use at this point.

.. image:: Images/Matchmaking/SteamLobbyCreated.jpg
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

   * - SteamLobbyResult
     - Integer 
     - Result of the create lobby operation as an `EResult. <EnumPage#echatmemberstatechange>`__

   * - SteamLobbyID
     - Integer
     - Steam ID of the lobby.


SteamLobbyEntered
==================
.. centered:: Result of entering a lobby.

.. image:: Images/Matchmaking/SteamLobbyEntered.jpg
	:width: 600px
	:height: 350px
	:align: center

.. list-table:: Returns **FLobbyEnteredStruct**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Type
     - Description

   * - SteamLobbyID
     - Integer
     - Steam ID of the lobby.

   * - SteamLobbyBlocked
     - bool
     - When true only invited users may join.


   * - LobbyEnteredResponse
     - `ELobbyEnteredResponse <#elobbyenteredresponse>`__
     - Response to determine if lobby was entered successfully.

ELobbyEnteredResponse
======================

.. image:: Images/Matchmaking/ELobbyEnteredResponse.jpg
	:width: 600px
	:height: 350px
	:align: center

.. list-table:: **ELobbyEnteredResponse**
   :widths: 25 25 50
   :header-rows: 1
   :align: center

   * - Name
     - Value
     - Description

   * - EResponse_Success
     - Success (1)
     - Successful entry to chat/lobby.

   * - EResponse_DoesntExist
     - DoesntExist (2)
     - Lobby/Chat doesn't exist (maybe closed).

   * - EResponse_NotAllowed
     - NotAllowed (3)
     - Do not have permission to join.

   * - EResponse_Full
     - Full (4)
     - Chat/Lobby room is full.

   * - EResponse_UnexpectedError
     - UnexpectedError (5)
     - UnexpectedError.

   * - EResponse_Banned
     - Banned (6)
     - The User has been banned from this lobby/chat and cannot join.

   * - EResponse_Limited
     - Limited (7)
     - Cannot join this lobby because the user is limited.

   * - EResponse_ClanDisabled
     - ClanDisabled (8)
     - Attempt to join a chat when clan chat is locked or disabled.

   * - EResponse_CommunityBan
     - CommunityBan (9)
     - Cannot join this chat/lobby because the user is banned from the community

   * - EResponse_MemberBlockedYou
     - MemberBlockedYou (10)
     - Cannot join this chat/lobby because a member in this chat/lobby blocked you.

   * - EResponse_YouBlockedMember
     - YouBlockedMember (11)
     - Cannot join this chat/lobby because the user has blocked a user already in the chat/lobby
