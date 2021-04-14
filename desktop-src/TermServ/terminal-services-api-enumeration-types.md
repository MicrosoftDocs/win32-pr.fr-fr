---
title: Types d’énumération d’API Services Bureau à distance
description: Répertorie les types énumération utilisés avec l’API Services Bureau à distance.
ms.assetid: b5ef61e2-07fa-4963-9b9b-977cc04dab10
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9523a7528fddff4e2dbcf6dde16c29084d4811d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310345"
---
# <a name="remote-desktop-services-api-enumeration-types"></a><span data-ttu-id="a549a-103">Types d’énumération d’API Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="a549a-103">Remote Desktop Services API Enumeration Types</span></span>

<span data-ttu-id="a549a-104">Les types d’énumération suivants sont utilisés avec l’API Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="a549a-104">The following enumeration types are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a549a-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a549a-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a549a-106">**\_classe de configuration WTS \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-106">**WTS\_CONFIG\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_class)
</dt> <dd>

<span data-ttu-id="a549a-107">Contient des valeurs qui indiquent le type d’informations de configuration utilisateur à définir ou à récupérer dans un appel aux fonctions [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) et [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="a549a-107">Contains values that indicate the type of user configuration information to set or retrieve in a call to the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) and [**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga) functions.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-108">**\_source de configuration WTS \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-108">**WTS\_CONFIG\_SOURCE**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_config_source)
</dt> <dd>

<span data-ttu-id="a549a-109">Spécifie la source des informations de configuration retournées par la fonction [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) .</span><span class="sxs-lookup"><span data-stu-id="a549a-109">Specifies the source of configuration information returned by the [**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga) function.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-110">**WTS \_ CONNECTSTATE, \_ classe**</span><span class="sxs-lookup"><span data-stu-id="a549a-110">**WTS\_CONNECTSTATE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_connectstate_class)
</dt> <dd>

<span data-ttu-id="a549a-111">Spécifie l’état de connexion d’une session de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="a549a-111">Specifies the connection state of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-112">**\_classe WTS info \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-112">**WTS\_INFO\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_info_class)
</dt> <dd>

<span data-ttu-id="a549a-113">Contient des valeurs qui indiquent le type d’informations de session à récupérer dans un appel à la fonction [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="a549a-113">Contains values that indicate the type of session information to retrieve in a call to the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-114">**\_classe de type WTS \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-114">**WTS\_TYPE\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_type_class)
</dt> <dd>

<span data-ttu-id="a549a-115">Spécifie le type de structure qu’une fonction de Services Bureau à distance a retourné dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a549a-115">Specifies the type of structure that a Remote Desktop Services function has returned in a buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-116">**\_classe virtuelle \_ WTS**</span><span class="sxs-lookup"><span data-stu-id="a549a-116">**WTS\_VIRTUAL\_CLASS**</span></span>](/windows/desktop/api/Wtsapi32/ne-wtsapi32-wts_virtual_class)
</dt> <dd>

<span data-ttu-id="a549a-117">Contient des valeurs qui indiquent le type d’informations de canal virtuel à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a549a-117">Contains values that indicate the type of virtual channel information to retrieve.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-118">**\_famille d’adresses WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-118">**WTSSBX\_ADDRESS\_FAMILY**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_address_family)
</dt> <dd>

<span data-ttu-id="a549a-119">Contient des valeurs qui indiquent la famille d’adresses d’une adresse réseau utilisée pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="a549a-119">Contains values that indicate the address family of a network address that is being used for redirection.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-120">**\_drain machine \_ WTSSBX**</span><span class="sxs-lookup"><span data-stu-id="a549a-120">**WTSSBX\_MACHINE\_DRAIN**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_drain)
</dt> <dd>

<span data-ttu-id="a549a-121">Contient des valeurs qui indiquent l’état de drainage d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="a549a-121">Contains values that indicate the drain state of a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-122">**MODE de session de l' \_ ordinateur WTSSBX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-122">**WTSSBX\_MACHINE\_SESSION\_MODE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_session_mode)
</dt> <dd>

<span data-ttu-id="a549a-123">Contient des valeurs qui indiquent le mode de session d’un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="a549a-123">Contains values that indicate the session mode of a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-124">**État de l' \_ ordinateur WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-124">**WTSSBX\_MACHINE\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_machine_state)
</dt> <dd>

<span data-ttu-id="a549a-125">Contient des valeurs qui indiquent l’état actuel d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="a549a-125">Contains values that indicate the current state of a server.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-126">**\_type de notification WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-126">**WTSSBX\_NOTIFICATION\_TYPE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type)
</dt> <dd>

<span data-ttu-id="a549a-127">Contient des valeurs qui indiquent le type de modification d’État qui s’est produit sur un serveur hôte de session Bureau à distance ou une session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a549a-127">Contains values that indicate the type of status change that occurred on a RD Session Host server or a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="a549a-128">**\_État de session WTSSBX \_**</span><span class="sxs-lookup"><span data-stu-id="a549a-128">**WTSSBX\_SESSION\_STATE**</span></span>](/windows/win32/api/tssbx/ne-tssbx-wtssbx_session_state)
</dt> <dd>

<span data-ttu-id="a549a-129">Contient des valeurs qui indiquent l’état de connexion d’une session utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a549a-129">Contains values that indicate the connection state of a user session.</span></span>

</dd> </dl>

 

 




