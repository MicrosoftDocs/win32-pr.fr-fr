---
title: Capturer sans utiliser Stockage sur disque
description: Capturer sans utiliser Stockage sur disque
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Message WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106508970"
---
# <a name="capture-without-using-disk-storage"></a>Capturer sans utiliser Stockage sur disque

Vous pouvez utiliser les services de capture sans écrire les données dans un fichier de disque à l’aide du message de [**\_ \_ séquence \_**](wm-cap-sequence-nofile.md) de la limite WM (ou de la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ). Ce message est utile uniquement avec les fonctions de rappel qui permettent à votre application d’utiliser directement les données vidéo et audio. Par exemple, les applications de visioconférence peuvent utiliser ce message pour obtenir des images vidéo en streaming. Les fonctions de rappel transfèrent les images capturées à l’ordinateur distant.

 

 




