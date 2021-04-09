---
description: Les applications peuvent utiliser Unicode pour représenter des chaînes dans plusieurs formulaires.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Utilisation de la normalisation Unicode pour représenter des chaînes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869073"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Utilisation de la normalisation Unicode pour représenter des chaînes

Les applications peuvent utiliser Unicode pour représenter des chaînes dans plusieurs formulaires. Au fur et à mesure de l’augmentation de l’acceptation Unicode, en particulier via Internet, le besoin est venu d’éliminer les différences non essentielles dans les chaînes Unicode. Plusieurs représentations pour une combinaison de caractères compliquent le logiciel, par exemple, lorsqu’un serveur Web répond à une demande de page ou lorsqu’un éditeur de liens recherche un identificateur particulier dans une bibliothèque.

> [!Caution]  
> Différentes chaînes Unicode peuvent sembler identiques visuellement, ce qui soulève des problèmes de sécurité. Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

En réponse à cette exigence, le consortium Unicode a défini un processus appelé « normalisation », qui produit une représentation binaire pour toute représentation binaire équivalente d’un caractère. Une fois normalisé, deux chaînes sont équivalentes si et seulement si elles ont des représentations binaires identiques. La normalisation élimine certaines différences, mais conserve la casse.

Pour utiliser la normalisation Unicode, une application peut appeler les fonctions [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) et [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) pour la réorganisation des chaînes microsoft au format Unicode 4,0 tr \# 15. La normalisation peut contribuer à améliorer la sécurité en réduisant les autres représentations de chaîne qui ont la même signification linguistique. N’oubliez pas, cependant, que la normalisation ne peut pas éliminer entièrement d’autres représentations.

