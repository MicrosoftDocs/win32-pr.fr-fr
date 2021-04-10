---
title: VML Fill, élément
description: VML Fill, élément
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc7205baa9db0eaa7d84d4022057f81804ea790
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941343"
---
# <a name="vml-fill-element"></a>VML Fill, élément

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit un remplissage pour une forme.

Les attributs suivants modifient un remplissage.



| Attribut                                                          | Description                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [AlignShape](msdn-online-vml-alignshape-attribute.md)             | Détermine si une image est alignée sur une forme.   |
| [AltHRef](althref-attribute--fill--vml.md)                        | Spécifie une autre référence pour une image.         |
| [Angle](angle-attribute--fill--vml.md)                            | Définit l’angle d’un dégradé.                  |
| [Aspect](msdn-online-vml-aspect-attribute.md)                     | Spécifie la manière dont l’aspect de l’image de remplissage sera préservé. |
| [Color](color-attribute--fill--vml.md)                            | Définit la couleur d’un remplissage.                           |
| [Couleur2](color2-attribute--fill--vml.md)                          | Définit la deuxième couleur d’un remplissage.                   |
| [Couleurs](msdn-online-vml-colors-attribute.md)                     | Définit plusieurs couleurs pour un remplissage dégradé.           |
| [DetectMouseClick](detectmouseclick-attribute--fill--vml.md)      | Détermine si un clic de souris est détecté.          |
| [Priorité](msdn-online-vml-focus-attribute.md)                       | Définit le centre d’un remplissage dégradé linéaire.          |
| [FocusPosition](msdn-online-vml-focusposition-attribute.md)       | Définit le centre d’un remplissage dégradé radial.          |
| [FocusSize](msdn-online-vml-focussize-attribute.md)               | Définit la taille de focus d’un remplissage radial.              |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Définit une URL vers le fichier image d’origine.              |
| [Identifiant](id-attribute--fill--vml.md)                                  | Définit un identificateur unique pour le remplissage.              |
| [Méthode](msdn-online-vml-method-attribute.md)                     | Définit la méthode utilisée pour générer un remplissage dégradé.   |
| [Activé](on-attribute--fill--vml.md)                                  | Détermine si le remplissage est affiché.          |
| [Opacity](opacity-attribute--fill--vml.md)                        | Définit la transparence d’un remplissage.                    |
| [Opacity2](msdn-online-vml-opacity2-attribute.md)                 | Définit la transparence de la deuxième couleur de remplissage.     |
| [Origine](origin-attribute--fill--vml.md)                          | Définit le centre d’une image.                        |
| [Position](position-attribute--fill--vml.md)                      | Définit la position d’une image.                      |
| [Taille](size-attribute--fill--vml.md)                              | Définit la taille d’une image.                          |
| [Sources](src-attribute--fill--vml.md)                                | Définit l’image à charger pour un remplissage.                  |
| [Titre](title-attribute--fill--vml.md)                            | Définit le titre d’un remplissage.                           |
| [Type](type-attribute--fill--vml.md)                              | Définit le type de remplissage.                              |



 

**Remarques**

Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .

Le code suivant illustre un remplissage dégradé simple pour une forme.


```HTML
   <v:shape
   style="position:relative;top:1;left:1;width:400;height:400"
   path = "m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type=gradient color="blue" color2="yellow"/>
   </v:shape>
```



**Exemples**

-   [Remplissage dégradé simple](/previous-versions/bb229620(v=vs.85))
-   [Exemple de remplissage dynamique](/previous-versions/bb229621(v=vs.85))

 

 