---
description: La méthode RenderOutputPins crée la partie aperçu du graphique de filtre.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'IRenderEngine :: RenderOutputPins, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541590"
---
# <a name="irenderenginerenderoutputpins-method"></a><span data-ttu-id="1410b-103">IRenderEngine :: RenderOutputPins, méthode</span><span class="sxs-lookup"><span data-stu-id="1410b-103">IRenderEngine::RenderOutputPins method</span></span>

> [!Note]  
> <span data-ttu-id="1410b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="1410b-104">\[Deprecated.</span></span> <span data-ttu-id="1410b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1410b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1410b-106">La `RenderOutputPins` méthode crée la partie aperçu du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="1410b-106">The `RenderOutputPins` method creates the previewing portion of the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="1410b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1410b-107">Syntax</span></span>


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a><span data-ttu-id="1410b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1410b-108">Parameters</span></span>

<span data-ttu-id="1410b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1410b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1410b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1410b-110">Return value</span></span>

<span data-ttu-id="1410b-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1410b-111">Returns an **HRESULT** values.</span></span> <span data-ttu-id="1410b-112">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1410b-112">The following are possible values:</span></span>



| <span data-ttu-id="1410b-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1410b-113">Return code</span></span>                                                                                                  | <span data-ttu-id="1410b-114">Description</span><span class="sxs-lookup"><span data-stu-id="1410b-114">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1410b-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1410b-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="1410b-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="1410b-116">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1410b-117"><dt>**VFW \_ S \_ audio \_ non \_ restitué**</dt></span><span class="sxs-lookup"><span data-stu-id="1410b-117"><dt>**VFW\_S\_AUDIO\_NOT\_RENDERED**</dt></span></span> </dl>  | <span data-ttu-id="1410b-118">Impossible de lire le flux audio.</span><span class="sxs-lookup"><span data-stu-id="1410b-118">Cannot play back the audio stream.</span></span><br/>                              |
| <dl> <span data-ttu-id="1410b-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1410b-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="1410b-120">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="1410b-120">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1410b-121"><dt>**le \_ moteur de rendu E \_ \_ est \_ défectueux**</dt></span><span class="sxs-lookup"><span data-stu-id="1410b-121"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="1410b-122">L’opération a échoué, car le projet n’a pas été rendu correctement.</span><span class="sxs-lookup"><span data-stu-id="1410b-122">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1410b-123"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="1410b-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="1410b-124">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="1410b-124">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="1410b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1410b-125">Remarks</span></span>

<span data-ttu-id="1410b-126">Avant d’appeler cette méthode, appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le composant frontal du graphique.</span><span class="sxs-lookup"><span data-stu-id="1410b-126">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="1410b-127">Pour effectuer une opération autre que la version préliminaire, n’appelez pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1410b-127">To perform an operation other than preview, do not call this method.</span></span> <span data-ttu-id="1410b-128">Au lieu de cela, appelez [**IRenderEngine :: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) pour obtenir des pointeurs vers les broches de sortie.</span><span class="sxs-lookup"><span data-stu-id="1410b-128">Instead, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to obtain pointers to the output pins.</span></span>

<span data-ttu-id="1410b-129">S’il n’y a aucune carte son sur l’ordinateur de l’utilisateur, cette méthode retourne VFW \_ s \_ audio \_ non \_ restitué.</span><span class="sxs-lookup"><span data-stu-id="1410b-129">If there is no sound card on the user's computer, this method returns VFW\_S\_AUDIO\_NOT\_RENDERED.</span></span> <span data-ttu-id="1410b-130">Dans ce cas, il n’y aura pas de préversion audio, mais la version préliminaire de la vidéo n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="1410b-130">There will not be audio preview in this case, but video preview is unaffected.</span></span>

<span data-ttu-id="1410b-131">Si le code PIN provient d’un groupe vidéo, cette méthode crée une fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="1410b-131">If the pin is from a video group, this method creates a video window.</span></span> <span data-ttu-id="1410b-132">Le thread appelant doit distribuer les messages (par exemple, pour déplacer la fenêtre ou répondre aux clics de souris dans la zone cliente de la fenêtre).</span><span class="sxs-lookup"><span data-stu-id="1410b-132">The calling thread must dispatch messages—for example, to move the window, or respond to mouse clicks in the window's client area.</span></span>

> [!Note]  
> <span data-ttu-id="1410b-133">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="1410b-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1410b-134">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1410b-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1410b-135">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1410b-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1410b-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1410b-136">Requirements</span></span>



| <span data-ttu-id="1410b-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1410b-137">Requirement</span></span> | <span data-ttu-id="1410b-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="1410b-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1410b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="1410b-139">Header</span></span><br/>  | <dl> <span data-ttu-id="1410b-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1410b-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1410b-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1410b-141">Library</span></span><br/> | <dl> <span data-ttu-id="1410b-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1410b-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1410b-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1410b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1410b-144">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="1410b-144">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="1410b-145">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="1410b-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




