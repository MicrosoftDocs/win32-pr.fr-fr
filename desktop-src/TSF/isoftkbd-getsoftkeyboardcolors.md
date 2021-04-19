---
title: Méthode ISoftKbd GetSoftKeyboardColors (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardColors récupère la couleur de clavier programmable correspondant au type de couleur fourni.
ms.assetid: d59d249c-a1c4-4d6a-add6-632be55a7549
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardColors
- GetSoftKeyboardColors méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f8f184dc04ddcbef18a9279000b1a68acd35bd3
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "106523089"
---
# <a name="isoftkbdgetsoftkeyboardcolors-method"></a><span data-ttu-id="32882-106">ISoftKbd :: GetSoftKeyboardColors, méthode</span><span class="sxs-lookup"><span data-stu-id="32882-106">ISoftKbd::GetSoftKeyboardColors method</span></span>

<span data-ttu-id="32882-107">La méthode **ISoftKbd :: GetSoftKeyboardColors** récupère la couleur de clavier programmable correspondant au type de couleur fourni.</span><span class="sxs-lookup"><span data-stu-id="32882-107">The **ISoftKbd::GetSoftKeyboardColors** method retrieves the soft keyboard color corresponding to the supplied color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="32882-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32882-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardColors(
  [in]  COLORTYPE colorType,
  [out] COLORREF  *lpColor
);
```



## <a name="parameters"></a><span data-ttu-id="32882-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32882-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32882-110">*colorType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32882-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32882-111">Valeur qui spécifie le type de couleur à récupérer pour le clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="32882-111">A value specifying the color type to retrieve for the soft keyboard.</span></span> <span data-ttu-id="32882-112">Les valeurs possibles sont définies pour l’énumération [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="32882-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="32882-113">*lpColor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="32882-113">*lpColor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32882-114">Pointeur vers une mémoire tampon dans laquelle cette méthode récupère une valeur [**COLORREF**](/windows/desktop/gdi/colorref) 32 bits spécifiant une couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="32882-114">Pointer to a buffer in which this method retrieves a 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32882-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32882-115">Return value</span></span>

<span data-ttu-id="32882-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="32882-116">This method can return one of these values.</span></span>



| <span data-ttu-id="32882-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="32882-117">Value</span></span>                                                                                        | <span data-ttu-id="32882-118">Description</span><span class="sxs-lookup"><span data-stu-id="32882-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="32882-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="32882-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="32882-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="32882-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="32882-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="32882-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="32882-122">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="32882-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="32882-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32882-123">Requirements</span></span>



| <span data-ttu-id="32882-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32882-124">Requirement</span></span> | <span data-ttu-id="32882-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="32882-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32882-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32882-126">Minimum supported client</span></span><br/> | <span data-ttu-id="32882-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32882-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="32882-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32882-128">Minimum supported server</span></span><br/> | <span data-ttu-id="32882-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32882-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="32882-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="32882-130">Redistributable</span></span><br/>          | <span data-ttu-id="32882-131">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="32882-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="32882-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="32882-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="32882-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="32882-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="32882-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="32882-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32882-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32882-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="32882-136">DLL</span><span class="sxs-lookup"><span data-stu-id="32882-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32882-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32882-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32882-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32882-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32882-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="32882-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="32882-140">**ISoftKbd::SetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="32882-140">**ISoftKbd::SetSoftKeyboardColors**</span></span>](/windows/desktop/TSF/isoftkbd-setsoftkeyboardcolors)
</dt> <dt>

[<span data-ttu-id="32882-141">**COLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="32882-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="32882-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="32882-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

