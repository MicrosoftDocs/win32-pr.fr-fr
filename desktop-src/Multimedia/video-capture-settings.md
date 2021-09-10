---
title: Paramètres de Capture vidéo
description: Paramètres de Capture vidéo
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- CAPTUREPARMS, structure
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369375"
---
# <a name="video-capture-settings"></a>Paramètres de Capture vidéo

La structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contient les paramètres de contrôle pour la capture vidéo en continu. Cette structure contrôle plusieurs aspects du processus de capture et vous permet d’effectuer les tâches suivantes :

-   Spécifiez la fréquence d’images.
-   Spécifiez le nombre de mémoires tampons vidéo allouées.
-   Désactivez et activez la capture audio.
-   Spécifiez l’intervalle de temps pour la capture.
-   Spécifiez si un périphérique MCI (VCR ou videodisc) est utilisé lors de la capture.
-   Spécifiez le contrôle du clavier ou de la souris pour terminer la diffusion en continu.
-   Spécifiez le type de moyenne vidéo appliqué pendant la capture.

Vous pouvez récupérer les paramètres de capture actuels dans la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) en envoyant le message [**\_ \_ \_ \_ d’installation de la séquence WM**](wm-cap-get-sequence-setup.md) (ou la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) à une fenêtre de capture. Vous pouvez définir un ou plusieurs paramètres de capture actuels en mettant à jour les membres appropriés de la structure **CAPTUREPARMS** , puis en envoyant le message [**\_ \_ \_ \_ d’installation de la séquence de l’ensemble WM Cap**](wm-cap-set-sequence-setup.md) (ou la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) et **CAPTUREPARMS** à une fenêtre de capture.

 

 