Pour obtenir une description détaillée des normes Unicode pour la normalisation, reportez-vous à la [norme Unicode annexe \# 15 : formulaires de normalisation Unicode](https://www.unicode.org/reports/tr15) (uax \# 15).

> [!Caution]  
> Étant donné que la normalisation peut modifier la forme d’une chaîne, les mécanismes de sécurité ou les algorithmes de validation de caractères doivent généralement être implémentés après la normalisation. Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Fournir plusieurs représentations de la même chaîne

Dans de nombreux cas, Unicode autorise plusieurs représentations de ce qui est, linguistiquement, de la même chaîne. Par exemple :

-   Le capital A avec ditréma (tréma) peut être représenté comme un seul point de code Unicode « Ä » (U + 00C4) ou la combinaison du capital A et du caractère ditréma (« A » + « ̈ », c’est-à-dire U + 0041 U + 0308). Des considérations similaires s’appliquent à de nombreux autres caractères avec des marques diacritiques.
-   Le capital A lui-même peut être représenté de la manière habituelle (lettre majuscule latine A, U + 0041) ou par la lettre majuscule latine A pleine chasse (U + FF21). Des considérations similaires s’appliquent aux autres lettres latines simples (majuscules et minuscules) et aux caractères katakana utilisés lors de l’écriture du japonais.
-   La chaîne « fi » peut être représentée par les caractères « f » et « i » (U + 0066 U + 0069) ou par la ligature « fi » (U + FB01). Des considérations similaires s’appliquent à de nombreuses autres combinaisons de caractères pour lesquelles Unicode définit des ligatures.

## <a name="use-the-four-defined-normalization-forms"></a>Utiliser les quatre formulaires de normalisation définis

Vos applications peuvent effectuer une normalisation Unicode à l’aide de plusieurs algorithmes, appelés « formulaires de normalisation », qui obéissent à différentes règles. Le consortium Unicode a défini quatre formulaires de normalisation : NFC (Form C), NFD (Form D), NFKC (Form KC) et NFKD (Form KD). Chaque formulaire élimine quelques différences, mais conserve la casse. Win32 et le .NET Framework prennent en charge les quatre formulaires de normalisation.

La [**\_ forme**](/windows/desktop/api/Winnls/ne-winnls-norm_form) normale de type énumération nls prend en charge les quatre formulaires standard de normalisation Unicode. Les formulaires C et D fournissent des formes canoniques pour les chaînes. Les formes non canoniques KC et KD offrent une meilleure compatibilité et peuvent révéler certaines équivalences sémantiques qui ne sont pas visibles dans les formulaires C et D. Toutefois, ils le font au détriment d’une certaine perte d’informations et ne doivent généralement pas être utilisés comme un moyen canonique de stocker des chaînes.

Parmi les deux formes canoniques, le formulaire C est un formulaire « composé » et le formulaire D est un formulaire « décomposé ». Par exemple, le formulaire C utilise le point de code Unicode unique « Ä » (U + 00C4), tandis que le format D utilise (« A » + « ̈ », c’est-à-dire U + 0041 U + 0308). Elles s’affichent de la même façon, car « ̈ » (U + 0308) est un caractère d’association. Le formulaire D peut utiliser un nombre quelconque de points de code pour représenter un point de code unique utilisé par le formulaire C.

Si deux chaînes sont identiques au format C ou au format D, elles sont identiques dans l’autre formulaire. En outre, lorsqu’elles sont correctement rendues, elles s’affichent de façon indifférenciée les unes des autres et de la chaîne non normalisée d’origine.

Une fois normalisés, les chaînes ne peuvent pas être retournées de façon cohérente à leur représentation d’origine. Par exemple, si une chaîne avec un mélange de représentations de caractères composés et décomposées est convertie en une forme normalisée, il n’existe aucun moyen de la dénormaliser dans la chaîne mixte d’origine. Par conséquent, si une application requiert la représentation d’origine de la chaîne, elle doit stocker cette représentation explicitement. Toutefois, la conversion entre les deux formes canoniques est réversible. Une chaîne dans le formulaire C peut être convertie au format D, puis revers le formulaire C, et le résultat est identique à la chaîne C du formulaire d’origine.

Les formulaires KC et KD sont similaires aux formulaires C et D, respectivement, mais ces « formulaires de compatibilité » comportent des mappages supplémentaires de caractères compatibles avec la forme de base de chaque caractère. De tels mappages peuvent entraîner la perte de modifications de caractères mineurs. Ils combinent certains caractères qui sont visuellement distincts. Par exemple, ils combinent des caractères à pleine chasse et demi-chasse avec la même signification sémantique, ou différentes formes de la même lettre arabe, ou la ligature « fi » (U + FB01) et la paire de caractères « fi » (U + 0066 U + 0069). Ils combinent également certains caractères qui peuvent parfois avoir une signification sémantique différente, par exemple un chiffre écrit sous la forme d’un exposant, sous la forme d’un indice ou placé dans un cercle. En raison de cette perte d’informations, les formulaires KC et KD ne doivent généralement pas être utilisés comme formes canoniques de chaînes, mais ils sont utiles pour certaines applications.

Le formulaire KC est un formulaire composé et le formulaire KD est un formulaire décomposé. L’application peut basculer entre les formulaires KC et KD, mais il n’existe pas de méthode cohérente pour revenir de la forme KC ou KD à la chaîne d’origine, même si la chaîne d’origine est au format C ou D.

Windows, les applications Microsoft et le .NET Framework génèrent généralement des caractères au format C à l’aide de méthodes d’entrée normales. Pour la plupart des cas sur Windows, le formulaire C est le formulaire par défaut. Par exemple, les caractères du formulaire C sont générés par l’entrée clavier Windows. Toutefois, les caractères importés à partir du Web et d’autres plateformes peuvent introduire d’autres formulaires de normalisation dans le flux de données.

Les exemples suivants sont tirés de UAX \# 15 et illustrent les différences entre les quatre formulaires de normalisation.



<table>
<thead>
<tr class="header">
<th>Original</th>
<th>Formulaire D</th>
<th>Formulaire C</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">La ffi_ligature (U + FB03) n’est pas décomposée, car elle a un mappage de compatibilité, et non un mappage canonique. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;Ä \ uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">Le chiffre romain IV (U + 2163) n’est pas décomposé. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + dix</td>
<td>ga</td>
<td rowspan="5">Les équivalents de compatibilité différents d’un caractère japonais unique n’entraînent pas la même chaîne au format C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + dix</td>
<td>Ka + dix</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka + dix</td>
<td>hw_ka + dix</td>
<td>hw_ka + dix</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>kaks</td>
<td>Les syllabes Hangul sont conservées dans une normalisation.<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Original</th>
<th>Forme KD</th>
<th>Forme KC</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Le ffi_ligature (U + FB03) est décomposé sous forme KC, mais pas dans le formulaire C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">Les chaînes résultantes sont identiques sous la forme KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + dix</td>
<td>ga</td>
<td rowspan="5">Différents équivalents de compatibilité d’un caractère japonais unique génèrent la même chaîne sous la forme KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + dix</td>
<td>Ka + dix</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>Ka + dix</td>
<td>ga</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + dix</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + dix</td>
<td>Ka + dix</td>
<td>ga</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>kaks</td>
<td>Les syllabes Hangul sont conservées dans une normalisation. Dans les versions Unicode antérieures, les caractères Jamos comme KS <sub>f</sub> avaient des mappages de compatibilité à k <sub>f</sub> + s <sub>f</sub>. Ces mappages ont été supprimés dans les 2.1.9 Unicode pour garantir le maintien des syllabes Hangul.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Les deux tableaux ci-dessus ont un copyright de © 1998-2006 Unicode, Inc. Tous droits réservés.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Utiliser des formulaires composés pour des glyphes uniques

De nombreuses séquences de caractères qui correspondent à un seul glyphe n’ont pas de formes composées. Même en cas de normalisation par le formulaire C, un seul élément de texte logique ou de glyphe visuel peut être composé de plusieurs points de code Unicode. Par exemple, plusieurs caractères utilisés pour écrire du lituanien ont des signes diacritiques doubles, car ils ont uniquement des formulaires décomposés. Par exemple, U minuscule avec macron et tilde ("ū̃", U + 016b U + 0303, où le premier point de code est un U minuscule avec macron et le second est un accent aigu de combinaison).

## <a name="example"></a>Exemple

Un exemple pertinent se trouve dans l' [exemple nls : Unicode Normalization](nls--unicode-normalization-sample.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la prise en charge linguistique nationale](using-national-language-support.md)
</dt> <dt>

[Considérations relatives à la sécurité : fonctionnalités internationales](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




