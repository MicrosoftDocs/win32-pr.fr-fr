---
description: Le protocole search-ms ? application est une convention d’interrogation de l’index de recherche Windows.
ms.assetid: e8b18018-c712-4007-bb0a-af90a75780d6
title: Prise en main avec des arguments Parameter-Value
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6e3df2ddb1d0c3f62293d3d3dc2615e855f93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201293"
---
# <a name="getting-started-with-parameter-value-arguments"></a>Prise en main avec des arguments Parameter-Value

La **recherche-MS** ? le [protocole d’application](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) est une convention pour l’interrogation de l’index de recherche Windows. Le protocole permet aux applications, telles que l’Explorateur Windows, d’interroger l’index avec des arguments de valeur de paramètre, notamment des arguments de propriété, des recherches précédemment enregistrées, une syntaxe de requête avancée (AQS), une syntaxe de requête naturelle (NQS) et des identificateurs de code de langue (LCID) pour l’indexeur et la requête elle-même.

Cette rubrique est organisée comme suit :

- [À propos des arguments Parameter-Value](#about-parameter-value-arguments)
- [Exemples](#examples)
- [Rubriques connexes](#related-topics)

## <a name="about-parameter-value-arguments"></a>À propos des arguments Parameter-Value

Le protocole search-ms utilise la syntaxe encodée par URL standard suivante :

```
search-ms:parameter=value[&parameter=value]&
```

La syntaxe commence par identifier le protocole lui-même (search-ms :). Les paires paramètre/valeur sont des arguments passés au moteur de recherche, comme décrit dans le tableau suivant.

| Paramètre                                                    | Valeur                                                         | Description                                                                                                                                                                                                                                                                | Version                  |
|--------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| query                                                        | Texte encodé URL                                              | Texte de la requête entré par l’utilisateur.                                                                                                                                                                                                                                        | Windows XP et versions ultérieures    |
| [InputLocale](-search-3x-wds-qryidx-localeidentifiers.md)   | Tout LCID valide                                                | LCID qui identifie la langue d’entrée de la requête.                                                                                                                                                                                                                 | Windows XP et versions ultérieures    |
| [keywordlocale](-search-3x-wds-qryidx-localeidentifiers.md) | Tout LCID valide                                                | LCID qui identifie la langue de la version internationale de l’indexeur. La valeur par défaut est 1033 (en-US).                                                                                                                                                            | Windows XP et versions ultérieures    |
| [navigation](-search-3x-wds-qryidx-crumb.md)                     | Instruction AQS                                                 | Cet argument restreint l’étendue dans laquelle la recherche est effectuée. Dans Windows Vista et versions ultérieures, search-ms prend en charge la AQS complète, ainsi qu’une implémentation spéciale pour un `location` argument. Dans Windows XP, search-ms prend également en charge la AQS complète, à l’exception d’une implémentation spéciale de `kind` et `store` . | Windows XP et versions ultérieures    |
| [stockéesyntaxe](-search-3x-wds-qryidx-syntaxargument.md)           | NQS, AQS (ne respecte pas la casse)                                 | Syntaxe de requête à utiliser pour effectuer une recherche dans l’index : syntaxe de requête naturelle ou syntaxe de requête avancée (AQS). AQS est la valeur par défaut et est toujours supposé analysé et pris en charge.                                                                                                    | Windows Vista et versions ultérieures |
| [stackedby](-search-3x-wds-qryidx-stackedby.md)             | Toute propriété valide du système de propriétés                   | Propriété qui spécifie la colonne par laquelle piler les résultats.                                                                                                                                                                                                                  | Windows Vista et versions ultérieures |
| [subquery](-search-3x-wds-qryidx-subquery.md)               | Un chemin d’accès complètement spécifié pour un fichier de recherche enregistré ( \* . search-ms) | Les résultats de la sous-requête sont utilisés en tant que source de la requête. Autrement dit, les termes de la requête sont recherchés par rapport aux résultats de la sous-requête.                                                                                                                           | Windows Vista et versions ultérieures |
| displayname                                                  | Chaîne encodée URL                                            | Nom de la recherche actuelle.                                                                                                                                                                                                                                            | Windows Vista et versions ultérieures |


Pour obtenir des informations connexes, consultez [inscription d’une application à un protocole d’URL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)).

## <a name="examples"></a>Exemples

```
search-ms:query=microsoft&
search-ms:query=vacation&subquery=mydepartment.search-ms&
search-ms:query=seattle&crumb=kind:pics&
search-ms:query=seattle&crumb=folder:C:\MyFolder&
```

## <a name="related-topics"></a>Rubriques connexes

[Arguments de l’identificateur de paramètres régionaux](-search-3x-wds-qryidx-localeidentifiers.md)

[Argument de navigation](-search-3x-wds-qryidx-crumb.md)

[Argument de syntaxe](-search-3x-wds-qryidx-syntaxargument.md)

[Argument STACKEDBY](-search-3x-wds-qryidx-stackedby.md)

[Argument de sous-requête](-search-3x-wds-qryidx-subquery.md)
