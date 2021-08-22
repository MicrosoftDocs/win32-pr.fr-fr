---
description: Le système utilise des compteurs pour collecter les données de performances.
ms.assetid: d1f1a90c-425a-4606-b86d-2948305ea84a
title: Spécification d’un chemin d’accès au compteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a359762e4d959992bebd338c4b3ee29825c63b4cb081b70722c82fb3376b5d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143802"
---
# <a name="specifying-a-counter-path"></a>Spécification d’un chemin d’accès au compteur

Le système utilise des compteurs pour collecter les données de performances. Chaque compteur est identifié de manière unique par son nom, son chemin d’accès ou son emplacement. La syntaxe du chemin d’accès aux compteurs est la suivante :

``` syntax
\\Computer\PerfObject(ParentInstance/ObjectInstance#InstanceIndex)\Counter
```

L’élément ordinateur spécifie le nom ou l’adresse IP de l’ordinateur à partir duquel vous souhaitez interroger les données de performances. Le nom de l’ordinateur est facultatif si le compteur se trouve sur l’ordinateur local.

L’élément PerfObject spécifie l’objet de performance à interroger. Un objet de performance peut être un composant physique, tel que des processeurs, des disques et de la mémoire, ou un objet système, tel que des processus et des threads. Chaque objet système est lié à un élément fonctionnel au sein de l’ordinateur et est associé à un ensemble de compteurs standard. Chaque ordinateur peut avoir un ensemble différent d’objets de performance et de compteurs installés sur celui-ci, car les applications peuvent installer leurs propres objets et compteurs de performances. Pour obtenir la liste des objets et compteurs de performance installés sur votre ordinateur, consultez la boîte de dialogue **Ajouter des compteurs** dans l’outil performances de votre ordinateur. Ces objets sont également répertoriés dans la boîte de dialogue de navigation PDH (voir [compteurs de navigation](browsing-counters.md)). Pour obtenir la liste des compteurs et des objets de performance système, consultez [compteurs par objet](/previous-versions/windows/it-pro/windows-server-2003/cc783073(v=ws.10)).

ParentInstance, ObjectInstance et InstanceIndex sont inclus dans le chemin d’accès si plusieurs instances de l’objet peuvent exister. Par exemple, les processus et les threads sont des objets d’instance multiples, car plusieurs processus ou threads peuvent s’exécuter en même temps. Si un objet peut avoir plusieurs instances, le chemin d’accès au compteur doit spécifier une instance d’objet.

Le format des éléments liés à l’instance dépend du type d’objet. Si l’objet a des instances simples, le format est uniquement le nom de l’instance entre parenthèses. Par exemple :

``` syntax
(Explorer)
```

Si l’instance de cet objet requiert également un nom d’instance parente, le nom de l’instance parente doit précéder l’instance de l’objet et être séparé par un caractère de barre oblique. Par exemple, les threads appartiennent à des processus. Si vous interrogez un objet thread, vous devez également spécifier le processus auquel il appartient, comme indiqué dans l’exemple suivant :

``` syntax
(Explorer/0)
```

Si l’objet a plusieurs instances qui ont la même chaîne de nom, elles peuvent être indexées séquentiellement en spécifiant l’index d’instance préfixé par un signe dièse. Les index d’instance sont de base 0. Si vous souhaitez interroger la première instance, n’incluez pas \# 0. spécifiez simplement le nom de l’instance. Pour spécifier la deuxième instance, utilisez \# 1 ; pour spécifier la troisième instance, utilisez \# 2, et ainsi de suite. Par exemple :

``` syntax
(Explorer/0#1)
```

L’élément Counter spécifie le compteur de performance que vous souhaitez interroger pour l’objet de performance donné.

PDH utilise les caractères spéciaux suivants dans un chemin d’accès de compteur. Les fournisseurs ne doivent pas utiliser ces caractères dans leurs noms. Si un fournisseur utilise ces caractères spéciaux, PDH ne peut pas analyser le chemin d’accès complet au compteur pour obtenir les noms des compteurs et des instances.



| Caractère | Description                                                |
|-----------|------------------------------------------------------------|
| \\        | Séparateur générique pour l’ordinateur, l’objet et le compteur.       |
| (         | Début du nom de l’instance.                                |
| )         | Fin du nom de l’instance.                                   |
| /         | Sépare l’instance et l’instance parente.                    |
| \#n       | Identifie une occurrence spécifique d’une instance de même nom. |
| \*        | Caractère générique.                                        |



 

Les exemples suivants illustrent les formats possibles pour les chemins de compteur :

-   \\\\\\compteur objet ordinateur (index parent/instance \# ) \\
-   \\\\\\compteur objet ordinateur (parent/instance) \\
-   \\\\\\compteur de l’objet ordinateur (index d’instance \# ) \\
-   \\\\\\compteur de l’objet ordinateur (instance) \\
-   \\\\\\compteur d’objets ordinateur \\
-   \\compteur de l’objet (index parent/instance \# ) \\
-   \\compteur de l’objet (parent/instance) \\
-   \\compteur de l’objet (index d’instance \# ) \\
-   \\compteur de l’objet (instance) \\
-   \\compteur d’objets \\

## <a name="using-wildcard-characters"></a>Utilisation de caractères génériques

Les chemins d’accès des compteurs peuvent contenir un caractère générique uniquement pour le nom de l’instance, comme indiqué dans l’exemple suivant.

``` syntax
\Process(*)\% Processor Time
```

Pour développer le caractère générique dans une liste de chemins de compteurs qui contiennent des instances trouvées sur l’ordinateur ou dans le fichier journal, appelez [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha).

 

 
