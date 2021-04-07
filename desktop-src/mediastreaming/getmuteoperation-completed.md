---
title: GetMuteOperation. Completed, propriété
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetMuteAsync est terminée.
ms.assetid: B8E1DE71-46AC-4F6A-B873-AE3239BE492C
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface GetMuteOperation
- API de diffusion multimédia en continu de l’interface GetMuteOperation, propriété terminée
topic_type:
- apiref
api_name:
- GetMuteOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40c360dc3597d8cf04d1a8c505e479a38136f592
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726580"
---
# <a name="getmuteoperationcompleted-property"></a><span data-ttu-id="0bd41-106">GetMuteOperation. Completed, propriété</span><span class="sxs-lookup"><span data-stu-id="0bd41-106">GetMuteOperation.Completed property</span></span>

<span data-ttu-id="0bd41-107">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) est terminée.</span><span class="sxs-lookup"><span data-stu-id="0bd41-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) is completed.</span></span>

<span data-ttu-id="0bd41-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0bd41-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd41-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bd41-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetMuteCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetMuteCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="0bd41-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0bd41-110">Property value</span></span>

<span data-ttu-id="0bd41-111">Gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="0bd41-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="0bd41-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bd41-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd41-113">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="0bd41-113">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

 