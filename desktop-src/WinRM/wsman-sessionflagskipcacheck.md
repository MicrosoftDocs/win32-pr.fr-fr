---
title: Méthode WSMan. SessionFlagSkipCACheck (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’authentification WSManFlagSkipCACheck à utiliser dans le paramètre flags de WSMan. CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode SessionFlagSkipCACheck
- Méthode SessionFlagSkipCACheck Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode SessionFlagSkipCACheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032368"
---
# <a name="wsmansessionflagskipcacheck-method"></a><span data-ttu-id="b3011-106">Méthode WSMan. SessionFlagSkipCACheck</span><span class="sxs-lookup"><span data-stu-id="b3011-106">WSMan.SessionFlagSkipCACheck method</span></span>

<span data-ttu-id="b3011-107">La méthode **WSMan. SessionFlagSkipCACheck** retourne la valeur de l’indicateur d’authentification **WSManFlagSkipCACheck** pour une utilisation dans le paramètre *Flags* de [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="b3011-107">The **WSMan.SessionFlagSkipCACheck** method returns the value of the **WSManFlagSkipCACheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="b3011-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="b3011-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="b3011-109">Pour plus d’informations sur l’appel de cette méthode et des exemples de code, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b3011-109">For more information about how to call this method and code examples, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="b3011-110">**WSManFlagSkipCACheck** est une constante dans l’énumération **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="b3011-110">**WSManFlagSkipCACheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="b3011-111">Pour plus d’informations, consultez [**constantes d’authentification**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b3011-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b3011-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3011-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCACheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="b3011-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3011-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3011-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b3011-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3011-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="b3011-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3011-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3011-116">Return value</span></span>

<span data-ttu-id="b3011-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b3011-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b3011-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b3011-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3011-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3011-119">Requirements</span></span>



| <span data-ttu-id="b3011-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3011-120">Requirement</span></span> | <span data-ttu-id="b3011-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3011-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3011-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3011-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3011-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3011-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="b3011-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3011-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3011-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3011-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b3011-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3011-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3011-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3011-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3011-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="b3011-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3011-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3011-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b3011-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b3011-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3011-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b3011-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b3011-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b3011-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3011-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3011-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3011-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3011-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3011-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="b3011-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="b3011-136">**session**</span><span class="sxs-lookup"><span data-stu-id="b3011-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





