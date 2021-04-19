---
title: Énumération ExtendedDisconnectReasonCode
description: Définit des informations étendues sur la raison de la déconnexion du contrôle.
ms.assetid: E73E73B4-6C6B-4270-A1BD-947FA6D7B31B
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération ExtendedDisconnectReasonCode
topic_type:
- apiref
api_name:
- ExtendedDisconnectReasonCode
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 657d0faee03ca37b9a5a49b95b978a24b0c8955c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511592"
---
# <a name="extendeddisconnectreasoncode-enumeration"></a><span data-ttu-id="f24c4-104">Énumération ExtendedDisconnectReasonCode</span><span class="sxs-lookup"><span data-stu-id="f24c4-104">ExtendedDisconnectReasonCode enumeration</span></span>

<span data-ttu-id="f24c4-105">Définit des informations étendues sur la raison de la déconnexion du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f24c4-105">Defines extended information about the control's reason for disconnection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24c4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f24c4-106">Syntax</span></span>


```C++
typedef enum _ExtendedDisconnectReasonCode { 
  exDiscReasonNoInfo                            = 0,
  exDiscReasonAPIInitiatedDisconnect            = 1,
  exDiscReasonAPIInitiatedLogoff                = 2,
  exDiscReasonServerIdleTimeout                 = 3,
  exDiscReasonServerLogonTimeout                = 4,
  exDiscReasonReplacedByOtherConnection         = 5,
  exDiscReasonOutOfMemory                       = 6,
  exDiscReasonServerDeniedConnection            = 7,
  exDiscReasonServerDeniedConnectionFips        = 8,
  exDiscReasonServerInsufficientPrivileges      = 9,
  exDiscReasonServerFreshCredsRequired          = 10,
  exDiscReasonRpcInitiatedDisconnectByUser      = 11,
  exDiscReasonLogoffByUser                      = 2,
  exDiscReasonLicenseInternal                   = 256,
  exDiscReasonLicenseNoLicenseServer            = 257,
  exDiscReasonLicenseNoLicense                  = 258,
  exDiscReasonLicenseErrClientMsg               = 259,
  exDiscReasonLicenseHwidDoesntMatchLicense     = 260,
  exDiscReasonLicenseErrClientLicense           = 261,
  exDiscReasonLicenseCantFinishProtocol         = 262,
  exDiscReasonLicenseClientEndedProtocol        = 263,
  exDiscReasonLicenseErrClientEncryption        = 264,
  exDiscReasonLicenseCantUpgradeLicense         = 265,
  exDiscReasonLicenseNoRemoteConnections        = 266,
  exDiscReasonLicenseCreatingLicStoreAccDenied  = 267,
  exDiscReasonRdpEncInvalidCredentials          = 768,
  exDiscReasonProtocolRangeStart                = 4096,
  exDiscReasonProtocolRangeEnd                  = 32767
} ExtendedDisconnectReasonCode;
```



