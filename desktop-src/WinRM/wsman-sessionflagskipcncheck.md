---
title: Méthode WSMan. SessionFlagSkipCNCheck (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagSkipCNCheck à utiliser dans le paramètre flags de WSMan. CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagSkipCNCheck
- Méthode SessionFlagSkipCNCheck Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagSkipCNCheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942404"
---
# <a name="wsmansessionflagskipcncheck-method"></a><span data-ttu-id="05f5a-106">Méthode WSMan. SessionFlagSkipCNCheck</span><span class="sxs-lookup"><span data-stu-id="05f5a-106">WSMan.SessionFlagSkipCNCheck method</span></span>

<span data-ttu-id="05f5a-107">La méthode **WSMan. SessionFlagSkipCNCheck** retourne la valeur de l’indicateur d’authentification **WSManFlagSkipCNCheck** pour une utilisation dans le paramètre *Flags* de [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="05f5a-107">The **WSMan.SessionFlagSkipCNCheck** method returns the value of the **WSManFlagSkipCNCheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="05f5a-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="05f5a-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="05f5a-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="05f5a-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="05f5a-110">**WSManFlagSkipCNCheck** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="05f5a-110">**WSManFlagSkipCNCheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="05f5a-111">Pour plus d’informations, consultez [**constantes d’authentification**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="05f5a-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="05f5a-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05f5a-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="05f5a-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05f5a-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f5a-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="05f5a-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05f5a-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="05f5a-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f5a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05f5a-116">Return value</span></span>

<span data-ttu-id="05f5a-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="05f5a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="05f5a-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="05f5a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f5a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05f5a-119">Requirements</span></span>



| <span data-ttu-id="05f5a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05f5a-120">Requirement</span></span> | <span data-ttu-id="05f5a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="05f5a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f5a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05f5a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="05f5a-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05f5a-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="05f5a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05f5a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="05f5a-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05f5a-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="05f5a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="05f5a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="05f5a-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="05f5a-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="05f5a-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="05f5a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05f5a-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05f5a-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="05f5a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="05f5a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="05f5a-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="05f5a-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="05f5a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="05f5a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05f5a-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05f5a-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05f5a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05f5a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f5a-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="05f5a-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="05f5a-136">**session**</span><span class="sxs-lookup"><span data-stu-id="05f5a-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





