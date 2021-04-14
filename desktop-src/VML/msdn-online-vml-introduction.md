---
title: Présentation de VML
description: Présentation de VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Langage VML (VML), référence
- VML (langage VML), référence
- graphiques vectoriels, référence VML
- graphismes vectoriels, langage VML (VML)
- référence pour langage VML (VML)
- Référence VML
- Langage VML (VML), élément de forme
- VML (langage VML), élément de forme
- graphismes vectoriels, élément Shape
- Élément Shape
- Éléments VML, forme
- Langage VML (VML), VBScript
- VML (langage VML), VBScript
- Langage VML (VML), JavaScript
- VML (langage VML), JavaScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7a370519e3f173e7418f1aa0510cac768ff46c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382113"
---
# <a name="vml-introduction"></a>Présentation de VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Ce document fournit une référence détaillée complète sur l’implémentation du langage VML (VML) fourni avec Microsoft Office 2000. D’autres implémentations peuvent varier. Consultez la [spécification VML](https://www.w3.org/TR/NOTE-datetime.html) pour plus d’informations sur VML comme standard.

VML est défini comme un ensemble d’éléments XML et les attributs correspondants pour chaque élément. Étant donné que l’élément **Shape** est le bloc de construction de base de VML, cliquez [ici](shape-element--vml.md) pour commencer la référence.

Notez que cette référence contient plusieurs exemples et démonstrations. Vous devez avoir installé Microsoft Internet Explorer 5,0 ou version ultérieure pour afficher le VML en direct.

En plus des informations sur l’utilisation des éléments et des attributs en tant que balises XML qui étendent du code HTML, cette référence contient la syntaxe et des exemples qui montrent comment utiliser les fonctionnalités de script et de Document Object Model d’Internet Explorer 5 ou version ultérieure. L’utilisation de script avec VML vous permet de créer des éléments « à la volée » et de manipuler des attributs en temps réel.

Les exemples de cette référence utilisent VBScript et JavaScript. Si vous utilisez un langage de script différent de celui indiqué dans un exemple, vous devez respecter la casse de tous les noms d’éléments et d’attributs. La référence fournit une syntaxe de script correcte pour les langages qui respectent la casse, tels que JavaScript. En cas de doute sur le caractère correct, utilisez un Explorateur d’objets (tel que OLEView) pour explorer l' VGX.DLL afin de déterminer la casse exacte d’un élément ou d’un attribut. Notez que lorsque VML est utilisé en tant que balises XML, le respect de la casse dépend du type de document du document sous-jacent. Si vous utilisez un mode strict ! DOCTYPE, les éléments et les attributs sont sensibles à la casse.

[Référence VML](shape-element--vml.md)

 

 