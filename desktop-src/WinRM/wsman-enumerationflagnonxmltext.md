---
title: Méthode WSMan. EnumerationFlagNonXmlText (WSManDisp. h)
description: Retourne la valeur de la constante d’énumération WSManFlagNonXmlText à utiliser dans le paramètre flags de la méthode session. Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagNonXmlText
- Méthode EnumerationFlagNonXmlText Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode EnumerationFlagNonXmlText
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26a9547f85a07702dc3735129842e5bc286ee9b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742357"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a><span data-ttu-id="c2539-106">Méthode WSMan. EnumerationFlagNonXmlText</span><span class="sxs-lookup"><span data-stu-id="c2539-106">WSMan.EnumerationFlagNonXmlText method</span></span>

<span data-ttu-id="c2539-107">**WSMan. EnumerationFlagNonXmlText** retourne la valeur de la constante d’énumération **WSManFlagNonXmlText** pour une utilisation dans le paramètre *Flags* de la méthode [**session. Enumerate**](session-enumerate.md) .</span><span class="sxs-lookup"><span data-stu-id="c2539-107">The **WSMan.EnumerationFlagNonXmlText** returns the value of the enumeration constant **WSManFlagNonXmlText** for use in the *flags* parameter of the [**Session.Enumerate**](session-enumerate.md) method.</span></span> <span data-ttu-id="c2539-108">Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante.</span><span class="sxs-lookup"><span data-stu-id="c2539-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="c2539-109">Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c2539-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="c2539-110">**WSManFlagNonXmlText** est une constante dans l’énumération **\_ \_ WSManEnumFlags** .</span><span class="sxs-lookup"><span data-stu-id="c2539-110">**WSManFlagNonXmlText** is a constant in the **\_\_WSManEnumFlags** enumeration.</span></span> <span data-ttu-id="c2539-111">Pour plus d’informations, consultez [**énumération, constantes**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c2539-111">For more information, see [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2539-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2539-112">Syntax</span></span>


```VB
WSMan.EnumerationFlagNonXmlText( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="c2539-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2539-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2539-114">*indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c2539-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2539-115">Valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="c2539-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2539-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2539-116">Return value</span></span>

<span data-ttu-id="c2539-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c2539-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2539-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2539-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2539-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2539-119">Requirements</span></span>



| <span data-ttu-id="c2539-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2539-120">Requirement</span></span> | <span data-ttu-id="c2539-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2539-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2539-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2539-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2539-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2539-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c2539-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2539-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2539-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2539-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c2539-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2539-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2539-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2539-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2539-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="c2539-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2539-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2539-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="c2539-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c2539-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2539-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c2539-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c2539-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c2539-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2539-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2539-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2539-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2539-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2539-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="c2539-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="c2539-136">**IWSManEx**</span><span class="sxs-lookup"><span data-stu-id="c2539-136">**IWSManEx**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[<span data-ttu-id="c2539-137">**IWSManSession**</span><span class="sxs-lookup"><span data-stu-id="c2539-137">**IWSManSession**</span></span>](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





