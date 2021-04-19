---
description: La méthode Item de l’objet SWbemObjectSet obtient un SWbemObject à partir de la collection.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: SWbemObjectSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519818"
---
# <a name="swbemobjectsetitem-method"></a><span data-ttu-id="7cccb-103">SWbemObjectSet. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="7cccb-103">SWbemObjectSet.Item method</span></span>

<span data-ttu-id="7cccb-104">La méthode **Item** de l’objet [**SWbemObjectSet**](swbemobjectset.md) obtient un [**SWbemObject**](swbemobject.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="7cccb-104">The **Item** method of the [**SWbemObjectSet**](swbemobjectset.md) object gets an [**SWbemObject**](swbemobject.md) from the collection.</span></span>

<span data-ttu-id="7cccb-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7cccb-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cccb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cccb-106">Syntax</span></span>


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a><span data-ttu-id="7cccb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cccb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cccb-108">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="7cccb-108">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="7cccb-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7cccb-109">Required.</span></span> <span data-ttu-id="7cccb-110">Chemin d’accès relatif de l’objet à récupérer de la collection.</span><span class="sxs-lookup"><span data-stu-id="7cccb-110">Relative path of the object to retrieve from the collection.</span></span> <span data-ttu-id="7cccb-111">Exemple : \_ disque logique Win32 = "C :"</span><span class="sxs-lookup"><span data-stu-id="7cccb-111">Example: Win32\_LogicalDisk="C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cccb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cccb-112">Return value</span></span>

<span data-ttu-id="7cccb-113">En cas de réussite, l’objet [**SWbemObject**](swbemobject.md) demandé retourne.</span><span class="sxs-lookup"><span data-stu-id="7cccb-113">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7cccb-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7cccb-114">Error codes</span></span>

<span data-ttu-id="7cccb-115">À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7cccb-115">Upon completion of the **Item** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="7cccb-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7cccb-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7cccb-117">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7cccb-117">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7cccb-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7cccb-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7cccb-119">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="7cccb-119">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="7cccb-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7cccb-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7cccb-121">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7cccb-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7cccb-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="7cccb-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="7cccb-123">L’élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7cccb-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cccb-124">Notes</span><span class="sxs-lookup"><span data-stu-id="7cccb-124">Remarks</span></span>

<span data-ttu-id="7cccb-125">La méthode **Item** peut nécessiter beaucoup de temps processeur, car une énumération complète par le fournisseur des éléments de l’ensemble est nécessaire pour retourner le résultat.</span><span class="sxs-lookup"><span data-stu-id="7cccb-125">The **Item** method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cccb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cccb-126">Requirements</span></span>



| <span data-ttu-id="7cccb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cccb-127">Requirement</span></span> | <span data-ttu-id="7cccb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cccb-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cccb-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cccb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7cccb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cccb-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7cccb-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cccb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7cccb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cccb-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7cccb-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cccb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cccb-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cccb-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7cccb-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7cccb-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="7cccb-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7cccb-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7cccb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7cccb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cccb-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cccb-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7cccb-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="7cccb-139">CLSID</span></span><br/>                    | <span data-ttu-id="7cccb-140">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="7cccb-140">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="7cccb-141">IID</span><span class="sxs-lookup"><span data-stu-id="7cccb-141">IID</span></span><br/>                      | <span data-ttu-id="7cccb-142">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="7cccb-142">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




