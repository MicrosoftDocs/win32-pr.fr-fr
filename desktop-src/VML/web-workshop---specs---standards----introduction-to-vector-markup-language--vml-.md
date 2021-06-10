---
title: Langage VML (VML)
description: Langage VML (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Langage VML (VML), à propos de
- VML (langage VML), à propos de
- graphiques vectoriels, à propos de
- graphismes vectoriels, langage VML (VML)
- Langage VML (VML), World Wide Web Consortium (W3C)
- VML (langage VML), World Wide Web Consortium (W3C)
- graphismes vectoriels, World Wide Web Consortium (W3C)
- graphiques vectoriels, avantages VML
- Langage VML (VML), avantages
- VML (langage VML), avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4637fff0550ce9c93e295c51fc529f62c370b8aa
ms.sourcegitcommit: 78ce1d1e3f12ee3e08390868e5b93c034f437657
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111910260"
---
# <a name="vector-markup-language-vml"></a>Langage VML (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!NOTE]
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

Langage VML (VML) est un format d’échange, de modification et de remise basé sur XML pour les graphiques vectoriels de haute qualité sur le Web, qui répond aux besoins des utilisateurs de la productivité et des professionnels de la conception graphique. XML est un langage basé sur du texte simple, flexible et ouvert qui complète HTML. (Consultez la [section XML](/documentation/?frame=true) de MSDN Library pour obtenir des informations détaillées sur XML.)

VML est actuellement pris en charge par Microsoft Internet Explorer version 5,0 ou ultérieure.

VML a été proposé au W3C comme standard pour les graphiques vectoriels sur le Web (voir [langage VML (VML)](https://www.w3.org/TR/NOTE-VML)). Microsoft continue à s’engager dans le développement et l’implémentation de technologies basées sur XML, en collaboration avec les principaux partenaires de l’industrie (AutoDesk, Hewlett-Packard, Macromedia, Visio) et le W3C pour anticiper les normes basées sur le Web. Nous nous attendons à travailler avec le W3C pour atteindre un format standard pour les graphiques vectoriels sur le Web.

VML est également pris en charge par Microsoft Office 2000 ou version ultérieure. Microsoft Word, Microsoft Excel et Microsoft PowerPoint peuvent être utilisés pour créer des graphiques VML.

### <a name="using-vml"></a>Utilisation de VML

Pour utiliser VML dans vos pages Web, utilisez un élément style pour importer le comportement VML, comme indiqué dans le code suivant.

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

Ensuite, déclarez l’espace de noms VML, comme indiqué dans l’exemple de code suivant.

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

Enfin, ajoutez des éléments VML pour définir des effets visuels. Par exemple, le code VML suivant crée un ovale rouge.

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> Pour de meilleurs résultats lors de l’utilisation de documents en mode strict, assurez-vous que le balisage est valide et bien formé. Pour plus d’informations, consultez le. Page de référence DOCTYPE.


### <a name="benefits-of-vml"></a>Avantages du VML

-   VML facilite la création pour les utilisateurs et les auteurs de productivité. Il facilite l’échange (par couper-coller) et la modification ultérieure des graphiques vectoriels entre une grande variété d’applications de conception et de productivité.
-   VML offre des téléchargements de graphiques plus rapides et une meilleure expérience utilisateur. Il permet de fournir des graphiques vectoriels de grande qualité, entièrement intégrés et évolutifs au Web, dans un format texte ouvert. Plutôt que de référencer des graphiques en tant que fichiers externes, les graphiques VML sont remis en ligne avec la page HTML, ce qui leur permet d’interagir et de s’adapter à l’interaction de l’utilisateur.
-   VML est ouvert et basé sur des normes. Il s’agit d’un format XML. XML 1,0 est un langage textuel, simple et ouvert pour la description des données structurées sur le Web, qui complète le HTML en vue de son affichage. VML prend également en charge d’autres normes W3C, telles que feuilles de style en cascade 2,0 (CSS), qui spécifient les informations de style et le positionnement 2D, ainsi que le Document Object Model (DOM), qui permet aux développeurs d’interagir de manière cohérente avec les éléments de page en tant qu’objets.

### <a name="for-additional-information"></a>Pour plus d’informations

Consultez les liens ci-dessous :

-   Pour obtenir des réponses aux questions fréquemment posées sur VML, consultez le [FAQ VML](frequently-asked-questions-about-vml.yml).
-   Pour obtenir un didacticiel sur l’utilisation de VML sur les pages Web, consultez [comment utiliser VML sur des pages Web](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), qui complète la [spécification VML](https://www.w3.org/TR/NOTE-datetime.html) soumise au W3C.
-   Pour plus d’informations sur les types de données VML, consultez le document [types VML de base](basic-vml-types.md) .
-   Pour obtenir une référence complète sur VML, y compris des informations sur l’utilisation de VML avec les balises et les scripts, consultez la [référence VML](msdn-online-vml-introduction.md).