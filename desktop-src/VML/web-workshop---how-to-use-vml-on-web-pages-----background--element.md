---
title: Utilisation de l’élément background
description: Utilisation de l’élément background
ms.assetid: d11c1542-7f44-4ca7-9fb2-c8858fde3bc4
keywords:
- Atelier Web, élément d’arrière-plan
- conception de pages Web, élément d’arrière-plan
- Langage VML (VML), élément d’arrière-plan
- VML (langage VML), élément d’arrière-plan
- graphiques vectoriels, élément d’arrière-plan
- élément d’arrière-plan
- Éléments VML, arrière-plan
- Formes VML, élément d’arrière-plan
- Langage VML (VML), personnalisation des arrière-plans
- VML (langage VML), personnalisation des arrière-plans
- graphiques vectoriels, personnalisation des arrière-plans
- Formes VML, personnaliser les arrière-plans
- personnalisation des arrière-plans
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0108b91f199fbc3bff1c28ebdf016bfba11957
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842393"
---
# <a name="using-the-background-element"></a>Utilisation de l’élément background

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Dans cette rubrique, nous allons illustrer comment personnaliser l’arrière-plan d’une page Web à l’aide de l' `<background>` élément fourni dans Vml.

Comme vous l’avez appris dans la rubrique [use `<fill>` ](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md) , vous pouvez placer le `<fill>` sous-élément à l’intérieur de `<shape>` , `<shapetype>` ou tout élément de forme prédéfini pour décrire comment remplir la forme.

De même, vous pouvez placer le `<fill>` sous-élément à l’intérieur de l' `<background>` élément pour décrire comment remplir l’arrière-plan d’une page Web. Vous pouvez ensuite utiliser les attributs de propriété du `<fill>` sous-élément pour personnaliser l’effet de remplissage, tel que le [remplissage dégradé](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md), le [remplissage de motif](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md)ou le remplissage de l' [image](web-workshop---how-to-use-vml-on-web-pages-----fill--element.md).

Par exemple, pour dessiner un arrière-plan dégradé rempli, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :


```HTML
<v:background fillcolor="red">
<v:fill type="gradient"/>
</v:background>
```





Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858389) .

 

 