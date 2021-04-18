---
title: TableProperties VML (attribut)
description: TableProperties VML (attribut)
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512502"
---
# <a name="vml-tableproperties-attribute"></a>TableProperties VML (attribut)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Détermine les propriétés de la table. En lecture/écriture. **Integer**.

**S’applique à**

[Graphique à base de formes](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :TableProperties = " *expression* " >

**Remarques**

Utilisé par Microsoft PowerPoint pour les tables natives. La valeur par défaut est 0. Seuls les trois premiers bits de cet entier sont utilisés.

Même si la valeur est stockée dans une forme, l’attribut n’est utile que lorsque la table est constituée de formes regroupées. Les bits peuvent être combinés.

Les valeurs de bits suivantes sont incluses.



| bit | Description                              |
|-----|------------------------------------------|
| 1   | Définit si le groupe de formes est une table.   |
| 2   | Définit si la forme est un espace réservé.       |
| 3   | Définit si le texte de la table est bidirectionnel. |



 

*Attribut extensions Microsoft Office*

 

 