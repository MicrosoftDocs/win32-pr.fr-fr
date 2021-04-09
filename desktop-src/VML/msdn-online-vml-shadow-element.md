---
title: Élément Shadow VML
description: Élément Shadow VML
ms.assetid: 3e7d3e8c-45f8-4db3-95f3-7d993b7c2ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd73bb7087c2736ba5bec75102ffcb4337407650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941030"
---
# <a name="vml-shadow-element"></a>Élément Shadow VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit une ombre pour une forme.

Les attributs suivants modifient une ombre.



| Attribut                                          | Description                                        |
|----------------------------------------------------|----------------------------------------------------|
| [Color](color-attribute--shadow--vml.md)          | Définit la couleur d’une ombre.                     |
| [Couleur2](color2-attribute--shadow--vml.md)        | Définit la deuxième couleur d’une ombre.              |
| [Identifiant](id-attribute--shadow--vml.md)                | Spécifie l’identificateur unique d’une ombre.       |
| [Matrice](matrix-attribute--shadow--vml.md)        | Définit la transformation de perspective d’une ombre.     |
| [Masquée](msdn-online-vml-obscured-attribute.md) | Détermine si l’ombre est transparente.      |
| [Offset](offset-attribute--shadow--vml.md)        | Définit le degré d’extension de l’ombre au-delà de la forme. |
| [Offset2](msdn-online-vml-offset2-attribute.md)   | Définit un deuxième offset.                           |
| [Activé](on-attribute--shadow--vml.md)                | Détermine si une ombre est affichée.          |
| [Opacity](opacity-attribute--shadow--vml.md)      | Détermine la transparence d’une ombre.           |
| [Origine](origin-attribute--shadow--vml.md)        | Définit le centre de l’ombre.                  |
| [Type](type-attribute--shadow--vml.md)            | Spécifie le type d’ombre.                      |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

En outre, l’attribut [on](on-attribute--shadow--vml.md) doit avoir la valeur **true**.

Voici le code minimal nécessaire pour produire une ombre.


```HTML
   <v:rect
   fillcolor="green"
   style="top:1;left:1;width:50;height:50">
   <v:shadow on="True"/>
   </v:rect>
```



Vous ne pouvez pas remarquer l’ombre sauf si vous augmentez les valeurs de [décalage](offset-attribute--shadow--vml.md) , car le décalage par défaut est 2pt, 2pt.

**Exemples**

-   [Exemple d’ombre simple](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/t_shadow.md)
-   [Exemple d’instantané dynamique](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/shadow/x_shadow.md)

 

 