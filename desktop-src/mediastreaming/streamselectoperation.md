---
title: StreamSelectOperation, classe
description: Inscrit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par GetMuteAsync se termine, et fournit une méthode qui retourne les résultats de l’opération. | StreamSelectOperation, classe
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- API de diffusion multimédia en continu de la classe StreamSelectOperation
- API de diffusion multimédia en continu de la classe StreamSelectOperation, décrite
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161434aad9c4eb20960950ba2dd1979c9caaa2ccc5bbe3c2683ee3e4f839a0b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461559"
---
# <a name="streamselectoperation-class"></a>StreamSelectOperation, classe

Inscrit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) se termine, et fournit une méthode qui retourne les résultats de l’opération.

**StreamSelectOperation** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **StreamSelectOperation** possède ces méthodes.



| Méthode                                                 | Description                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](streamselectoperation-getresults.md) | Retourne les résultats de l’opération asynchrone démarrée par [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).<br/> |



 

### <a name="properties"></a>Propriétés

La classe **StreamSelectOperation** possède les propriétés suivantes.



| Propriété                                                        | Type d’accès           | Description                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Completed**](streamselectoperation-completed.md)<br/> | Lecture/écriture<br/> | Obtient ou définit un gestionnaire d’événements qui est appelé lorsque l’opération asynchrone démarrée par [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) est terminée.<br/> |



 

 

