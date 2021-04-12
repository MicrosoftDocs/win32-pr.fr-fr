---
title: GetStreamPropertiesOperation. Completed, propriété
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetStreamPropertiesAsync est terminée.
ms.assetid: 97194F8E-DE36-4DC6-ADB5-F1EDE8AEF079
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface GetStreamPropertiesOperation
- API de diffusion multimédia en continu de l’interface GetStreamPropertiesOperation, propriété terminée
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb60ad137c8dafa42a58394d58a105267dabda3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381855"
---
# <a name="getstreampropertiesoperationcompleted-property"></a><span data-ttu-id="1319c-106">GetStreamPropertiesOperation. Completed, propriété</span><span class="sxs-lookup"><span data-stu-id="1319c-106">GetStreamPropertiesOperation.Completed property</span></span>

<span data-ttu-id="1319c-107">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) est terminée.</span><span class="sxs-lookup"><span data-stu-id="1319c-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)) is completed.</span></span>

<span data-ttu-id="1319c-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1319c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1319c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1319c-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IGetStreamPropertiesCompletedHandler *value
);

HRESULT get_Completed(
  [out] IGetStreamPropertiesCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="1319c-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1319c-110">Property value</span></span>

<span data-ttu-id="1319c-111">Gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="1319c-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="1319c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1319c-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1319c-113">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="1319c-113">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

 