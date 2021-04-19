---
description: La méthode SetSourceNameValidation spécifie la manière dont le moteur de rendu valide les noms de fichiers.
ms.assetid: b33904cd-ed7d-41b5-9ebf-50983ec9f7b3
title: 'IRenderEngine :: SetSourceNameValidation, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetSourceNameValidation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 96164a817fd04f505b32c17be1bff3268e847df8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543267"
---
# <a name="irenderenginesetsourcenamevalidation-method"></a><span data-ttu-id="b4438-103">IRenderEngine :: SetSourceNameValidation, méthode</span><span class="sxs-lookup"><span data-stu-id="b4438-103">IRenderEngine::SetSourceNameValidation method</span></span>

> [!Note]  
> <span data-ttu-id="b4438-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b4438-104">\[Deprecated.</span></span> <span data-ttu-id="b4438-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b4438-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b4438-106">La `SetSourceNameValidation` méthode spécifie la manière dont le moteur de rendu valide les noms de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b4438-106">The `SetSourceNameValidation` method specifies how the render engine validates file names.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4438-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4438-107">Syntax</span></span>


```C++
HRESULT SetSourceNameValidation(
   BSTR          FilterString,
   IMediaLocator *pOverride,
   LONG          Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b4438-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4438-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4438-109">*FilterString*</span><span class="sxs-lookup"><span data-stu-id="b4438-109">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="b4438-110">Valeur **BSTR** contenant des paires de chaînes de filtre, au format requis par le membre **lpstrFilter** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="b4438-110">**BSTR** value containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="b4438-111">Le localisateur de média utilise ce filtre s’il présente une boîte de dialogue Ouvrir un fichier à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="b4438-111">The media locator uses this filter if it presents an Open File dialog box to the end user.</span></span>

</dd> <dt>

<span data-ttu-id="b4438-112">*pOverride*</span><span class="sxs-lookup"><span data-stu-id="b4438-112">*pOverride*</span></span> 
</dt> <dd>

<span data-ttu-id="b4438-113">Pointeur facultatif vers l’interface [**IMediaLocator**](imedialocator.md) d’un localisateur de média à utiliser à la place de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4438-113">Optional pointer to the [**IMediaLocator**](imedialocator.md) interface of a media locator to use in place of the default.</span></span> <span data-ttu-id="b4438-114">Pour utiliser le localisateur de média par défaut, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="b4438-114">To use the default media locator, set the value of this parameter to **NULL**.</span></span> <span data-ttu-id="b4438-115">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b4438-115">See Remarks for more information.</span></span>

</dd> <dt>

<span data-ttu-id="b4438-116">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="b4438-116">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="b4438-117">Combinaison d’opérations de bits des [**indicateurs de validation de nom de fichier**](file-name-validation-flags.md) spécifiant le comportement du localisateur de média.</span><span class="sxs-lookup"><span data-stu-id="b4438-117">Bitwise combination of [**File Name Validation Flags**](file-name-validation-flags.md) specifying the behavior of the media locator.</span></span> <span data-ttu-id="b4438-118">L' \_ indicateur de vérification SFN VALIDATEF \_ doit être présent.</span><span class="sxs-lookup"><span data-stu-id="b4438-118">The SFN\_VALIDATEF\_CHECK flag must be present.</span></span> <span data-ttu-id="b4438-119">L' \_ indicateur SFN VALIDATEF \_ hlinkMUTED n’a aucun effet avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b4438-119">The SFN\_VALIDATEF\_hlinkMUTED flag has no effect with this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4438-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4438-120">Return value</span></span>

<span data-ttu-id="b4438-121">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="b4438-121">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b4438-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4438-122">Return code</span></span>                                                                                            | <span data-ttu-id="b4438-123">Description</span><span class="sxs-lookup"><span data-stu-id="b4438-123">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="b4438-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4438-124"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="b4438-125">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b4438-125">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="b4438-126"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="b4438-126"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="b4438-127">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="b4438-127">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4438-128">Notes</span><span class="sxs-lookup"><span data-stu-id="b4438-128">Remarks</span></span>

<span data-ttu-id="b4438-129">À l’aide du paramètre *pOverride* , vous pouvez fournir votre propre implémentation personnalisée de l’interface [**IMediaLocator**](imedialocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b4438-129">Using the *pOverride* parameter, you can supply your own custom implementation of the [**IMediaLocator**](imedialocator.md) interface.</span></span> <span data-ttu-id="b4438-130">Par exemple, le localisateur de média par défaut n’avertit pas une application des fichiers qu’elle trouve (ou ne peut pas trouver).</span><span class="sxs-lookup"><span data-stu-id="b4438-130">For example, the default media locator does not notify an application about the files that it finds (or cannot find).</span></span> <span data-ttu-id="b4438-131">Pour contourner cette limitation, vous pouvez implémenter un localisateur de média personnalisé, ce qui en fait un wrapper pour la version par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4438-131">To get around this limitation, you could implement a custom media locator, making it a wrapper for the default version.</span></span> <span data-ttu-id="b4438-132">Ensuite, transmettez [**IMediaLocator :: FindMediaFile**](imedialocator-findmediafile.md) appelle directement à la version par défaut et examinez la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="b4438-132">Then pass [**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md) calls directly to the default version and examine the return value.</span></span>

<span data-ttu-id="b4438-133">Actuellement, cette méthode ne valide pas les sources chargées dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="b4438-133">Currently, this method does not validate dynamically loaded sources.</span></span> <span data-ttu-id="b4438-134">Consultez [**IRenderEngine :: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="b4438-134">See [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="b4438-135">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b4438-135">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b4438-136">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b4438-136">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b4438-137">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b4438-137">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4438-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4438-138">Requirements</span></span>



| <span data-ttu-id="b4438-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4438-139">Requirement</span></span> | <span data-ttu-id="b4438-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4438-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4438-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4438-141">Header</span></span><br/>  | <dl> <span data-ttu-id="b4438-142"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4438-142"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b4438-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4438-143">Library</span></span><br/> | <dl> <span data-ttu-id="b4438-144"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4438-144"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4438-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4438-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4438-146">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="b4438-146">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="b4438-147">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b4438-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
