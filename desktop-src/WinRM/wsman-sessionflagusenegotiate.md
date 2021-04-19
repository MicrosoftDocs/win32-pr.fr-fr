---
title: Méthode WSMan. SessionFlagUseNegotiate (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUseNegotiate à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: 86d8ed13-5eae-4a06-8ceb-b0ec067f4a4c
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUseNegotiate
- Méthode SessionFlagUseNegotiate Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagUseNegotiate
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNegotiate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b57e463ccf71f22f12a964b1e1de72f426963c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512807"
---
# <a name="wsmansessionflagusenegotiate-method"></a><span data-ttu-id="e42a3-106">Méthode WSMan. SessionFlagUseNegotiate</span><span class="sxs-lookup"><span data-stu-id="e42a3-106">WSMan.SessionFlagUseNegotiate method</span></span>

<span data-ttu-id="e42a3-107">La méthode **WSMan. SessionFlagUseNegotiate** retourne la valeur de l’indicateur d’authentification **WSManFlagUseNegotiate** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="e42a3-107">The **WSMan.SessionFlagUseNegotiate** method returns the value of the **WSManFlagUseNegotiate** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="e42a3-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="e42a3-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="e42a3-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e42a3-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="e42a3-110">**WSManFlagUseNegotiate** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="e42a3-110">**WSManFlagUseNegotiate** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="e42a3-111">Pour plus d’informations, consultez [constantes d’authentification](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e42a3-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e42a3-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e42a3-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseNegotiate( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="e42a3-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e42a3-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42a3-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e42a3-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e42a3-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="e42a3-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42a3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e42a3-116">Return value</span></span>

<span data-ttu-id="e42a3-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e42a3-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e42a3-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e42a3-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e42a3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e42a3-119">Requirements</span></span>



| <span data-ttu-id="e42a3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e42a3-120">Requirement</span></span> | <span data-ttu-id="e42a3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e42a3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e42a3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e42a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e42a3-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e42a3-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e42a3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e42a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e42a3-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e42a3-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e42a3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e42a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e42a3-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e42a3-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e42a3-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="e42a3-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e42a3-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e42a3-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e42a3-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e42a3-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e42a3-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e42a3-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e42a3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e42a3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e42a3-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e42a3-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e42a3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e42a3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e42a3-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="e42a3-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="e42a3-136">**session**</span><span class="sxs-lookup"><span data-stu-id="e42a3-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





