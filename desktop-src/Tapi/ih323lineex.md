---
description: L’interface IH323LineEx est implémentée par le MSP H323 et n’est disponible que sur les objets d’adresse H. 323. Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interface IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535290"
---
# <a name="ih323lineex-interface"></a><span data-ttu-id="87420-104">Interface IH323LineEx</span><span class="sxs-lookup"><span data-stu-id="87420-104">IH323LineEx interface</span></span>

<span data-ttu-id="87420-105">\[**IH323LineEx** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="87420-105">\[**IH323LineEx** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="87420-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="87420-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="87420-107">L’interface **IH323LineEx** est implémentée par le [MSP H323](h323-msp.md) et n’est disponible que sur les objets d’adresse H. 323.</span><span class="sxs-lookup"><span data-stu-id="87420-107">The **IH323LineEx** interface is implemented by the [H323 MSP](h323-msp.md) and is available only on H.323 address objects.</span></span> <span data-ttu-id="87420-108">Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP.</span><span class="sxs-lookup"><span data-stu-id="87420-108">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span>

> [!Note]  
> <span data-ttu-id="87420-109">Toutes les méthodes dans cette interface doivent être appelées uniquement après l’inscription des appels entrants sur cette adresse.</span><span class="sxs-lookup"><span data-stu-id="87420-109">All methods in this interface should be called only after registering for incoming calls on this address.</span></span>

 

## <a name="members"></a><span data-ttu-id="87420-110">Membres</span><span class="sxs-lookup"><span data-stu-id="87420-110">Members</span></span>

<span data-ttu-id="87420-111">L’interface **IH323LineEx** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="87420-111">The **IH323LineEx** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="87420-112">**IH323LineEx** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="87420-112">**IH323LineEx** also has these types of members:</span></span>

-   [<span data-ttu-id="87420-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87420-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="87420-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="87420-114">Methods</span></span>

<span data-ttu-id="87420-115">L’interface **IH323LineEx** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="87420-115">The **IH323LineEx** interface has these methods.</span></span>



| <span data-ttu-id="87420-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="87420-116">Method</span></span>                                                                                 | <span data-ttu-id="87420-117">Description</span><span class="sxs-lookup"><span data-stu-id="87420-117">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="87420-118">**SetAlias**</span><span class="sxs-lookup"><span data-stu-id="87420-118">**SetAlias**</span></span>](ih323lineex-setalias.md)                                               | <span data-ttu-id="87420-119">Configure un alias H. 323 par défaut pour l’adresse.</span><span class="sxs-lookup"><span data-stu-id="87420-119">Configures a default H.323 alias for the address.</span></span><br/>             |
| [<span data-ttu-id="87420-120">**SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="87420-120">**SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md) | <span data-ttu-id="87420-121">Configure la pondération des préférences pour les fonctionnalités par défaut.</span><span class="sxs-lookup"><span data-stu-id="87420-121">Configures the preference weighting for default capabilities.</span></span><br/> |
| [<span data-ttu-id="87420-122">**SetExternalT120Address**</span><span class="sxs-lookup"><span data-stu-id="87420-122">**SetExternalT120Address**</span></span>](ih323lineex-setexternalt120address.md)                   | <span data-ttu-id="87420-123">Configure une adresse T. 120 externe pour l’échange de données.</span><span class="sxs-lookup"><span data-stu-id="87420-123">Configures an external T.120 address for data exchange.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="87420-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87420-124">Requirements</span></span>



| <span data-ttu-id="87420-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87420-125">Requirement</span></span> | <span data-ttu-id="87420-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="87420-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87420-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="87420-127">TAPI version</span></span><br/> | <span data-ttu-id="87420-128">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="87420-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="87420-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="87420-129">Header</span></span><br/>       | <dl> <span data-ttu-id="87420-130"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="87420-130"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="87420-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="87420-131">Library</span></span><br/>      | <dl> <span data-ttu-id="87420-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87420-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="87420-133">DLL</span><span class="sxs-lookup"><span data-stu-id="87420-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="87420-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87420-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="87420-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87420-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87420-136">MSP H323</span><span class="sxs-lookup"><span data-stu-id="87420-136">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

