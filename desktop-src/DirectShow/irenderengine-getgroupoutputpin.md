---
description: La méthode GetGroupOutputPin récupère la broche de sortie pour le groupe spécifié.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'IRenderEngine :: GetGroupOutputPin, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528909"
---
# <a name="irenderenginegetgroupoutputpin-method"></a><span data-ttu-id="b674a-103">IRenderEngine :: GetGroupOutputPin, méthode</span><span class="sxs-lookup"><span data-stu-id="b674a-103">IRenderEngine::GetGroupOutputPin method</span></span>

> [!Note]  
> <span data-ttu-id="b674a-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b674a-104">\[Deprecated.</span></span> <span data-ttu-id="b674a-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b674a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b674a-106">La `GetGroupOutputPin` méthode récupère la broche de sortie pour le groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="b674a-106">The `GetGroupOutputPin` method retrieves the output pin for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="b674a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b674a-107">Syntax</span></span>


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a><span data-ttu-id="b674a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b674a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b674a-109">*Groupe*</span><span class="sxs-lookup"><span data-stu-id="b674a-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="b674a-110">Index de base zéro qui spécifie le groupe.</span><span class="sxs-lookup"><span data-stu-id="b674a-110">Zero-based index that specifies the group.</span></span>

</dd> <dt>

<span data-ttu-id="b674a-111">*ppRenderPin* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b674a-111">*ppRenderPin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b674a-112">Reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="b674a-112">Receives a pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b674a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b674a-113">Return value</span></span>

<span data-ttu-id="b674a-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b674a-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b674a-115">Il peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="b674a-115">Possible values include the following:</span></span>



| <span data-ttu-id="b674a-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b674a-116">Return code</span></span>                                                                                                  | <span data-ttu-id="b674a-117">Description</span><span class="sxs-lookup"><span data-stu-id="b674a-117">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b674a-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-118"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="b674a-119">Le groupe n’a pas de broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="b674a-119">Group does not have an output pin.</span></span><br/>                              |
| <dl> <span data-ttu-id="b674a-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-120"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="b674a-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="b674a-121">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b674a-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="b674a-123">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="b674a-123">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b674a-124"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-124"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="b674a-125">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="b674a-125">Render engine failed to initialize.</span></span><br/>                             |
| <dl> <span data-ttu-id="b674a-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-126"><dt>**E\_POINTER**</dt></span></span> </dl>                    | <span data-ttu-id="b674a-127">Pointeur non valide.</span><span class="sxs-lookup"><span data-stu-id="b674a-127">Invalid pointer.</span></span><br/>                                                |
| <dl> <span data-ttu-id="b674a-128"><dt>**le \_ moteur de rendu E \_ \_ est \_ défectueux**</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-128"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="b674a-129">L’opération a échoué, car le projet n’a pas été rendu correctement.</span><span class="sxs-lookup"><span data-stu-id="b674a-129">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b674a-130"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-130"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="b674a-131">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="b674a-131">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="b674a-132">Notes</span><span class="sxs-lookup"><span data-stu-id="b674a-132">Remarks</span></span>

<span data-ttu-id="b674a-133">Avant d’appeler cette méthode, appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le composant frontal du graphique.</span><span class="sxs-lookup"><span data-stu-id="b674a-133">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="b674a-134">Chaque groupe représente un flux de données multimédia unique et le serveur frontal a une broche de sortie correspondante.</span><span class="sxs-lookup"><span data-stu-id="b674a-134">Each group represents a single media stream, and the front end has a corresponding output pin.</span></span>

<span data-ttu-id="b674a-135">Vous pouvez utiliser cette méthode pour créer la partie de rendu d’un graphique d’écriture de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b674a-135">You can use this method to create the rendering portion of a file-writing graph.</span></span> <span data-ttu-id="b674a-136">Connectez les broches de sortie aux filtres de multiplexeur et de writer de fichier.</span><span class="sxs-lookup"><span data-stu-id="b674a-136">Connect the output pins to multiplexer filters and file writer filters.</span></span> <span data-ttu-id="b674a-137">Pour plus d’informations, consultez [rendu d’un projet](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="b674a-137">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="b674a-138">Pour la version préliminaire, vous n’avez pas besoin d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="b674a-138">For preview, you don't need to call this method.</span></span> <span data-ttu-id="b674a-139">Appelez simplement **ConnectFrontEnd** suivi de [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md).</span><span class="sxs-lookup"><span data-stu-id="b674a-139">Just call **ConnectFrontEnd** followed by [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span>

<span data-ttu-id="b674a-140">Si la méthode retourne la valeur \_ OK, l’interface **IPIN** qu’elle retourne a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="b674a-140">If the method returns S\_OK, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="b674a-141">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="b674a-141">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="b674a-142">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="b674a-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b674a-143">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b674a-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b674a-144">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b674a-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b674a-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b674a-145">Requirements</span></span>



| <span data-ttu-id="b674a-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b674a-146">Requirement</span></span> | <span data-ttu-id="b674a-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="b674a-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b674a-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="b674a-148">Header</span></span><br/>  | <dl> <span data-ttu-id="b674a-149"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b674a-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b674a-150">Library</span></span><br/> | <dl> <span data-ttu-id="b674a-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b674a-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b674a-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b674a-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b674a-153">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="b674a-153">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="b674a-154">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="b674a-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




