---
title: Annexe (VML)
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Atelier Web, espaces de noms
- Atelier Web, styles de comportement
- conception de pages Web, espaces de noms
- conception de pages Web, styles de comportement
- Langage VML (VML), espaces de noms
- VML (langage VML), espaces de noms
- graphiques vectoriels, espaces de noms
- Langage VML (VML), styles de comportement
- VML (langage VML), styles de comportement
- graphiques vectoriels, styles de comportement
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383680"
---
# <a name="appendix-vml"></a>Annexe (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

Pour permettre aux navigateurs de savoir comment transférer des données vers un processeur VML spécifique, vous devez taper des informations telles que les espaces de noms et les styles de comportement. Vous pouvez ensuite utiliser VML pour taper des graphiques dans la `<BODY>` région.

Dans cette rubrique :

-   [Espaces de noms](#namespaces)
-   [Styles de comportement](#behavior-styles)

## <a name="namespaces"></a>Espaces de noms

Un mécanisme XML indique l’espace de noms à partir duquel un élément provient. Si vous passez de l’analyse en HTML à l’analyse en XML, ce mécanisme indique le commutateur dans le code HTML.

Demandez à l’distributeur de votre processeur VML quelles informations sont requises pour l’espace de noms XML.

Si vous utilisez Microsoft Internet Explorer pour afficher le VML, tapez toujours la ligne suivante dans la `<HTML>` balise :


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Ces informations indiquent à Internet Explorer de basculer vers l’espace de noms « urn : schemas-microsoft-com : VML » lors de l’analyse d’une balise XML avec un préfixe `v:` , et de transmettre les données résultantes au processeur Vml.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="behavior-styles"></a>Styles de comportement

VML est défini dans Microsoft Internet Explorer comme un comportement par défaut.

Pour afficher le VML, tapez toujours les lignes suivantes dans la `<HEAD>` région :


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



VML est implémenté dans Internet Explorer par le biais de VGX.DLL. Si votre installation initiale du navigateur n’incluait pas le comportement VML, vous devrez peut-être l’ajouter en tant qu’option. Vous n’avez pas besoin d’ajouter une `<object>` balise.

 

 
