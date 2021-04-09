---
description: Avec Windows Vista, l’arborescence des éléments de l’acquisition d’images Windows (WIA) a changé de manière significative.
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: À propos de l’arborescence d’éléments IWiaItem2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865257"
---
# <a name="about-the-iwiaitem2-item-tree"></a>À propos de l’arborescence d’éléments IWiaItem2

Avec Windows Vista, l’arborescence des éléments de l’acquisition d’images Windows (WIA) a changé de manière significative. Les éléments [**IWiaItem2**](-wia-iwiaitem2.md) sont utilisés pour représenter des attributs d’appareil et des données de périphérique. Les applications de création d’images voient un appareil WIA (Windows Image Acquisition) 2,0 sous la forme d’une arborescence d’éléments hiérarchique, avec l’élément racine représentant l’appareil lui-même et les éléments enfants représentant des éléments tels que des sources de données programmables, des images ou des dossiers qui contiennent des images.

-   [Éléments d’application](#application-items)
-   [Indicateurs d’élément](#item-flags)
-   [Catégories d’éléments](#item-categories)
-   [Élément racine](#root-item)
-   [Élément de données](#data-item)
-   [Rubriques connexes](#related-topics)

## <a name="application-items"></a>Éléments d’application

L’arborescence d’éléments WIA 2,0 qu’une application peut voir est distincte de l’arborescence créée et gérée par un minipilote WIA 2,0. Lorsqu’un minipilote crée une arborescence, le service WIA 2,0 utilise cette arborescence d’éléments WIA 2,0 comme guide pour créer une copie de l’arborescence qui peut être affichée par des applications de création d’images. Les éléments de l’arborescence copiée sont appelés éléments d' *application* . Les éléments de l’arborescence créés par un *minipilote* sont appelés éléments de pilote.

Un élément WIA peut représenter une source de données programmable pour le chargeur de documents d’un scanneur ou les données stockées sur cet appareil. Un appareil WIA doit être divisé en éléments individuels qui décrivent les différentes données produites par cet appareil.

Par exemple, un scanneur WIA qui prend en charge la numérisation à plat et l’analyse du flux de documents peut être divisé en deux éléments enfants. L’une représente la fonctionnalité d’analyse à plat et l’autre représente la fonctionnalité d’analyse du flux de documents.

Plusieurs images disposées sur un scanneur à plat et analysées en même temps peuvent être placées dans un dossier. À l’aide du filtre de segmentation ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), chaque image ou sous-région peut ensuite être créée en tant qu’élément enfant du dossier.

L’arborescence WIA pour un appareil photo qui stocke des photos (« film ») peut être divisée en éléments qui représentent des dossiers, des sous-dossiers et des photos.

## <a name="item-flags"></a>Indicateurs d’élément

Les indicateurs d’élément WIA aident à classifier le contenu ou le comportement pris en charge d’un élément WIA particulier. Les indicateurs d’élément WIA se répartissent en deux groupes.

1.  Les indicateurs d’état de l’élément signalent l’état actuel de l’élément WIA, par exemple [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md), **WiaItemTypeDeleted**, etc.
2.  Les indicateurs d’utilisation/représentation des données d’élément signalent les données que l’élément WIA représente ou peuvent produire en cas de transfert. Par exemple, [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) est un indicateur de représentation de données qui indique à l’application que les données associées à l’élément WIA actuel sont des données image et doivent avoir des propriétés de données image. **WIA \_ Les \_ \_ indicateurs d’élément** de la Loi sont un indicateur d’utilisation d’élément qui indique à l’application que l’élément WIA est configurable et qui suit un ensemble de règles de configuration prédéfinies basées sur la catégorie d’éléments de la [**\_ Loi \_ \_ WIA**](-wia-wiaitempropcommonitem.md) et que la configuration peut éventuellement modifier le résultat pour chaque transfert de données. (Pour plus d’informations sur les définitions de catégorie, consultez catégories d’éléments catégories [d’éléments.](#item-categories) )

Le graphique suivant montre un exemple d’arborescence d’éléments WIA et les différents indicateurs qui peuvent être associés à chaque élément.

![exemples d’indicateurs d’élément pour les éléments d’une arborescence](images/scannertree1.jpg)

## <a name="item-categories"></a>Catégories d’éléments

Les éléments WIA sont regroupés en catégories à l’aide des valeurs de propriété de [**\_ \_ \_ catégorie d’élément WIA**](-wia-wiaitempropcommonitem.md) . Ces catégories définissent la façon dont un élément WIA doit être traité ou utilisé. Par exemple, si l’élément représente un fichier fini ( \_ fichier de catégorie WIA \_ terminé \_ ), une application WIA doit supposer que les données sont statiques et situées sur l’appareil. Si l’élément représente un alimentation (chargeur de \_ catégorie WIA \_ ), l’application doit s’attendre à ce qu’elle contienne les propriétés du chargeur de documents requis et fonctionne comme un chargeur de documents.

Les catégories définies par WIA sont les suivantes :

-   WIA \_ catégorie \_ auto
-   \_chargeur de catégorie WIA \_
-   \_film de catégorie WIA \_
-   \_fichier de catégorie WIA \_ terminé \_
-   \_plateau de catégorie WIA \_

Par exemple, l’élément à plat WIA d’un scanneur peut avoir les indicateurs d’élément de la [**\_ Loi \_ \_ WIA**](-wia-wiaitempropcommonitem.md) définis sur [**WiaItemTypeImage**](-wia-wia-item-type-flags.md), **WiaItemTypeTransfer** et **WiaItemTypeProgrammableDataSource**, et la propriété de **\_ \_ \_ catégorie d’élément WIA** de l’acquisition d’images est définie sur le plateau de catégorie WIA \_ \_ .

Le tableau suivant montre le regroupement des catégories WIA avec les indicateurs d’élément et les éléments WIA. Cette table n’inclut pas une liste complète des indicateurs d’éléments WIA définis par WIA.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Catégorie WIA</th>
<th>Indicateurs d’élément WIA valides</th>
<th>Jeu de propriétés WIA</th>
<th>Éléments WIA</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_AUTO</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></li>
</ul></td>
<td>Le jeu de propriétés comprend les propriétés de l’analyseur configuré automatiquement.</td>
<td>Élément auto WIA qui représente les paramètres d’analyse automatique configurés pour le scanneur.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FEEDER</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>Le jeu de propriétés comprend les propriétés du contrôle de l’analyseur du chargeur (généralement un jeu de propriétés d’image et de document spécifique).</td>
<td>Éléments de chargeur WIA, y compris les éléments enfants qui représentent les pages frontale et précédente d’un document.</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>Le jeu de propriétés comprend les propriétés du contrôle scanner de film (généralement un jeu de propriétés d’image et de document spécifique).</td>
<td>Éléments de film WIA, y compris les éléments enfants qui représentent les trames d’analyse individuelles.</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
</ul></td>
<td>La propriété définie sur cet élément dépend du type d’élément signalé. Par exemple, <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> doit inclure des propriétés d’élément d’image, telles que les bits par pixel et ainsi de suite.</td>
<td>Éléments de stockage WIA, y compris les éléments enfants qui représentent le contenu du fichier fini (fichiers de données tels que JPEG, HTML, TXT, etc.).</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>: peut être présent si le scanneur prend en charge l’analyse de plusieurs éléments.</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>: peut être présent si l’application génère un élément WIA au cours d’une session d’analyse de plusieurs éléments.</li>
</ul></td>
<td>Le jeu de propriétés comprend des propriétés de contrôle de scanneur à plat (généralement un jeu de propriétés d’image et de document spécifique).</td>
<td>Éléments à plat WIA, y compris les éléments enfants qui représentent des régions en cours d’analyse sur le plateau à plateau du scanneur.</td>
</tr>
</tbody>
</table>



 

Le graphique suivant montre un exemple d’arborescence d’éléments WIA et les différentes catégories qui peuvent être associées à chaque élément.

![exemples de catégories d’éléments pour les éléments d’une arborescence](images/scannertree2.jpg)

## <a name="root-item"></a>Élément racine

Un élément racine WIA est un élément de dossier marqué avec des indicateurs [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) et **WiaItemTypeDevice** qui représente l’appareil lui-même. Il contient des attributs d’appareil tels que le fabricant, le nom de périphérique et les attributs de pilote tels que la version de pilote et l’identificateur de classe d’interface utilisateur (CLSID). Les applications d’acquisition d’images obtiennent la racine de l’arborescence des éléments WIA en appelant la méthode [**IWiaDevMgr2 :: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) . L’application utilise l’élément racine pour accéder aux éléments WIA enfants individuels en énumérant l’arborescence (voir [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)).

## <a name="data-item"></a>DataItem

Tout élément pouvant être utilisé pour transférer des données est considéré comme un élément de données. Cela comprend les éléments marqués avec l’indicateur [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) .

Les éléments de dossier et les éléments sans dossier peuvent exposer la possibilité de transférer des données en étant marqués avec l’indicateur [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) . Tout élément avec cet indicateur doit fournir les propriétés d’élément WIA suivantes :

-   [**\_droits d' \_ accès WIA pour WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**taille de l’élément WIA de la \_ Loi WIA \_ \_**](-wia-wiaitempropcommonitem.md)
-   [**taille de la \_ \_ mémoire tampon WIA de la loi WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**FORMAT WIA de la \_ Loi WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_ \_ format préféré WIA de la loi WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**TYMED de la \_ Loi WIA \_**](-wia-wiaitempropcommonitem.md)
-   [**\_extension de \_ nom de fichier WIA de la loi WIA \_**](-wia-wiaitempropcommonitem.md)

Les éléments de source de données programmables marqués avec l’indicateur [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) doivent également fournir le jeu de propriétés d’élément de données requis.

Les éléments de données WIA peuvent avoir des propriétés supplémentaires en fonction des paramètres de l’indicateur de l’élément. Par exemple, les éléments WIA marqués avec l’indicateur [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) doivent avoir des propriétés d’informations spécifiques à l’image, telles que WIA et le **\_ \_ nombre \_ de \_ lignes WIA de** la loi WIA. [**\_ \_**](-wia-wiaitempropcommonitem.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)
</dt> <dt>

[**IWiaDevMgr2**](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



