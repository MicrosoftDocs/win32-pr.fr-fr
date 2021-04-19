---
description: La fonction GetCaptureCommentFromFilename extrait le commentaire de capture à partir d’un fichier de capture.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: GetCaptureCommentFromFilename, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515615"
---
# <a name="getcapturecommentfromfilename-function"></a><span data-ttu-id="1cd6e-103">GetCaptureCommentFromFilename fonction)</span><span class="sxs-lookup"><span data-stu-id="1cd6e-103">GetCaptureCommentFromFilename function</span></span>

<span data-ttu-id="1cd6e-104">La fonction **GetCaptureCommentFromFilename** extrait le commentaire de capture à partir d’un [*fichier de capture*](c.md).</span><span class="sxs-lookup"><span data-stu-id="1cd6e-104">The **GetCaptureCommentFromFilename** function extracts the capture comment from a [*capture file*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cd6e-105">Syntax</span></span>


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="1cd6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cd6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd6e-107">*lpFilename* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cd6e-107">*lpFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd6e-108">Pointeur vers le nom du fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-108">Pointer to the name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="1cd6e-109">*lpComment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cd6e-109">*lpComment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd6e-110">Pointeur vers une chaîne pré-allouée pour le commentaire.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-110">Pointer to a pre-allocated string for the comment.</span></span>

</dd> <dt>

<span data-ttu-id="1cd6e-111">*BufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1cd6e-111">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cd6e-112">Taille de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-112">Size of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd6e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cd6e-113">Return value</span></span>

<span data-ttu-id="1cd6e-114">Si la fonction réussit (autrement dit, si le commentaire est trouvé et copié, ou s’il n’y a aucun commentaire dans le fichier de capture), la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-114">If the function is successful (that is, if the comment is found and copied, or there is no comment in the capture file), the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1cd6e-115">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-115">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="1cd6e-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1cd6e-116">Return code</span></span>                                                                                                 | <span data-ttu-id="1cd6e-117">Description</span><span class="sxs-lookup"><span data-stu-id="1cd6e-117">Description</span></span>                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cd6e-118"><dt>**\_erreur de \_ lecture du fichier NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-118"><dt>**NMERR\_FILE\_READ\_ERROR**</dt></span></span> </dl>     | <span data-ttu-id="1cd6e-119">Impossible de lire le commentaire de capture.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-119">The capture comment cannot be read.</span></span><br/>                               |
| <dl> <span data-ttu-id="1cd6e-120"><dt>**\_format de \_ fichier non valide NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-120"><dt>**NMERR\_INVALID\_FILE\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="1cd6e-121">La trame de commentaire n’est pas un format de fichier valide.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-121">The Comment frame is not a valid file format.</span></span><br/>                     |
| <dl> <span data-ttu-id="1cd6e-122"><dt>**\_fichier NMERR \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-122"><dt>**NMERR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>      | <span data-ttu-id="1cd6e-123">Impossible de trouver le fichier spécifié par le paramètre *lpFilename* .</span><span class="sxs-lookup"><span data-stu-id="1cd6e-123">The file specified by the *lpFilename* parameter cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="1cd6e-124"><dt>**\_paramètre NMERR non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-124"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="1cd6e-125">L’un des paramètres est spécifié de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="1cd6e-125">One of the parameters is specified incorrectly.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="1cd6e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="1cd6e-126">Remarks</span></span>

<span data-ttu-id="1cd6e-127">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureCommentFromFilename** .</span><span class="sxs-lookup"><span data-stu-id="1cd6e-127">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureCommentFromFilename** function.</span></span>

<span data-ttu-id="1cd6e-128">Pour récupérer le commentaire d’une capture en temps réel, appelez la fonction [GetCaptureComment](getcapturecomment.md) .</span><span class="sxs-lookup"><span data-stu-id="1cd6e-128">To retrieve the comment of a real-time capture, call the [GetCaptureComment](getcapturecomment.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd6e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cd6e-129">Requirements</span></span>



| <span data-ttu-id="1cd6e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cd6e-130">Requirement</span></span> | <span data-ttu-id="1cd6e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cd6e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd6e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cd6e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1cd6e-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cd6e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1cd6e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cd6e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1cd6e-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cd6e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1cd6e-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cd6e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cd6e-137"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-137"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1cd6e-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1cd6e-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cd6e-139"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-139"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1cd6e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1cd6e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cd6e-141"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cd6e-141"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cd6e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cd6e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cd6e-143">GetCaptureComment</span><span class="sxs-lookup"><span data-stu-id="1cd6e-143">GetCaptureComment</span></span>](getcapturecomment.md)
</dt> </dl>

 

 




