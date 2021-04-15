---
title: Attribut SRC (Fill) (VML)
description: Attribut SRC (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463186"
---
# <a name="src-attribute-fillvml"></a>Attribut SRC (Fill) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit l’image à charger pour un remplissage. En lecture/écriture. **Chaîne**.

**S’applique à**

[Complète](msdn-online-vml-fill-element.md)

**Syntaxe de balise**

<v : *Element* SRC = " *expression* " >

**Syntaxe du script**

*Element* . src = "*expression * * *"**

*expression* = *élément*. SRC

**Remarques**

URL vers une image à charger pour les remplissages d’image et de motif. Cet attribut doit toujours être présent et pointer vers des données d’image valides pour qu’une image s’affiche. Si cet attribut apparaît seul (autrement dit, aucun attribut **href** ou **title** ), l’image est liée.

*Attribut standard VML*

**Exemple**

Une image en mosaïque utilisant le fichier myimage.gif en tant que source est affichée.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 