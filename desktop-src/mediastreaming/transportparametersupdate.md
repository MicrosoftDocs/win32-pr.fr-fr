---
title: Événement TransportParametersUpdate
description: Se produit chaque fois qu’un ensemble de paramètres de transport est mis à jour sur le DMR.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- API de diffusion de contenu multimédia d’événements TransportParametersUpdate
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842249"
---
# <a name="transportparametersupdate-event"></a><span data-ttu-id="7ad53-104">Événement TransportParametersUpdate</span><span class="sxs-lookup"><span data-stu-id="7ad53-104">TransportParametersUpdate event</span></span>

<span data-ttu-id="7ad53-105">Se produit chaque fois qu’un ensemble de paramètres de transport est mis à jour sur le DMR.</span><span class="sxs-lookup"><span data-stu-id="7ad53-105">Occurs whenever any of a set of transport parameters are updated on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad53-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ad53-106">Syntax</span></span>


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a><span data-ttu-id="7ad53-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ad53-107">Parameters</span></span>

<span data-ttu-id="7ad53-108">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="7ad53-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ad53-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7ad53-109">Return value</span></span>

<span data-ttu-id="7ad53-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7ad53-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad53-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7ad53-111">Remarks</span></span>

<span data-ttu-id="7ad53-112">Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) à l’aide de la méthode [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="7ad53-112">To handle notifications from this event, register a [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) event handler function using the [**add\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) method.</span></span> <span data-ttu-id="7ad53-113">Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .</span><span class="sxs-lookup"><span data-stu-id="7ad53-113">To unregister the event handler, use the [**remove\_TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) method.</span></span>

 

 