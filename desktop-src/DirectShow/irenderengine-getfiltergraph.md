---
description: La méthode GetFilterGraph récupère le graphique de filtre que le moteur de rendu a construit, le cas échéant.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'IRenderEngine :: GetFilterGraph, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530283"
---
# <a name="irenderenginegetfiltergraph-method"></a><span data-ttu-id="e1f91-103">IRenderEngine :: GetFilterGraph, méthode</span><span class="sxs-lookup"><span data-stu-id="e1f91-103">IRenderEngine::GetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="e1f91-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e1f91-104">\[Deprecated.</span></span> <span data-ttu-id="e1f91-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e1f91-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e1f91-106">La `GetFilterGraph` méthode récupère le graphique de filtre que le moteur de rendu a construit, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e1f91-106">The `GetFilterGraph` method retrieves the filter graph that the render engine has constructed, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f91-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1f91-107">Syntax</span></span>


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a><span data-ttu-id="e1f91-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1f91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f91-109">*ppFG* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e1f91-109">*ppFG* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e1f91-110">Reçoit un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1f91-110">Receives a pointer to the filter graph's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="e1f91-111">Elle reçoit la valeur **null** s’il n’existe aucun graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1f91-111">It receives the value **NULL** if there is no filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f91-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1f91-112">Return value</span></span>

<span data-ttu-id="e1f91-113">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1f91-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e1f91-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e1f91-114">Return code</span></span>                                                                                            | <span data-ttu-id="e1f91-115">Description</span><span class="sxs-lookup"><span data-stu-id="e1f91-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e1f91-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e1f91-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="e1f91-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="e1f91-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="e1f91-118"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="e1f91-118"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="e1f91-119">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="e1f91-119">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="e1f91-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e1f91-120"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="e1f91-121">Pointeur non valide.</span><span class="sxs-lookup"><span data-stu-id="e1f91-121">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e1f91-122">Notes</span><span class="sxs-lookup"><span data-stu-id="e1f91-122">Remarks</span></span>

<span data-ttu-id="e1f91-123">Utilisez la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le serveur frontal du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e1f91-123">Use the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method to build the front end of the filter graph.</span></span> <span data-ttu-id="e1f91-124">Pour la version préliminaire, utilisez [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md) pour terminer le graphique.</span><span class="sxs-lookup"><span data-stu-id="e1f91-124">For preview, use the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) to complete the graph.</span></span> <span data-ttu-id="e1f91-125">Pour la sortie de fichier, connectez le serveur frontal à une combinaison multiplexeur de fichiers/Mux.</span><span class="sxs-lookup"><span data-stu-id="e1f91-125">For file output, connect the front end to a mux/file writer combination.</span></span> <span data-ttu-id="e1f91-126">Pour plus d’informations, consultez [rendu d’un projet](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="e1f91-126">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="e1f91-127">Le graphique résultant peut être exécuté, suspendu, arrêté et cherché ; Toutefois, la vitesse de lecture ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="e1f91-127">The resulting graph can be run, paused, stopped, and seeked; the playback rate cannot be changed, however.</span></span>

<span data-ttu-id="e1f91-128">En cas de retour, si la valeur de *\* ppFG* est non **null**, l’interface **IGraphBuilder** a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="e1f91-128">On return, if the value of *\*ppFG* is non-**NULL**, the **IGraphBuilder** interface has an outstanding reference count.</span></span> <span data-ttu-id="e1f91-129">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="e1f91-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e1f91-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e1f91-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e1f91-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1f91-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e1f91-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e1f91-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1f91-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1f91-133">Requirements</span></span>



| <span data-ttu-id="e1f91-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1f91-134">Requirement</span></span> | <span data-ttu-id="e1f91-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1f91-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f91-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1f91-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e1f91-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1f91-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e1f91-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1f91-138">Library</span></span><br/> | <dl> <span data-ttu-id="e1f91-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1f91-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f91-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1f91-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f91-141">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="e1f91-141">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="e1f91-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="e1f91-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




