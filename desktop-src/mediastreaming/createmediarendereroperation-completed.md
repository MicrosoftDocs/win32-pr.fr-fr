---
title: CreateMediaRendererOperation. Completed, propriété
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par CreateMediaRendererAsync ou CreateMediaRendererFromBasicDeviceAsync est terminée.
ms.assetid: B62CF929-13D0-4665-89E4-DEC48A38DDF7
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface CreateMediaRendererOperation
- API de diffusion multimédia en continu de l’interface CreateMediaRendererOperation, propriété terminée
topic_type:
- apiref
api_name:
- CreateMediaRendererOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3b4ebafc1441741a352f4573709495228bf13e4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678478"
---
# <a name="createmediarendereroperationcompleted-property"></a><span data-ttu-id="4ea1a-106">CreateMediaRendererOperation. Completed, propriété</span><span class="sxs-lookup"><span data-stu-id="4ea1a-106">CreateMediaRendererOperation.Completed property</span></span>

<span data-ttu-id="4ea1a-107">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) ou [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) est terminée.</span><span class="sxs-lookup"><span data-stu-id="4ea1a-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**CreateMediaRendererAsync**](imediarendererfactory-createmediarendererasync.md) or [**CreateMediaRendererFromBasicDeviceAsync**](imediarendererfactory-createmediarendererfrombasicdeviceasync.md) is completed.</span></span>

<span data-ttu-id="4ea1a-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4ea1a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea1a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ea1a-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  ICreateMediaRendererCompletedHandler value
);

HRESULT get_Completed(
  [out] ICreateMediaRendererCompletedHandler *value
);
```



## <a name="property-value"></a><span data-ttu-id="4ea1a-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4ea1a-110">Property value</span></span>

<span data-ttu-id="4ea1a-111">Gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="4ea1a-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ea1a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ea1a-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea1a-113">**CreateMediaRendererOperation**</span><span class="sxs-lookup"><span data-stu-id="4ea1a-113">**CreateMediaRendererOperation**</span></span>](createmediarendereroperation.md)
</dt> </dl>

 

 




