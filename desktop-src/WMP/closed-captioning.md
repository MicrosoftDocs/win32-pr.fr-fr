---
title: Sous-titrage
description: Sous-titrage
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- modèle objet Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Lecteur Windows Media Mobile, accessible en SAMI (Synchronized Accessible Media Interchange)
- contrôle de ActiveX Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- Lecteur Windows Media contrôle Mobile ActiveX, SAMI (synchronized Accessible Media Interchange)
- contrôle de ActiveX, SAMI (synchronized Accessible Media Interchange)
- Lecteur Windows Media, migration des sous-titres
- Lecteur Windows Media modèle objet, Smigrating les sous-titres fermés
- modèle objet, migrer des sous-titres
- Lecteur Windows Media Mobile, migration des sous-titres
- Lecteur Windows Media ActiveX contrôle, migration des sous-titres
- Lecteur Windows Media contrôle de ActiveX Mobile, migration des sous-titres
- contrôle de ActiveX, migration des sous-titres
- Synchronized Accessible Media Interchange (SAMI), migration des sous-titres fermés
- SAMI (Synchronized Accessible Media Interchange), migration de sous-titres fermés
- Guide de migration, SAMI (Synchronized Accessible Media Interchange)
- Guide de migration, sous-titrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa83cb5fb6735475a883986673c958db9642386bd8ce2c76151ddd6c2f23ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119597"
---
# <a name="closed-captioning"></a>Sous-titrage

le contrôle Lecteur Windows Media 6,4 ActiveX comprend un panneau d’affichage de sous-titres intégré qui, lorsqu’il est rendu visible, active les sous-titres SAMI (synchronized Accessible Media Interchange) et affiche le texte de la légende fermée. le contrôle Lecteur Windows Media 7 ou version ultérieure active l’affichage des sous-titres SAMI fermés à l’aide d’un **<DIV>** élément HTML. Par exemple :


```C++
<DIV  ID = "CCDiv"></DIV>

```



Cette technique vous offre une flexibilité totale, car vous pouvez concevoir votre page Web pour afficher des sous-titres de manière personnalisée. l’affichage des sous-titres n’est plus nécessaire pour se trouver à un emplacement fixe adjacent à l’interface utilisateur Lecteur Windows Media.

Une fois que vous avez créé une zone pour afficher les sous-titres, utilisez *ClosedCaption*. propriété **captioningID** pour spécifier l’emplacement où Lecteur Windows Media restitue le texte de la légende fermée.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



le kit de développement logiciel (SDK) Lecteur Windows Media contient un exemple fonctionnel d’un lecteur incorporé qui affiche le texte de la légende fermée. pour obtenir les exemples du kit de développement logiciel (sdk), téléchargez et installez le kit de développement logiciel (sdk) Lecteur Windows Media complet à partir du Site Web Microsoft. Pour plus d’informations sur les sous-titres et le same, consultez le [site Web Microsoft Accessibility](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objet ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> </dl>

 

 




