---
title: Méthode ISoftKbd SetSoftKeyboardTypeMode (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardTypeMode définit le mode de saisie d’un clavier conditionnel.
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardTypeMode
- SetSoftKeyboardTypeMode méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466303"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a><span data-ttu-id="63b15-106">ISoftKbd :: SetSoftKeyboardTypeMode, méthode</span><span class="sxs-lookup"><span data-stu-id="63b15-106">ISoftKbd::SetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="63b15-107">La méthode **ISoftKbd :: SetSoftKeyboardTypeMode** définit le mode de saisie d’un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="63b15-107">The **ISoftKbd::SetSoftKeyboardTypeMode** method sets the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b15-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63b15-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="63b15-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63b15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63b15-110">*TypeMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63b15-110">*TypeMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63b15-111">Mode de type.</span><span class="sxs-lookup"><span data-stu-id="63b15-111">The type mode.</span></span> <span data-ttu-id="63b15-112">Les valeurs possibles sont définies pour l’énumération [**TYPEMODE**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="63b15-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63b15-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63b15-113">Return value</span></span>

<span data-ttu-id="63b15-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="63b15-114">This method can return one of these values.</span></span>



| <span data-ttu-id="63b15-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="63b15-115">Value</span></span>                                                                                        | <span data-ttu-id="63b15-116">Description</span><span class="sxs-lookup"><span data-stu-id="63b15-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="63b15-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63b15-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="63b15-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="63b15-118">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="63b15-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="63b15-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="63b15-120">Le paramètre *TypeMode* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="63b15-120">The *TypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="63b15-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63b15-121">Requirements</span></span>



| <span data-ttu-id="63b15-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63b15-122">Requirement</span></span> | <span data-ttu-id="63b15-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="63b15-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63b15-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63b15-124">Minimum supported client</span></span><br/> | <span data-ttu-id="63b15-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63b15-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="63b15-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63b15-126">Minimum supported server</span></span><br/> | <span data-ttu-id="63b15-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63b15-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63b15-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="63b15-128">Redistributable</span></span><br/>          | <span data-ttu-id="63b15-129">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="63b15-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="63b15-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="63b15-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b15-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b15-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="63b15-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="63b15-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63b15-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63b15-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="63b15-134">DLL</span><span class="sxs-lookup"><span data-stu-id="63b15-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63b15-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63b15-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b15-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63b15-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b15-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="63b15-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="63b15-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="63b15-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="63b15-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="63b15-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





