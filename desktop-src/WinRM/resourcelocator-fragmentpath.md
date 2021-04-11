---
title: ResourceLocator. FragmentPath, propriété (WSManDisp. h)
description: Obtient ou définit le chemin d’accès d’un fragment ou d’une propriété de ressource lorsque ResourceLocator est utilisé dans les opérations d’objet de session, telles que session. obtenir, session. put ou session. Enumerate.
ms.assetid: 4d059b57-fca5-4a75-9396-6505920498c3
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété FragmentPath
- Windows Remote Management de la propriété FragmentPath, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, propriété FragmentPath
topic_type:
- apiref
api_name:
- ResourceLocator.FragmentPath
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e15fba102f9a7c8a2581271c575857b49bc5df1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032899"
---
# <a name="resourcelocatorfragmentpath-property"></a><span data-ttu-id="288b0-106">ResourceLocator. FragmentPath, propriété</span><span class="sxs-lookup"><span data-stu-id="288b0-106">ResourceLocator.FragmentPath property</span></span>

<span data-ttu-id="288b0-107">Obtient ou définit le chemin d’accès d’un [*fragment*](windows-remote-management-glossary.md) ou d’une propriété de [*ressource*](windows-remote-management-glossary.md) lorsque [**ResourceLocator**](resourcelocator.md) est utilisé dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="288b0-107">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property when [**ResourceLocator**](resourcelocator.md) is used in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="288b0-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="288b0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="288b0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="288b0-109">Syntax</span></span>


```VB
ResourceLocator.FragmentPath
```



## <a name="property-value"></a><span data-ttu-id="288b0-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="288b0-110">Property value</span></span>

<span data-ttu-id="288b0-111">Chaîne qui identifie le fragment ou la propriété de la ressource.</span><span class="sxs-lookup"><span data-stu-id="288b0-111">String that identifies the fragment or property of the resource.</span></span> <span data-ttu-id="288b0-112">Par exemple, si la ressource est un lecteur de disque et que la propriété demandée est fabricant, la chaîne peut contenir `Diskdrive/Manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="288b0-112">For example, if the resource is a disk drive and the requested property is Manufacturer, the string may contain `Diskdrive/Manufacturer`.</span></span> <span data-ttu-id="288b0-113">Le texte du fragment respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="288b0-113">The fragment text is case-sensitive.</span></span> <span data-ttu-id="288b0-114">Dans ce cas, vous ne pouvez pas utiliser `diskdrive/manufacturer` .</span><span class="sxs-lookup"><span data-stu-id="288b0-114">In this case, you cannot use `diskdrive/manufacturer`.</span></span>

## <a name="remarks"></a><span data-ttu-id="288b0-115">Notes</span><span class="sxs-lookup"><span data-stu-id="288b0-115">Remarks</span></span>

<span data-ttu-id="288b0-116">**IWSManResourceLocator :: FragmentPath** est la propriété C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="288b0-116">**IWSManResourceLocator::FragmentPath** is the corresponding C++ property.</span></span>

<span data-ttu-id="288b0-117">Vous pouvez spécifier un élément d’une propriété de tableau en fournissant l’index de tableau comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="288b0-117">You can specify one element of an array property by supplying the array index as shown in the following example.</span></span> <span data-ttu-id="288b0-118">N’oubliez pas que l’indexation de tableau commence par 1 au lieu de 0.</span><span class="sxs-lookup"><span data-stu-id="288b0-118">Be aware that array indexing starts with 1 rather than 0.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder[1]"
```



<span data-ttu-id="288b0-119">Pour récupérer le tableau entier, spécifiez le nom de la propriété de tableau comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="288b0-119">To get the whole array, specify the array property name as shown in the following example.</span></span>


```VB
Const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
Const FragmentPath = "DNSServerSearchOrder"
```



## <a name="requirements"></a><span data-ttu-id="288b0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="288b0-120">Requirements</span></span>



| <span data-ttu-id="288b0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="288b0-121">Requirement</span></span> | <span data-ttu-id="288b0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="288b0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="288b0-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="288b0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="288b0-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="288b0-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="288b0-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="288b0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="288b0-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="288b0-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="288b0-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="288b0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="288b0-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="288b0-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="288b0-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="288b0-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="288b0-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="288b0-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="288b0-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="288b0-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="288b0-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="288b0-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="288b0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="288b0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="288b0-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="288b0-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="288b0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="288b0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="288b0-136">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="288b0-136">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 





