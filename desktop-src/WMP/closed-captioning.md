---
title: Sous-titrage
description: Sous-titrage
ms.assetid: a5d4d591-4b4d-49c5-b7da-01d7ee303ffd
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Lecteur Windows Media, migration des sous-titres
- Windows Media Player Object Model, Smigrating Closed Captions
- modèle objet, migrer des sous-titres
- Windows Media Player Mobile, migration des sous-titres
- Contrôle ActiveX du lecteur Windows Media, migration des sous-titres
- Contrôle ActiveX Windows Media Player Mobile, migration des sous-titres
- Contrôle ActiveX, migration de sous-titres
- Synchronized Accessible Media Interchange (SAMI), migration des sous-titres fermés
- SAMI (Synchronized Accessible Media Interchange), migration de sous-titres fermés
- Guide de migration, SAMI (Synchronized Accessible Media Interchange)
- Guide de migration, sous-titrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04cc3dfdeff7a9893b617e99cd3f0b8fb5c62f4f
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101305"
---
# <a name="closed-captioning"></a>Sous-titrage

Le contrôle ActiveX du lecteur Windows Media 6,4 comprend un panneau d’affichage de sous-titres intégré qui, lorsqu’il est rendu visible, active les sous-titres en SAMI (Synchronized Accessible Media Interchange) et affiche le texte de la légende fermée. Le contrôle Windows Media Player 7 ou version ultérieure active l’affichage de sous-titres SAMI fermé à l’aide d’un **<DIV>** élément HTML. Par exemple :


```C++
<DIV  ID = "CCDiv"></DIV>

```



Cette technique vous offre une flexibilité totale, car vous pouvez concevoir votre page Web pour afficher des sous-titres de manière personnalisée. l’affichage des sous-titres n’est plus nécessaire pour se trouver à un emplacement fixe adjacent à l’interface utilisateur du lecteur Windows Media.

Une fois que vous avez créé une zone pour afficher les sous-titres, utilisez *ClosedCaption*. propriété **captioningID** pour spécifier l’emplacement où le lecteur Windows Media effectue le rendu du texte de la légende fermée.


```C++
Player.closedCaption.captioningID = "CCDiv";

```



Le kit de développement logiciel (SDK) du lecteur Windows Media contient un exemple fonctionnel d’un lecteur intégré qui affiche le texte de la légende fermée. Pour obtenir les exemples du kit de développement logiciel (SDK), téléchargez et installez le kit de développement logiciel (SDK) Windows Media Player complet à partir du site Web Microsoft. Pour plus d’informations sur les sous-titres et le same, consultez le [site Web Microsoft Accessibility](https://www.microsoft.com/enable/).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objet ClosedCaption**](closedcaption-object.md)
</dt> <dt>

[**Guide de migration du modèle objet**](object-model-migration-guide.md)
</dt> </dl>

 

 




