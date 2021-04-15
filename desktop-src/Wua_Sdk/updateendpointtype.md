---
description: Définit le type de points de terminaison qui peuvent être utilisés pour se connecter à un service.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Énumération UpdateEndpointType (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525072"
---
# <a name="updateendpointtype-enumeration"></a><span data-ttu-id="b846f-103">Énumération UpdateEndpointType</span><span class="sxs-lookup"><span data-stu-id="b846f-103">UpdateEndpointType enumeration</span></span>

<span data-ttu-id="b846f-104">Définit le type de points de terminaison qui peuvent être utilisés pour se connecter à un service.</span><span class="sxs-lookup"><span data-stu-id="b846f-104">Defines the type of endpoints that can be used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b846f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b846f-105">Syntax</span></span>


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a><span data-ttu-id="b846f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b846f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b846f-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span><span class="sxs-lookup"><span data-stu-id="b846f-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="b846f-108">Point de terminaison client-serveur utilisé pour se connecter au service de mise à jour, tel que Windows Update, Microsoft Update et serveur WSUS dans un environnement d’entreprise, pour rechercher des informations sur les mises à jour qui peuvent s’appliquer à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b846f-108">A client-server endpoint that is used to connect to the update service, such as Windows Update, Microsoft Update, and WSUS server in a corporate environment, to find information on updates that may be applicable to the computer.</span></span>

<span data-ttu-id="b846f-109">Le service de mise à jour retourne des informations sur les mises à jour qui ont été publiées, révisées ou retirées depuis la dernière synchronisation avec le serveur par le client.</span><span class="sxs-lookup"><span data-stu-id="b846f-109">The update service returns information on updates that have been published, revised, or withdrawn since the last time that client performed a sync with the server.</span></span>

</dd> <dt>

<span data-ttu-id="b846f-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span><span class="sxs-lookup"><span data-stu-id="b846f-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>
</dt> <dd>

<span data-ttu-id="b846f-111">Point de terminaison de création de rapports utilisé lorsque le client signale les résultats des analyses, des téléchargements et des réinstallations dans le service de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b846f-111">A reporting endpoint that is used when the client reports the results of scans, downloads, and installs back to the update service.</span></span>

<span data-ttu-id="b846f-112">Dans le cas des services publics (Windows Update et Microsoft Update), cette opération est effectuée à des fins de surveillance de la qualité.</span><span class="sxs-lookup"><span data-stu-id="b846f-112">In the case of public services (Windows Update and Microsoft Update), this is done for quality monitoring purposes.</span></span>

<span data-ttu-id="b846f-113">Dans le cas de services privés, tels qu’un serveur WSUS d’entreprise, le type de point de terminaison thhis permet également au serveur de collecter l’inventaire et d’autres informations sur les ordinateurs clients sous gestion.</span><span class="sxs-lookup"><span data-stu-id="b846f-113">In the case of private services, such as a corporate WSUS server, thhis type of endpoint also allows the server to collect inventory and other information about the client computers under management.</span></span>

</dd> <dt>

<span data-ttu-id="b846f-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span><span class="sxs-lookup"><span data-stu-id="b846f-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="b846f-115">Point de terminaison à mise à jour automatique qui est utilisé lorsque l’ordinateur client contacte un service de mise à jour pour déterminer s’il existe une nouvelle version du logiciel client de l’agent Windows Update.</span><span class="sxs-lookup"><span data-stu-id="b846f-115">A self-update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

<span data-ttu-id="b846f-116">Le point de terminaison de mise à jour automatique utilise un protocole différent, puis le point de terminaison Client-Server pour que les mises à jour automatiques puissent être distribuées même en cas de condition d’erreur susceptible d’empêcher la synchronisation client-serveur normale de fonctionner sur un ordinateur client particulier.</span><span class="sxs-lookup"><span data-stu-id="b846f-116">The Self-update endpoint uses a different protocol then the Client-Server endpoint so that self-updates can be distributed even if there is an error condition that might be preventing the normal client-server sync from working on a particular client computer.</span></span>

</dd> <dt>

<span data-ttu-id="b846f-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span><span class="sxs-lookup"><span data-stu-id="b846f-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>
</dt> <dd>

<span data-ttu-id="b846f-118">Point de terminaison de réglementation utilisé lorsque l’ordinateur client contacte le service de régulation pour agir sur une mise à jour particulière applicable à l’ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="b846f-118">A regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

<span data-ttu-id="b846f-119">Le service de régulation peut indiquer si la mise à jour est « réglementée » (également appelée « limitation »). en d’autres termes, le service de régulation peut indiquer à l’ordinateur client qu’il ne doit pas agir sur une mise à jour particulière, même si cette mise à jour s’applique.</span><span class="sxs-lookup"><span data-stu-id="b846f-119">The regulation service can indicate whether the update is “regulated” (also known as “throttled”) – in other words, the regulation service can tell the client computer that it should not act on a particular update, even though that update appears to be applicable.</span></span>

</dd> <dt>

<span data-ttu-id="b846f-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span><span class="sxs-lookup"><span data-stu-id="b846f-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>
</dt> <dd>

<span data-ttu-id="b846f-121">Point de terminaison de ciblage simple utilisé uniquement avec les services privés (serveurs WSUS dans les environnements d’entreprise).</span><span class="sxs-lookup"><span data-stu-id="b846f-121">A simple-targeting endpoint that is used only with private services (WSUS servers in corporate environments).</span></span> <span data-ttu-id="b846f-122">Dans un environnement d’entreprise, les ordinateurs clients peuvent être attribués à des groupes cibles particuliers et les mises à jour peuvent être installées sur les ordinateurs de certains groupes, mais pas sur d’autres.</span><span class="sxs-lookup"><span data-stu-id="b846f-122">In a corporate environment, client computers can be assigned to particular target groups, and updates can be approved for installation on computers in some groups but not others.</span></span>

<span data-ttu-id="b846f-123">Par exemple, l’administrateur WSUS peut créer un groupe de « test » pour les ordinateurs utilisés pour tester les nouvelles mises à jour, et l’administrateur peut approuver les mises à jour nouvellement publiées à installer sur les ordinateurs du groupe de test sans les approuver pour l’installation sur d’autres ordinateurs de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="b846f-123">For example, the WSUS administrator may create a “Testing” group for computers that are used to test new updates, and the administrator may approve newly-released updates for installation on computers in the Testing group without approving them for installation on other computers in the organization.</span></span> <span data-ttu-id="b846f-124">Le simple ciblage d’Exchange est utilisé pour permettre à un ordinateur client de s’inscrire auprès du serveur WSUS et d’autoriser le serveur à indiquer à l’ordinateur client le groupe dans lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="b846f-124">The simple targeting exchange is used to allow a client computer to register itself with the WSUS server, and to allow the server to tell the client computer what group it is in.</span></span>

</dd> <dt>

<span data-ttu-id="b846f-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span><span class="sxs-lookup"><span data-stu-id="b846f-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="b846f-126">Point de terminaison sécurisé client-serveur qui permet à un client d’obtenir des informations sur les applications qui ont besoin d’une licence pour pouvoir les utiliser sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="b846f-126">A secured-client-server endpoint that allows a client to obtain info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="b846f-127">Cette infrastructure de licences est actuellement utilisée uniquement par Windows 8 pour déployer des applications et des mises à jour obtenues par le biais du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b846f-127">This licensing framework is currently only used by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="b846f-128">Le point de terminaison sécurisé-client-serveur n’est actuellement pas utilisé par Windows Update, Microsoft Update ou WSUS.</span><span class="sxs-lookup"><span data-stu-id="b846f-128">The secured-client-server endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> <dt>

<span data-ttu-id="b846f-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span><span class="sxs-lookup"><span data-stu-id="b846f-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span></span>
</dt> <dd>

<span data-ttu-id="b846f-130">Le point de terminaison d’authentification de service secondaire est utilisé par un client pour fournir l’authentification avant d’obtenir des informations sur les applications qui ont besoin d’une licence pour pouvoir les utiliser sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="b846f-130">The secondary-service-authentication endpoint is used by a client to provide authentication before it obtains info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="b846f-131">Cette infrastructure de licences est actuellement utilisée uniquement par Windows 8 pour déployer des applications et des mises à jour obtenues par le biais du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b846f-131">This licensing framework is currently only utilized by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="b846f-132">Le point de terminaison d’authentification de service secondaire n’est actuellement pas utilisé par Windows Update, Microsoft Update ou WSUS.</span><span class="sxs-lookup"><span data-stu-id="b846f-132">The secondary-service-authentication endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b846f-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b846f-133">Requirements</span></span>



| <span data-ttu-id="b846f-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b846f-134">Requirement</span></span> | <span data-ttu-id="b846f-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b846f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b846f-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b846f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b846f-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b846f-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="b846f-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b846f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b846f-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b846f-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b846f-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="b846f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b846f-141"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="b846f-141"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="b846f-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="b846f-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b846f-143"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b846f-143"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




