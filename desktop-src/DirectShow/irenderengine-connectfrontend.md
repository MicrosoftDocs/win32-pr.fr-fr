---
description: La méthode ConnectFrontEnd génère la partie frontale du graphique de filtre à partir de la chronologie actuelle.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'IRenderEngine :: ConnectFrontEnd, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543851"
---
# <a name="irenderengineconnectfrontend-method"></a><span data-ttu-id="f311e-103">IRenderEngine :: ConnectFrontEnd, méthode</span><span class="sxs-lookup"><span data-stu-id="f311e-103">IRenderEngine::ConnectFrontEnd method</span></span>

> [!Note]  
> <span data-ttu-id="f311e-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f311e-104">\[Deprecated.</span></span> <span data-ttu-id="f311e-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f311e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f311e-106">La `ConnectFrontEnd` méthode génère la partie frontale du graphique de filtre à partir de la chronologie actuelle.</span><span class="sxs-lookup"><span data-stu-id="f311e-106">The `ConnectFrontEnd` method builds the front end of the filter graph from the current timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="f311e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f311e-107">Syntax</span></span>


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a><span data-ttu-id="f311e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f311e-108">Parameters</span></span>

<span data-ttu-id="f311e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f311e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f311e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f311e-110">Return value</span></span>

<span data-ttu-id="f311e-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f311e-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f311e-112">Les valeurs de retour possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f311e-112">Possible return values include the following:</span></span>



| <span data-ttu-id="f311e-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f311e-113">Return code</span></span>                                                                                                  | <span data-ttu-id="f311e-114">Description</span><span class="sxs-lookup"><span data-stu-id="f311e-114">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f311e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="f311e-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f311e-116">Success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="f311e-117"><dt>**\_OUTPUTRESET avertir \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-117"><dt>**S\_WARN\_OUTPUTRESET**</dt></span></span> </dl>          | <span data-ttu-id="f311e-118">La partie de rendu du graphique a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="f311e-118">Rendering portion of the graph was deleted.</span></span><br/>                         |
| <dl> <span data-ttu-id="f311e-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="f311e-120">Aucune chronologie n’est définie pour ce moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="f311e-120">No timeline set for this render engine.</span></span><br/>                             |
| <dl> <span data-ttu-id="f311e-121"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="f311e-122">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="f311e-122">Render engine failed to initialize.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f311e-123"><dt>**le \_ moteur de rendu E \_ \_ est \_ défectueux**</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-123"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="f311e-124">L’opération a échoué, car le projet n’a pas été rendu correctement.</span><span class="sxs-lookup"><span data-stu-id="f311e-124">Operation failed because the project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f311e-125"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-125"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="f311e-126">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="f311e-126">Unexpected error.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="f311e-127"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-127"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl>      | <span data-ttu-id="f311e-128">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="f311e-128">Invalid media type.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f311e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="f311e-129">Remarks</span></span>

<span data-ttu-id="f311e-130">Cette méthode ne génère pas la partie de rendu du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="f311e-130">This method does not build the rendering portion of the filter graph.</span></span> <span data-ttu-id="f311e-131">L’application doit connecter les broches de sortie du serveur frontal aux filtres de rendu souhaités :</span><span class="sxs-lookup"><span data-stu-id="f311e-131">The application must connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="f311e-132">Pour afficher un aperçu, appelez la méthode [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md) .</span><span class="sxs-lookup"><span data-stu-id="f311e-132">To preview, call the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) method.</span></span>
-   <span data-ttu-id="f311e-133">Pour générer un fichier, appelez [**IRenderEngine :: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) pour récupérer la broche de sortie de chaque groupe, puis connectez les broches à un filtre multiplexeur.</span><span class="sxs-lookup"><span data-stu-id="f311e-133">To output a file, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to retrieve the output pin for each group, then connect the pins to a multiplexer filter.</span></span>

<span data-ttu-id="f311e-134">Si vous utilisez le moteur de rendu de base, les broches de sortie sur le serveur frontal produisent des données non compressées.</span><span class="sxs-lookup"><span data-stu-id="f311e-134">If you are using the basic render engine, the output pins on the front end produce uncompressed data.</span></span> <span data-ttu-id="f311e-135">Si vous utilisez le moteur de rendu intelligent, les broches de sortie produisent des données compressées.</span><span class="sxs-lookup"><span data-stu-id="f311e-135">If you are using the smart render engine, the output pins produce compressed data.</span></span>

<span data-ttu-id="f311e-136">Si vous modifiez la chronologie après avoir généré le graphique de filtre, vous devez à `ConnectFrontEnd` nouveau appeler pour reconstruire le serveur frontal.</span><span class="sxs-lookup"><span data-stu-id="f311e-136">If you change the timeline after you build the filter graph, you must call `ConnectFrontEnd` again to rebuild the front end.</span></span> <span data-ttu-id="f311e-137">La méthode conserve la partie de rendu du graphique chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="f311e-137">The method preserves the rendering portion of the graph whenever possible.</span></span> <span data-ttu-id="f311e-138">Toutefois, si vous ajoutez ou supprimez un groupe, ou si vous modifiez l’ordre des groupes, `ConnectFrontEnd` supprime la partie de rendu et votre application doit la reconstruire.</span><span class="sxs-lookup"><span data-stu-id="f311e-138">However, if you add or delete a group, or change the order of the groups, `ConnectFrontEnd` deletes the rendering portion and your application must rebuild it.</span></span> <span data-ttu-id="f311e-139">Si la méthode supprime la partie de rendu, elle retourne S \_ WARN \_ OUTPUTRESET.</span><span class="sxs-lookup"><span data-stu-id="f311e-139">If the method deletes the rendering portion, it returns S\_WARN\_OUTPUTRESET.</span></span>

> [!Note]  
> <span data-ttu-id="f311e-140">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f311e-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f311e-141">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f311e-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f311e-142">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f311e-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f311e-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f311e-143">Requirements</span></span>



| <span data-ttu-id="f311e-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f311e-144">Requirement</span></span> | <span data-ttu-id="f311e-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="f311e-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f311e-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="f311e-146">Header</span></span><br/>  | <dl> <span data-ttu-id="f311e-147"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f311e-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f311e-148">Library</span></span><br/> | <dl> <span data-ttu-id="f311e-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f311e-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f311e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f311e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f311e-151">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="f311e-151">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="f311e-152">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="f311e-152">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




