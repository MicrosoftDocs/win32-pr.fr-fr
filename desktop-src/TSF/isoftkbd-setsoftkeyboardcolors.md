---
title: Méthode ISoftKbd SetSoftKeyboardColors (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardColors définit la couleur du clavier logiciel pour le type de couleur spécifié.
ms.assetid: 1abbff35-a5ef-4119-9367-60b6e0961c59
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardColors
- SetSoftKeyboardColors méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardColors
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardColors
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38357331db2440c35ca7557d08c97729fde9c9f0
ms.sourcegitcommit: d6bf2018c588c9782e1eed21b3cdea3523ec6955
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2021
ms.locfileid: "106527718"
---
# <a name="isoftkbdsetsoftkeyboardcolors-method"></a><span data-ttu-id="75d3b-106">ISoftKbd :: SetSoftKeyboardColors, méthode</span><span class="sxs-lookup"><span data-stu-id="75d3b-106">ISoftKbd::SetSoftKeyboardColors method</span></span>

<span data-ttu-id="75d3b-107">La méthode **ISoftKbd :: SetSoftKeyboardColors** définit la couleur du clavier logiciel pour le type de couleur spécifié.</span><span class="sxs-lookup"><span data-stu-id="75d3b-107">The **ISoftKbd::SetSoftKeyboardColors** method sets the soft keyboard color for the specified color type.</span></span>

## <a name="syntax"></a><span data-ttu-id="75d3b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75d3b-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardColors(
  [in] COLORTYPE colorType,
  [in] COLORREF  Color
);
```



## <a name="parameters"></a><span data-ttu-id="75d3b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75d3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d3b-110">*colorType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75d3b-110">*colorType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d3b-111">Valeur qui spécifie le type de couleur du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="75d3b-111">A value specifying the color type for the soft keyboard.</span></span> <span data-ttu-id="75d3b-112">Les valeurs possibles sont définies pour l’énumération [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) .</span><span class="sxs-lookup"><span data-stu-id="75d3b-112">Possible values are defined for the [**COLORTYPE**](/windows/win32/api/icm/ne-icm-colortype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="75d3b-113">*Couleur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75d3b-113">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d3b-114">Valeur [**COLORREF**](/windows/desktop/gdi/colorref) 32 bits spécifiant une couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="75d3b-114">A 32-bit [**COLORREF**](/windows/desktop/gdi/colorref) value specifying an RGB color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d3b-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75d3b-115">Return value</span></span>

<span data-ttu-id="75d3b-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="75d3b-116">This method can return one of these values.</span></span>



| <span data-ttu-id="75d3b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="75d3b-117">Value</span></span>                                                                                        | <span data-ttu-id="75d3b-118">Description</span><span class="sxs-lookup"><span data-stu-id="75d3b-118">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="75d3b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="75d3b-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="75d3b-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="75d3b-120">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="75d3b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75d3b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="75d3b-122">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="75d3b-122">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75d3b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75d3b-123">Requirements</span></span>



| <span data-ttu-id="75d3b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75d3b-124">Requirement</span></span> | <span data-ttu-id="75d3b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="75d3b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75d3b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d3b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="75d3b-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75d3b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="75d3b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75d3b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="75d3b-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75d3b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="75d3b-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="75d3b-130">Redistributable</span></span><br/>          | <span data-ttu-id="75d3b-131">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="75d3b-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="75d3b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="75d3b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="75d3b-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="75d3b-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="75d3b-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="75d3b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75d3b-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75d3b-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="75d3b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="75d3b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d3b-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d3b-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d3b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75d3b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d3b-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="75d3b-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="75d3b-140">**ISoftKbd::GetSoftKeyboardColors**</span><span class="sxs-lookup"><span data-stu-id="75d3b-140">**ISoftKbd::GetSoftKeyboardColors**</span></span>](isoftkbd-getsoftkeyboardcolors.md)
</dt> <dt>

[<span data-ttu-id="75d3b-141">**COLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="75d3b-141">**COLORTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colortype)
</dt> <dt>

[<span data-ttu-id="75d3b-142">**COLORREF**</span><span class="sxs-lookup"><span data-stu-id="75d3b-142">**COLORREF**</span></span>](/windows/desktop/gdi/colorref)
</dt> </dl>

 

