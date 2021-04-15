---
title: IVgColor VML
description: IVgColor VML
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d4800fbb99557acfbd3fd6e0dbbd893f30158f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463318"
---
# <a name="vml-ivgcolor"></a>IVgColor VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Spécifie une couleur.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>String</td>
<td>Chaîne. Représentation textuelle de la couleur. Les types de couleur nommés suivants sont pris en charge :
<ul>
<li>Noir (#000000)</li>
<li>Silver (#C0C0C0)</li>
<li>Gris (#808080)</li>
<li>Blanc (#FFFFFF)</li>
<li>Marron (#800000)</li>
<li>Rouge (#FF0000)</li>
<li>Violet (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Vert (#008000)</li>
<li>Chaux (#00FF00)</li>
<li>Vert olive (#808000)</li>
<li>Jaune (#FFFF00)</li>
<li>Bleu marine (#000080)</li>
<li>Bleu (#0000FF)</li>
<li>Bleu-vert (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Type</td>
<td>VgColorType. Type de couleur. L’un des types suivants :
<ul>
<li>Mixte</li>
<li>RGB</li>
<li>Schéma</li>
<li>named</li>
</ul></td>
</tr>
<tr class="odd">
<td>RGB</td>
<td>VgRGBType. Valeur RVB (<strong>longue</strong>) de la couleur. Valide uniquement si le type est &quot; <strong>RVB</strong> &quot; .</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Integer</strong>. Composant rouge de la couleur. Peut être compris entre 0 et 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Integer</strong>. Composant vert de la couleur. Peut être compris entre 0 et 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Integer</strong>. Composant bleu de la couleur. Peut être compris entre 0 et 255.</td>
</tr>
</tbody>
</table>



 

 

 