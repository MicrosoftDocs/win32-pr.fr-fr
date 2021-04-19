---
description: La méthode SWbemRefreshableItem. Remove supprime l’objet SWbemRefreshableItem de l’objet SWbemRefresher parent. Objet SWbemRefreshableItem de l’objet SWbemRefresher parent.
ms.assetid: 8d3f5e22-c343-4191-a20a-6bca2ec9b01a
ms.tgt_platform: multiple
title: SWbemRefreshableItem. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
- ISWbemRefreshableItem.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 028bff202108481ce498be02c6014141313f27cc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106543549"
---
# <a name="swbemrefreshableitemremove-method"></a><span data-ttu-id="79c39-103">SWbemRefreshableItem. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="79c39-103">SWbemRefreshableItem.Remove method</span></span>

<span data-ttu-id="79c39-104">La méthode **SWbemRefreshableItem. Remove** supprime l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) de l’objet [**SWbemRefresher**](swbemrefresher.md) parent.</span><span class="sxs-lookup"><span data-stu-id="79c39-104">The **SWbemRefreshableItem.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="79c39-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="79c39-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="79c39-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79c39-106">Syntax</span></span>


```VB
SWbemRefreshableItem.Remove( _
  [ ByVal lFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="79c39-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79c39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79c39-108">*lFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="79c39-108">*lFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="79c39-109">Ce paramètre doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="79c39-109">This parameter must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79c39-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79c39-110">Return value</span></span>

<span data-ttu-id="79c39-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="79c39-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79c39-112">Notes</span><span class="sxs-lookup"><span data-stu-id="79c39-112">Remarks</span></span>

<span data-ttu-id="79c39-113">**Codes d’erreur** Si l’actualisateur n’a pas d’élément avec l’index spécifié, **wbemErrNotFound** est généré.</span><span class="sxs-lookup"><span data-stu-id="79c39-113">**Error Codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="79c39-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79c39-114">Requirements</span></span>



| <span data-ttu-id="79c39-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79c39-115">Requirement</span></span> | <span data-ttu-id="79c39-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="79c39-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79c39-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79c39-117">Minimum supported client</span></span><br/> | <span data-ttu-id="79c39-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="79c39-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="79c39-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79c39-119">Minimum supported server</span></span><br/> | <span data-ttu-id="79c39-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79c39-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="79c39-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="79c39-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="79c39-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="79c39-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="79c39-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="79c39-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="79c39-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79c39-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79c39-125">DLL</span><span class="sxs-lookup"><span data-stu-id="79c39-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79c39-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79c39-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="79c39-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="79c39-127">CLSID</span></span><br/>                    | <span data-ttu-id="79c39-128">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="79c39-128">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="79c39-129">IID</span><span class="sxs-lookup"><span data-stu-id="79c39-129">IID</span></span><br/>                      | <span data-ttu-id="79c39-130">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="79c39-130">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="79c39-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79c39-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c39-132">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="79c39-132">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="79c39-133">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="79c39-133">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




