---
title: Méthode ISoftKbd SetSoftKeyboardPosSize (Softkbdc. h)
description: La méthode ISoftKbd SetSoftKeyboardPosSize définit la position de départ et la taille d’un clavier conditionnel.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Infrastructure des services de texte de méthode SetSoftKeyboardPosSize
- SetSoftKeyboardPosSize méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode SetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466302"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a><span data-ttu-id="f34ad-106">ISoftKbd :: SetSoftKeyboardPosSize, méthode</span><span class="sxs-lookup"><span data-stu-id="f34ad-106">ISoftKbd::SetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="f34ad-107">La méthode **ISoftKbd :: SetSoftKeyboardPosSize** définit la position de départ et la taille d’un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f34ad-107">The **ISoftKbd::SetSoftKeyboardPosSize** method sets the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="f34ad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f34ad-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a><span data-ttu-id="f34ad-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f34ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f34ad-110">*StartPoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f34ad-110">*StartPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f34ad-111">Structure de [points](/previous-versions//dd162805(v=vs.85)) indiquant les coordonnées de la position supérieure gauche du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f34ad-111">A [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="f34ad-112">*largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f34ad-112">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f34ad-113">Largeur du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f34ad-113">Width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="f34ad-114">*hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f34ad-114">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f34ad-115">Hauteur du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="f34ad-115">Height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f34ad-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f34ad-116">Return value</span></span>

<span data-ttu-id="f34ad-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f34ad-117">This method can return one of these values.</span></span>



| <span data-ttu-id="f34ad-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f34ad-118">Value</span></span>                                                                                        | <span data-ttu-id="f34ad-119">Description</span><span class="sxs-lookup"><span data-stu-id="f34ad-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f34ad-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f34ad-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f34ad-121">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f34ad-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="f34ad-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f34ad-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f34ad-123">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f34ad-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f34ad-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f34ad-124">Requirements</span></span>



| <span data-ttu-id="f34ad-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f34ad-125">Requirement</span></span> | <span data-ttu-id="f34ad-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f34ad-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f34ad-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f34ad-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f34ad-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f34ad-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f34ad-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f34ad-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f34ad-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f34ad-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f34ad-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f34ad-131">Redistributable</span></span><br/>          | <span data-ttu-id="f34ad-132">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="f34ad-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f34ad-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="f34ad-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f34ad-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="f34ad-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f34ad-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="f34ad-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f34ad-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f34ad-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f34ad-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f34ad-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f34ad-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f34ad-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f34ad-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f34ad-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f34ad-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="f34ad-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

