---
title: Interface INapServerCallback (NapSystemHealthValidator. h)
description: Les validateurs d’intégrité utilisent pour signaler la fin de la requête asynchrone.
ms.assetid: 0138767a-9553-4de0-87da-97dd92906406
keywords:
- NAP de l’interface INapServerCallback
- INapServerCallback interface NAP, Description
topic_type:
- apiref
api_name:
- INapServerCallback
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18aaf900a603a577ec12835441c67c20453a5dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464342"
---
# <a name="inapservercallback-interface"></a><span data-ttu-id="536f9-105">Interface INapServerCallback</span><span class="sxs-lookup"><span data-stu-id="536f9-105">INapServerCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="536f9-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="536f9-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="536f9-107">**INapServerCallback** fournit une méthode que les validateurs d’intégrité du système utilisent pour signaler la fin de la requête asynchrone.</span><span class="sxs-lookup"><span data-stu-id="536f9-107">The **INapServerCallback** provides a method that SHVs use to signal asynchronous request completion.</span></span>

## <a name="members"></a><span data-ttu-id="536f9-108">Membres</span><span class="sxs-lookup"><span data-stu-id="536f9-108">Members</span></span>

<span data-ttu-id="536f9-109">L’interface **INapServerCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="536f9-109">The **INapServerCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="536f9-110">**INapServerCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="536f9-110">**INapServerCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="536f9-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="536f9-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="536f9-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="536f9-112">Methods</span></span>

<span data-ttu-id="536f9-113">L’interface **INapServerCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="536f9-113">The **INapServerCallback** interface has these methods.</span></span>



| <span data-ttu-id="536f9-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="536f9-114">Method</span></span>                                                                         | <span data-ttu-id="536f9-115">Description</span><span class="sxs-lookup"><span data-stu-id="536f9-115">Description</span></span>                                                        |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="536f9-116">**INapServerCallback :: OnComplete**</span><span class="sxs-lookup"><span data-stu-id="536f9-116">**INapServerCallback::OnComplete**</span></span>](inapservercallback-oncomplete-method.md) | <span data-ttu-id="536f9-117">Utilisé par les validateurs d’intégrité du système pour signaler la fin de la requête asynchrone.</span><span class="sxs-lookup"><span data-stu-id="536f9-117">Used by SHVs to signal asynchronous request completion.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="536f9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="536f9-118">Requirements</span></span>



| <span data-ttu-id="536f9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="536f9-119">Requirement</span></span> | <span data-ttu-id="536f9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="536f9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="536f9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="536f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="536f9-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="536f9-122">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="536f9-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="536f9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="536f9-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="536f9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="536f9-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="536f9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="536f9-126"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="536f9-126"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="536f9-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="536f9-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="536f9-128"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="536f9-128"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="536f9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="536f9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="536f9-130"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="536f9-130"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="536f9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="536f9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="536f9-132">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="536f9-132">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="536f9-133">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="536f9-133">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

