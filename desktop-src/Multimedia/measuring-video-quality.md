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
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368620"
---
# <a name="measuring-video-quality"></a>Mesure de la qualité vidéo

Une façon de mesurer la qualité vidéo consiste à limiter le nombre de trames capturées supprimées pendant l’opération de capture. Une fois la capture en continu terminée, la valeur de qualité est comparée au rapport entre les images supprimées et le nombre total de trames. Si le pourcentage de frames supprimés est supérieur à la valeur du membre **wPercentDropForError** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap envoie un message d’erreur à la fonction de rappel d’erreur si elle est installée.

Vous pouvez récupérer la limite actuelle d’images supprimées (exprimées sous forme de pourcentage) à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Vous pouvez définir une nouvelle limite en spécifiant un pourcentage comme valeur du membre **wPercentDropForError** de la structure **CAPTUREPARMS** , puis en envoyant la structure mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de la définition de l’embout WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). La valeur par défaut de **wPercentDropForError** est 10 pour cent.

 

 




