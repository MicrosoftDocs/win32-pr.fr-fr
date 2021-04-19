---
description: La méthode ValidateSourceNames valide les noms de sources dans la chronologie, à l’aide du localisateur de média. Si vous le souhaitez, cette méthode met également à jour tout objet source pour lequel il localise un fichier.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'IAMTimeline :: ValidateSourceNames, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529910"
---
# <a name="iamtimelinevalidatesourcenames-method"></a><span data-ttu-id="15c05-104">IAMTimeline :: ValidateSourceNames, méthode</span><span class="sxs-lookup"><span data-stu-id="15c05-104">IAMTimeline::ValidateSourceNames method</span></span>

> [!Note]  
> <span data-ttu-id="15c05-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="15c05-105">\[Deprecated.</span></span> <span data-ttu-id="15c05-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15c05-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="15c05-107">La `ValidateSourceNames` méthode valide les noms de sources dans la chronologie, à l’aide du localisateur de média.</span><span class="sxs-lookup"><span data-stu-id="15c05-107">The `ValidateSourceNames` method validates source names in the timeline, using the media locator.</span></span> <span data-ttu-id="15c05-108">Si vous le souhaitez, cette méthode met également à jour tout objet source pour lequel il localise un fichier.</span><span class="sxs-lookup"><span data-stu-id="15c05-108">Optionally, this method also updates any source object for which it locates a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c05-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15c05-109">Syntax</span></span>


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a><span data-ttu-id="15c05-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15c05-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c05-111">*ValidateFlags*</span><span class="sxs-lookup"><span data-stu-id="15c05-111">*ValidateFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="15c05-112">Combinaison d’opérations de bits des [**indicateurs de validation de nom de fichier**](file-name-validation-flags.md) spécifiant le comportement du localisateur de média.</span><span class="sxs-lookup"><span data-stu-id="15c05-112">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="15c05-113">Les \_ indicateurs SFN VALIDATEF \_ Replace et SFN \_ VALIDATEF \_ Check doivent être présents, sinon la méthode renvoie E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="15c05-113">The SFN\_VALIDATEF\_REPLACE and SFN\_VALIDATEF\_CHECK flags must be present, or the method returns E\_INVALIDARG.</span></span>

</dd> <dt>

<span data-ttu-id="15c05-114">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="15c05-114">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="15c05-115">Pointeur facultatif vers l’interface [**IMediaLocator**](imedialocator.md) d’un localisateur de média à utiliser à la place de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="15c05-115">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="15c05-116">Pour utiliser le localisateur de média par défaut, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="15c05-116">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="15c05-117">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="15c05-117">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="15c05-118">*NotifyEventHandle*</span><span class="sxs-lookup"><span data-stu-id="15c05-118">*NotifyEventHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="15c05-119">Handle vers un événement.</span><span class="sxs-lookup"><span data-stu-id="15c05-119">Handle to an event.</span></span> <span data-ttu-id="15c05-120">La méthode signale l’événement une fois la validation terminée.</span><span class="sxs-lookup"><span data-stu-id="15c05-120">The method signals the event after it has completed the validation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c05-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15c05-121">Return value</span></span>

<span data-ttu-id="15c05-122">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="15c05-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15c05-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15c05-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="15c05-124">Notes</span><span class="sxs-lookup"><span data-stu-id="15c05-124">Remarks</span></span>

<span data-ttu-id="15c05-125">À l’aide du paramètre *pOverride* , vous pouvez fournir votre propre implémentation personnalisée de l’interface [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="15c05-125">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="15c05-126">Par exemple, le localisateur de média par défaut n’informe pas votre application des fichiers qu’il trouve (ou ne peut pas trouver).</span><span class="sxs-lookup"><span data-stu-id="15c05-126">For example, the default media locator will not notify your application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="15c05-127">Pour contourner cette limitation, vous pouvez implémenter un localisateur de média personnalisé, ce qui en fait un wrapper pour la version par défaut.</span><span class="sxs-lookup"><span data-stu-id="15c05-127">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="15c05-128">Dans votre version personnalisée, transmettez [**IMediaLocator :: FindMediaFile**](imedialocator-findmediafile.md) appelle directement à la version par défaut, puis examinez la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="15c05-128">In your custom version, pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version, and examine the return value.</span></span>

> [!Note]  
> <span data-ttu-id="15c05-129">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="15c05-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="15c05-130">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="15c05-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="15c05-131">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="15c05-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15c05-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15c05-132">Requirements</span></span>



| <span data-ttu-id="15c05-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15c05-133">Requirement</span></span> | <span data-ttu-id="15c05-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="15c05-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15c05-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="15c05-135">Header</span></span><br/>  | <dl> <span data-ttu-id="15c05-136"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="15c05-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="15c05-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="15c05-137">Library</span></span><br/> | <dl> <span data-ttu-id="15c05-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15c05-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15c05-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15c05-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c05-140">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="15c05-140">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="15c05-141">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="15c05-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




