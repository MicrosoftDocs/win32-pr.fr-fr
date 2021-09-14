---
title: Granularité des blocs vidéo et audio
description: Granularité des blocs vidéo et audio
ms.assetid: 02c94de7-c7cb-4150-8b3e-0542d317c19b
keywords:
- Fichiers AVI, granularité des blocs
- AVICap, classe, blocs de remplissage
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2245b133fbf14bfd6403fa2f3d7e02ed328de6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194875"
---
# <a name="video-and-audio-chunk-granularity"></a>Granularité des blocs vidéo et audio

La granularité du segment est une taille de bloc logique pour un fichier AVI utilisé pour l’écriture et la récupération des blocs de données audio et vidéo. Lors de l’écriture de blocs audio et vidéo sur disque, AVICap ajoute des blocs de remplissage (segments RIFF « indésirables ») si nécessaire pour remplir chaque bloc logique de données.

Vous pouvez récupérer le paramètre de granularité de segment actuel à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). La granularité du bloc actuel est stockée dans le membre **wChunkGranularity** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Vous pouvez spécifier une nouvelle granularité de bloc en tant que valeur de **wChunkGranularity** , puis envoyer la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). Vous pouvez également spécifier zéro pour ce membre afin de définir la granularité du segment sur la taille de secteur du disque.

 

 




