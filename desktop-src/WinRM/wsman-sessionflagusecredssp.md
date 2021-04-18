---
title: Méthode WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUseCredSsp à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUseCredSsp
- Méthode SessionFlagUseCredSsp Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465406"
---
# <a name="wsmansessionflagusecredssp-method"></a><span data-ttu-id="551a0-106">Méthode WSMan. SessionFlagUseCredSsp</span><span class="sxs-lookup"><span data-stu-id="551a0-106">WSMan.SessionFlagUseCredSsp method</span></span>

<span data-ttu-id="551a0-107">Retourne la valeur de l’indicateur d’authentification **WSManFlagUseCredSsp** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="551a0-107">Returns the value of the **WSManFlagUseCredSsp** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="551a0-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="551a0-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="551a0-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="551a0-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="551a0-110">**WSManFlagUseCredSsp** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="551a0-110">**WSManFlagUseCredSsp** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="551a0-111">Pour plus d’informations, consultez [constantes d’authentification](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="551a0-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="551a0-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="551a0-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="551a0-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="551a0-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="551a0-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="551a0-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="551a0-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="551a0-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="551a0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="551a0-116">Return value</span></span>

<span data-ttu-id="551a0-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="551a0-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="551a0-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="551a0-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="551a0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="551a0-119">Requirements</span></span>



| <span data-ttu-id="551a0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="551a0-120">Requirement</span></span> | <span data-ttu-id="551a0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="551a0-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="551a0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="551a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="551a0-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="551a0-123">Windows 7</span></span><br/>                                                                                                        |
| <span data-ttu-id="551a0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="551a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="551a0-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="551a0-125">Windows Server 2008 R2</span></span><br/>                                                                                           |
| <span data-ttu-id="551a0-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="551a0-126">Redistributable</span></span><br/>          | <span data-ttu-id="551a0-127">Windows Management Framework sur Windows Server 2008 avec SP2, Windows Vista avec SP1 et Windows Vista avec SP2</span><span class="sxs-lookup"><span data-stu-id="551a0-127">Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2</span></span><br/> |
| <span data-ttu-id="551a0-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="551a0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="551a0-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="551a0-129"><dt>WSManDisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="551a0-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="551a0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="551a0-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="551a0-131"><dt>WSManDisp.idl</dt></span></span> </dl>                                    |
| <span data-ttu-id="551a0-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="551a0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="551a0-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="551a0-133"><dt>WSManDisp.tlb</dt></span></span> </dl>                                    |
| <span data-ttu-id="551a0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="551a0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="551a0-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="551a0-135"><dt>WSMAuto.dll</dt></span></span> </dl>                                      |



## <a name="see-also"></a><span data-ttu-id="551a0-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="551a0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="551a0-137">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="551a0-137">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="551a0-138">**session**</span><span class="sxs-lookup"><span data-stu-id="551a0-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





