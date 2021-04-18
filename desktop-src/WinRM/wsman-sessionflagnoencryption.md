---
title: Méthode WSMan. SessionFlagNoEncryption (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagNoEncryption à utiliser dans le paramètre flags de la méthode WSMan. CreateSession.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagNoEncryption
- Méthode SessionFlagNoEncryption Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagNoEncryption
topic_type:
- apiref
api_name:
- WSMan.SessionFlagNoEncryption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4c7a85e97afd67ab6b1114248a9c4b3ee3ebbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509293"
---
# <a name="wsmansessionflagnoencryption-method"></a><span data-ttu-id="62457-106">Méthode WSMan. SessionFlagNoEncryption</span><span class="sxs-lookup"><span data-stu-id="62457-106">WSMan.SessionFlagNoEncryption method</span></span>

<span data-ttu-id="62457-107">La méthode **WSMan. SessionFlagNoEncryption** retourne la valeur de l’indicateur d’authentification **WSManFlagNoEncryption** à utiliser dans le paramètre *Flags* de la méthode [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="62457-107">The **WSMan.SessionFlagNoEncryption** method returns the value of the **WSManFlagNoEncryption** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="62457-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="62457-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="62457-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="62457-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="62457-110">**WSManFlagNoEncryption** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="62457-110">**WSManFlagNoEncryption** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="62457-111">Pour plus d’informations, consultez [autres constantes de session](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="62457-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62457-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62457-112">Syntax</span></span>


```VB
WSMan.SessionFlagNoEncryption( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="62457-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62457-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62457-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="62457-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62457-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="62457-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62457-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="62457-116">Return value</span></span>

<span data-ttu-id="62457-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62457-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62457-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62457-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62457-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62457-119">Requirements</span></span>



| <span data-ttu-id="62457-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62457-120">Requirement</span></span> | <span data-ttu-id="62457-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="62457-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62457-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62457-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62457-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62457-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="62457-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62457-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62457-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62457-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="62457-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="62457-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62457-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="62457-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="62457-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="62457-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62457-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62457-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="62457-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="62457-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="62457-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="62457-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="62457-132">DLL</span><span class="sxs-lookup"><span data-stu-id="62457-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62457-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62457-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="62457-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62457-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62457-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="62457-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="62457-136">**session**</span><span class="sxs-lookup"><span data-stu-id="62457-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





