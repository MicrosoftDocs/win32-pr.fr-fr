---
title: Méthode ISoftKbd GetSoftKeyboardTypeMode (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardTypeMode récupère le mode de type pour un clavier conditionnel.
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardTypeMode
- GetSoftKeyboardTypeMode méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardTypeMode
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383824"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a><span data-ttu-id="21f92-106">ISoftKbd :: GetSoftKeyboardTypeMode, méthode</span><span class="sxs-lookup"><span data-stu-id="21f92-106">ISoftKbd::GetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="21f92-107">La méthode **ISoftKbd :: GetSoftKeyboardTypeMode** récupère le mode de type pour un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="21f92-107">The **ISoftKbd::GetSoftKeyboardTypeMode** method retrieves the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f92-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21f92-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="21f92-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21f92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f92-110">*lpTypeMode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="21f92-110">*lpTypeMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21f92-111">Pointeur vers une mémoire tampon dans laquelle cette méthode récupère le mode de type.</span><span class="sxs-lookup"><span data-stu-id="21f92-111">Pointer to a buffer in which this method retrieves the type mode.</span></span> <span data-ttu-id="21f92-112">Les valeurs possibles sont définies pour l’énumération [**TYPEMODE**](typemode.md) .</span><span class="sxs-lookup"><span data-stu-id="21f92-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f92-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21f92-113">Return value</span></span>

<span data-ttu-id="21f92-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="21f92-114">This method can return one of these values.</span></span>



| <span data-ttu-id="21f92-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f92-115">Value</span></span>                                                                                        | <span data-ttu-id="21f92-116">Description</span><span class="sxs-lookup"><span data-stu-id="21f92-116">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="21f92-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="21f92-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="21f92-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="21f92-118">The method was successful.</span></span><br/>             |
| <dl> <span data-ttu-id="21f92-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="21f92-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="21f92-120">Le paramètre *lpTypeMode* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="21f92-120">The *lpTypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="21f92-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21f92-121">Requirements</span></span>



| <span data-ttu-id="21f92-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21f92-122">Requirement</span></span> | <span data-ttu-id="21f92-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="21f92-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21f92-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f92-124">Minimum supported client</span></span><br/> | <span data-ttu-id="21f92-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f92-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="21f92-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21f92-126">Minimum supported server</span></span><br/> | <span data-ttu-id="21f92-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21f92-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="21f92-128">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="21f92-128">Redistributable</span></span><br/>          | <span data-ttu-id="21f92-129">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="21f92-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="21f92-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="21f92-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="21f92-131"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f92-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="21f92-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="21f92-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21f92-133"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21f92-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="21f92-134">DLL</span><span class="sxs-lookup"><span data-stu-id="21f92-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21f92-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21f92-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f92-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21f92-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f92-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="21f92-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="21f92-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="21f92-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="21f92-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="21f92-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





