---
title: Méthode ISoftKbd SetKeyboardLabelText (Softkbdc. h)
description: La méthode ISoftKbd SetKeyboardLabelText définit le texte de l’étiquette à partir de la disposition d’un clavier conditionnel.
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- Infrastructure des services de texte de méthode SetKeyboardLabelText
- SetKeyboardLabelText méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetKeyboardLabelText
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742789"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a><span data-ttu-id="a85d8-106">ISoftKbd :: SetKeyboardLabelText, méthode</span><span class="sxs-lookup"><span data-stu-id="a85d8-106">ISoftKbd::SetKeyboardLabelText method</span></span>

<span data-ttu-id="a85d8-107">La méthode **ISoftKbd :: SetKeyboardLabelText** définit le texte de l’étiquette à partir de la disposition d’un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a85d8-107">The **ISoftKbd::SetKeyboardLabelText** method sets the label text from the layout for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="a85d8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a85d8-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a><span data-ttu-id="a85d8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a85d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a85d8-110">*hKl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a85d8-110">*hKl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a85d8-111">Handle utilisé pour récupérer la disposition installée pour le clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a85d8-111">Handle that is used to retrieve the installed layout for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a85d8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a85d8-112">Return value</span></span>

<span data-ttu-id="a85d8-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a85d8-113">This method can return one of these values.</span></span>



| <span data-ttu-id="a85d8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a85d8-114">Value</span></span>                                                                                        | <span data-ttu-id="a85d8-115">Description</span><span class="sxs-lookup"><span data-stu-id="a85d8-115">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="a85d8-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a85d8-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a85d8-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a85d8-117">The method was successful.</span></span><br/>      |
| <dl> <span data-ttu-id="a85d8-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a85d8-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a85d8-119">Le paramètre *hKl* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a85d8-119">The *hKl* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a85d8-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a85d8-120">Requirements</span></span>



| <span data-ttu-id="a85d8-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a85d8-121">Requirement</span></span> | <span data-ttu-id="a85d8-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a85d8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a85d8-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a85d8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a85d8-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a85d8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a85d8-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a85d8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a85d8-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a85d8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a85d8-127">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a85d8-127">Redistributable</span></span><br/>          | <span data-ttu-id="a85d8-128">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a85d8-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a85d8-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a85d8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a85d8-130"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a85d8-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a85d8-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="a85d8-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a85d8-132"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a85d8-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a85d8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a85d8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a85d8-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a85d8-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a85d8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a85d8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85d8-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a85d8-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="a85d8-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="a85d8-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





