---
title: capturer sans utiliser Stockage sur disque
description: capturer sans utiliser Stockage sur disque
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Message WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368751"
---
# <a name="capture-without-using-disk-storage"></a>capturer sans utiliser Stockage sur disque

Vous pouvez utiliser les services de capture sans écrire les données dans un fichier de disque à l’aide du message de [**\_ \_ séquence \_**](wm-cap-sequence-nofile.md) de la limite WM (ou de la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ). Ce message est utile uniquement avec les fonctions de rappel qui permettent à votre application d’utiliser directement les données vidéo et audio. Par exemple, les applications de visioconférence peuvent utiliser ce message pour obtenir des images vidéo en streaming. Les fonctions de rappel transfèrent les images capturées à l’ordinateur distant.

 

 




