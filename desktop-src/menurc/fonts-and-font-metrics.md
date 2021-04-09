---
title: Polices et mesures de texte
description: Cette rubrique décrit les polices vectorielles fournies par les fenêtres, les valeurs de mesure de police qui peuvent changer entre les versions de Windows et vous aide à utiliser les métriques de police dans vos applications de bureau.
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27d4eb5f34f5a88e4a0e3e866f9a14784c3895
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940981"
---
# <a name="fonts-and-text-metrics"></a>Polices et mesures de texte

Cette rubrique décrit les polices vectorielles fournies par les fenêtres, les valeurs de mesure de police qui peuvent changer entre les versions de Windows et vous aide à utiliser les métriques de police dans vos applications de bureau.

-   Pour plus d’informations sur les métriques de police dans DirectWrite, consultez [mesures de texte](/windows/desktop/DirectWrite/text-metrics).
-   Pour plus d’informations sur la gestion du texte dans les applications à l’aide de GDI, consultez les rubriques dans [polices et texte](/windows/desktop/gdi/fonts-and-text).

Pour plus d’informations sur l’utilisation des polices et les spécifications de type, consultez le [site Microsoft Typography](https://www.microsoft.com/typography/default.mspx).

## <a name="available-fonts"></a>Polices disponibles

Les polices vectorielles fournies avec Windows sont fournies sous forme de polices OpenType avec des contours TrueType (Windows prend également en charge les polices OpenType au format CFF). Pour obtenir la liste de toutes les polices fournies par Windows, consultez [typographie Microsoft : Polices par produit ou famille](https://www.microsoft.com/typography/fonts/default.aspx). Toutes les polices Windows Outline sont conformes à la dernière version de la [spécification OpenType](https://www.microsoft.com/typography/otspec/).

Pour obtenir la liste de toutes les polices d’interface utilisateur actuelles et héritées, consultez [mesures de police verrouillées](#locked-font-metrics) ci-dessous.

## <a name="font-modifications"></a>Modifications des polices

Pour garantir la compatibilité descendante, les polices sont rarement supprimées de Windows. Toutefois, les polices sont souvent modifiées. Les modifications peuvent inclure l’ajout de caractères, le redessin de caractères existants, la modification d’indicateurs ou l’ajout ou la modification de la prise en charge des fonctionnalités OpenType avancées et de la mise en forme complexe des scripts.

### <a name="locked-font-metrics"></a>Mesures des polices verrouillées

Notez que certaines valeurs associées aux polices d’interface utilisateur et aux polices par défaut utilisées dans les applications Microsoft sont verrouillées. Les polices de l’interface utilisateur sont utilisées pour restituer des éléments d’interface utilisateur tels que des légendes, des boîtes de dialogue et des menus. Très peu de modifications sont apportées à ces polices, étant donné leur grande visibilité et leur utilisation fréquente. Toutefois, étant donné que les valeurs signalées associées à ces polices sont verrouillées, il peut y avoir des différences entre les valeurs de police signalées et réelles.

Les valeurs signalées suivantes sont verrouillées pour l’interface utilisateur et les polices par défaut et peuvent être signalées de manière incorrecte :

-   Ces valeurs à partir de la [table OS/2](https://www.microsoft.com/typography/otspec/os2.htm)de la police :
    -   xAvgCharWidth
    -   sTypoLineGap
    -   sTypoAscender
    -   sTypoDescender
    -   usWinAscent
    -   usWinDescent
-   Valeur [unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm) définie dans l’en-tête de la police
-   Valeurs de la [table de métriques d’appareil verticale (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
-   Les largeurs d’avance pour les glyphes individuels

Voici une liste des polices d’interface utilisateur fournies avec Windows 8.1 (affectées par les valeurs verrouillées) :

| Nom du script                   | Police de l’interface utilisateur               |
|-------------------------------|-----------------------|
| Arabe                        | Segoe UI              |
| Arménien                      | Segoe UI              |
| Bangla (anciennement bengali)     | Nirmala UI            |
| Bopomofo                      | Microsoft JhengHei UI |
| Braille                       | Segoe UI Symbol       |
| Bugi                      | Leelawadee UI         |
| SYLLABE autochtones canadienne | Gadugi                |
| Cherokee                      | Gadugi                |
| Copte                        | Segoe UI Symbol       |
| Chinois (simplifié)          | Microsoft YaHei UI    |
| Chinois (traditionnel)         | Microsoft JhengHei UI |
| Cyrillique                      | Segoe UI              |
| Dévanâgarî                    | Nirmala UI            |
| Deseret                       | Segoe UI Symbol       |
| Éthiopien                      | Ebrima                |
| Géorgien                      | Segoe UI              |
| Lettre                    | Segoe UI Symbol       |
| La                        | Segoe UI Symbol       |
| Grec                         | Segoe UI              |
| Goudjrati                      | Nirmala UI            |
| Gurmukhi                      | Nirmala UI            |
| Hébreu                        | Segoe UI              |
| Ancien italique                    | Segoe UI Symbol       |
| Javanais                      | Texte javanais         |
| Japonais                      | Interface utilisateur Meiryo             |
| Kannada                       | Interface utilisateur Mirmala            |
| Khmer                         | Leelawadee UI         |
| Coréen                        | Malgun Gothic         |
| Lao                           | Leelawadee UI         |
| Latin                         | Segoe UI              |
| Malayalam                     | Nirmala UI            |
| Mongol                     | Mongolian Baiti       |
| Myanmar                       | Myanmar Text          |
| N’ko                          | Ebrima                |
| OGAM                         | Segoe UI Symbol       |
| Ol tchiki                      | Nirmala UI            |
| Ancien turc                    | Segoe UI Symbol       |
| Odia (anciennement Oriya)         | Nirmala UI            |
| Osmanya                       | Ebrima                |
| PHAGS-PA                      | Microsoft PhagsPa     |
| Lettre                         | Segoe UI Symbol       |
| Sora Sompeng                  | Nirmala UI            |
| Cingalais                       | Nirmala UI            |
| Syriaque                        | Estrangelo Edessa     |
| LETTRE TAÏ le                        | Microsoft Tai Le      |
| Nouveau taï lü                   | Microsoft New Tai Lue |
| Tamoul                         | Nirmala UI            |
| Télougou                        | Nirmala UI            |
| Tifinagh                      | Ebrima                |
| Tana                        | MV Boli               |
| Thaï                          | Leelawadee UI         |
| Tibétain                       | Microsoft Himalaya    |
| Vaï                           | Ebrima                |
| Yi                            | Microsoft Yi Baiti    |



 

Voici une liste des polices héritées de l’interface utilisateur qui sont également affectées par les valeurs verrouillées :

| Nom du script (hérité)          | Police de l’interface utilisateur (héritée)               |
|-------------------------------|--------------------------------|
| Bangla (anciennement bengali)     | Vrinda                         |
| SYLLABE autochtones canadienne | Euphemia                       |
| Cherokee                      | Plantagenet                    |
| Chinois (simplifié)          | Microsoft YaHei et SimSun     |
| Chinois (traditionnel)         | MingLiU et Microsoft JhengHei |
| Dévanâgarî                    | Mangal                         |
| Langues européennes            | Tahoma                         |
| Goudjrati                      | Shruti                         |
| Gurmukhi                      | Raavi                          |
| Japonais                      | Interface utilisateur Meiryo et MS Gothic        |
| Kannada                       | Tunga                          |
| Khmer                         | Khmer                          |
| Coréen                        | Gulim                          |
| Lao                           | Interface utilisateur lao                         |
| Malayalam                     | Kartika                        |
| Langues du Moyen-Orient      | Tahoma                         |
| Odia (anciennement Oriya)         | Kalinga                        |
| Singhalais                     | Iskoola Pota                   |
| Tamoul                         | Latha et Vijaya               |
| Télougou                        | Gautami                        |
| Thaï                          | Leelawadee et Tahoma          |



 

Ces polices sont utilisées comme valeurs par défaut dans les applications Microsoft et sont également affectées par les valeurs verrouillées :

-   Arial
-   Calibri
-   Cambria
-   Consolas
-   Courier New
-   MS Mincho
-   Times New Roman
-   Verdana

### <a name="dynamic-font-metrics"></a>Métriques de polices dynamiques

En dehors des mesures verrouillées répertoriées ci-dessus, les valeurs de police sont signalées avec précision. Si une police est modifiée dans une nouvelle version de Windows, les valeurs de police dynamiques diffèrent entre les nouvelles et anciennes. Par exemple, lorsqu’un glyphe est ajouté à une police, les valeurs de l’en-tête de la police peuvent changer. Le découpage peut se produire si ces valeurs (qui incluent xMin, xMax, yMin et yMax, et signalent le cadre englobant minimal et maximal pour les glyphes dans la police) ont été verrouillées et n’ont pas signalé de valeurs True.

> [!IMPORTANT]
> Si vous utilisez des valeurs de police dynamiques dans votre application (comme celles de [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)), ces valeurs seront modifiées si les polices sont modifiées dans les versions futures de Windows. N’utilisez pas ces valeurs réelles dans les situations où le texte doit rester statique.

 

## <a name="guidelines-for-using-font-metrics"></a>Instructions pour l’utilisation des métriques de police

-   Calculez les métriques d’écran et les métriques de police (par exemple, la largeur moyenne) quand une application est lancée, et utilisez ces valeurs pour disposer votre application. Cela fournira un rendu précis et cohérent, et votre disposition répondra aux modifications apportées aux polices ou s’adaptera aux polices de secours. Pour obtenir une vue d’ensemble de la police de substitution et de la liaison de police, consultez [Global Step by Step : polices](https://msdn.microsoft.com/goglobal/bb688134.aspx). Consultez [utilisation](/windows/desktop/Intl/using-font-fallback) de la police de substitution pour obtenir des informations spécifiques à Uniscribe.
    -   Pour calculer une métrique de base, affichez le texte représentatif pour le langage/script souhaité.
    -   Pour les contrôles qui ne contiennent qu’une seule ligne de texte non renvoyé à la ligne, ajustez-les pour qu’ils correspondent à la largeur totale du texte non réduit.
    -   Pour les contrôles à plusieurs lignes, obtenez la longueur totale, divisez-la par la longueur de caractère et vous obtenez une largeur unie à utiliser. Notez que cela est plus difficile pour les scripts complexes où un seul « caractère » du lecteur peut être plusieurs points de code.
-   Utilisez sTypoAscender, sTypoDescender et unitsPerEm (à partir de la [table OS/2](https://www.microsoft.com/typography/otspec/os2.htm)) pour calculer l’espacement vertical. sTypoAscender est utilisé pour déterminer le décalage optimal à partir du haut d’un cadre de texte jusqu’à la première ligne de base et sTypoDescender détermine le décalage optimal entre le bas d’un cadre de texte et la dernière ligne de base.
-   Si vous utilisez DirectWrite, créez une disposition à l’aide de [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextLayout** fournit des lineGap **ascendants**  +  **descendants**  +   dans une disposition naturelle. Vous pouvez accéder à ces valeurs spécifiques avec les [**\_ \_ métriques de police DWRITE**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics). Pour plus d’informations sur cette interface, consultez [mise en forme et disposition du texte](/windows/desktop/DirectWrite/text-formatting-and-layout).
-   Si vous utilisez GDI, rendez-vous sur l’écran, puis examinez la disposition (par exemple, la longueur de ligne ou les caractères par ligne) et recalculez les paramètres de disposition finale utilisés dans le rendu réel.
-   Ne générez pas de dispositions statiques en fonction de valeurs particulières pour des versions particulières de polices. Les valeurs réelles peuvent changer d’une version à l’autres.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**\_métriques de police DWRITE \_**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[Table OS/2](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[Table de métriques d’appareil verticale (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[Typographie Microsoft : Polices par produit ou famille](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Métriques du texte (DirectWrite)](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[Polices et texte (GDI)](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[Typographie Microsoft](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 