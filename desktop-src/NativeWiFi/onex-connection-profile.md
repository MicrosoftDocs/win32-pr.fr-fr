---
description: Contient des informations sur le profil de connexion 802.1 X actuellement utilisé pour l’authentification 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Structure ONEX_CONNECTION_PROFILE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543700"
---
# <a name="onex_connection_profile-structure"></a><span data-ttu-id="58ac3-103">Structure du profil de \_ connexion Onex \_</span><span class="sxs-lookup"><span data-stu-id="58ac3-103">ONEX\_CONNECTION\_PROFILE structure</span></span>

<span data-ttu-id="58ac3-104">La structure du **\_ \_ profil de connexion Onex** contient des informations sur le profil de connexion 802.1 x actuellement utilisé pour l’authentification 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-104">The **ONEX\_CONNECTION\_PROFILE** structure contains information on the 802.1X connection profile currently used for 802.1X authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ac3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58ac3-105">Syntax</span></span>


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a><span data-ttu-id="58ac3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="58ac3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="58ac3-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="58ac3-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-108">Version de cette structure **de \_ \_ profil de connexion Onex** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-108">The version of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-109">**dwTotalLen**</span><span class="sxs-lookup"><span data-stu-id="58ac3-109">**dwTotalLen**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-110">Longueur, en octets, de cette structure **de \_ \_ profil de connexion Onex** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-110">The length, in bytes, of this **ONEX\_CONNECTION\_PROFILE** structure.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-111">**fOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="58ac3-111">**fOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-112">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwOneXSupplicantFlags** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-112">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwOneXSupplicantFlags** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-113">**fsupplicantMode**</span><span class="sxs-lookup"><span data-stu-id="58ac3-113">**fsupplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-114">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **supplicantMode** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-114">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **supplicantMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-115">**fauthMode**</span><span class="sxs-lookup"><span data-stu-id="58ac3-115">**fauthMode**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-116">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **authmode** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-116">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **authMode** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-117">**fHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="58ac3-117">**fHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-118">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwHeldPeriod** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-118">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwHeldPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-119">**fAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="58ac3-119">**fAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-120">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwAuthPeriod** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-120">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwAuthPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-121">**fStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="58ac3-121">**fStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-122">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwStartPeriod** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-122">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwStartPeriod** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-123">**fMaxStart**</span><span class="sxs-lookup"><span data-stu-id="58ac3-123">**fMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-124">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwMaxStart** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-124">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxStart** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-125">**fMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="58ac3-125">**fMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-126">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwMaxAuthFailures** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-126">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwMaxAuthFailures** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-127">**fNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="58ac3-127">**fNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-128">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwNetworkAuthTimeout** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-128">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthTimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-129">**fAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="58ac3-129">**fAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-130">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **bAllowLogonDialogs** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-130">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bAllowLogonDialogs** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-131">**fNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="58ac3-131">**fNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-132">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **dwNetworkAuthWithUITimeout** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-132">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **dwNetworkAuthWithUITimeout** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-133">**fUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="58ac3-133">**fUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-134">Indique si la structure du **\_ \_ profil de connexion Onex** contient des données valides dans le membre **bUserBasedVLan** .</span><span class="sxs-lookup"><span data-stu-id="58ac3-134">Indicates if the **ONEX\_CONNECTION\_PROFILE** structure contains valid data in the **bUserBasedVLan** member.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-135">**dwOneXSupplicantFlags**</span><span class="sxs-lookup"><span data-stu-id="58ac3-135">**dwOneXSupplicantFlags**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-136">Ensemble d’indicateurs 802.1 X qui peuvent être présents dans le profil.</span><span class="sxs-lookup"><span data-stu-id="58ac3-136">A set of 802.1X flags that can be present in the profile.</span></span> <span data-ttu-id="58ac3-137">Ces indicateurs sont réservés à un usage interne par le module d’authentification 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="58ac3-137">These flags are reserved for internal use by the 802.1X authentication module.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-138">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="58ac3-138">**supplicantMode**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-139">Élément supplicantMode dans le schéma 802.1 X qui spécifie la méthode de transmission utilisée pour EAPOL-Start messages.</span><span class="sxs-lookup"><span data-stu-id="58ac3-139">The supplicantMode element in the 802.1X schema that specifies the method of transmission used for EAPOL-Start messages.</span></span> <span data-ttu-id="58ac3-140">Pour plus d’informations, consultez l' [**élément supplicantMode (Onex)**](onexschema-supplicantmode-onex-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-140">For more information, see the [**supplicantMode (OneX) Element**](onexschema-supplicantmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="58ac3-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ac3-141">Value</span></span>                                                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="58ac3-142">Signification</span><span class="sxs-lookup"><span data-stu-id="58ac3-142">Meaning</span></span>                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <span data-ttu-id="58ac3-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-143"><dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="58ac3-144">Les messages de EAPOL-Start ne sont pas transmis.</span><span class="sxs-lookup"><span data-stu-id="58ac3-144">EAPOL-Start messages are not transmitted.</span></span> <span data-ttu-id="58ac3-145">Valide pour les profils LAN câblés uniquement.</span><span class="sxs-lookup"><span data-stu-id="58ac3-145">Valid for wired LAN profiles only.</span></span><br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <span data-ttu-id="58ac3-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-146"><dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt></span></span> </dl>                                                         | <span data-ttu-id="58ac3-147">Le client détermine quand envoyer des paquets EAPOL-Start en fonction de la capacité du réseau.</span><span class="sxs-lookup"><span data-stu-id="58ac3-147">The client determines when to send EAPOL-Start packets based on network capability.</span></span> <span data-ttu-id="58ac3-148">Les messages de EAPOL-Start sont envoyés uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="58ac3-148">EAPOL-Start messages are only sent when required.</span></span> <span data-ttu-id="58ac3-149">Valide pour les profils LAN câblés uniquement.</span><span class="sxs-lookup"><span data-stu-id="58ac3-149">Valid for wired LAN profiles only.</span></span><br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <span data-ttu-id="58ac3-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-150"><dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt></span></span> </dl>                                         | <span data-ttu-id="58ac3-151">EAPOL-Start messages sont transmis comme spécifié par 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="58ac3-151">EAPOL-Start messages are transmitted as specified by 802.1X.</span></span> <span data-ttu-id="58ac3-152">Valide pour les profils de réseau local câblés et sans fil.</span><span class="sxs-lookup"><span data-stu-id="58ac3-152">Valid for both wired and wireless LAN profiles.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="58ac3-153">**authMode**</span><span class="sxs-lookup"><span data-stu-id="58ac3-153">**authMode**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-154">Élément authMode dans le schéma 802.1 X qui spécifie le type d’informations d’identification utilisé pour l’authentification 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="58ac3-154">The authMode element in the 802.1X schema that specifies the type of credentials used for 802.1X authentication.</span></span> <span data-ttu-id="58ac3-155">Pour plus d’informations, consultez l' [**élément authmode (Onex)**](onexschema-authmode-onex-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-155">For more information, see the [**authMode (OneX) Element**](onexschema-authmode-onex-element.md) in the 802.1X scheme.</span></span>



| <span data-ttu-id="58ac3-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ac3-156">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="58ac3-157">Signification</span><span class="sxs-lookup"><span data-stu-id="58ac3-157">Meaning</span></span>                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <span data-ttu-id="58ac3-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-158"><dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="58ac3-159">Utilisez les informations d’identification de l’ordinateur ou de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58ac3-159">Use machine or user credentials.</span></span> <span data-ttu-id="58ac3-160">Lorsqu’un utilisateur a ouvert une session, les informations d’identification de l’utilisateur sont utilisées pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="58ac3-160">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="58ac3-161">Quand aucun utilisateur n’est connecté, les informations d’identification de l’ordinateur sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="58ac3-161">When no user is logged on, machine credentials are used.</span></span><br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <span data-ttu-id="58ac3-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-162"><dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="58ac3-163">Utiliser uniquement les informations d’identification de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="58ac3-163">Use machine credentials only.</span></span><br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <span data-ttu-id="58ac3-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-164"><dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="58ac3-165">Utiliser uniquement les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58ac3-165">Use user credentials only.</span></span><br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <span data-ttu-id="58ac3-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-166"><dt>**OneXAuthModeGuest**</dt> <dt>3</dt></span></span> </dl>                                 | <span data-ttu-id="58ac3-167">Utilisez uniquement les informations d’identification invité (vide).</span><span class="sxs-lookup"><span data-stu-id="58ac3-167">Use guest (empty) credentials only.</span></span><br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <span data-ttu-id="58ac3-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="58ac3-168"><dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="58ac3-169">Les informations d’identification à utiliser ne sont pas spécifiées.</span><span class="sxs-lookup"><span data-stu-id="58ac3-169">Credentials to use are not specified.</span></span><br/>                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="58ac3-170">**dwHeldPeriod**</span><span class="sxs-lookup"><span data-stu-id="58ac3-170">**dwHeldPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-171">Élément heldPeriod dans le schéma 802.1 X qui spécifie la durée, en secondes, pendant laquelle un client ne tentera pas une nouvelle tentative d’authentification après l’échec d’une tentative d’authentification.</span><span class="sxs-lookup"><span data-stu-id="58ac3-171">The heldPeriod element in the 802.1X schema that specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span> <span data-ttu-id="58ac3-172">Pour plus d’informations, consultez l' [**élément heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-172">For more information, see the [**heldPeriod (OneX) Element**](onexschema-heldperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-173">**dwAuthPeriod**</span><span class="sxs-lookup"><span data-stu-id="58ac3-173">**dwAuthPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-174">Élément authPeriod dans le schéma 802.1 X qui spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="58ac3-174">The authPeriod element in the 802.1X schema that specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="58ac3-175">Si aucune réponse n’est reçue pendant la période spécifiée, le client part du principe qu’aucun authentificateur n’est présent sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="58ac3-175">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="58ac3-176">Pour plus d’informations, consultez l' [**élément authPeriod (Onex)**](onexschema-authperiod-onex-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-176">For more information, see the [**authPeriod (OneX) Element**](onexschema-authperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-177">**dwStartPeriod**</span><span class="sxs-lookup"><span data-stu-id="58ac3-177">**dwStartPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-178">Élément startPeriod dans le schéma 802.1 X qui spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="58ac3-178">The startPeriod element in the 802.1X schema that specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="58ac3-179">Un message de EAPOL-Start est envoyé pour démarrer le processus d’authentification 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="58ac3-179">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span> <span data-ttu-id="58ac3-180">Pour plus d’informations, consultez l' [**élément startPeriod (Onex)**](onexschema-startperiod-onex-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-180">For more information, see the [**startPeriod (OneX) Element**](onexschema-startperiod-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-181">**dwMaxStart**</span><span class="sxs-lookup"><span data-stu-id="58ac3-181">**dwMaxStart**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-182">Élément maxStart dans le schéma 802.1 X qui spécifie le nombre maximal de messages EAPOL-Start envoyés.</span><span class="sxs-lookup"><span data-stu-id="58ac3-182">The maxStart element in the 802.1X schema that specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="58ac3-183">Une fois que le nombre maximal de messages de EAPOL-Start a été envoyé, le client suppose qu’il n’y a aucun authentificateur présent sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="58ac3-183">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span> <span data-ttu-id="58ac3-184">Pour plus d’informations, consultez l' [**élément Maxstart (Onex)**](onexschema-maxstart-onex-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-184">For more information, see the [**maxStart (OneX) Element**](onexschema-maxstart-onex-element.md) in the 802.1X scheme.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-185">**dwMaxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="58ac3-185">**dwMaxAuthFailures**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-186">Élément maxAuthFailures dans le schéma 802.1 X qui spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="58ac3-186">The maxAuthFailures element in the 802.1X schema that specifies the maximum number of authentication failures allowed for a set of credentials.</span></span> <span data-ttu-id="58ac3-187">Pour plus d’informations, consultez l’élément [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-187">For more information, see the [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-188">**dwNetworkAuthTimeout**</span><span class="sxs-lookup"><span data-stu-id="58ac3-188">**dwNetworkAuthTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-189">Durée, en secondes, d’attente de l’achèvement de l’authentification 802.1 X avant le démarrage de l’ouverture de session normale.</span><span class="sxs-lookup"><span data-stu-id="58ac3-189">The time, in seconds, to wait for 802.1X authentication completion before normal logon proceeds.</span></span> <span data-ttu-id="58ac3-190">Cette valeur est utilisée dans les scénarios d’authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="58ac3-190">This value is used in single signon (SSO) scenarios.</span></span> <span data-ttu-id="58ac3-191">Cette valeur est par défaut de 10 secondes dans un profil 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="58ac3-191">This value defaults to 10 seconds in an 802.1X profile.</span></span> <span data-ttu-id="58ac3-192">Pour plus d’informations, consultez l' [**élément maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-192">For more information, see the [**maxDelay (singleSignOn) Element**](onexschema-maxdelay-singlesignon-element.md) in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-193">**dwNetworkAuthWithUITimeout**</span><span class="sxs-lookup"><span data-stu-id="58ac3-193">**dwNetworkAuthWithUITimeout**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-194">Durée maximale, en secondes, d’attente d’une connexion au cas où une boîte de dialogue d’interface utilisateur nécessitant une entrée utilisateur s’affiche pendant l’authentification unique par ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="58ac3-194">The maximum duration time, in seconds, to wait for a connection in case a user interface dialog box that requires user input is displayed during the per-logon SSO.</span></span>

<span data-ttu-id="58ac3-195">Sur Windows Vista avec SP1 et versions ultérieures, cette valeur est codée en dur à 10 minutes et n’est pas configurable.</span><span class="sxs-lookup"><span data-stu-id="58ac3-195">On Windows Vista with SP1 and later, this value is hardcoded to 10 minutes and is not configurable.</span></span> <span data-ttu-id="58ac3-196">Sur Windows Vista en production, cette valeur est définie par défaut sur 60 secondes dans un profil 802.1 X et est contrôlée par l’élément **maxDelayWithAdditionalDialogs** dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="58ac3-196">On Windows Vista Release to Manufacturing, this value defaults to 60 seconds in an 802.1X profile and was controlled by the **maxDelayWithAdditionalDialogs** element in the schema.</span></span>

<span data-ttu-id="58ac3-197">Sur Windows Vista avec SP1 et versions ultérieures, l’élément **maxDelayWithAdditionalDialogs** dans le schéma 802.1 x est ignoré et déconseillé.</span><span class="sxs-lookup"><span data-stu-id="58ac3-197">On Windows Vista with SP1 and later, the **maxDelayWithAdditionalDialogs** element in the 802.1X schema is ignored and deprecated.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-198">**bAllowLogonDialogs**</span><span class="sxs-lookup"><span data-stu-id="58ac3-198">**bAllowLogonDialogs**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-199">Valeur qui spécifie s’il faut autoriser l’affichage de boîtes de dialogue EAP lors de l’utilisation de l’authentification unique préalable à l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="58ac3-199">A value that specifies whether to allow EAP dialogs to be displayed when using pre-logon SSO.</span></span> <span data-ttu-id="58ac3-200">Pour plus d’informations, consultez l’élément **allowAdditionalDialogs** dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-200">For more information, see the **allowAdditionalDialogs** element in the 802.1X schema.</span></span>

</dd> <dt>

<span data-ttu-id="58ac3-201">**bUserBasedVLan**</span><span class="sxs-lookup"><span data-stu-id="58ac3-201">**bUserBasedVLan**</span></span>
</dt> <dd>

<span data-ttu-id="58ac3-202">Élément userBasedVirtualLan dans le schéma 802.1 X qui spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58ac3-202">The userBasedVirtualLan element in the 802.1X schema that specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="58ac3-203">Certains périphériques NAS (Network Access Server) modifient le réseau local virtuel après l’authentification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58ac3-203">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="58ac3-204">Quand userBasedVirtualLan a la valeur TRUE, le NAS peut modifier le réseau local virtuel d’un appareil après l’authentification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="58ac3-204">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span> <span data-ttu-id="58ac3-205">Pour plus d’informations, consultez l' [**élément userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) dans le schéma 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-205">For more information, see the [**userBasedVirtualLan (singleSignOn) Element**](onexschema-userbasedvirtuallan-singlesignon-element.md) in the 802.1X scheme.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58ac3-206">Notes</span><span class="sxs-lookup"><span data-stu-id="58ac3-206">Remarks</span></span>

<span data-ttu-id="58ac3-207">La structure du **\_ \_ profil de connexion Onex** est utilisée par le module 802.1 x, un nouveau composant de configuration sans fil pris en charge sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="58ac3-207">The **ONEX\_CONNECTION\_PROFILE** structure is used by the 802.1X module, a new wireless configuration component supported on Windows Vista and later.</span></span>

<span data-ttu-id="58ac3-208">Les [**\_ données de \_ mise \_ à jour du résultat Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contiennent des informations sur un changement d’état de l’authentification 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-208">The [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contains information on a status change to 802.1X authentication.</span></span> <span data-ttu-id="58ac3-209">La structure de **\_ \_ \_ données de mise à jour du résultat Onex** est retournée lorsque le membre **NotificationSource** de la structure de [**\_ \_ données de notification WLAN**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) est **\_ source de notification \_ \_ WLAN** et que le membre **NotificationCode** de la structure de **\_ \_ données de notification WLAN** pour la notification reçue est **OneXNotificationTypeResultUpdate**.</span><span class="sxs-lookup"><span data-stu-id="58ac3-209">The **ONEX\_RESULT\_UPDATE\_DATA** structure is returned when the **NotificationSource** member of the [**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) structure is **WLAN\_NOTIFICATION\_SOURCE\_ONEX** and the **NotificationCode** member of the **WLAN\_NOTIFICATION\_DATA** structure for received notification is **OneXNotificationTypeResultUpdate**.</span></span> <span data-ttu-id="58ac3-210">Pour cette notification, le membre **pData** de la structure de **\_ \_ données de notification WLAN** pointe vers une structure de **\_ \_ \_ données de mise à jour de résultat Onex** qui contient des informations sur le changement d’état d’authentification 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="58ac3-210">For this notification, the **pData** member of the **WLAN\_NOTIFICATION\_DATA** structure points to an **ONEX\_RESULT\_UPDATE\_DATA** structure that contains information on the 802.1X authentication status change.</span></span>

<span data-ttu-id="58ac3-211">Si le membre **fOneXAuthParams** dans la structure de [**\_ \_ \_ données de mise à jour du résultat Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) est défini, le membre **authParams** de la structure de **\_ \_ \_ données de mise à jour du résultat Onex** contient une structure d' [**\_ \_ objet blob de variable Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) avec une structure de [**\_ \_ paramètres d’authentification Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) incorporée à partir du membre **dwOffset** de l' **\_ \_ objet blob de variable Onex**.</span><span class="sxs-lookup"><span data-stu-id="58ac3-211">If the **fOneXAuthParams** member in the [**ONEX\_RESULT\_UPDATE\_DATA**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) structure is set, then the **authParams** member of the **ONEX\_RESULT\_UPDATE\_DATA** structure contains an [**ONEX\_VARIABLE\_BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) structure with an [**ONEX\_AUTH\_PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span> <span data-ttu-id="58ac3-212">Le **membre oneXConnProfile** de la structure de **\_ \_ paramètres d’authentification Onex** contient une structure d' **\_ \_ objet blob de variable Onex** avec une structure de **\_ \_ profil de connexion Onex** incorporée à partir du membre **dwOffset** de l' **\_ \_ objet blob de variable Onex**.</span><span class="sxs-lookup"><span data-stu-id="58ac3-212">The **oneXConnProfile** member of the **ONEX\_AUTH\_PARAMS** structure contains an **ONEX\_VARIABLE\_BLOB** structure with an **ONEX\_CONNECTION\_PROFILE** structure embedded starting at the **dwOffset** member of the **ONEX\_VARIABLE\_BLOB**.</span></span>

<span data-ttu-id="58ac3-213">La structure du **\_ \_ profil de connexion Onex** n’est pas définie dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="58ac3-213">The **ONEX\_CONNECTION\_PROFILE** structure is not defined in a public header file.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ac3-214">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58ac3-214">Requirements</span></span>



| <span data-ttu-id="58ac3-215">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58ac3-215">Requirement</span></span> | <span data-ttu-id="58ac3-216">Valeur</span><span class="sxs-lookup"><span data-stu-id="58ac3-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58ac3-217">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ac3-217">Minimum supported client</span></span><br/> | <span data-ttu-id="58ac3-218">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58ac3-218">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58ac3-219">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58ac3-219">Minimum supported server</span></span><br/> | <span data-ttu-id="58ac3-220">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="58ac3-220">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58ac3-221">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58ac3-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ac3-222">À propos de l’architecture ACM</span><span class="sxs-lookup"><span data-stu-id="58ac3-222">About the ACM Architecture</span></span>](about-the-acm-architecture.md)
</dt> <dt>

[<span data-ttu-id="58ac3-223">Schéma OneX</span><span class="sxs-lookup"><span data-stu-id="58ac3-223">OneX Schema</span></span>](onexschema-schema.md)
</dt> <dt>

[<span data-ttu-id="58ac3-224">**Élément authMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-224">**authMode (OneX) Element**</span></span>](onexschema-authmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-225">**Élément authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-225">**authPeriod (OneX) Element**</span></span>](onexschema-authperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-226">**Élément heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-226">**heldPeriod (OneX) Element**</span></span>](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-227">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-227">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-228">**Élément maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-228">**maxStart (OneX) Element**</span></span>](onexschema-maxstart-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-229">**Élément startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-229">**startPeriod (OneX) Element**</span></span>](onexschema-startperiod-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-230">**Élément supplicantMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-230">**supplicantMode (OneX) Element**</span></span>](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-231">**Élément userBasedVirtualLan (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="58ac3-231">**userBasedVirtualLan (singleSignOn) Element**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-232">**\_paramètres d’authentification Onex \_**</span><span class="sxs-lookup"><span data-stu-id="58ac3-232">**ONEX\_AUTH\_PARAMS**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[<span data-ttu-id="58ac3-233">**\_type de notification Onex \_**</span><span class="sxs-lookup"><span data-stu-id="58ac3-233">**ONEX\_NOTIFICATION\_TYPE**</span></span>](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[<span data-ttu-id="58ac3-234">**\_données de \_ mise à jour du résultat Onex \_**</span><span class="sxs-lookup"><span data-stu-id="58ac3-234">**ONEX\_RESULT\_UPDATE\_DATA**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[<span data-ttu-id="58ac3-235">**Élément de schéma OneX**</span><span class="sxs-lookup"><span data-stu-id="58ac3-235">**OneX Schema Element**</span></span>](onexschema-onex-element.md)
</dt> <dt>

[<span data-ttu-id="58ac3-236">**\_blob de variable Onex \_**</span><span class="sxs-lookup"><span data-stu-id="58ac3-236">**ONEX\_VARIABLE\_BLOB**</span></span>](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

<span data-ttu-id="58ac3-237">[**\_données de notification WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="58ac3-237">[**WLAN\_NOTIFICATION\_DATA**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="58ac3-238">**WlanRegisterNotification**</span><span class="sxs-lookup"><span data-stu-id="58ac3-238">**WlanRegisterNotification**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
