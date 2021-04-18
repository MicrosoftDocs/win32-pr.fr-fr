---
title: PlaybackOperation. Completed, propriété
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par l’une des méthodes de lecture MediaRenderer est terminée.
ms.assetid: E8F8D3FC-C31F-485C-A30B-2457F4B1DE82
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface PlaybackOperation
- API de diffusion multimédia en continu de l’interface PlaybackOperation, propriété terminée
topic_type:
- apiref
api_name:
- PlaybackOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bf305b4028e223c36df0c8a59c5246228c5b8d40
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106533548"
---
# <a name="playbackoperationcompleted-property"></a><span data-ttu-id="beb23-106">PlaybackOperation. Completed, propriété</span><span class="sxs-lookup"><span data-stu-id="beb23-106">PlaybackOperation.Completed property</span></span>

<span data-ttu-id="beb23-107">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par l’une des méthodes de lecture [**MediaRenderer**](mediarenderer.md) est terminée.</span><span class="sxs-lookup"><span data-stu-id="beb23-107">Gets or sets an event handler that is invoked when the asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods is completed.</span></span>

<span data-ttu-id="beb23-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="beb23-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb23-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="beb23-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="beb23-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="beb23-110">Property value</span></span>

<span data-ttu-id="beb23-111">Gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="beb23-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="beb23-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="beb23-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb23-113">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="beb23-113">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 




