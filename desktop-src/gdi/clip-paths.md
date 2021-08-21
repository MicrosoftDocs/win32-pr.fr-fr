---
description: Comme pour une zone de découpage, un tracé de clip est un autre objet graphique qu’une application peut sélectionner dans un contexte de périphérique.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Tracés de clip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91e77e3867951d09f464393fde6b416b9319f9ab914bcc393448d2b01a1eb24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038147"
---
# <a name="clip-paths"></a>Tracés de clip

Comme pour une zone de découpage, un tracé de clip est un autre objet graphique qu’une application peut sélectionner dans un contexte de périphérique. Contrairement à une zone de découpage, un tracé de clip est toujours créé par une application et il est utilisé pour le découpage vers une ou plusieurs formes irrégulières. Par exemple, une application peut utiliser les lignes et les courbes qui forment les contours de caractères dans une chaîne de texte pour définir un tracé de clip.

Pour créer un tracé de clip, il est tout d’abord nécessaire de créer un chemin d’accès qui décrit la forme irrégulière requise. Les chemins d’accès sont créés en appelant les fonctions de dessin GDI (Graphics Device Interface) appropriées après l’appel de la fonction [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) et avant l’appel de la fonction [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Cette collection de fonctions est appelée un crochet de tracé. Pour plus d’informations sur les chemins d’accès et les crochets, consultez [chemins](paths.md)d’accès.

Une fois le chemin d’accès créé, il peut être converti en chemin d’accès de clip en appelant la fonction [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , en identifiant un contexte de périphérique et en spécifiant un mode d’utilisation. Le mode d’utilisation détermine la façon dont le système combine le nouveau chemin d’accès au clip avec la région de découpage d’origine du contexte de périphérique. Le tableau suivant décrit les modes d’utilisation.



| Mode      | Description                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| RGN \_ et  | Le chemin d’accès au clip comprend l’intersection (zones qui se chevauchent) de la zone de découpage du contexte de périphérique et du chemin d’accès actuel.    |
| \_copie RGN | Le chemin d’accès au clip est le chemin d’accès actuel.                                                                                           |
| \_diff RGN | Le chemin d’accès au clip comprend la région de découpage du contexte de périphérique et les parties d’intersection du chemin d’accès actuel sont exclues.        |
| RGN \_ ou   | Le chemin d’accès au clip comprend l’Union (zones combinées) de la zone de découpage du contexte de périphérique et le chemin d’accès actuel.              |
| RGN \_ Xor  | Le chemin d’accès au clip inclut l’Union entre la zone de découpage du contexte de périphérique et le chemin d’accès actuel, mais exclut l’intersection. |



 

 

 



