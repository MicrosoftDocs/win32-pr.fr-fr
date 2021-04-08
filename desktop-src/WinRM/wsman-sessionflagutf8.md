---
title: Méthode WSMan. SessionFlagUTF8 (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagUTF8 à utiliser dans le paramètre flags de WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagUTF8
- Méthode SessionFlagUTF8 Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743213"
---
# <a name="wsmansessionflagutf8-method"></a><span data-ttu-id="915a6-106">Méthode WSMan. SessionFlagUTF8</span><span class="sxs-lookup"><span data-stu-id="915a6-106">WSMan.SessionFlagUTF8 method</span></span>

<span data-ttu-id="915a6-107">La méthode **WSMan. SessionFlagUTF8** retourne la valeur de l’indicateur d’authentification **WSManFlagUTF8** pour une utilisation dans le paramètre *Flags* de [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="915a6-107">The **WSMan.SessionFlagUTF8** method returns the value of the **WSManFlagUTF8** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="915a6-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="915a6-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="915a6-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="915a6-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="915a6-110">**WSManFlagUTF8** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="915a6-110">**WSManFlagUTF8** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="915a6-111">Pour plus d’informations, consultez [autres constantes de session](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="915a6-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="915a6-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="915a6-112">Syntax</span></span>


```VB
WSMan.SessionFlagUTF8( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="915a6-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="915a6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="915a6-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="915a6-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="915a6-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="915a6-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="915a6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="915a6-116">Return value</span></span>

<span data-ttu-id="915a6-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="915a6-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="915a6-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="915a6-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="915a6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="915a6-119">Requirements</span></span>



| <span data-ttu-id="915a6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="915a6-120">Requirement</span></span> | <span data-ttu-id="915a6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="915a6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="915a6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="915a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="915a6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="915a6-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="915a6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="915a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="915a6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="915a6-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="915a6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="915a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="915a6-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="915a6-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="915a6-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="915a6-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="915a6-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="915a6-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="915a6-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="915a6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="915a6-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="915a6-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="915a6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="915a6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="915a6-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="915a6-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="915a6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="915a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="915a6-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="915a6-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="915a6-136">**session**</span><span class="sxs-lookup"><span data-stu-id="915a6-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





