---
title: Méthode WSMan. SessionFlagUseBasic (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUseBasic à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUseBasic
- Méthode SessionFlagUseBasic Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagUseBasic
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseBasic
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41641e0398791ab46c81f71f967f2d43700a2984
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032508"
---
# <a name="wsmansessionflagusebasic-method"></a><span data-ttu-id="eb3c5-106">Méthode WSMan. SessionFlagUseBasic</span><span class="sxs-lookup"><span data-stu-id="eb3c5-106">WSMan.SessionFlagUseBasic method</span></span>

<span data-ttu-id="eb3c5-107">La méthode **WSMan. SessionFlagUseBasic** retourne la valeur de l’indicateur d’authentification **WSManFlagUseBasic** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="eb3c5-107">The **WSMan.SessionFlagUseBasic** method returns the value of the authentication flag **WSManFlagUseBasic** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="eb3c5-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="eb3c5-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="eb3c5-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="eb3c5-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="eb3c5-110">**WSManFlagUseBasic** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="eb3c5-110">**WSManFlagUseBasic** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="eb3c5-111">Pour plus d’informations, consultez [**constantes d’authentification**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="eb3c5-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3c5-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb3c5-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseBasic( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="eb3c5-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb3c5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb3c5-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb3c5-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb3c5-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="eb3c5-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb3c5-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb3c5-116">Return value</span></span>

<span data-ttu-id="eb3c5-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb3c5-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb3c5-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb3c5-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3c5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb3c5-119">Requirements</span></span>



| <span data-ttu-id="eb3c5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb3c5-120">Requirement</span></span> | <span data-ttu-id="eb3c5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb3c5-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3c5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb3c5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eb3c5-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb3c5-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="eb3c5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb3c5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eb3c5-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb3c5-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="eb3c5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb3c5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb3c5-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb3c5-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb3c5-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="eb3c5-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb3c5-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb3c5-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="eb3c5-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb3c5-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="eb3c5-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb3c5-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb3c5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="eb3c5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb3c5-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb3c5-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb3c5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb3c5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3c5-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="eb3c5-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="eb3c5-136">**session**</span><span class="sxs-lookup"><span data-stu-id="eb3c5-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





