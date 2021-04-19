---
description: La méthode SetDynamicReconnectLevel définit le niveau de reconnexion dynamique lors du rendu.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'IRenderEngine :: SetDynamicReconnectLevel, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543864"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a><span data-ttu-id="f5278-103">IRenderEngine :: SetDynamicReconnectLevel, méthode</span><span class="sxs-lookup"><span data-stu-id="f5278-103">IRenderEngine::SetDynamicReconnectLevel method</span></span>

> [!Note]  
> <span data-ttu-id="f5278-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f5278-104">\[Deprecated.</span></span> <span data-ttu-id="f5278-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5278-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5278-106">La `SetDynamicReconnectLevel` méthode définit le niveau de reconnexion dynamique lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="f5278-106">The `SetDynamicReconnectLevel` method sets the level of dynamic reconnection during rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5278-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5278-107">Syntax</span></span>


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="f5278-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5278-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5278-109">*Niveau*</span><span class="sxs-lookup"><span data-stu-id="f5278-109">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="f5278-110">Combinaison d' [**indicateurs de reconnexion dynamique**](dynamic-reconnection-flags.md), spécifiant le niveau de reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="f5278-110">Combination of [**Dynamic Reconnection Flags**](dynamic-reconnection-flags.md), specifying the level of dynamic reconnection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5278-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5278-111">Return value</span></span>

<span data-ttu-id="f5278-112">Retourne l’une des valeurs **HRESULT** suivantes :</span><span class="sxs-lookup"><span data-stu-id="f5278-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="f5278-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f5278-113">Return code</span></span>                                                                               | <span data-ttu-id="f5278-114">Description</span><span class="sxs-lookup"><span data-stu-id="f5278-114">Description</span></span>                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="f5278-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5278-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f5278-116">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f5278-116">Success.</span></span><br/>         |
| <dl> <span data-ttu-id="f5278-117"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="f5278-117"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="f5278-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="f5278-118">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5278-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f5278-119">Remarks</span></span>

<span data-ttu-id="f5278-120">Par défaut, le moteur de rendu de base charge chaque source avant d’effectuer le rendu d’un projet.</span><span class="sxs-lookup"><span data-stu-id="f5278-120">By default, the basic render engine loads every source before rendering a project.</span></span> <span data-ttu-id="f5278-121">Cela peut se traduire par un temps de démarrage long.</span><span class="sxs-lookup"><span data-stu-id="f5278-121">This can result in a long start-up time.</span></span> <span data-ttu-id="f5278-122">Avec la reconnexion dynamique, les sources sont chargées uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f5278-122">With dynamic reconnection, sources are loaded only when needed.</span></span> <span data-ttu-id="f5278-123">Cela peut raccourcir le temps de démarrage, mais risque d’interférer avec la lecture en douceur.</span><span class="sxs-lookup"><span data-stu-id="f5278-123">This can shorten the start-up time, but possibly interfere with smooth playback.</span></span> <span data-ttu-id="f5278-124">En règle générale, plus le nombre d’éléments sources utilisés par un projet est grand, plus vous pouvez tirer parti de la reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="f5278-124">Generally, the more source clips that a project uses, the more you might benefit from dynamic reconnection.</span></span>

<span data-ttu-id="f5278-125">Le moteur de rendu intelligent n’implémente pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f5278-125">The smart render engine does not implement this method.</span></span>

> [!Note]  
> <span data-ttu-id="f5278-126">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f5278-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5278-127">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5278-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5278-128">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f5278-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5278-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5278-129">Requirements</span></span>



| <span data-ttu-id="f5278-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5278-130">Requirement</span></span> | <span data-ttu-id="f5278-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5278-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5278-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5278-132">Header</span></span><br/>  | <dl> <span data-ttu-id="f5278-133"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5278-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5278-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5278-134">Library</span></span><br/> | <dl> <span data-ttu-id="f5278-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5278-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5278-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5278-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5278-137">**Interface IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="f5278-137">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="f5278-138">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="f5278-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




