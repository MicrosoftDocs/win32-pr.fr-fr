---
title: Flux de script dans DirectShow
description: Flux de script dans DirectShow
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
ms.openlocfilehash: 09f08fab54dbdfe61dcc2ce78790cd471985cdeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311158"
---
# <a name="script-streams-in-directshow"></a>Flux de script dans DirectShow

Quand le filtre de lecteur ASF WM reçoit un fichier qui comprend un flux de type WMMEDIATYPE \_ script, il crée une broche de sortie qui peut être connectée au filtre de convertisseur de commande de script interne DirectShow. Quand vous appelez **IGraphBuilder :: RenderFile**, ce filtre est automatiquement ajouté au graphique et connecté. Quand le convertisseur de commande de script interne reçoit un exemple contenant une commande de script, il déclenche un **\_ \_ événement OLE** de l’EC dont **lParam** contient le script. L’application est entièrement responsable de la gestion de cet événement. Pour plus d’informations sur l' **\_ \_ événement OLE EC**, consultez la documentation du kit de développement logiciel (SDK) DirectShow.

 

 




