---
title: Méthode ResourceLocator. AddSelector (WSManDisp. h)
description: Ajoute un sélecteur à l’objet ResourceLocator. Le sélecteur spécifie une instance particulière d’une ressource.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode AddSelector
- Méthode AddSelector Windows Remote Management, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, méthode AddSelector
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942176"
---
# <a name="resourcelocatoraddselector-method"></a><span data-ttu-id="e80e4-107">Méthode ResourceLocator. AddSelector</span><span class="sxs-lookup"><span data-stu-id="e80e4-107">ResourceLocator.AddSelector method</span></span>

<span data-ttu-id="e80e4-108">Ajoute un [*Sélecteur*](windows-remote-management-glossary.md) à l’objet [**ResourceLocator**](resourcelocator.md) .</span><span class="sxs-lookup"><span data-stu-id="e80e4-108">Adds a [*selector*](windows-remote-management-glossary.md) to the [**ResourceLocator**](resourcelocator.md) object.</span></span> <span data-ttu-id="e80e4-109">Le sélecteur spécifie une instance particulière d’une *ressource*.</span><span class="sxs-lookup"><span data-stu-id="e80e4-109">The selector specifies a particular instance of a *resource*.</span></span> <span data-ttu-id="e80e4-110">Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="e80e4-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e80e4-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e80e4-111">Syntax</span></span>


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a><span data-ttu-id="e80e4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e80e4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80e4-113">*resourceSelName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e80e4-113">*resourceSelName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80e4-114">Nom du sélecteur.</span><span class="sxs-lookup"><span data-stu-id="e80e4-114">The selector name.</span></span> <span data-ttu-id="e80e4-115">Par exemple, lors de la demande de données WMI, ce paramètre est la propriété de clé pour une classe WMI.</span><span class="sxs-lookup"><span data-stu-id="e80e4-115">For example, when requesting WMI data, this parameter is the key property for a WMI class.</span></span>

</dd> <dt>

<span data-ttu-id="e80e4-116">*selValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e80e4-116">*selValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e80e4-117">Valeur du sélecteur.</span><span class="sxs-lookup"><span data-stu-id="e80e4-117">The selector value.</span></span> <span data-ttu-id="e80e4-118">Par exemple, pour les données WMI, ce paramètre contient une valeur pour une propriété de clé qui identifie une instance spécifique.</span><span class="sxs-lookup"><span data-stu-id="e80e4-118">For example, for WMI data, this parameter contains a value for a key property that identifies a specific instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e80e4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e80e4-119">Remarks</span></span>

<span data-ttu-id="e80e4-120">**IWSManResourceLocator :: AddSelector** est la méthode C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="e80e4-120">**IWSManResourceLocator::AddSelector** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80e4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e80e4-121">Requirements</span></span>



| <span data-ttu-id="e80e4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e80e4-122">Requirement</span></span> | <span data-ttu-id="e80e4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e80e4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80e4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e80e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e80e4-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e80e4-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e80e4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e80e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e80e4-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e80e4-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e80e4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e80e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e80e4-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e80e4-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e80e4-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="e80e4-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e80e4-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e80e4-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e80e4-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e80e4-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e80e4-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e80e4-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e80e4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e80e4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e80e4-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e80e4-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e80e4-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e80e4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80e4-137">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="e80e4-137">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





