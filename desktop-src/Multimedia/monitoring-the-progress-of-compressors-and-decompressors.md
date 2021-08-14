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
ms.openlocfilehash: 44707cb6a8fbdb19b1d71fed6c71498b51936b9d089354277c6767586b4b8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373492"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Surveillance de la progression des compresseurs et des décompresseurs

Votre application peut surveiller la progression d’une longue opération effectuée par un compresseur ou un décompresseur en lui envoyant l’adresse d’une fonction de rappel. Vous pouvez utiliser la fonction [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) pour envoyer l’adresse au compresseur ou au décompresseur. Lorsque le compresseur ou le décompresseur reçoit cette adresse, il envoie des messages d’État à la fonction. Ces messages indiquent si l’opération est en cours de démarrage, d’arrêt, de production ou de poursuite.

 

 




