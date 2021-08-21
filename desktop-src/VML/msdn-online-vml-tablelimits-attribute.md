---
title: TableLimits VML (attribut)
description: TableLimits VML (attribut)
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af52ba570b04e56f1dede169045f7ee1addf374fae5ca4f1cd5de4d9390f1235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959249"
---
# <a name="vml-tablelimits-attribute"></a>TableLimits VML (attribut)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Liste des valeurs de hauteur minimale pour chaque ligne d’une table. En lecture/écriture. **VgLengthArray**.

**S’applique à**

[Forme](shape-element--vml.md)

**Syntaxe de balise**

<v : *Element* o :tablelimits = " *expression* " >

**Remarques**

utilisé par Microsoft PowerPoint pour les tables natives. La valeur par défaut est **null**.

Même si la valeur est stockée dans une forme, l’attribut n’est utile que lorsque la table est constituée de formes regroupées. Lorsque du texte est ajouté à des cellules de tableau, la hauteur de ligne peut augmenter. L’attribut **TableLimits** stocke la hauteur de ligne d’origine, de sorte que si le texte est supprimé, la hauteur de ligne ne sera pas inférieure à la valeur d’origine.

*Microsoft Office Attribut extensions*

 

 