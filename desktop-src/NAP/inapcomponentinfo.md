---
title: Interface INapComponentInfo (NapCommon. h)
description: Fournit des méthodes que les composants de plug-in (tels que les Sha et les SHV) doivent implémenter pour que le système NAP communique avec eux.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- NAP de l’interface INapComponentInfo
- INapComponentInfo interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941920"
---
# <a name="inapcomponentinfo-interface"></a><span data-ttu-id="bac01-105">Interface INapComponentInfo</span><span class="sxs-lookup"><span data-stu-id="bac01-105">INapComponentInfo interface</span></span>

> [!Note]  
> <span data-ttu-id="bac01-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bac01-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bac01-107">L’interface **INapComponentInfo** fournit des méthodes que les composants de plug-in (tels que les Sha et les SHV) doivent implémenter pour que le système NAP communique avec eux.</span><span class="sxs-lookup"><span data-stu-id="bac01-107">The **INapComponentInfo** interface provides methods that plug-in components (such as SHAs and SHVs) must implement for the NAP system to communicate with them.</span></span> <span data-ttu-id="bac01-108">Le système NAP appelle l’implémentation de ces méthodes pour récupérer des informations d’administration statiques (par exemple, un nom convivial ou des chaînes localisées).</span><span class="sxs-lookup"><span data-stu-id="bac01-108">The NAP system calls your implementation of these methods to retrieve static administrative information (for example, friendly name or localized strings).</span></span>

## <a name="members"></a><span data-ttu-id="bac01-109">Membres</span><span class="sxs-lookup"><span data-stu-id="bac01-109">Members</span></span>

<span data-ttu-id="bac01-110">L’interface **INapComponentInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bac01-110">The **INapComponentInfo** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bac01-111">**INapComponentInfo** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bac01-111">**INapComponentInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="bac01-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bac01-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bac01-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bac01-113">Methods</span></span>

<span data-ttu-id="bac01-114">L’interface **INapComponentInfo** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bac01-114">The **INapComponentInfo** interface has these methods.</span></span>



| <span data-ttu-id="bac01-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="bac01-115">Method</span></span>                                                                                                         | <span data-ttu-id="bac01-116">Description</span><span class="sxs-lookup"><span data-stu-id="bac01-116">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bac01-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span><span class="sxs-lookup"><span data-stu-id="bac01-117">**INapComponentInfo::ConvertErrorCodeToMessageId**</span></span>](inapcomponentinfo-converterrorcodetomessageid-method.md) | <span data-ttu-id="bac01-118">Utilisé par le système NAP pour demander au client d’intégrité de convertir un code d’erreur HRESULT en ID de message.</span><span class="sxs-lookup"><span data-stu-id="bac01-118">Used by the NAP System to request the health client convert an HRESULT error code to a message ID.</span></span><br/> |
| [<span data-ttu-id="bac01-119">**INapComponentInfo :: GetDescription**</span><span class="sxs-lookup"><span data-stu-id="bac01-119">**INapComponentInfo::GetDescription**</span></span>](inapcomponentinfo-getdescription-method.md)                           | <span data-ttu-id="bac01-120">Utilisé par le système NAP pour obtenir la description d’un client d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="bac01-120">Used by the NAP System to get the description of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="bac01-121">**INapComponentInfo::GetFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="bac01-121">**INapComponentInfo::GetFriendlyName**</span></span>](inapcomponentinfo-getfriendlyname-method.md)                         | <span data-ttu-id="bac01-122">Utilisé par le système NAP pour obtenir le nom convivial d’un client d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="bac01-122">Used by the NAP System to get the friendly name of a health client.</span></span><br/>                                |
| [<span data-ttu-id="bac01-123">**INapComponentInfo::GetIcon**</span><span class="sxs-lookup"><span data-stu-id="bac01-123">**INapComponentInfo::GetIcon**</span></span>](inapcomponentinfo-geticon-method.md)                                         | <span data-ttu-id="bac01-124">Utilisé par le système NAP pour obtenir l’icône d’un client d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="bac01-124">Used by the NAP System to get the icon of a health client.</span></span><br/>                                         |
| [<span data-ttu-id="bac01-125">**INapComponentInfo::GetLocalizedString**</span><span class="sxs-lookup"><span data-stu-id="bac01-125">**INapComponentInfo::GetLocalizedString**</span></span>](inapcomponentinfo-getlocalizedstring-method.md)                   | <span data-ttu-id="bac01-126">Utilisé par le système NAP pour récupérer les chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="bac01-126">Used by the NAP System to get localized strings.</span></span><br/>                                                   |
| [<span data-ttu-id="bac01-127">**INapComponentInfo::GetVendorName**</span><span class="sxs-lookup"><span data-stu-id="bac01-127">**INapComponentInfo::GetVendorName**</span></span>](inapcomponentinfo-getvendorname-method.md)                             | <span data-ttu-id="bac01-128">Utilisé par le système NAP pour obtenir le nom du fournisseur d’un client d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="bac01-128">Used by the NAP System to get the vendor name of a health client.</span></span><br/>                                  |
| [<span data-ttu-id="bac01-129">**INapComponentInfo :: GetVersion**</span><span class="sxs-lookup"><span data-stu-id="bac01-129">**INapComponentInfo::GetVersion**</span></span>](inapcomponentinfo-getversion-method.md)                                   | <span data-ttu-id="bac01-130">Utilisé par le système NAP pour obtenir la version d’un client de contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="bac01-130">Used by the NAP System to get the version of a health client.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="bac01-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bac01-131">Requirements</span></span>



| <span data-ttu-id="bac01-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bac01-132">Requirement</span></span> | <span data-ttu-id="bac01-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="bac01-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bac01-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bac01-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bac01-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bac01-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bac01-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bac01-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bac01-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bac01-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bac01-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="bac01-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bac01-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="bac01-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="bac01-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="bac01-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bac01-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bac01-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bac01-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bac01-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bac01-143">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="bac01-143">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bac01-144">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="bac01-144">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

