---
title: Méthode WSMan. SessionFlagUseNoAuthentication (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUseNoAuthentication à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUseNoAuthentication
- Méthode SessionFlagUseNoAuthentication Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagUseNoAuthentication
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNoAuthentication
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9676d3baa9a18ae8a3feb5eb4092c63586a94b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466682"
---
# <a name="wsmansessionflagusenoauthentication-method"></a><span data-ttu-id="d4f7b-106">Méthode WSMan. SessionFlagUseNoAuthentication</span><span class="sxs-lookup"><span data-stu-id="d4f7b-106">WSMan.SessionFlagUseNoAuthentication method</span></span>

<span data-ttu-id="d4f7b-107">La méthode **WSMan. SessionFlagUseNoAuthentication** retourne la valeur de l’indicateur d’authentification **WSManFlagUseNoAuthentication** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="d4f7b-107">The **WSMan.SessionFlagUseNoAuthentication** method returns the value of the **WSManFlagUseNoAuthentication** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="d4f7b-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="d4f7b-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d4f7b-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="d4f7b-110">**WSManFlagUseNoAuthentication** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="d4f7b-110">**WSManFlagUseNoAuthentication** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="d4f7b-111">Pour plus d’informations, consultez//[constantes d’authentification](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="d4f7b-111">For more information, see //[Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f7b-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4f7b-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseNoAuthentication( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="d4f7b-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4f7b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f7b-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4f7b-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f7b-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f7b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4f7b-116">Return value</span></span>

<span data-ttu-id="d4f7b-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d4f7b-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d4f7b-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d4f7b-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f7b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4f7b-119">Requirements</span></span>



| <span data-ttu-id="d4f7b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4f7b-120">Requirement</span></span> | <span data-ttu-id="d4f7b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4f7b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f7b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4f7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f7b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4f7b-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d4f7b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4f7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f7b-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4f7b-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d4f7b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4f7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f7b-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4f7b-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4f7b-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="d4f7b-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4f7b-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4f7b-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d4f7b-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4f7b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4f7b-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d4f7b-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d4f7b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d4f7b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4f7b-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4f7b-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4f7b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4f7b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f7b-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="d4f7b-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="d4f7b-136">**session**</span><span class="sxs-lookup"><span data-stu-id="d4f7b-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





