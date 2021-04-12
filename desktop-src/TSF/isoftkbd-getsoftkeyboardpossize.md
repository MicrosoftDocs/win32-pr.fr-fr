---
title: Méthode ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: La méthode ISoftKbd GetSoftKeyboardPosSize récupère la position de départ et la taille d’un clavier conditionnel.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Infrastructure des services de texte de méthode GetSoftKeyboardPosSize
- GetSoftKeyboardPosSize méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317341"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a><span data-ttu-id="a64b9-106">ISoftKbd :: GetSoftKeyboardPosSize, méthode</span><span class="sxs-lookup"><span data-stu-id="a64b9-106">ISoftKbd::GetSoftKeyboardPosSize method</span></span>

<span data-ttu-id="a64b9-107">La méthode **ISoftKbd :: GetSoftKeyboardPosSize** récupère la position de départ et la taille d’un clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a64b9-107">The **ISoftKbd::GetSoftKeyboardPosSize** method retrieves the starting position and size of a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64b9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a64b9-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a><span data-ttu-id="a64b9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a64b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a64b9-110">*lpStartPoint* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a64b9-110">*lpStartPoint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64b9-111">Pointeur vers une mémoire tampon dans laquelle cette méthode récupère une structure de [points](/previous-versions//dd162805(v=vs.85)) indiquant les coordonnées de la position supérieure gauche du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a64b9-111">Pointer to a buffer in which this method retrieves a [POINT](/previous-versions//dd162805(v=vs.85)) structure indicating the coordinates of the upper left position of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="a64b9-112">*lpwidth* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a64b9-112">*lpwidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64b9-113">Pointeur vers une mémoire tampon dans laquelle cette méthode récupère la largeur du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a64b9-113">Pointer to a buffer in which this method retrieves the width of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="a64b9-114">*lpheight* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a64b9-114">*lpheight* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64b9-115">Pointeur vers une mémoire tampon dans laquelle cette méthode récupère la hauteur du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="a64b9-115">Pointer to a buffer in which this method retrieves the height of the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a64b9-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a64b9-116">Return value</span></span>

<span data-ttu-id="a64b9-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a64b9-117">This method can return one of these values.</span></span>



| <span data-ttu-id="a64b9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a64b9-118">Value</span></span>                                                                                        | <span data-ttu-id="a64b9-119">Description</span><span class="sxs-lookup"><span data-stu-id="a64b9-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a64b9-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a64b9-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a64b9-121">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a64b9-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="a64b9-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a64b9-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a64b9-123">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a64b9-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a64b9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a64b9-124">Requirements</span></span>



| <span data-ttu-id="a64b9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a64b9-125">Requirement</span></span> | <span data-ttu-id="a64b9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a64b9-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a64b9-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a64b9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a64b9-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a64b9-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a64b9-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a64b9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a64b9-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a64b9-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a64b9-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a64b9-131">Redistributable</span></span><br/>          | <span data-ttu-id="a64b9-132">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a64b9-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a64b9-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a64b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a64b9-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="a64b9-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a64b9-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="a64b9-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a64b9-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a64b9-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a64b9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a64b9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a64b9-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a64b9-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a64b9-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a64b9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64b9-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a64b9-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="a64b9-141">**ISoftKbd::SetSoftKeyboardPosSize**</span><span class="sxs-lookup"><span data-stu-id="a64b9-141">**ISoftKbd::SetSoftKeyboardPosSize**</span></span>](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

