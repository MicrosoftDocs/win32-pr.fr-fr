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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368996"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Surveillance de la progression des compresseurs et des décompresseurs

Votre application peut surveiller la progression d’une longue opération effectuée par un compresseur ou un décompresseur en lui envoyant l’adresse d’une fonction de rappel. Vous pouvez utiliser la fonction [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) pour envoyer l’adresse au compresseur ou au décompresseur. Lorsque le compresseur ou le décompresseur reçoit cette adresse, il envoie des messages d’État à la fonction. Ces messages indiquent si l’opération est en cours de démarrage, d’arrêt, de production ou de poursuite.

 

 




