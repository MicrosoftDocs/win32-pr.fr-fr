---
description: Une largeur ABC est une valeur composite définie par une structure GDI ABC. La structure contient les membres abcA, abcB et abcC, qui correspondent au &\# 0034 ;&\# 0034 ;, &\# 0034 ; B&\# 0034 ; et &\# 0034 ; C&\# 0034 ; largeurs d’un glyphe ou exécution.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Glossaire Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808ff2e9620810fe2ec344a037437e6ce8d62bff9460a53cf7b777cedc9d46b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146968"
---
# <a name="uniscribe-glossary"></a>Glossaire Uniscribe

Une largeur ABC est une valeur composite définie par une structure GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) . La structure contient les membres **abcA**, **abcB** et **abcC**, qui correspondent aux largeurs « A », « B » et « C » d’un [glyphe](#glyph) ou d’une [exécution](#run).

La largeur « A » est [débloquée](#underhang) (positive, également appelée « remplissage ») ou [dépassement](#overhang) (négatif) à gauche de l’équivalent à l’écran de l’encre qui représente le glyphe ou l’exécution. La largeur « B » correspond à la largeur en noir, à la largeur de l’encre la plus à gauche à l’encre la plus à droite. La largeur « C » est le dépassement à droite de l’encre.

L’illustration suivante montre un F minuscule italique avec un porte-à-faux à gauche et à droite. Autrement dit, les largeurs « A » et « C » sont toutes deux négatives. Pour obtenir une illustration des largeurs positives « A » et « C », reportez-vous à la section sous- [blocage](#underhang) .

![Illustration montrant un F minuscule italique avec un surplomb à gauche et à droite.](images/abcwidth.gif)

Quand au moins deux glyphes sont affichés en tant qu’unité, le glyphe le plus à gauche contribue généralement à la largeur « A » de l’exécution et seul le glyphe le plus à droite contribue à la largeur « C » de l’exécution. Toutefois, il ne s’agit pas d’une règle stricte. Par exemple, si le premier glyphe d’une série est une lettre étroite et que le deuxième glyphe est une marque DIACRITIQUE étendue, et qu’ils sont gérés comme des glyphes séparés, la marque DIACRITIQUE peut en fait s’étendre au-delà de la lettre.

## <a name="abc-width"></a>Largeur ABC

Une largeur ABC est une valeur composite définie par une structure GDI [**ABC**](/windows/win32/api/wingdi/ns-wingdi-abc) . La structure contient les membres **abcA**, **abcB** et **abcC**, qui correspondent aux largeurs « A », « B » et « C » d’un [glyphe](#glyph) ou d’une [exécution](#run).

La largeur « A » est [débloquée](#underhang) (positive, également appelée « remplissage ») ou [dépassement](#overhang) (négatif) à gauche de l’équivalent à l’écran de l’encre qui représente le glyphe ou l’exécution. La largeur « B » correspond à la largeur en noir, à la largeur de l’encre la plus à gauche à l’encre la plus à droite. La largeur « C » est le dépassement à droite de l’encre.

L’illustration suivante montre un F minuscule italique avec un porte-à-faux à gauche et à droite. Autrement dit, les largeurs « A » et « C » sont toutes deux négatives. Pour obtenir une illustration des largeurs positives « A » et « C », reportez-vous à la section sous- [blocage](#underhang) .

![Illustration montrant un F minuscule italique avec un surplomb à gauche et à droite.](images/abcwidth.gif)

Quand au moins deux glyphes sont affichés en tant qu’unité, le glyphe le plus à gauche contribue généralement à la largeur « A » de l’exécution et seul le glyphe le plus à droite contribue à la largeur « C » de l’exécution. Toutefois, il ne s’agit pas d’une règle stricte. Par exemple, si le premier glyphe d’une série est une lettre étroite et que le deuxième glyphe est une marque DIACRITIQUE étendue, et qu’ils sont gérés comme des glyphes séparés, la marque DIACRITIQUE peut en fait s’étendre au-delà de la lettre.

## <a name="advance-width"></a>largeur avancée

La largeur d’avance d’un [glyphe](#glyph) est le déplacement dans la direction de l’écriture à partir du point de départ pour le rendu du glyphe au point de départ pour le rendu du glyphe suivant.

## <a name="bidirectional-stack"></a>pile bidirectionnelle

La pile bidirectionnelle est un entier 5 bits qui effectue le suivi des niveaux d’imbrication entre le texte de gauche à droite et le texte de droite à gauche. Elle démarre toujours à zéro pour la gauche vers la droite. Par conséquent, toutes les valeurs paires représentent du texte de gauche à droite et toutes les valeurs impaires représentent le texte de droite à gauche. La pile bidirectionnelle est représentée dans le membre **uBidiLevel** d’une structure d' [**\_ État de script**](/windows/win32/api/usp10/ns-usp10-script_state) .

## <a name="bidirectional-text"></a>texte bidirectionnel

Le texte bidirectionnel contient des parties de gauche à droite et de droite à gauche, mais le terme est parfois faiblement appliqué au texte pur de droite à gauche. Le texte de droite à gauche requiert l’utilisation de la [pile bidirectionnelle](#bidirectional-stack), car le niveau d' [incorporation](#embedding-level) par défaut de zéro implique du texte de gauche à droite.

## <a name="cell-width"></a>largeur de cellule

Une application peut justifier du texte pour s’ajuster à une ligne en ajustant la largeur de cellule pour certains glyphes. Pour du texte non justifié, la largeur de cellule pour un glyphe est identique à sa [largeur d’avance](#advance-width).

## <a name="cluster"></a>cluster

Un cluster est la plus petite unité linguistique qui peut être mise en forme. Dans les langages tels que l’arabe et la plupart des langages indo-aryens, les glyphes utilisés pour représenter chaque caractère (point de code Unicode) dépendent fortement des points de code environnants, qui constituent le cluster. Dans ces langages, les applications peuvent traduire des points de code en glyphes appropriés uniquement en examinant le cluster. Dans certains scripts, tels que le DÉVANÂGARÎ, l’ordre des glyphes au sein d’un cluster peut différer de l’ordre des points de code Unicode correspondants. pour plus d’informations, consultez [Windows traitement des glyphes](/typography/develop/processing-part1) sur le site de typographie de Microsoft.

## <a name="complex-script"></a>script complexe

Un script complexe est un [script](#complex-script) avec l’une des propriétés suivantes :

-   Autorise le rendu bidirectionnel.
-   A une mise en forme contextuelle.
-   A des caractères d’association.
-   A des règles de justification et de justification de mot spécialisées.
-   Filtre les combinaisons de caractères non conformes.
-   n’est pas pris en charge dans les polices de Windows principales et peut donc nécessiter une [police de secours](#font-fallback).

Dans certains scripts complexes, l’ordre des glyphes peut être très différent de l’ordre des caractères Unicode sous-jacents qu’ils représentent. Pour plus d’informations, consultez [à propos des scripts complexes](about-complex-scripts.md) .

> [!Note]  
> Dans le contexte de la typographie, il est parfois souhaitable de gérer le script latin utilisé en écrivant l’anglais comme script complexe. Il peut s’agir, par exemple, de la fonctionnalité de remplaçants stylistiques décrite dans la documentation d’un [**\_ \_ enregistrement de fonctionnalité OpenType**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)ou de ligatures, telles que « fi », où un seul glyphe représente deux caractères consécutifs ou plus.

 

## <a name="embedding-level"></a>niveau d’incorporation

Dans le [texte bidirectionnel](#bidirectional-text), le niveau d’incorporation est l’index de la [pile bidirectionnelle](#bidirectional-stack).

## <a name="font-fallback"></a>police de secours

La police de secours est la sélection automatisée d’une police autre que la police sélectionnée par l’utilisateur dans une application. Dans Uniscribe, la police de secours est appliquée par la fonction [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) lorsque la totalité ou une partie du texte est dans un script que la police sélectionnée par l’utilisateur ne prend pas en charge.

## <a name="glyph"></a>glyphe

Un glyphe est une unité unique d’affichage dans une police. Pour OpenType, cette unité est définie par un plan. Pour les autres types de polices, il peut être défini par une image bitmap, un ensemble de commandes graphiques et autres. Un glyphe ne correspond pas nécessairement à un caractère unique. Par exemple, la ligature « fi » (« FI ») représente les deux caractères « f » et « i ». Le « o » minuscule vietnamien et le tilde (« ỗ ») sont généralement composés de plusieurs glyphes.

## <a name="item"></a>item

Un élément a un seul [script](#complex-script) et une seule direction. La fonction [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) ou [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) peut analyser un paragraphe dans des éléments. Un élément n’est pas nécessairement une [exécution](#run). Il peut contenir des caractères de plusieurs styles. Les informations d’élément et d’exécution doivent être combinées pour déterminer des [plages](#range).

## <a name="lrm"></a>LRM

LRM indique la marque de gauche à droite (point de code Unicode U + 200E). Cette marque spécifie que les caractères qui la suivent dans l’ordre logique doivent être rendus de gauche à droite.

## <a name="ltr"></a>LTR

LTR indique de gauche à droite.

## <a name="range"></a>range

Une plage est un cas spécial d’une [exécution](#run). Il se situe entièrement dans un [élément](#item). Par conséquent, si un élément est divisé en séries, chacune de ces exécutions est une plage.

## <a name="rlm"></a>RLM

RLM indique la marque de droite à gauche (point de code Unicode U + 200F). Cette marque indique que les caractères qui la suivent dans l’ordre logique doivent être affichés de droite à gauche.

## <a name="rtl"></a>DàG

RTL indique de droite à gauche.

## <a name="run"></a>Exécuter

Une exécution est un passage de texte à afficher par Uniscribe. Elle doit avoir un seul style, c’est-à-dire la police, la taille et la couleur, mais elle peut être dessinée à partir d’un grand nombre de [scripts](#complex-script). Une exécution peut contenir du contenu de gauche à droite et de droite à gauche.

## <a name="nads"></a>NADS

NADS indique les formes de chiffres nationales (point de code Unicode U + 206E. Le terme spécifie que les chiffres européens (U + 0030 à U + 0039) doivent être rendus en tant que chiffres nationaux. Pour plus d’informations sur les chiffres nationaux, consultez [formes de chiffres](digit-shapes.md) .

## <a name="nods"></a>NŒUDS

NŒUDS indique des formes numériques NOMINALEs (point de code Unicode U + 206F). Le terme spécifie que les chiffres européens (U + 0030 à U + 0039) doivent être rendus normalement, et non pas en tant que chiffres nationaux.

## <a name="overhang"></a>dépassement

Le dépassement est la partie de l’encre d’un glyphe qui s’étend au-delà de la [largeur d’avance](#advance-width) du glyphe. La plupart des glyphes (tels que « H ») n’ont pas de dépassement, car il y a un peu d’espace blanc de part et d’autre pour les séparer des glyphes adjacents. Un exemple de glyphe avec dépassement est le « f » italique utilisé dans cette rubrique pour illustrer la [largeur ABC](#abc-width). Le haut et le bas de l’italique « f » dépassent les glyphes adjacents. Le dépassement correspond à une largeur négative « A » ou « C ».

## <a name="padding"></a>remplissage

Voir sous- [blocage](#underhang).

## <a name="script"></a>script

Un script est un système de langage écrit, par exemple un script latin, un script arabe, un script chinois. Un seul script peut s’appliquer à une ou plusieurs langues humaines. Le script n’a pas de relation particulière avec une police. Par exemple, le script latin peut être rendu de la même façon que la police Times New Roman ou Arial.

## <a name="underhang"></a>blocage

Le sous-blocage est une largeur d’espace blanc à gauche ou à droite de la partie unie d’un glyphe. Le sous-blocage correspond à une largeur positive « A » ou « C », comme décrit pour la [largeur ABC](#abc-width). Le sous-blocage est parfois appelé « remplissage ». L’illustration suivante montre le blocage de la lettre n minuscule.

![Illustration montrant le sous-blocage de la lettre n minuscule.](images/underhang.gif)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 
