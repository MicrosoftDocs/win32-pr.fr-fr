---
title: Mesure de la qualité vidéo
description: Mesure de la qualité vidéo
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d3a4d28c12905722447189eabc494b220d737fc0c87f7a9ebc12948390920d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373513"
---
# <a name="measuring-video-quality"></a>Mesure de la qualité vidéo

Une façon de mesurer la qualité vidéo consiste à limiter le nombre de trames capturées supprimées pendant l’opération de capture. Une fois la capture en continu terminée, la valeur de qualité est comparée au rapport entre les images supprimées et le nombre total de trames. Si le pourcentage de frames supprimés est supérieur à la valeur du membre **wPercentDropForError** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap envoie un message d’erreur à la fonction de rappel d’erreur si elle est installée.

Vous pouvez récupérer la limite actuelle d’images supprimées (exprimées sous forme de pourcentage) à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Vous pouvez définir une nouvelle limite en spécifiant un pourcentage comme valeur du membre **wPercentDropForError** de la structure **CAPTUREPARMS** , puis en envoyant la structure mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). La valeur par défaut de **wPercentDropForError** est 10 pour cent.

 

 




