---
title: Méthode ISoftKbd SelectSoftKeyboard (Softkbdc. h)
description: La méthode ISoftKbd SelectSoftKeyboard sélectionne le clavier logiciel spécifié.
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- Infrastructure des services de texte de méthode SelectSoftKeyboard
- SelectSoftKeyboard méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SelectSoftKeyboard
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509066"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a><span data-ttu-id="8dc7c-106">ISoftKbd :: SelectSoftKeyboard, méthode</span><span class="sxs-lookup"><span data-stu-id="8dc7c-106">ISoftKbd::SelectSoftKeyboard method</span></span>

<span data-ttu-id="8dc7c-107">La méthode **ISoftKbd :: SelectSoftKeyboard** sélectionne le clavier logiciel spécifié.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-107">The **ISoftKbd::SelectSoftKeyboard** method selects the specified soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dc7c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dc7c-108">Syntax</span></span>


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a><span data-ttu-id="8dc7c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8dc7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dc7c-110">*dwKeyboardId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8dc7c-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8dc7c-111">Identificateur du clavier conditionnel à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-111">Identifier of the soft keyboard to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dc7c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8dc7c-112">Return value</span></span>

<span data-ttu-id="8dc7c-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="8dc7c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dc7c-114">Value</span></span>                                                                                        | <span data-ttu-id="8dc7c-115">Description</span><span class="sxs-lookup"><span data-stu-id="8dc7c-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="8dc7c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8dc7c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8dc7c-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-117">The method was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="8dc7c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8dc7c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8dc7c-119">Le paramètre *dwKeyboardId* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8dc7c-119">The *dwKeyboardId* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8dc7c-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dc7c-120">Requirements</span></span>



| <span data-ttu-id="8dc7c-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dc7c-121">Requirement</span></span> | <span data-ttu-id="8dc7c-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dc7c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dc7c-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dc7c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8dc7c-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dc7c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8dc7c-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dc7c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8dc7c-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dc7c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8dc7c-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="8dc7c-127">Redistributable</span></span><br/>          | <span data-ttu-id="8dc7c-128">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="8dc7c-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="8dc7c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="8dc7c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dc7c-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dc7c-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="8dc7c-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="8dc7c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8dc7c-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8dc7c-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="8dc7c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8dc7c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8dc7c-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8dc7c-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dc7c-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dc7c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dc7c-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="8dc7c-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





