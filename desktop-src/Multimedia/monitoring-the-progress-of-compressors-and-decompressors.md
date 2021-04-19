---
title: Surveillance de la progression des compresseurs et des décompresseurs
description: Surveillance de la progression des compresseurs et des décompresseurs
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- Gestionnaire de compression vidéo (VCM), surveillance
- VCM (gestionnaire de compression vidéo), surveillance
- ICSetStatusProc fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510009"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Surveillance de la progression des compresseurs et des décompresseurs

Votre application peut surveiller la progression d’une longue opération effectuée par un compresseur ou un décompresseur en lui envoyant l’adresse d’une fonction de rappel. Vous pouvez utiliser la fonction [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) pour envoyer l’adresse au compresseur ou au décompresseur. Lorsque le compresseur ou le décompresseur reçoit cette adresse, il envoie des messages d’État à la fonction. Ces messages indiquent si l’opération est en cours de démarrage, d’arrêt, de production ou de poursuite.

 

 




