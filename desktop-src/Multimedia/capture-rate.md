---
title: Taux de capture
description: Taux de capture
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
- CAPTUREPARMS, structure
- Message WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855cff56e36d9a246e1f18ae5fc4e3c09a200a2114104424f053a8780881de93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691659"
---
# <a name="capture-rate"></a>Taux de capture

Le taux de capture est le nombre de trames capturées chaque seconde d’une session de capture. Vous pouvez récupérer le taux de capture actuel à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de l’aide de WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Le taux de capture actuel est stocké dans le membre **dwRequestMicroSecPerFrame** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Vous pouvez définir le taux de capture en spécifiant le nombre de microsecondes entre les frames successifs comme valeur de ce membre, puis en envoyant la structure **CAPTUREPARMS** mise à jour à la fenêtre de capture à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-set-sequence-setup.md) de la séquence de l’ensemble de la plage WM (ou de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). La valeur par défaut de **dwRequestMicroSecPerFrame** est 66667, qui correspond à 15 images par seconde.

 

 




