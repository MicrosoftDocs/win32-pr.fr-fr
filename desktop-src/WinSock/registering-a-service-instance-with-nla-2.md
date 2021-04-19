---
description: Les clients NLA peuvent enregistrer les informations de configuration du réseau à l’échelle du système, ce qui permet aux futures requêtes de retourner les informations de configuration spécifiées, que le réseau soit actif ou non.
ms.assetid: 7e92dd8f-d3a1-4e53-885c-ebc9626fd5dc
title: Inscription d’une instance de service avec NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae2e73e638e4bf0152c2c6c5a4f5ab87dda7312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545809"
---
# <a name="registering-a-service-instance-with-nla"></a><span data-ttu-id="32587-103">Inscription d’une instance de service avec NLA</span><span class="sxs-lookup"><span data-stu-id="32587-103">Registering a Service Instance with NLA</span></span>

<span data-ttu-id="32587-104">Les clients NLA peuvent enregistrer les informations de configuration du réseau à l’échelle du système, ce qui permet aux futures requêtes de retourner les informations de configuration spécifiées, que le réseau soit actif ou non.</span><span class="sxs-lookup"><span data-stu-id="32587-104">NLA clients can record network configuration information on a system-wide basis, enabling future queries to return the specified configuration information regardless of whether the network is active.</span></span> <span data-ttu-id="32587-105">Cette fonctionnalité permet aux clients NLA d’affecter une expérience utilisateur d’informations réseau cohérente sur plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="32587-105">This capability allows NLA clients to affect a consistent network information user experience across multiple applications.</span></span>

## <a name="parameters"></a><span data-ttu-id="32587-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32587-106">Parameters</span></span>

<span data-ttu-id="32587-107">Pour inscrire une instance de service auprès du fournisseur de service de reconnaissance d’emplacement réseau, utilisez la fonction [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) .</span><span class="sxs-lookup"><span data-stu-id="32587-107">To register a service instance with the Network Location Awareness service provider, use the [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function.</span></span> <span data-ttu-id="32587-108">Pour pouvoir inscrire correctement une instance de service, certains paramètres de la fonction **WSASetService** doivent être définis avec les informations appropriées, comme expliqué dans cette section.</span><span class="sxs-lookup"><span data-stu-id="32587-108">In order to properly register a service instance certain parameters of the **WSASetService** function must be set with the appropriate information, as explained in this section.</span></span> <span data-ttu-id="32587-109">Pour référence rapide, la fonction **WSASetService** a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="32587-109">For quick reference, the **WSASetService** function has the following syntax:</span></span>

``` syntax
INT WSASetService(
  LPWSAQUERYSET lpqsRegInfo,
  WSAESETSERVICEOP essOperation,
  DWORD dwControlFlags
);
```

<span data-ttu-id="32587-110">Pour le paramètre *lpqsRegInfo* , fournissez une structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) à partir d’un résultat de requête NLA SP ou construite conformément aux exigences d’une requête NLA SP, comme indiqué dans [interrogation NLA](querying-nla-2.md).</span><span class="sxs-lookup"><span data-stu-id="32587-110">For the *lpqsRegInfo* parameter, provide a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure from either an NLA SP query result, or constructed adhering to the requirements of an NLA SP query, as specified in [Querying NLA](querying-nla-2.md).</span></span>

<span data-ttu-id="32587-111">Les opérations prises en charge pour le paramètre *essOperation* sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="32587-111">Operations supported for the *essOperation* parameter are the following:</span></span>

<dl> <dt>

<span data-ttu-id="32587-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>\_Registre RNRSERVICE</span><span class="sxs-lookup"><span data-stu-id="32587-112"><span id="RNRSERVICE_REGISTER"></span><span id="rnrservice_register"></span>RNRSERVICE\_REGISTER</span></span>
</dt> <dd>

<span data-ttu-id="32587-113">Le réseau défini dans la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fournie dans *lpqsRegInfo* est rendu persistant pour l’utilisateur actif en stockant l’instance réseau dans la ruche du registre de l’utilisateur actuel, ce qui autorise l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="32587-113">The network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is made persistent for the active user by storing the network instance in the registry hive for the current user, which allows impersonation.</span></span>

</dd> <dt>

<span data-ttu-id="32587-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="32587-114"><span id="RNRSERVICE_DELETE"></span><span id="rnrservice_delete"></span>RNRSERVICE\_DELETE</span></span>
</dt> <dd>

<span data-ttu-id="32587-115">Si le réseau défini dans la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) fournie dans *lpqsRegInfo* est persistant, il sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="32587-115">If the network defined in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure provided in *lpqsRegInfo* is persistent, it will be removed.</span></span>

</dd> </dl>

<span data-ttu-id="32587-116">L’opération spécifiée dans le paramètre *essOperation* peut être modifiée par les options suivantes, qui peuvent être spécifiées avec binaire ou logique :</span><span class="sxs-lookup"><span data-stu-id="32587-116">The operation specified in the *essOperation* parameter can be modified by the following options, which can be specified with binary OR logic:</span></span>

<dl> <dt>

<span data-ttu-id="32587-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>\_nom convivial de l' \_ extension NLA</span><span class="sxs-lookup"><span data-stu-id="32587-117"><span id="NLA_FRIENDLY_NAME"></span><span id="nla_friendly_name"></span>NLA\_FRIENDLY\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="32587-118">Lorsqu’il est utilisé avec RNRSERVICE \_ Register, le champ *lpszComment* du réseau défini dans *lpqsRegInfo* est vérifié pour la validité et stocké de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="32587-118">When used with RNRSERVICE\_REGISTER, the *lpszComment* field of the network defined in *lpqsRegInfo* is checked for validity and stored persistently.</span></span> <span data-ttu-id="32587-119">Lorsqu’il est utilisé avec RNRSERVICE \_ Delete et que le réseau défini a un nom convivial, le nom convivial est supprimé, mais l’entrée réseau reste intacte.</span><span class="sxs-lookup"><span data-stu-id="32587-119">When used with RNRSERVICE\_DELETE and the defined network has a friendly name, the friendly name is removed but the network entry is left intact.</span></span>

