---
description: À propos des périphériques de capture vidéo
ms.assetid: 1bf6e64f-c3cf-45a4-9f87-1b8cf503d98b
title: À propos des périphériques de capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ab9797c11b5c22f6196a5b4e781e50ce34edec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112389"
---
# <a name="about-video-capture-devices"></a>À propos des périphériques de capture vidéo

la plupart des nouveaux périphériques de capture vidéo utilisent des pilotes Windows Driver Model (WDM). Dans l’architecture WDM, Microsoft fournit un ensemble de pilotes indépendants du matériel, appelés pilotes de classe, et le fournisseur de matériel fournit des minipilotes spécifiques au matériel. Un minipilote implémente toutes les fonctions spécifiques à l’appareil. pour la plupart des fonctions, le minipilote appelle le pilote de classe Microsoft.

dans un graphique de filtre DirectShow, tous les périphériques de capture wdm apparaissent en tant que filtre de [capture vidéo wdm](wdm-video-capture-filter.md) . Le filtre de capture vidéo WDM se configure lui-même en fonction des caractéristiques du pilote. Il apparaît sous un nom fourni par le pilote : vous ne verrez pas de filtre appelé « filtre de capture vidéo WDM » n’importe où dans le graphique.

certains périphériques de capture plus anciens utilisent encore des pilotes de vidéo pour Windows (VFW). bien que ces pilotes soient à présent obsolètes, ils sont pris en charge dans DirectShow par le biais du filtre de [Capture VFW](vfw-capture-filter.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la capture vidéo dans DirectShow](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



