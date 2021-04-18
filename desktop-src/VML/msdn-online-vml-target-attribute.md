---
title: Attribut cible VML
description: Attribut cible VML
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512103"
---
# <a name="vml-target-attribute"></a>Attribut cible VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Définit un frame ou une fenêtre dans laquelle une URL est affichée. En lecture/écriture. **Chaîne**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *élément* target = " *expression* " >

**Remarques**

L’attribut **cible** est semblable à l’attribut **cible** HTML standard des ancres.

Ces valeurs comprennent :



| Valeur      | Description                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TargetName | Chaîne contenant le nom du frame ou de la fenêtre dans lequel charger le document.                                                                                                                                                                                 |
| \_Occult    | Spécifie que le document lié est chargé dans une nouvelle fenêtre vide. Cette fenêtre n’est pas nommée.                                                                                                                                                                  |
| \_Media    | À compter d’Internet Explorer 6 pour Windows XP Service Pack 2, l' \_ attribut Media est obsolète et n’est plus pris en charge. Tout d’abord disponible dans Internet Explorer 6, cette valeur spécifie que le document lié doit être chargé dans la barre de médias.                |
| \_parent   | Spécifie que le document lié est chargé dans le parent immédiat du document contenant le lien.                                                                                                                                                      |
| \_recherche   | À compter d’Internet Explorer 7 pour Windows XP Service Pack 2, : l' \_ attribut de recherche est obsolète et n’est plus pris en charge. Tout d’abord disponible dans Internet Explorer 6, cette valeur spécifiait que le document lié devait être chargé dans le volet de recherche du navigateur. |
| \_self     | Spécifie que le document lié est chargé dans la fenêtre dans laquelle l’utilisateur a cliqué sur le lien (fenêtre active).                                                                                                                                                  |
| \_Retour au début      | Spécifie que le document lié est chargé dans la fenêtre de premier plan.                                                                                                                                                                                            |



 

*Attribut standard VML*

**Exemple**

Lorsque vous cliquez sur le rectangle, le navigateur charge la page d’accueil de Microsoft Corporation dans la même fenêtre.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Exemple d’attribut cible](/previous-versions/bb264096(v=vs.85)). (Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)

 

 