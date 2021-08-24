---
title: État de la fenêtre de capture
description: État de la fenêtre de capture
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- Message WM_CAP_GET_STATUS
- capGetStatus macro)
- CAPSTATUS, structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 367d35c3869adb6f4e960fa472e0cd6a22483c37fa981e886b3a78f0b7410029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375285"
---
# <a name="capture-window-status"></a>État de la fenêtre de capture

Vous pouvez récupérer l’état actuel d’une fenêtre de capture à l’aide du message d' [**\_ \_ \_ État WM Cap obtenir**](wm-cap-get-status.md) (ou la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ). Ce message récupère une copie de la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) avec les valeurs actuelles de ses membres. La structure **CAPSTATUS** contient des informations sur les dimensions de l’image, la position de défilement et si la superposition ou l’aperçu de l’image est activé. Étant donné que les informations représentées dans **CAPSTATUS** sont dynamiques, votre application doit actualiser le contenu de la structure chaque fois que la taille ou le format du flux vidéo capturé peut avoir changé (par exemple, après avoir affiché le format vidéo du pilote de capture).

La modification des dimensions de la fenêtre de capture n’a aucun effet sur les dimensions du flux vidéo capturé réel. La boîte de dialogue Format affichée par le pilote de périphérique de capture vidéo contrôle les dimensions du flux vidéo capturé.

 

 




