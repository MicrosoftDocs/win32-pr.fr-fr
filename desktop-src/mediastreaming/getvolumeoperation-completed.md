---
title: GetVolumeOperation. Completed, propriété
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetVolumeAsync est terminée.
ms.assetid: 34100EE7-C4CB-4AE0-BD3E-9E23A643F87E
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface GetVolumeOperation
- API de diffusion multimédia en continu de l’interface GetVolumeOperation, propriété terminée
topic_type:
- apiref
api_name:
- GetVolumeOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d21577d57e1e29aff1d2b12b92bcbef58a529eba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101512"
---
# <a name="getvolumeoperationcompleted-property"></a><span data-ttu-id="40448-106">GetVolumeOperation. Completed, propriété</span><span class="sxs-lookup"><span data-stu-id="40448-106">GetVolumeOperation.Completed property</span></span>

<span data-ttu-id="40448-107">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) est terminée.</span><span class="sxs-lookup"><span data-stu-id="40448-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync) is completed.</span></span>

<span data-ttu-id="40448-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="40448-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="40448-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40448-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetVolumeCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetVolumeCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="40448-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="40448-110">Property value</span></span>

<span data-ttu-id="40448-111">Gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="40448-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="40448-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40448-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40448-113">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="40448-113">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

 