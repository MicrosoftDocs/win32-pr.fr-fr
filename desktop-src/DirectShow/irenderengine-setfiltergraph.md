---
description: La méthode SetFilterGraph spécifie un graphique de filtre que le moteur de rendu utilise.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'IRenderEngine :: SetFilterGraph, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541772"
---
# <a name="irenderenginesetfiltergraph-method"></a><span data-ttu-id="205e1-103">IRenderEngine :: SetFilterGraph, méthode</span><span class="sxs-lookup"><span data-stu-id="205e1-103">IRenderEngine::SetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="205e1-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="205e1-104">\[Deprecated.</span></span> <span data-ttu-id="205e1-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="205e1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="205e1-106">La `SetFilterGraph` méthode spécifie un graphique de filtre que le moteur de rendu utilise.</span><span class="sxs-lookup"><span data-stu-id="205e1-106">The `SetFilterGraph` method specifies a filter graph for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="205e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="205e1-107">Syntax</span></span>


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a><span data-ttu-id="205e1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="205e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205e1-109">*pFG*</span><span class="sxs-lookup"><span data-stu-id="205e1-109">*pFG*</span></span> 
</dt> <dd>

<span data-ttu-id="205e1-110">Pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="205e1-110">Pointer to the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface of the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205e1-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="205e1-111">Return value</span></span>

<span data-ttu-id="205e1-112">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="205e1-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="205e1-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="205e1-113">Return code</span></span>                                                                                            | <span data-ttu-id="205e1-114">Description</span><span class="sxs-lookup"><span data-stu-id="205e1-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="205e1-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="205e1-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="205e1-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="205e1-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="205e1-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="205e1-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="205e1-118">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="205e1-118">Invalid argument.</span></span><br/>                   |
| <dl> <span data-ttu-id="205e1-119"><dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt></span><span class="sxs-lookup"><span data-stu-id="205e1-119"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="205e1-120">Le moteur de rendu n’a pas pu s’initialiser.</span><span class="sxs-lookup"><span data-stu-id="205e1-120">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="205e1-121">Notes</span><span class="sxs-lookup"><span data-stu-id="205e1-121">Remarks</span></span>

<span data-ttu-id="205e1-122">La plupart des applications n’ont pas besoin d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="205e1-122">Most applications do not need to call this method.</span></span> <span data-ttu-id="205e1-123">Il est plus courant de laisser le moteur de rendu générer le graphique pour vous, en appelant la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="205e1-123">It is more typical to let the render engine build the graph for you, by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span>

<span data-ttu-id="205e1-124">Cette méthode échoue si le moteur de rendu a déjà un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="205e1-124">This method fails if the render engine already has a filter graph.</span></span>

<span data-ttu-id="205e1-125">Ne récupérez jamais un pointeur vers un graphique de filtre créé par un moteur de rendu et utilisez-le en tant que paramètre de cette méthode sur un autre moteur de rendu.</span><span class="sxs-lookup"><span data-stu-id="205e1-125">Never retrieve a pointer to a filter graph created by one render engine and then use it as the parameter to this method on another render engine.</span></span> <span data-ttu-id="205e1-126">Cela entraînera des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="205e1-126">Doing so will cause unpredictable results.</span></span>

<span data-ttu-id="205e1-127">La méthode **ConnectFrontEnd** détruit tout graphique de filtre existant, mais conserve la même instance du gestionnaire de graphes de filtre.</span><span class="sxs-lookup"><span data-stu-id="205e1-127">The **ConnectFrontEnd** method tears down any existing filter graph, but keeps the same Filter Graph Manager instance.</span></span>

> [!Note]  
> <span data-ttu-id="205e1-128">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="205e1-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="205e1-129">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="205e1-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="205e1-130">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="205e1-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="205e1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="205e1-131">Requirements</span></span>



| <span data-ttu-id="205e1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="205e1-132">Requirement</span></span> | <span data-ttu-id="205e1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="205e1-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="205e1-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="205e1-134">Header</span></span><br/>  | <dl> <span data-ttu-id="205e1-135"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="205e1-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="205e1-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="205e1-136">Library</span></span><br/> | <dl> <span data-ttu-id="205e1-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="205e1-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="205e1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="205e1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205e1-139">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="205e1-139">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="205e1-140">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="205e1-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




