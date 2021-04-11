---
title: Événement RenderingParametersUpdate
description: Se produit chaque fois qu’un jeu de paramètres de contrôle de rendu est mis à jour sur le DMR.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- API de diffusion de contenu multimédia d’événements RenderingParametersUpdate
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314849"
---
# <a name="renderingparametersupdate-event"></a><span data-ttu-id="82675-104">Événement RenderingParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="82675-104">RenderingParametersUpdate event</span></span>

<span data-ttu-id="82675-105">Se produit chaque fois qu’un jeu de paramètres de contrôle de rendu est mis à jour sur le DMR.</span><span class="sxs-lookup"><span data-stu-id="82675-105">Occurs whenever any of a set of rendering control parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="82675-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82675-106">Syntax</span></span>


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="82675-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82675-107">Parameters</span></span>

<span data-ttu-id="82675-108">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="82675-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82675-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82675-109">Return value</span></span>

<span data-ttu-id="82675-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="82675-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82675-111">Notes</span><span class="sxs-lookup"><span data-stu-id="82675-111">Remarks</span></span>

<span data-ttu-id="82675-112">Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) à l’aide de la méthode [**Add \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="82675-112">To handle notifications from this event, register a [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) event handler function using the [**add\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) method.</span></span> <span data-ttu-id="82675-113">Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="82675-113">To unregister the event handler, use the [**remove\_RenderingParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate) method.</span></span>

 

 