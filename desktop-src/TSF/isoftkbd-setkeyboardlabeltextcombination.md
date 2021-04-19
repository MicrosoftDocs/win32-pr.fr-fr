---
title: Méthode ISoftKbd SetKeyboardLabelTextCombination (Softkbdc. h)
description: La méthode ISoftKbd SetKeyboardLabelTextCombination définit une combinaison d’étiquette et de texte utilisée pour décrire un clavier conditionnel.
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- Infrastructure des services de texte de méthode SetKeyboardLabelTextCombination
- SetKeyboardLabelTextCombination méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetKeyboardLabelTextCombination
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509738"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a><span data-ttu-id="bfa60-106">ISoftKbd :: SetKeyboardLabelTextCombination, méthode</span><span class="sxs-lookup"><span data-stu-id="bfa60-106">ISoftKbd::SetKeyboardLabelTextCombination method</span></span>

<span data-ttu-id="bfa60-107">La méthode **ISoftKbd :: SetKeyboardLabelTextCombination** définit une combinaison d’étiquette et de texte utilisée pour décrire un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="bfa60-107">The **ISoftKbd::SetKeyboardLabelTextCombination** method sets a combination of label and text used to describe a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfa60-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfa60-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a><span data-ttu-id="bfa60-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfa60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa60-110">*nModifierCombination* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfa60-110">*nModifierCombination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfa60-111">Combinaison d’étiquette et de texte utilisée pour décrire le clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="bfa60-111">Combination of label and text used to describe the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa60-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bfa60-112">Return value</span></span>

<span data-ttu-id="bfa60-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="bfa60-113">This method can return one of these values.</span></span>



| <span data-ttu-id="bfa60-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfa60-114">Value</span></span>                                                                                        | <span data-ttu-id="bfa60-115">Description</span><span class="sxs-lookup"><span data-stu-id="bfa60-115">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="bfa60-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa60-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bfa60-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="bfa60-117">The method was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="bfa60-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bfa60-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bfa60-119">Le paramètre *nModifierCombination* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bfa60-119">The *nModifierCombination* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bfa60-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfa60-120">Requirements</span></span>



| <span data-ttu-id="bfa60-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfa60-121">Requirement</span></span> | <span data-ttu-id="bfa60-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfa60-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa60-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa60-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa60-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfa60-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bfa60-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfa60-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa60-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfa60-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bfa60-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bfa60-127">Redistributable</span></span><br/>          | <span data-ttu-id="bfa60-128">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="bfa60-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="bfa60-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfa60-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa60-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa60-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="bfa60-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="bfa60-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bfa60-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bfa60-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="bfa60-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bfa60-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfa60-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfa60-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfa60-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfa60-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfa60-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="bfa60-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="bfa60-137">**ISoftKbd::SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="bfa60-137">**ISoftKbd::SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





