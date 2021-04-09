---
title: Capture de User-Initiated
description: Capture de User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840509"
---
# <a name="user-initiated-capture"></a>Capture de User-Initiated

Vous pouvez récupérer la valeur actuelle de l’indicateur de capture initié par l’utilisateur à l’aide du message [**\_ \_ \_ \_ d’installation**](wm-cap-get-sequence-setup.md) de la séquence de bits WM (ou de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). La valeur de l’indicateur est stockée dans le membre **fMakeUserHitOKToCapture** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Vous pouvez fournir à l’utilisateur un contrôle précis sur le moment où démarrer une session de capture en affectant à ce membre la **valeur true**. AVICap affiche une boîte de dialogue après avoir alloué toutes les mémoires tampons vidéo et audio pour une session de capture. Cela permet à l’utilisateur d’éliminer les retards de capture en raison de l’initialisation du logiciel. Si votre application utilise un petit nombre de mémoires tampons vidéo, cette boîte de dialogue n’est probablement pas nécessaire. La valeur par défaut est **FALSE**.

 

 




