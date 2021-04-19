---
title: StreamSelectOperation. Completed, propriété
description: Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par SelectBestStreamAsync est terminée.
ms.assetid: 693CC002-2D91-4656-954D-8A556480155C
keywords:
- API de diffusion multimédia en continu des propriétés terminées
- API de diffusion multimédia en continu des propriétés, interface StreamSelectOperation
- API de diffusion multimédia en continu de l’interface StreamSelectOperation, propriété terminée
topic_type:
- apiref
api_name:
- StreamSelectOperation.Completed
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74cfdf1a3db4f6843a5f12522b688e889e156f33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106510061"
---
# <a name="streamselectoperationcompleted-property"></a><span data-ttu-id="6ad11-106">StreamSelectOperation. Completed, propriété</span><span class="sxs-lookup"><span data-stu-id="6ad11-106">StreamSelectOperation.Completed property</span></span>

<span data-ttu-id="6ad11-107">Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) est terminée.</span><span class="sxs-lookup"><span data-stu-id="6ad11-107">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span>

<span data-ttu-id="6ad11-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6ad11-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad11-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ad11-109">Syntax</span></span>


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a><span data-ttu-id="6ad11-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6ad11-110">Property value</span></span>

<span data-ttu-id="6ad11-111">Gestionnaire d'événements.</span><span class="sxs-lookup"><span data-stu-id="6ad11-111">The event handler.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ad11-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ad11-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad11-113">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="6ad11-113">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

 