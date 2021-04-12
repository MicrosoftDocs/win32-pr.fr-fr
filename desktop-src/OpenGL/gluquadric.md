---
title: gluQuadricCallback, fonction (Glu. h)
description: La fonction gluQuadricCallback définit un rappel pour un objet quadric.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluQuadricCallback fonction OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508998"
---
# <a name="gluquadriccallback-function"></a><span data-ttu-id="15450-104">gluQuadricCallback fonction)</span><span class="sxs-lookup"><span data-stu-id="15450-104">gluQuadricCallback function</span></span>

<span data-ttu-id="15450-105">La fonction **gluQuadricCallback** définit un rappel pour un objet quadric.</span><span class="sxs-lookup"><span data-stu-id="15450-105">The **gluQuadricCallback** function defines a callback for a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="15450-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15450-106">Syntax</span></span>


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="15450-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15450-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15450-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="15450-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="15450-109">Objet quadric (créé avec [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="15450-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="15450-110">*et*</span><span class="sxs-lookup"><span data-stu-id="15450-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="15450-111">Rappel en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="15450-111">The callback being defined.</span></span> <span data-ttu-id="15450-112">La seule valeur valide est GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="15450-112">The only valid value is GLU\_ERROR.</span></span>



| <span data-ttu-id="15450-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="15450-113">Value</span></span>                                                                                                                                             | <span data-ttu-id="15450-114">Signification</span><span class="sxs-lookup"><span data-stu-id="15450-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <span data-ttu-id="15450-115"><dt>**\_erreur Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="15450-115"><dt>**GLU\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="15450-116">La fonction **gluQuadricCallback** est appelée lorsqu’une erreur est rencontrée.</span><span class="sxs-lookup"><span data-stu-id="15450-116">The **gluQuadricCallback** function is called when an error is encountered.</span></span> <span data-ttu-id="15450-117">Son argument unique est de type **GLenum** et indique l’erreur spécifique qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="15450-117">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="15450-118">Les chaînes de caractères décrivant ces erreurs peuvent être récupérées avec l’appel [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="15450-118">Character strings describing these errors can be retrieved with the [**gluErrorString**](gluerrorstring.md) call.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="15450-119">*FN*</span><span class="sxs-lookup"><span data-stu-id="15450-119">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="15450-120">Fonction à appeler.</span><span class="sxs-lookup"><span data-stu-id="15450-120">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15450-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="15450-121">Return value</span></span>

<span data-ttu-id="15450-122">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="15450-122">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15450-123">Notes</span><span class="sxs-lookup"><span data-stu-id="15450-123">Remarks</span></span>

<span data-ttu-id="15450-124">Utilisez **gluQuadricCallback** pour définir un nouveau rappel devant être utilisé par un objet quadric.</span><span class="sxs-lookup"><span data-stu-id="15450-124">Use **gluQuadricCallback** to define a new callback to be used by a quadric object.</span></span> <span data-ttu-id="15450-125">Si le rappel spécifié est déjà défini, il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="15450-125">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="15450-126">Si *FN* a la **valeur null**, tous les rappels existants sont effacés.</span><span class="sxs-lookup"><span data-stu-id="15450-126">If *fn* is **NULL**, any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="15450-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15450-127">Requirements</span></span>



| <span data-ttu-id="15450-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15450-128">Requirement</span></span> | <span data-ttu-id="15450-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="15450-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="15450-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15450-130">Minimum supported client</span></span><br/> | <span data-ttu-id="15450-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15450-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="15450-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15450-132">Minimum supported server</span></span><br/> | <span data-ttu-id="15450-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15450-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="15450-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="15450-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="15450-135"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="15450-135"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="15450-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="15450-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="15450-137"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15450-137"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="15450-138">DLL</span><span class="sxs-lookup"><span data-stu-id="15450-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15450-139"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15450-139"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15450-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15450-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15450-141">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="15450-141">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="15450-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="15450-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





