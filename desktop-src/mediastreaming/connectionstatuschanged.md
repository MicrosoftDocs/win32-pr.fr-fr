---
title: Événement ConnectionStatusChanged
description: Se produit lorsque l’état de la connexion réseau de l’appareil change.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- API de diffusion de contenu multimédia d’événements ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726764"
---
# <a name="connectionstatuschanged-event"></a><span data-ttu-id="693ff-104">Événement ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="693ff-104">ConnectionStatusChanged event</span></span>

<span data-ttu-id="693ff-105">Se produit lorsque l’état de la connexion réseau de l’appareil change.</span><span class="sxs-lookup"><span data-stu-id="693ff-105">Occurs when the device’s network connection status changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="693ff-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="693ff-106">Syntax</span></span>


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a><span data-ttu-id="693ff-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="693ff-107">Parameters</span></span>

<span data-ttu-id="693ff-108">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="693ff-108">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="693ff-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="693ff-109">Return value</span></span>

<span data-ttu-id="693ff-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="693ff-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="693ff-111">Notes</span><span class="sxs-lookup"><span data-stu-id="693ff-111">Remarks</span></span>

<span data-ttu-id="693ff-112">Pour gérer les notifications à partir de cet événement, inscrivez une fonction de gestionnaire d’événements [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) à l’aide de la méthode [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="693ff-112">To handle notifications from this event, register a [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function using the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method.</span></span> <span data-ttu-id="693ff-113">Pour annuler l’inscription du gestionnaire d’événements, utilisez la méthode [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="693ff-113">To unregister the event handler, use the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

 

 