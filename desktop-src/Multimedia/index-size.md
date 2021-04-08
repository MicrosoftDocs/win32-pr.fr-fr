---
title: Taille d'index
description: Taille d'index
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673922"
---
# <a name="index-size"></a>Taille d'index

Chaque fichier AVI utilise un index d’une taille spécifiée pour localiser des blocs de données vidéo et audio dans le fichier. Une entrée dans l’index localise une image vidéo ou un tampon Waveform-Audio. Par conséquent, la valeur de la taille de l’index définit indirectement la limite supérieure du nombre de trames qui peuvent être capturées dans un fichier.

Vous pouvez récupérer la taille actuelle de l’index à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). La taille actuelle de l’index est stockée dans le membre **dwIndexSize** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Vous pouvez spécifier une nouvelle taille d’index comme valeur de **dwIndexSize** , puis envoyer la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). La taille de l’index par défaut est de 34 952 entrées (ce qui permet d’obtenir des trames de 32 Ko et un nombre proportionnel de mémoires tampons audio).

 

 




