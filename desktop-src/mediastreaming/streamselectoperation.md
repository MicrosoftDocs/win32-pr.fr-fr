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
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211535"
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



 

 

