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
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029604"
---
# <a name="capture-window-status"></a>État de la fenêtre de capture

Vous pouvez récupérer l’état actuel d’une fenêtre de capture à l’aide du message d' [**\_ \_ \_ État WM Cap obtenir**](wm-cap-get-status.md) (ou la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ). Ce message récupère une copie de la structure [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) avec les valeurs actuelles de ses membres. La structure **CAPSTATUS** contient des informations sur les dimensions de l’image, la position de défilement et si la superposition ou l’aperçu de l’image est activé. Étant donné que les informations représentées dans **CAPSTATUS** sont dynamiques, votre application doit actualiser le contenu de la structure chaque fois que la taille ou le format du flux vidéo capturé peut avoir changé (par exemple, après avoir affiché le format vidéo du pilote de capture).

La modification des dimensions de la fenêtre de capture n’a aucun effet sur les dimensions du flux vidéo capturé réel. La boîte de dialogue Format affichée par le pilote de périphérique de capture vidéo contrôle les dimensions du flux vidéo capturé.

 

 




