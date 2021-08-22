---
title: Élément de format VML VML
description: Élément de format VML VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0632919a141ae04f80b0b6cd6782ea907aa8cfe1d720e599964110c038f3998e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099089"
---
# <a name="vml-shapetype-element"></a>Élément de format VML VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit une forme qui peut être utilisée pour créer d’autres formes.

L’attribut suivant modifie un **Typedeforme**.



| Attribut                                      | Description                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Master](msdn-online-vml-master-attribute.md) | Détermine si un **Typedeforme** est un élément principal. |



 

**Remarques**

**Typedeforme** est identique à l’élément **Shape** , à ceci près qu’il ne peut pas faire référence à un autre élément **Typedeforme** .

Lorsqu’un élément **Shape** fait référence à un **Typedeforme**, la **forme** peut dupliquer certaines des propriétés qui ont déjà été spécifiées dans **Typedeforme**. Dans ces cas, les attributs de la **forme** remplacent ceux du **Typedeforme**.

L’attribut **type** ne peut pas être utilisé avec **Typedeforme**.

Les attributs de positionnement CSS (tels que **haut**, **gauche**, etc.) ne sont pas transmis à une **forme** à partir d’un **Typedeforme**.

Pour utiliser cet élément, créez un **Typedeforme** avec un attribut d' [ID](id-attribute--vml.md) spécifique. Créez ensuite une **forme** et référencez le **Typedeforme** avec l’attribut **type** . Pour plus d’informations, consultez l’attribut [type](type-attribute--shape--vml.md) .

 

 