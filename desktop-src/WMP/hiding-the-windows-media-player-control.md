---
title: masquage du contrôle Lecteur Windows Media
description: masquage du contrôle Lecteur Windows Media
ms.assetid: 754896af-b80d-4552-82c6-3fb65359accd
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media ActiveX contrôle, pages Web
- Lecteur Windows Media contrôle de ActiveX Mobile, pages Web
- contrôle ActiveX, pages Web
- incorporation, pages Web
- Lecteur Windows Media, masquer ActiveX contrôle
- Lecteur Windows Media le modèle objet, masquant ActiveX contrôle
- modèle objet, masquer le contrôle de ActiveX
- Lecteur Windows Media Mobile, contrôle hidingActiveX
- Lecteur Windows Media ActiveX contrôle, masquage
- Lecteur Windows Media contrôle de ActiveX Mobile, masquage
- contrôle ActiveX, masquage
- Lecteur Windows Media ActiveX contrôle, pages Web
- Lecteur Windows Media contrôle de ActiveX Mobile, pages Web
- contrôle ActiveX, pages Web
- incorporation de page Web, masquer le contrôle de ActiveX
- masquer Lecteur Windows Media contrôle de ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cf7c25f75538f1e20a08ef252b20212df48a565
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416244"
---
# <a name="hiding-the-windows-media-player-control"></a>masquage du contrôle Lecteur Windows Media

l’objet Lecteur Windows Media ActiveX est incorporé dans une page web à l’aide de l’élément objet. contrairement aux versions antérieures, l’élément objet qui définit Lecteur Windows Media doit être placé dans la section de corps d’une page web, entre le &lt; corps &gt; et </BODY> MetaTags. placer l’Lecteur Windows Media objet ActiveX dans la section d’en-tête d’une page web pour masquer l’interface utilisateur peut produire des résultats inattendus.

si vous placez le contrôle Lecteur Windows Media ActiveX dans la section corps d’une page web, l’interface utilisateur du contrôle s’affiche. Si vous ne souhaitez pas qu’il s’affiche et que vous souhaitiez créer votre propre interface utilisateur, affectez la valeur zéro aux attributs Height et Width de l’élément objet.

Le contrôle peut également être rendu invisible en définissant le *lecteur*. propriété **UIMODE** sur « invisible ». Pour ce faire, vous pouvez utiliser une balise PARAM comme indiqué dans la section suivante. Dans ce cas, l’espace est réservé pour le contrôle à l’aide de la hauteur et de la largeur, mais rien ne s’affiche dans l’espace réservé jusqu’à ce que **UIMODE** soit remplacé par un élément autre que « invisible ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**utilisation du contrôle Lecteur Windows Media dans une Page Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




