---
title: Nom du fichier de capture
description: Nom du fichier de capture
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- Message WM_CAP_FILE_SET_CAPTURE_FILE
- capFileSetCaptureFile macro)
- Message WM_CAP_FILE_GET_CAPTURE_FILE
- capFileGetCaptureFile macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e48ecd727accccb868d0f78c68a833ac6ec6655bada23db8a56f2a9aeaffd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941594"
---
# <a name="capture-filename"></a>Nom du fichier de capture

AVICap, par défaut, achemine les données de flux vidéo et audio d’une fenêtre de capture vers un fichier nommé CAPTURE.AVI dans le répertoire racine du lecteur actif. Vous pouvez spécifier un autre nom de fichier en envoyant le message du fichier de capture du jeu de fichiers de l' [**\_ embout \_ \_ \_ \_ WM**](wm-cap-file-set-capture-file.md) (ou la macro [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) à une fenêtre de capture. Ce message spécifie le nom de fichier ; il ne crée pas, n’alloue pas ou n’ouvre pas le fichier. Vous pouvez récupérer le nom de fichier de capture en cours en envoyant le message [**WM \_ Cap \_ file \_ obtenir un \_ \_ fichier de capture**](wm-cap-file-get-capture-file.md) (ou la macro [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) à une fenêtre de capture.

 

 




