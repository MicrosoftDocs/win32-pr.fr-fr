---
title: Élément pivot incliné
description: Élément pivot incliné
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d659d16e6d10e9ec88875989a812de82403d2ac5b946580e7c7b7def956b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099039"
---
# <a name="vml-skew-element"></a>Élément pivot incliné

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit une inclinaison pour une forme.

Les attributs suivants modifient un décalage.



| Attribut                                 | Description                                    |
|-------------------------------------------|------------------------------------------------|
| [Ext](ext-attribute--skew--vml.md)       | Définit le mode d’affichage d’une inclinaison.           |
| [Identifiant](id-attribute--skew--vml.md)         | Définit un identificateur unique pour une inclinaison.        |
| [Matrice](matrix-attribute--skew--vml.md) | Définit une transformation de perspective pour une inclinaison.    |
| [Offset](offset-attribute--skew--vml.md) | Définit le décalage d’une inclinaison.                  |
| [Activé](on-attribute--skew--vml.md)         | Détermine si l’inclinaison sera affichée. |
| [Origine](origin-attribute--skew--vml.md) | Détermine l’origine d’un décalage.               |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

En outre, la [matrice](matrix-attribute--skew--vml.md) et [les](on-attribute--skew--vml.md) attributs doivent avoir la valeur **true**.

Voici le code minimal nécessaire pour produire un décalage.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



l’élément **Skew** est une Extension de Microsoft Office à VML.

**Exemples**

-   [Exemple d’inclinaison simple](/previous-versions/bb229482(v=vs.85))
-   [Exemple d’inclinaison dynamique](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 