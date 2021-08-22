---
title: capturer sans utiliser Stockage sur disque
description: capturer sans utiliser Stockage sur disque
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Message WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea708bd99cc2c325623eb53d734fadb2acdd0112e3a727fae9bfa741b8d301e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691619"
---
# <a name="capture-without-using-disk-storage"></a>capturer sans utiliser Stockage sur disque

Vous pouvez utiliser les services de capture sans écrire les données dans un fichier de disque à l’aide du message de [**\_ \_ séquence \_**](wm-cap-sequence-nofile.md) de la limite WM (ou de la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ). Ce message est utile uniquement avec les fonctions de rappel qui permettent à votre application d’utiliser directement les données vidéo et audio. Par exemple, les applications de visioconférence peuvent utiliser ce message pour obtenir des images vidéo en streaming. Les fonctions de rappel transfèrent les images capturées à l’ordinateur distant.

 

 




