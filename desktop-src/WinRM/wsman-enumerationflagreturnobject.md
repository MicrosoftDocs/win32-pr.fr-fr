---
title: Méthode WSMan. EnumerationFlagReturnObject (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’énumération EnumerationFlagReturnObject à utiliser dans le paramètre flags de session. Enumerate.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagReturnObject
- Méthode EnumerationFlagReturnObject Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode EnumerationFlagReturnObject
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3019f880503f91d1488a2b7a41574cadc2df987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509349"
---
# <a name="wsmanenumerationflagreturnobject-method"></a><span data-ttu-id="9164f-106">Méthode WSMan. EnumerationFlagReturnObject</span><span class="sxs-lookup"><span data-stu-id="9164f-106">WSMan.EnumerationFlagReturnObject method</span></span>

<span data-ttu-id="9164f-107">La méthode **WSMan. EnumerationFlagReturnObject** retourne la valeur de l’indicateur d’énumération **EnumerationFlagReturnObject** pour une utilisation dans le paramètre *Flags* de [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="9164f-107">The **WSMan.EnumerationFlagReturnObject** method returns the value of the enumeration flag **EnumerationFlagReturnObject** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="9164f-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="9164f-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="9164f-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9164f-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="9164f-110">**EnumerationFlagReturnObject** est une constante dans l’énumération **\_ WSManEnumFlags** et est décrite dans [**constantes d’énumération**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="9164f-110">**EnumerationFlagReturnObject** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9164f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9164f-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnObject( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="9164f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9164f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9164f-113">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9164f-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9164f-114">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="9164f-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9164f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9164f-115">Return value</span></span>

<span data-ttu-id="9164f-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9164f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9164f-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9164f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9164f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9164f-118">Requirements</span></span>



| <span data-ttu-id="9164f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9164f-119">Requirement</span></span> | <span data-ttu-id="9164f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9164f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9164f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9164f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9164f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9164f-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9164f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9164f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9164f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9164f-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9164f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9164f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9164f-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9164f-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9164f-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="9164f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9164f-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9164f-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="9164f-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9164f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9164f-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9164f-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9164f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9164f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9164f-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9164f-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9164f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9164f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9164f-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="9164f-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="9164f-135">**session**</span><span class="sxs-lookup"><span data-stu-id="9164f-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





