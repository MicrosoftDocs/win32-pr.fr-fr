---
description: La méthode FindMediaFile recherche un fichier et, en cas de réussite, récupère le chemin d’accès au fichier.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'IMediaLocator :: FindMediaFile, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528018"
---
# <a name="imedialocatorfindmediafile-method"></a><span data-ttu-id="c4fc6-103">IMediaLocator :: FindMediaFile, méthode</span><span class="sxs-lookup"><span data-stu-id="c4fc6-103">IMediaLocator::FindMediaFile method</span></span>

> [!Note]  
> <span data-ttu-id="c4fc6-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-104">\[Deprecated.</span></span> <span data-ttu-id="c4fc6-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4fc6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4fc6-106">La `FindMediaFile` méthode recherche un fichier et, en cas de réussite, récupère le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-106">The `FindMediaFile` method searches for a file and, if successful, retrieves the path to the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4fc6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4fc6-107">Syntax</span></span>


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a><span data-ttu-id="c4fc6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4fc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4fc6-109">*Entrée*</span><span class="sxs-lookup"><span data-stu-id="c4fc6-109">*Input*</span></span> 
</dt> <dd>

<span data-ttu-id="c4fc6-110">Nom du fichier, y compris le chemin d’accès, où le fichier a été connu pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-110">File name, including path, where the file was last known to reside.</span></span> <span data-ttu-id="c4fc6-111">Pour les objets source de la chronologie, utilisez le nom du support actuel.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-111">For source objects in the timeline, use the current media name.</span></span>

</dd> <dt>

<span data-ttu-id="c4fc6-112">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="c4fc6-112">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="c4fc6-113">**BSTR** contenant des paires de chaînes de filtre, au format requis par le membre **lpstrFilter** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="c4fc6-113">A **BSTR** containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="c4fc6-114">Le localisateur de média utilise ce filtre s’il affiche une boîte de dialogue Ouvrir un fichier.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-114">The media locator uses this filter if it displays a File Open dialog box.</span></span> <span data-ttu-id="c4fc6-115">La valeur peut être **null** si le paramètre *Flags* n’inclut pas l' \_ \_ indicateur Popup SFN VALIDATEF.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-115">The value can be **NULL** if the *Flags* parameter does not include the SFN\_VALIDATEF\_POPUP flag.</span></span>

</dd> <dt>

<span data-ttu-id="c4fc6-116">*pOutput*</span><span class="sxs-lookup"><span data-stu-id="c4fc6-116">*pOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="c4fc6-117">Pointeur vers une variable qui reçoit le chemin d’accès réel au fichier, s’il diffère de la valeur contenue dans l' *entrée* et si la méthode parvient à localiser le fichier.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-117">Pointer to a variable that receives the actual path to the file, if it differs from the value contained in *Input* and if the method successfully locates the file.</span></span>

</dd> <dt>

<span data-ttu-id="c4fc6-118">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="c4fc6-118">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="c4fc6-119">Combinaison d’opérations de bits de zéro ou plusieurs indicateurs.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-119">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="c4fc6-120">Pour obtenir la liste des indicateurs possibles, consultez [**indicateurs de validation du nom de fichier**](file-name-validation-flags.md).</span><span class="sxs-lookup"><span data-stu-id="c4fc6-120">For a list of possible flags, see [**File Name Validation Flags**](file-name-validation-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4fc6-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4fc6-121">Return value</span></span>

<span data-ttu-id="c4fc6-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c4fc6-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4fc6-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4fc6-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c4fc6-124">Remarks</span></span>

<span data-ttu-id="c4fc6-125">La chaîne de filtre de la boîte de dialogue d’ouverture de fichier, qui est spécifiée par le paramètre *FilterString* , contient des caractères null internes.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-125">The filter string for the File Open dialog, which is specified by the *FilterString* parameter, contains internal Null characters.</span></span> <span data-ttu-id="c4fc6-126">Par exemple, Video \\ 0 \* . avi \\ 0 \\ 0 est une chaîne de filtre valide.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-126">For example, Video\\0\*.avi\\0\\0 is a valid filter string.</span></span> <span data-ttu-id="c4fc6-127">Vous ne pouvez pas utiliser la fonction **SysAllocStr** pour allouer le BSTR, car cette fonction attend une chaîne terminée par le caractère null et va tronquer la chaîne au premier caractère null.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-127">You cannot use the **SysAllocStr** function to allocate the BSTR, because that function expects a Null-terminated string and will truncate the string at the first Null character.</span></span> <span data-ttu-id="c4fc6-128">Par conséquent, utilisez une fonction telle que **SysAllocStringLen**, qui comprend un paramètre explicite pour la longueur :</span><span class="sxs-lookup"><span data-stu-id="c4fc6-128">Therefore, use a function such as **SysAllocStringLen**, which includes an explicit parameter for the length:</span></span>


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



<span data-ttu-id="c4fc6-129">Si l’utilisateur annule la boîte de dialogue d’ouverture de fichier, la méthode renvoie E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-129">If the user cancels the File Open dialog, the method returns E\_FAIL.</span></span>

<span data-ttu-id="c4fc6-130">La méthode alloue de la mémoire pour le **BSTR** dans *pOutput*.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-130">The method allocates memory for the **BSTR** in *pOutput*.</span></span> <span data-ttu-id="c4fc6-131">L’application doit appeler **SysFreeString** pour libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-131">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="c4fc6-132">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c4fc6-133">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4fc6-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c4fc6-134">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c4fc6-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4fc6-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4fc6-135">Requirements</span></span>



| <span data-ttu-id="c4fc6-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4fc6-136">Requirement</span></span> | <span data-ttu-id="c4fc6-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4fc6-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fc6-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4fc6-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c4fc6-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4fc6-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c4fc6-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c4fc6-140">Library</span></span><br/> | <dl> <span data-ttu-id="c4fc6-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4fc6-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4fc6-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4fc6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4fc6-143">**Interface IMediaLocator**</span><span class="sxs-lookup"><span data-stu-id="c4fc6-143">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="c4fc6-144">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="c4fc6-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
