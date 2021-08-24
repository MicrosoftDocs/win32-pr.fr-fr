---
description: un nom de paramètres régionaux est basé sur les conventions de balisage de langue de RFC 4646 (Windows Vista et versions ultérieures) et est représenté par les paramètres régionaux \_ SNAME.
ms.assetid: 221aae7b-3a7c-4995-ae78-50d97de436d8
title: Noms de paramètres régionaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed4c09900544e96c0f05166d1f4054972e9d8ff89fc108c185695a7506859bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147401"
---
# <a name="locale-names"></a>Noms de paramètres régionaux

un nom de [paramètres régionaux](locales-and-languages.md) est basé sur les conventions de balisage de langue de RFC 4646 (Windows Vista et versions ultérieures) et est représenté par les [paramètres régionaux \_ SNAME](locale-sname.md). En règle générale, le modèle `<language>-<REGION>` est utilisé. Ici, Language est un code de langue ISO 639 en minuscules. Les codes de la norme ISO 639-1 sont utilisés lorsqu’ils sont disponibles. Dans le cas contraire, les codes de ISO 639-2/T sont utilisés. REGION spécifie un identificateur de pays/région ISO 3166-1 en majuscules. Par exemple, le nom des paramètres régionaux pour l’anglais (États-Unis) est « en-US » et le nom des paramètres régionaux pour maldivien (Maldives) est « DV-MV ».

> [!Note]  
> La [longueur maximale du \_ nom \_ \_ de paramètres régionaux](locale-name-constants.md) donne la longueur maximale d’un nom de paramètres régionaux. Il comprend de l’espace pour un caractère null de fin.

 

Si les paramètres régionaux sont des paramètres régionaux neutres (sans région), la valeur [locale \_ sName](locale-sname.md) suit le modèle `<language>` . S’il s’agit d’un paramètre régional neutre pour lequel le script est significatif, le modèle est `<language>-<Script>` .

Si les paramètres régionaux doivent être distingués des autres paramètres régionaux de la même langue et de la même région à l’aide d’un autre script, la \_ valeur locale sName suit le modèle `<language>-<Script>-<REGION>` , où script est un code de script [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html) en majuscules. Par exemple, la valeur locale \_ sName pour les paramètres régionaux ouzbek (latin, Ouzbékistan) est « uz-LATN-uz ». Le composant script n’est pas inclus dans les cas où un langage est couramment écrit dans un seul script.

Les ordres de tri pour les paramètres régionaux sont désignés à l’aide d' [identificateurs d’ordre de tri](sort-order-identifiers.md), par exemple, trier \_ par défaut. Pour distinguer au moins deux ordres de tri pour la même langue et la même région, le nom des paramètres régionaux suit le modèle `<language>-<REGION>\_<sort order>` . Si vous devez faire la distinction entre le script et l’ordre de tri, le nom suit le modèle `<language>-<Script>-<REGION>\_<sort order>` . L’ordre de tri par défaut n’est jamais spécifié explicitement, mais uniquement l’ordre de tri alternatif. Par exemple, hongrois (Hongrie) avec \_ les valeurs par défaut de tri ou la valeur par défaut de tri équivalent numérique ( \_ hongrois) \_ est désigné « HU-HU ». La technique hongroise (Hongrie) avec tri d’ordre de tri \_ hongrois \_ Technical est désignée par « HU-HU \_ technl ».

Pour les [paramètres régionaux de remplacement](custom-locales.md), le nom des paramètres régionaux doit être identique au nom des paramètres régionaux remplacés. Pour les paramètres régionaux supplémentaires, le nom des paramètres régionaux doit suivre le modèle `<language>-<REGION>-x-<custom>` ou `<language>-<Script>-<REGION>-x-<custom>` , où `<custom>` est une chaîne alphanumérique spécifique aux paramètres régionaux supplémentaires. Par exemple, les paramètres régionaux supplémentaires spécifiques à une société appelée fabricam peuvent être appelés « en-US-x-fabricam ».

Une application peut récupérer les noms de paramètres régionaux actuels à l’aide des fonctions [**GetSystemDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlocalename) et [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename) . Tandis que chaque thread peut récupérer et définir son propre identificateur de paramètres régionaux avec [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale) et le définir avec [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale), il n’existe pas de fonctions analogues pour obtenir et définir des paramètres régionaux par nom.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres régionaux et langues](locales-and-languages.md)
</dt> <dt>

[Paramètres régionaux personnalisés](custom-locales.md)
</dt> <dt>

[Identificateurs de paramètres régionaux](locale-identifiers.md)
</dt> <dt>

[Identificateurs d’ordre de tri](sort-order-identifiers.md)
</dt> </dl>

 

 