## <a name="constants"></a><span data-ttu-id="f24c4-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="f24c4-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f24c4-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span><span class="sxs-lookup"><span data-stu-id="f24c4-108"><span id="exDiscReasonNoInfo"></span><span id="exdiscreasonnoinfo"></span><span id="EXDISCREASONNOINFO"></span>**exDiscReasonNoInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-109">Aucune information supplémentaire n'est disponible.</span><span class="sxs-lookup"><span data-stu-id="f24c4-109">No additional information is available.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span><span class="sxs-lookup"><span data-stu-id="f24c4-110"><span id="exDiscReasonAPIInitiatedDisconnect"></span><span id="exdiscreasonapiinitiateddisconnect"></span><span id="EXDISCREASONAPIINITIATEDDISCONNECT"></span>**exDiscReasonAPIInitiatedDisconnect**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-111">Une application a initié la déconnexion.</span><span class="sxs-lookup"><span data-stu-id="f24c4-111">An application initiated the disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span><span class="sxs-lookup"><span data-stu-id="f24c4-112"><span id="exDiscReasonAPIInitiatedLogoff"></span><span id="exdiscreasonapiinitiatedlogoff"></span><span id="EXDISCREASONAPIINITIATEDLOGOFF"></span>**exDiscReasonAPIInitiatedLogoff**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-113">Une application a été déconnectée du client.</span><span class="sxs-lookup"><span data-stu-id="f24c4-113">An application logged off the client.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span><span class="sxs-lookup"><span data-stu-id="f24c4-114"><span id="exDiscReasonServerIdleTimeout"></span><span id="exdiscreasonserveridletimeout"></span><span id="EXDISCREASONSERVERIDLETIMEOUT"></span>**exDiscReasonServerIdleTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-115">Le serveur a déconnecté le client car le client a été inactif pendant une période plus longue que le délai d’attente désigné.</span><span class="sxs-lookup"><span data-stu-id="f24c4-115">The server has disconnected the client because the client has been idle for a period of time longer than the designated time-out period.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span><span class="sxs-lookup"><span data-stu-id="f24c4-116"><span id="exDiscReasonServerLogonTimeout"></span><span id="exdiscreasonserverlogontimeout"></span><span id="EXDISCREASONSERVERLOGONTIMEOUT"></span>**exDiscReasonServerLogonTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-117">Le serveur a déconnecté le client car le client a dépassé la période indiquée pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="f24c4-117">The server has disconnected the client because the client has exceeded the period designated for connection.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span><span class="sxs-lookup"><span data-stu-id="f24c4-118"><span id="exDiscReasonReplacedByOtherConnection"></span><span id="exdiscreasonreplacedbyotherconnection"></span><span id="EXDISCREASONREPLACEDBYOTHERCONNECTION"></span>**exDiscReasonReplacedByOtherConnection**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-119">La connexion du client a été remplacée par une autre connexion.</span><span class="sxs-lookup"><span data-stu-id="f24c4-119">The client's connection was replaced by another connection.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="f24c4-120"><span id="exDiscReasonOutOfMemory"></span><span id="exdiscreasonoutofmemory"></span><span id="EXDISCREASONOUTOFMEMORY"></span>**exDiscReasonOutOfMemory**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-121">Aucune mémoire n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f24c4-121">No memory is available.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span><span class="sxs-lookup"><span data-stu-id="f24c4-122"><span id="exDiscReasonServerDeniedConnection"></span><span id="exdiscreasonserverdeniedconnection"></span><span id="EXDISCREASONSERVERDENIEDCONNECTION"></span>**exDiscReasonServerDeniedConnection**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-123">Le serveur a refusé la connexion.</span><span class="sxs-lookup"><span data-stu-id="f24c4-123">The server denied the connection.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span><span class="sxs-lookup"><span data-stu-id="f24c4-124"><span id="exDiscReasonServerDeniedConnectionFips"></span><span id="exdiscreasonserverdeniedconnectionfips"></span><span id="EXDISCREASONSERVERDENIEDCONNECTIONFIPS"></span>**exDiscReasonServerDeniedConnectionFips**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-125">Le serveur a refusé la connexion pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f24c4-125">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span><span class="sxs-lookup"><span data-stu-id="f24c4-126"><span id="exDiscReasonServerInsufficientPrivileges"></span><span id="exdiscreasonserverinsufficientprivileges"></span><span id="EXDISCREASONSERVERINSUFFICIENTPRIVILEGES"></span>**exDiscReasonServerInsufficientPrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-127">Le serveur a refusé la connexion pour des raisons de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f24c4-127">The server denied the connection for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span><span class="sxs-lookup"><span data-stu-id="f24c4-128"><span id="exDiscReasonServerFreshCredsRequired"></span><span id="exdiscreasonserverfreshcredsrequired"></span><span id="EXDISCREASONSERVERFRESHCREDSREQUIRED"></span>**exDiscReasonServerFreshCredsRequired**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-129">Les nouvelles informations d’identification sont requises.</span><span class="sxs-lookup"><span data-stu-id="f24c4-129">Fresh credentials are required.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span><span class="sxs-lookup"><span data-stu-id="f24c4-130"><span id="exDiscReasonRpcInitiatedDisconnectByUser"></span><span id="exdiscreasonrpcinitiateddisconnectbyuser"></span><span id="EXDISCREASONRPCINITIATEDDISCONNECTBYUSER"></span>**exDiscReasonRpcInitiatedDisconnectByUser**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-131">L’activité de l’utilisateur a initié la déconnexion.</span><span class="sxs-lookup"><span data-stu-id="f24c4-131">User activity has initiated the disconnect.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span><span class="sxs-lookup"><span data-stu-id="f24c4-132"><span id="exDiscReasonLogoffByUser"></span><span id="exdiscreasonlogoffbyuser"></span><span id="EXDISCREASONLOGOFFBYUSER"></span>**exDiscReasonLogoffByUser**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-133">L’utilisateur se déconnecte, déconnecter la session.</span><span class="sxs-lookup"><span data-stu-id="f24c4-133">The user logged off, disconnecting the session.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span><span class="sxs-lookup"><span data-stu-id="f24c4-134"><span id="exDiscReasonLicenseInternal"></span><span id="exdiscreasonlicenseinternal"></span><span id="EXDISCREASONLICENSEINTERNAL"></span>**exDiscReasonLicenseInternal**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-135">Erreur de licence interne.</span><span class="sxs-lookup"><span data-stu-id="f24c4-135">Internal licensing error.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="f24c4-136"><span id="exDiscReasonLicenseNoLicenseServer"></span><span id="exdiscreasonlicensenolicenseserver"></span><span id="EXDISCREASONLICENSENOLICENSESERVER"></span>**exDiscReasonLicenseNoLicenseServer**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-137">Aucun serveur de licences n’était disponible.</span><span class="sxs-lookup"><span data-stu-id="f24c4-137">No license server was available.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span><span class="sxs-lookup"><span data-stu-id="f24c4-138"><span id="exDiscReasonLicenseNoLicense"></span><span id="exdiscreasonlicensenolicense"></span><span id="EXDISCREASONLICENSENOLICENSE"></span>**exDiscReasonLicenseNoLicense**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-139">Aucune licence de logiciel valide n’était disponible.</span><span class="sxs-lookup"><span data-stu-id="f24c4-139">No valid software license was available.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span><span class="sxs-lookup"><span data-stu-id="f24c4-140"><span id="exDiscReasonLicenseErrClientMsg"></span><span id="exdiscreasonlicenseerrclientmsg"></span><span id="EXDISCREASONLICENSEERRCLIENTMSG"></span>**exDiscReasonLicenseErrClientMsg**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-141">L’ordinateur distant a reçu un message de licence non valide.</span><span class="sxs-lookup"><span data-stu-id="f24c4-141">The remote computer received a licensing message that was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span><span class="sxs-lookup"><span data-stu-id="f24c4-142"><span id="exDiscReasonLicenseHwidDoesntMatchLicense"></span><span id="exdiscreasonlicensehwiddoesntmatchlicense"></span><span id="EXDISCREASONLICENSEHWIDDOESNTMATCHLICENSE"></span>**exDiscReasonLicenseHwidDoesntMatchLicense**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-143">L’ID de matériel ne correspond pas à celui indiqué sur la licence logicielle.</span><span class="sxs-lookup"><span data-stu-id="f24c4-143">The hardware ID does not match the one designated on the software license.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span><span class="sxs-lookup"><span data-stu-id="f24c4-144"><span id="exDiscReasonLicenseErrClientLicense"></span><span id="exdiscreasonlicenseerrclientlicense"></span><span id="EXDISCREASONLICENSEERRCLIENTLICENSE"></span>**exDiscReasonLicenseErrClientLicense**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-145">Erreur de licence client.</span><span class="sxs-lookup"><span data-stu-id="f24c4-145">Client license error.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span><span class="sxs-lookup"><span data-stu-id="f24c4-146"><span id="exDiscReasonLicenseCantFinishProtocol"></span><span id="exdiscreasonlicensecantfinishprotocol"></span><span id="EXDISCREASONLICENSECANTFINISHPROTOCOL"></span>**exDiscReasonLicenseCantFinishProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-147">Des problèmes réseau se sont produits pendant le protocole de licence.</span><span class="sxs-lookup"><span data-stu-id="f24c4-147">Network problems occurred during the licensing protocol.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span><span class="sxs-lookup"><span data-stu-id="f24c4-148"><span id="exDiscReasonLicenseClientEndedProtocol"></span><span id="exdiscreasonlicenseclientendedprotocol"></span><span id="EXDISCREASONLICENSECLIENTENDEDPROTOCOL"></span>**exDiscReasonLicenseClientEndedProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-149">Le client a terminé le protocole de gestion de licences prématurément.</span><span class="sxs-lookup"><span data-stu-id="f24c4-149">The client ended the licensing protocol prematurely.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span><span class="sxs-lookup"><span data-stu-id="f24c4-150"><span id="exDiscReasonLicenseErrClientEncryption"></span><span id="exdiscreasonlicenseerrclientencryption"></span><span id="EXDISCREASONLICENSEERRCLIENTENCRYPTION"></span>**exDiscReasonLicenseErrClientEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-151">Un message de licence a été chiffré de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="f24c4-151">A licensing message was encrypted incorrectly.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span><span class="sxs-lookup"><span data-stu-id="f24c4-152"><span id="exDiscReasonLicenseCantUpgradeLicense"></span><span id="exdiscreasonlicensecantupgradelicense"></span><span id="EXDISCREASONLICENSECANTUPGRADELICENSE"></span>**exDiscReasonLicenseCantUpgradeLicense**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-153">La licence d’accès client de l’ordinateur local n’a pas pu être mise à niveau ou renouvelée.</span><span class="sxs-lookup"><span data-stu-id="f24c4-153">The local computer's client access license could not be upgraded or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span><span class="sxs-lookup"><span data-stu-id="f24c4-154"><span id="exDiscReasonLicenseNoRemoteConnections"></span><span id="exdiscreasonlicensenoremoteconnections"></span><span id="EXDISCREASONLICENSENOREMOTECONNECTIONS"></span>**exDiscReasonLicenseNoRemoteConnections**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-155">L’ordinateur distant ne dispose pas d’une licence pour accepter les connexions à distance.</span><span class="sxs-lookup"><span data-stu-id="f24c4-155">The remote computer is not licensed to accept remote connections.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span><span class="sxs-lookup"><span data-stu-id="f24c4-156"><span id="exDiscReasonLicenseCreatingLicStoreAccDenied"></span><span id="exdiscreasonlicensecreatinglicstoreaccdenied"></span><span id="EXDISCREASONLICENSECREATINGLICSTOREACCDENIED"></span>**exDiscReasonLicenseCreatingLicStoreAccDenied**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-157">Une erreur de refus d’accès a été reçue lors de la création d’une clé de Registre pour le magasin de licences.</span><span class="sxs-lookup"><span data-stu-id="f24c4-157">An access denied error was received while creating a registry key for the license store.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span><span class="sxs-lookup"><span data-stu-id="f24c4-158"><span id="exDiscReasonRdpEncInvalidCredentials"></span><span id="exdiscreasonrdpencinvalidcredentials"></span><span id="EXDISCREASONRDPENCINVALIDCREDENTIALS"></span>**exDiscReasonRdpEncInvalidCredentials**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-159">Des informations d’identification non valides ont été rencontrées.</span><span class="sxs-lookup"><span data-stu-id="f24c4-159">Invalid credentials were encountered.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span><span class="sxs-lookup"><span data-stu-id="f24c4-160"><span id="exDiscReasonProtocolRangeStart"></span><span id="exdiscreasonprotocolrangestart"></span><span id="EXDISCREASONPROTOCOLRANGESTART"></span>**exDiscReasonProtocolRangeStart**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-161">Début de la plage d’erreurs de protocole internes.</span><span class="sxs-lookup"><span data-stu-id="f24c4-161">Beginning the range of internal protocol errors.</span></span> <span data-ttu-id="f24c4-162">Pour plus d’informations, consultez le journal des événements du serveur.</span><span class="sxs-lookup"><span data-stu-id="f24c4-162">Check the server event log for additional details.</span></span>

