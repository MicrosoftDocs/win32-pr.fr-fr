---
title: Propriété GetTransportInformationOperation terminée
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetTransportInformationAsync est terminée.
ms.assetid: 11E60E00-75B5-4412-B115-4438255AEB8A
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface GetTransportInformationOperation
- API de diffusion multimédia en continu de l’interface GetTransportInformationOperation, propriété terminée
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.Completed
- GetTransportInformationOperation.get_Completed
- GetTransportInformationOperation.put_Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2948af2ed84a70c9f37efbc4aae985e9b1ab5804
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106513521"
---
# <a name="gettransportinformationoperationcompleted-property"></a><span data-ttu-id="06d0f-106">GetTransportInformationOperation :: Completed, propriété</span><span class="sxs-lookup"><span data-stu-id="06d0f-106">GetTransportInformationOperation::Completed property</span></span>

<span data-ttu-id="06d0f-107">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) est terminée.</span><span class="sxs-lookup"><span data-stu-id="06d0f-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync) is completed.</span></span>

<span data-ttu-id="06d0f-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="06d0f-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d0f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06d0f-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  GetTransportInformationCompletedHandler *value
);

HRESULT get_Completed(
  [out] GetTransportInformationCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="06d0f-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="06d0f-110">Property value</span></span>

<span data-ttu-id="06d0f-111">Gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="06d0f-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="06d0f-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06d0f-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06d0f-113">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="06d0f-113">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

 