---
title: Masquage du contrôle du lecteur Windows Media
description: Masquage du contrôle du lecteur Windows Media
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- incorporation, pages Web
- Lecteur Windows Media, masquage du contrôle ActiveX
- Windows Media Player Object Model, masquage du contrôle ActiveX
- modèle objet, masquer le contrôle ActiveX
- Windows Media Player Mobile, contrôle hidingActiveX
- Contrôle Windows Media Player ActiveX, masquage
- Windows Media Player Mobile (contrôle ActiveX), masquage
- Contrôle ActiveX, masquage
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- Incorporation de page Web, masquage du contrôle ActiveX
- masquage du contrôle ActiveX du lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba1add2b8f09829ad165f152c26c184d68ac183
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310769"
---
# <a name="hiding-the-windows-media-player-control"></a>Masquage du contrôle du lecteur Windows Media

L’objet ActiveX du lecteur Windows Media est incorporé dans une page Web à l’aide de l’élément objet. Contrairement aux versions antérieures, l’élément objet qui définit le lecteur Windows Media doit être placé dans la section de corps d’une page Web, entre les balises <BODY> et </BODY> . Placer l’objet Windows Media Player ActiveX dans la section HEAD d’une page Web pour masquer l’interface utilisateur peut produire des résultats inattendus.

Si vous placez le contrôle ActiveX du lecteur Windows Media dans la section corps d’une page Web, l’interface utilisateur du contrôle s’affiche. Si vous ne souhaitez pas qu’il s’affiche et que vous souhaitiez créer votre propre interface utilisateur, affectez la valeur zéro aux attributs Height et Width de l’élément objet.

Le contrôle peut également être rendu invisible en définissant le *lecteur*. propriété **UIMODE** sur « invisible ». Pour ce faire, vous pouvez utiliser une balise PARAM comme indiqué dans la section suivante. Dans ce cas, l’espace est réservé pour le contrôle à l’aide de la hauteur et de la largeur, mais rien ne s’affiche dans l’espace réservé jusqu’à ce que **UIMODE** soit remplacé par un élément autre que « invisible ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans une page Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