</dd> <dt>

<span data-ttu-id="f24c4-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span><span class="sxs-lookup"><span data-stu-id="f24c4-163"><span id="exDiscReasonProtocolRangeEnd"></span><span id="exdiscreasonprotocolrangeend"></span><span id="EXDISCREASONPROTOCOLRANGEEND"></span>**exDiscReasonProtocolRangeEnd**</span></span>
</dt> <dd>

<span data-ttu-id="f24c4-164">Fin de la plage des erreurs de protocole internes.</span><span class="sxs-lookup"><span data-stu-id="f24c4-164">Ending the range of internal protocol errors.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f24c4-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f24c4-165">Requirements</span></span>



| <span data-ttu-id="f24c4-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f24c4-166">Requirement</span></span> | <span data-ttu-id="f24c4-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="f24c4-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f24c4-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f24c4-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f24c4-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f24c4-169">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f24c4-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f24c4-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f24c4-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f24c4-171">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f24c4-172">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f24c4-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="f24c4-173"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f24c4-173"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f24c4-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f24c4-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24c4-175">**ExtendedDisconnectReason**</span><span class="sxs-lookup"><span data-stu-id="f24c4-175">**ExtendedDisconnectReason**</span></span>](imsrdpclient-extendeddisconnectreason.md)
</dt> </dl>

 

 





