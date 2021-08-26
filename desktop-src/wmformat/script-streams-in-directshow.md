---
title: Flux de Script dans DirectShow
description: Flux de Script dans DirectShow
ms.assetid: ad467897-1d25-4bb0-a0ec-84560fe7063b
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, flux de scripts
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), flux de scripts
- ASF (format de systèmes avancés), flux de script
- DirectShow, flux de script
- flux de script, DirectShow
- flux, flux de script dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30e832928b84ab0e1e755dcfdb8c79893c5d942e15e4beb9925f852251614bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929618"
---
# <a name="script-streams-in-directshow"></a>Flux de Script dans DirectShow

quand le filtre de lecteur ASF WM reçoit un fichier qui comprend un flux de type WMMEDIATYPE \_ script, il crée une broche de sortie qui peut être connectée au filtre de convertisseur de commande de Script interne DirectShow. Quand vous appelez **IGraphBuilder :: RenderFile**, ce filtre est automatiquement ajouté au graphique et connecté. Quand le convertisseur de commande de script interne reçoit un exemple contenant une commande de script, il déclenche un **\_ \_ événement OLE** de l’EC dont **lParam** contient le script. L’application est entièrement responsable de la gestion de cet événement. pour plus d’informations sur l' **\_ \_ événement OLE EC**, consultez la documentation du kit de développement logiciel (SDK) DirectShow.

 

 




