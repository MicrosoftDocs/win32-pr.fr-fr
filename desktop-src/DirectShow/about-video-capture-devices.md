---
description: À propos des périphériques de capture vidéo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: À propos des périphériques de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff3fff9f3d009006e300afdbe9986bfdc8d0a32ea618fdd2748efe0bd650b5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160182"
---
# <a name="about-video-capture-devices"></a>À propos des périphériques de capture vidéo

la plupart des nouveaux périphériques de capture vidéo utilisent des pilotes Windows Driver Model (WDM). Dans l’architecture WDM, Microsoft fournit un ensemble de pilotes indépendants du matériel, appelés pilotes de classe, et le fournisseur de matériel fournit des minipilotes spécifiques au matériel. Un minipilote implémente toutes les fonctions spécifiques à l’appareil. pour la plupart des fonctions, le minipilote appelle le pilote de classe Microsoft.

dans un graphique de filtre DirectShow, tous les périphériques de capture wdm apparaissent en tant que filtre de [capture vidéo wdm](wdm-video-capture-filter.md) . Le filtre de capture vidéo WDM se configure lui-même en fonction des caractéristiques du pilote. Il apparaît sous un nom fourni par le pilote : vous ne verrez pas de filtre appelé « filtre de capture vidéo WDM » n’importe où dans le graphique.

certains périphériques de capture plus anciens utilisent encore des pilotes de vidéo pour Windows (VFW). bien que ces pilotes soient à présent obsolètes, ils sont pris en charge dans DirectShow par le biais du filtre de [Capture VFW](vfw-capture-filter.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la capture vidéo dans DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



