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
# <a name="streamselectoperationcompleted-property"></a>StreamSelectOperation. Completed, propriété

Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) est terminée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Completed(
  [in]  IStreamSelectCompletedHandler *value
);

HRESULT get_Completed(
  [out] IStreamSelectCompletedHandler **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Gestionnaire d'événements.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**StreamSelectOperation**](streamselectoperation.md)
</dt> </dl>

 

 