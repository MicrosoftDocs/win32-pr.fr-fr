---
description: La méthode Render Initialise le graphique de filtre DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Méthode Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544544"
---
# <a name="render-method"></a><span data-ttu-id="f187d-103">Méthode Render</span><span class="sxs-lookup"><span data-stu-id="f187d-103">Render Method</span></span>

> [!Note]  
> <span data-ttu-id="f187d-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f187d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f187d-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f187d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f187d-106">La `Render` méthode initialise le graphique de filtre de DVD.</span><span class="sxs-lookup"><span data-stu-id="f187d-106">The `Render` method initializes the DVD filter graph.</span></span>

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a><span data-ttu-id="f187d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f187d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f187d-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span><span class="sxs-lookup"><span data-stu-id="f187d-108"><span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*</span></span>
</dt> <dd>

<span data-ttu-id="f187d-109">Spécifie une valeur entière indiquant si le graphique de filtre sera détruit et reconstruit.</span><span class="sxs-lookup"><span data-stu-id="f187d-109">Specifies an integer value indicating whether the filter graph will be destroyed and rebuilt.</span></span>



| <span data-ttu-id="f187d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="f187d-110">Value</span></span> | <span data-ttu-id="f187d-111">Description</span><span class="sxs-lookup"><span data-stu-id="f187d-111">Description</span></span>                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f187d-112">0</span><span class="sxs-lookup"><span data-stu-id="f187d-112">0</span></span>     | <span data-ttu-id="f187d-113">Le graphique de filtre ne sera pas détruit et reconstruit s’il existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f187d-113">The filter graph will not be destroyed and rebuilt if it already exists.</span></span> <span data-ttu-id="f187d-114">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f187d-114">This is the default value.</span></span> |
| <span data-ttu-id="f187d-115">1</span><span class="sxs-lookup"><span data-stu-id="f187d-115">1</span></span>     | <span data-ttu-id="f187d-116">Le graphique de filtre sera détruit et reconstruit s’il existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f187d-116">The filter graph will be destroyed and rebuilt if it already exists.</span></span>                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f187d-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f187d-117">Return Value</span></span>

<span data-ttu-id="f187d-118">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="f187d-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f187d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f187d-119">Remarks</span></span>

<span data-ttu-id="f187d-120">La `Render` méthode permet à l’objet **mswebdvd** d’initialiser complètement le graphique de filtre DirectShow sous-jacent au démarrage.</span><span class="sxs-lookup"><span data-stu-id="f187d-120">The `Render` method enables the **MSWebDVD** object to fully initialize the underlying DirectShow filter graph on startup.</span></span> <span data-ttu-id="f187d-121">Cela élimine le léger délai qui, autrement, se produit lorsque l’utilisateur émet la première commande pour lire un disque ou afficher un menu.</span><span class="sxs-lookup"><span data-stu-id="f187d-121">This eliminates the slight delay that otherwise occurs when the user issues the first command to play a disc or show a menu.</span></span> <span data-ttu-id="f187d-122">Il n’existe aucun cas dans lequel `Render` doit être appelé avant d’appeler une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="f187d-122">There is no case in which `Render` needs to be called before calling any other method.</span></span> <span data-ttu-id="f187d-123">Par exemple, si l’application appelle [**PlayTitle**](playtitle-method.md) avant que le graphique de filtre n’ait été initialisé, l’objet **mswebdvd** appelle `Render` automatiquement avant de tenter de lire le disque.</span><span class="sxs-lookup"><span data-stu-id="f187d-123">For example, if the application calls [**PlayTitle**](playtitle-method.md) before the filter graph has been initialized, the **MSWebDVD** object calls `Render` automatically before attempting to play the disc.</span></span>

 

 



