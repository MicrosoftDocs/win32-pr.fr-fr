---
title: Interface INapCertRelyingParty (NapCertRelyingParty. h)
description: Les parties de confiance de certificat doivent utiliser pour communiquer avec le NapAgent.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- NAP de l’interface INapCertRelyingParty
- INapCertRelyingParty interface NAP, Description
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033031"
---
# <a name="inapcertrelyingparty-interface"></a><span data-ttu-id="5cd15-105">Interface INapCertRelyingParty</span><span class="sxs-lookup"><span data-stu-id="5cd15-105">INapCertRelyingParty interface</span></span>

> [!Note]  
> <span data-ttu-id="5cd15-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5cd15-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5cd15-107">L’interface **INapCertRelyingParty** fournit des méthodes que les parties de confiance de certificat doivent utiliser pour communiquer avec le NapAgent.</span><span class="sxs-lookup"><span data-stu-id="5cd15-107">The **INapCertRelyingParty** interface provides methods that certificate-relying parties must use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="5cd15-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5cd15-108">Members</span></span>

<span data-ttu-id="5cd15-109">L’interface **INapCertRelyingParty** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5cd15-109">The **INapCertRelyingParty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5cd15-110">**INapCertRelyingParty** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5cd15-110">**INapCertRelyingParty** also has these types of members:</span></span>

-   [<span data-ttu-id="5cd15-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5cd15-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5cd15-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5cd15-112">Methods</span></span>

<span data-ttu-id="5cd15-113">L’interface **INapCertRelyingParty** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5cd15-113">The **INapCertRelyingParty** interface has these methods.</span></span>



| <span data-ttu-id="5cd15-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="5cd15-114">Method</span></span>                                                                                                        | <span data-ttu-id="5cd15-115">Description</span><span class="sxs-lookup"><span data-stu-id="5cd15-115">Description</span></span>                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="5cd15-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span><span class="sxs-lookup"><span data-stu-id="5cd15-116">**INapCertRelyingParty::GetSubscribedRelyingParties**</span></span>](inapcertrelyingparty-getsubscribedrelyingparties.md) | <span data-ttu-id="5cd15-117">Obtient une liste des parties de confiance qui sont abonnées.</span><span class="sxs-lookup"><span data-stu-id="5cd15-117">Gets a list of relying parties that have subscribed.</span></span><br/>                 |
| [<span data-ttu-id="5cd15-118">**INapCertRelyingParty::SubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="5cd15-118">**INapCertRelyingParty::SubscribeCertByGroup**</span></span>](inapcertrelyingparty-subscribecertbygroup.md)               | <span data-ttu-id="5cd15-119">S’abonne à un serveur de certificat d’intégrité déjà inscrit (HCS).</span><span class="sxs-lookup"><span data-stu-id="5cd15-119">Subscribes to an already-registered health certificate server (HCS).</span></span><br/> |
| [<span data-ttu-id="5cd15-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span><span class="sxs-lookup"><span data-stu-id="5cd15-120">**INapCertRelyingParty::UnSubscribeCertByGroup**</span></span>](inapcertrelyingparty-unsubscribecertbygroup.md)           | <span data-ttu-id="5cd15-121">Annule l’abonnement d’un serveur HCS.</span><span class="sxs-lookup"><span data-stu-id="5cd15-121">Unsubscribes from an HCS server.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="5cd15-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cd15-122">Requirements</span></span>



| <span data-ttu-id="5cd15-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cd15-123">Requirement</span></span> | <span data-ttu-id="5cd15-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cd15-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd15-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cd15-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5cd15-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cd15-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5cd15-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cd15-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5cd15-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cd15-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5cd15-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cd15-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cd15-130"><dt>NapCertRelyingParty. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cd15-130"><dt>NapCertRelyingParty.h</dt></span></span> </dl>   |
| <span data-ttu-id="5cd15-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="5cd15-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5cd15-132"><dt>NapCertRelyingParty. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5cd15-132"><dt>NapCertRelyingParty.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cd15-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cd15-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cd15-134">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="5cd15-134">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="5cd15-135">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="5cd15-135">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

