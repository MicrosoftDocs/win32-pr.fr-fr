---
description: La méthode DeleteAll de l’objet SWbemNamedValueSet supprime toutes les valeurs nommées de la collection, ce qui la vide.
ms.assetid: db5d2e68-028e-4902-ad42-0b46e1a96bcb
ms.tgt_platform: multiple
title: SWbemNamedValueSet. DeleteAll, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
- ISWbemNamedValueSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9df7b08dddf4cf9f1a687a262721452c0780267a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203354"
---
# <a name="swbemnamedvaluesetdeleteall-method"></a><span data-ttu-id="a5b2e-103">SWbemNamedValueSet. DeleteAll, méthode</span><span class="sxs-lookup"><span data-stu-id="a5b2e-103">SWbemNamedValueSet.DeleteAll method</span></span>

<span data-ttu-id="a5b2e-104">La méthode **DeleteAll** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) supprime toutes les valeurs nommées de la collection, ce qui la vide.</span><span class="sxs-lookup"><span data-stu-id="a5b2e-104">The **DeleteAll** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object removes all named values from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b2e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5b2e-105">Syntax</span></span>


```VB
SWbemNamedValueSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="a5b2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5b2e-106">Parameters</span></span>

<span data-ttu-id="a5b2e-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5b2e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5b2e-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5b2e-108">Return value</span></span>

<span data-ttu-id="a5b2e-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a5b2e-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5b2e-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a5b2e-110">Error codes</span></span>

<span data-ttu-id="a5b2e-111">À la fin de la méthode **DeleteAll** , l’objet **Err** peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a5b2e-111">Upon completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="a5b2e-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="a5b2e-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="a5b2e-113">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a5b2e-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5b2e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5b2e-114">Requirements</span></span>



| <span data-ttu-id="a5b2e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5b2e-115">Requirement</span></span> | <span data-ttu-id="a5b2e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5b2e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b2e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b2e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b2e-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5b2e-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5b2e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5b2e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b2e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5b2e-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5b2e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5b2e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b2e-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5b2e-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5b2e-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a5b2e-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5b2e-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5b2e-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a5b2e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a5b2e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5b2e-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5b2e-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a5b2e-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="a5b2e-127">CLSID</span></span><br/>                    | <span data-ttu-id="a5b2e-128">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="a5b2e-128">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="a5b2e-129">IID</span><span class="sxs-lookup"><span data-stu-id="a5b2e-129">IID</span></span><br/>                      | <span data-ttu-id="a5b2e-130">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="a5b2e-130">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="a5b2e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5b2e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b2e-132">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="a5b2e-132">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> <dt>

[<span data-ttu-id="a5b2e-133">**SWbemNamedValueSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="a5b2e-133">**SWbemNamedValueSet.Remove**</span></span>](swbemnamedvalueset-remove.md)
</dt> </dl>

 

 