</dd> <dt>

<span data-ttu-id="32587-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>\_réseau NLA ALLUSERS \_</span><span class="sxs-lookup"><span data-stu-id="32587-120"><span id="NLA_ALLUSERS_NETWORK"></span><span id="nla_allusers_network"></span>NLA\_ALLUSERS\_NETWORK</span></span>
</dt> <dd>

<span data-ttu-id="32587-121">Lorsqu’elle est utilisée avec RNRSERVICE \_ Register, l’entrée est stockée de façon permanente sous HKEY \_ local \_ machine, ce qui la rend disponible pendant les requêtes à tous les utilisateurs sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="32587-121">When used with RNRSERVICE\_REGISTER, the entry is stored persistently under HKEY\_LOCAL\_MACHINE, making it available during queries to all users on the local computer.</span></span> <span data-ttu-id="32587-122">Lorsqu’il est utilisé avec RNRSERVICE \_ Delete, le réseau spécifié est supprimé de HKEY \_ local \_ machine.</span><span class="sxs-lookup"><span data-stu-id="32587-122">When used with RNRSERVICE\_DELETE, the specified network is removed from HKEY\_LOCAL\_MACHINE.</span></span> <span data-ttu-id="32587-123">Une erreur est retournée si le réseau spécifié n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="32587-123">An error is returned if the specified network is not present.</span></span> <span data-ttu-id="32587-124">Pour supprimer un réseau de la ruche du registre de l’utilisateur actuel, cet indicateur ne doit pas être spécifié.</span><span class="sxs-lookup"><span data-stu-id="32587-124">In order to delete a network from the registry hive of the current user, this flag must not be specified.</span></span> <span data-ttu-id="32587-125">Cet indicateur n’est valide que dans le contexte de sécurité d’un administrateur système local.</span><span class="sxs-lookup"><span data-stu-id="32587-125">This flag is only valid in the security context of a local system administrator.</span></span>

</dd> </dl>

<span data-ttu-id="32587-126">NLA prend en charge les codes d’erreur suivants pour les appels de fonction [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="32587-126">NLA supports the following error codes for [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea) function calls:</span></span>

| <span data-ttu-id="32587-127">Error</span><span class="sxs-lookup"><span data-stu-id="32587-127">Error</span></span>             | <span data-ttu-id="32587-128">Signification</span><span class="sxs-lookup"><span data-stu-id="32587-128">Meaning</span></span>                                                                                                                                                                    |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32587-129">WSANOTINITIALISED</span><span class="sxs-lookup"><span data-stu-id="32587-129">WSANOTINITIALISED</span></span> | <span data-ttu-id="32587-130">Un appel réussi à la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) pour initialiser NLA n’a pas été effectué.</span><span class="sxs-lookup"><span data-stu-id="32587-130">A successful call to the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function to initialize NLA was not performed.</span></span>                                                                  |
| <span data-ttu-id="32587-131">WSAEACCESS</span><span class="sxs-lookup"><span data-stu-id="32587-131">WSAEACCESS</span></span>        | <span data-ttu-id="32587-132">\_ \_ Le réseau NLA AllUsers a été spécifié dans *dwControlFlags* alors qu’il n’est pas dans le contexte de sécurité d’un administrateur système local.</span><span class="sxs-lookup"><span data-stu-id="32587-132">NLA\_ALLUSERS\_NETWORK was specified in *dwControlFlags* while not in the security context of a local system administrator.</span></span>                                                |
| <span data-ttu-id="32587-133">WSAEALREADY</span><span class="sxs-lookup"><span data-stu-id="32587-133">WSAEALREADY</span></span>       | <span data-ttu-id="32587-134">Le réseau spécifié est déjà stocké de façon persistante de la manière demandée, et aucun indicateur n’a été spécifié dans *dwControlFlags* pour indiquer une mise à jour de l’entrée existante.</span><span class="sxs-lookup"><span data-stu-id="32587-134">The specified network is already persistently stored in the requested manner, and no flags were specified in *dwControlFlags* to indicate an update to the existing entry.</span></span> |
| <span data-ttu-id="32587-135">WSAEAFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="32587-135">WSAEAFNOSUPPORT</span></span>   | <span data-ttu-id="32587-136">Une famille de protocoles a été spécifiée pour laquelle il n’existe pas de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="32587-136">A protocol family was specified for which there is no support.</span></span> <span data-ttu-id="32587-137">Seules les familles de protocole IP sont prises en charge dans NLA.</span><span class="sxs-lookup"><span data-stu-id="32587-137">Only IP protocol families are supported in NLA.</span></span>                                                             |
| <span data-ttu-id="32587-138">WSAEPFNOSUPPORT</span><span class="sxs-lookup"><span data-stu-id="32587-138">WSAEPFNOSUPPORT</span></span>   | <span data-ttu-id="32587-139">Un protocole a été spécifié pour lequel il n’existe pas de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="32587-139">A protocol was specified for which there is no support.</span></span> <span data-ttu-id="32587-140">Seul le protocole IP est pris en charge dans NLA.</span><span class="sxs-lookup"><span data-stu-id="32587-140">Only IP protocol is supported in NLA.</span></span>                                                                              |



 

 

 



