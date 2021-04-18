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
# <a name="playbackoperationcompleted-property"></a>PlaybackOperation. Completed, propriété

Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par l’une des méthodes de lecture [**MediaRenderer**](mediarenderer.md) est terminée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Completed(
  [in]  PlaybackOperationCompletedHandler *value
);

HRESULT get_Completed(
  [out] PlaybackOperationCompletedHandler **value
);
```



## <a name="property-value"></a>Valeur de la propriété

Gestionnaire d'événements.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 




