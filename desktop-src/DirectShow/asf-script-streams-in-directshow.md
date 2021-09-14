---
description: Flux de Script ASF dans DirectShow
ms.assetid: afef1b8b-4be2-48a1-b72a-b2e6342a5e84
title: Flux de Script ASF dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da279c654a581bdb9eba23371882c5cbefbf5849
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112213"
---
# <a name="asf-script-streams-in-directshow"></a>Flux de Script ASF dans DirectShow

Quand le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) reçoit un fichier qui comprend un flux de type WMMEDIATYPE \_ script, il crée une broche de sortie qui peut être connectée au filtre de [convertisseur de commande de script interne](internal-script-command-renderer-filter.md) . Quand vous appelez [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile), ce filtre est automatiquement ajouté au graphique et connecté. Quand le convertisseur de commande de script interne reçoit un exemple contenant une commande de script, il déclenche un événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) dont *lParam* contient le script. L’application est entièrement responsable de la gestion de cet événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



