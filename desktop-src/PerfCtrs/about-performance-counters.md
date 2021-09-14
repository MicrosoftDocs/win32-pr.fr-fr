---
description: Les compteurs sont utilisés pour fournir des informations sur le fonctionnement du système d’exploitation ou d’une application, d’un service ou d’un pilote.
ms.assetid: d172a131-61d3-4fc1-8e0c-b07b2bd34f80
title: À propos des compteurs de performance
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dec7c71e99ab614ee64e3d1e8c9620f0be78c14a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119117"
---
# <a name="about-performance-counters"></a>À propos des compteurs de performance

Windows Les compteurs de performances fournissent une couche d’abstraction de haut niveau avec une interface cohérente pour la collecte de différents types de données système telles que les statistiques d’utilisation du processeur, de la mémoire et du disque. Les administrateurs système utilisent des compteurs de performances pour surveiller les problèmes de performances ou de comportement. Les développeurs de logiciels utilisent des compteurs de performances pour inspecter l’utilisation des ressources de leurs composants.

> [!IMPORTANT]
> Windows Les compteurs de performances sont optimisés pour la découverte et la collecte des données d’administration/de diagnostic. Ils ne sont pas appropriés pour la collecte de données à haute fréquence ou pour le profilage d’application, car ils ne sont pas conçus pour être collectés plusieurs fois par seconde. Pour un accès plus faible aux informations système, vous pouvez préférer des API plus directes, telles que [**Process Status Helper**](../psapi/process-status-helper.md), [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex), [**GetSystemTimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getsystemtimes)ou [**fonction getprocesstimes**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesstimes). Pour le profilage, vous pouvez collecter des journaux ETW avec les données de profilage système à l’aide de [**tracelog.exe**](/windows-hardware/drivers/devtest/tracelog) avec des `-critsec` options, `-dpcisr` , `-eflag` ou `-ProfileSource` , ou vous pouvez utiliser le [**profilage des compteurs matériels**](/previous-versions/windows/desktop/hcp/hcp-reference).

> [!NOTE]
> ne confondez pas Windows compteurs de performances avec l’API [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) . Windows Les compteurs de performances fournissent une abstraction de haut niveau pour de nombreux types d’informations système. La fonction QueryPerformanceCounter fournit un accès optimisé à un horodatage haute précision.

## <a name="getting-started"></a>Mise en route

- Utilisez les [outils de compteur de performance](performance-counters-tools.md) lorsque vous souhaitez collecter ou afficher les données de performances d’un système.
- Utilisez les [API de collection de compteurs de performance](consuming-counter-data.md) lorsque vous souhaitez écrire un script ou un programme qui collecte les données de performances à partir du système local.
- Utilisez les [classes de compteur de performances WMI](/windows/desktop/WmiSdk/monitoring-performance-data) lorsque vous souhaitez collecter des données de performances à partir d’un système local ou distant à l’aide de WMI.
- Utilisez les [API du fournisseur de compteurs de performance](providing-counter-data.md) lorsque vous souhaitez publier des données de performances à partir de votre composant logiciel.

## <a name="concepts"></a>Concepts

le système de compteurs de performances Windows est organisé en **consommateurs**, **fournisseurs**, **countersets**, **compteurs**, **instances** et **valeurs de compteur**.

Un **consommateur** est un composant logiciel qui utilise des données de performances. Windows comprend plusieurs [outils intégrés](performance-counters-tools.md) qui utilisent des données de performances. Il s’agit notamment du gestionnaire des tâches, du moniteur de ressource, de l’analyseur de performances, d' typeperf.exe, logman.exe et relog.exe. Les développeurs peuvent écrire des scripts et des applications qui accèdent aux compteurs de performances via des [API de compteur de performances](consuming-counter-data.md).

Un **fournisseur** est un composant logiciel qui [génère et publie des données de performances](providing-counter-data.md). Un fournisseur publiera des données pour un ou plusieurs *countersets*. Par exemple, un système de base de données peut s’inscrire lui-même en tant que fournisseur de données de performances.

- Un **fournisseur v1** est un composant logiciel qui publie des données de performances à l’aide d’une [dll de performance](providing-counter-data-using-a-performance-dll.md) qui s’exécute dans le processus du consommateur. Un fournisseur v1 est installé sur un système par le biais d’un `.ini` fichier. L’architecture du fournisseur v1 est déconseillée. Les nouveaux fournisseurs doivent utiliser l’architecture du fournisseur v2.
- Un **fournisseur v2** est un composant logiciel qui publie les données de performances via les [API du fournisseur de compteurs de performance](providing-counter-data-using-version-2-0.md). Un fournisseur v2 est installé sur un système via un `.man` fichier (manifeste XML).

Un **CounterSet** est un regroupement de données de performances au sein d’un fournisseur. Un CounterSet a un nom et un ou plusieurs *compteurs*. La collecte des données à partir d’un CounterSet retourne un certain nombre d' *instances*. dans certaines api Windows, les countersets sont appelés **objets de performance**. Par exemple, un fournisseur de données de performances pour un système de base de données peut fournir un CounterSet pour les statistiques par base de données.

Un **compteur** est la définition d’un élément de données de performances unique. Un compteur a un nom et un type. Par exemple, un CounterSet « statistiques par base de données » peut contenir un compteur nommé « transactions par seconde » avec le type `PERF_COUNTER_COUNTER` .

Une **instance** est une entité sur laquelle les données de performance sont signalées. Une instance a un nom (chaîne) et une ou plusieurs *valeurs de compteur*. Par exemple, un CounterSet « statistiques par base de données » peut contenir une instance par base de données. Le nom de l’instance est le nom de la base de données, et chaque instance contient des valeurs de compteur pour les compteurs « transactions par seconde », « utilisation de la mémoire » et « utilisation du disque ».

Une **valeur de compteur** est la valeur d’un seul élément de données de compteur de performance. Une valeur de compteur est un entier non signé, 32 bits ou 64 bits selon le type du compteur correspondant. Lorsque vous parlez d’une *instance*, une *valeur de compteur* peut parfois être appelée un *compteur* ou une *valeur*.

> [!TIP]
> Il peut être utile de mettre en relation les termes du compteur de performance avec des termes de feuille de calcul plus familiers. Un **CounterSet** est semblable à une table. Un **compteur** est semblable à une colonne. Une **instance** est comme une ligne. Une **valeur de compteur** est semblable à une cellule dans la table.

Les **countersets à instance unique** contiennent toujours des données pour une seule instance. Cela est courant pour les countersets qui signalent des statistiques système-globales. par exemple, Windows a un counterset intégré à instance unique nommé « Memory » qui rend compte de l’utilisation de la mémoire globale.

Les **Countersets multi-instances** contiennent des données pour un nombre variable d’instances. Cela est courant pour les countersets qui signalent des entités dans le système. par exemple, Windows dispose d’un counterset intégré à plusieurs instances nommé « informations sur le processeur » qui signale une instance pour chaque uc installée.

Les consommateurs recueillent et enregistrent périodiquement les données du CounterSet d’un fournisseur. Par exemple, le consommateur peut collecter des données une fois par seconde ou une fois par minute. Les données collectées sont appelées **exemples**. Un exemple se compose d’horodatages et de données pour les instances du CounterSet. Les données de chaque instance incluent le nom de l’instance (chaîne) et un ensemble de valeurs de compteur (entiers, une valeur pour chaque compteur dans le CounterSet).

Les noms d’instance doivent normalement être uniques dans un exemple, c’est-à-dire qu’un fournisseur ne doit pas retourner deux instances du même nom dans le cadre d’un seul échantillon. Certains fournisseurs plus anciens ne respectant pas cette règle, les [consommateurs doivent être en mesure de tolérer des noms d’instance non uniques](handling-duplicate-instance-names.md). Comme les noms d’instance ne respectent pas la casse, les instances ne doivent pas avoir de noms qui diffèrent uniquement par la casse.

> [!NOTE]
> Pour des raisons de compatibilité descendante, le CounterSet « Process » retourne des noms d’instance non uniques en fonction du nom de fichier EXE. Cela peut entraîner des résultats confus, en particulier lorsqu’un processus avec un nom non unique démarre ou s’arrête, car cela entraîne généralement des problèmes de données en raison d’une correspondance incorrecte des noms d’instance entre les exemples. Les consommateurs du CounterSet « process » doivent pouvoir tolérer ces noms d’instance non uniques et les problèmes de données résultants.

Les noms d’instance doivent être stables entre les exemples, c’est-à-dire qu’un fournisseur doit utiliser le même nom d’instance pour la même entité chaque fois que le CounterSet est collecté.

Chaque compteur a un type. Le type de compteur indique le type de la **valeur brute** du compteur (entier non signé 32 bits ou entier 64 bits non signé). Le type de compteur indique également ce que représente la valeur brute du compteur, qui détermine comment la valeur brute doit être traitée pour générer des statistiques utiles.

Alors que certains types de compteurs sont simples et ont une valeur brute qui est directement utile, de nombreux types de compteurs nécessitent un [traitement supplémentaire](calculating-counter-values.md) pour créer une **valeur mise en forme** utile. Pour produire la valeur mise en forme, certains types de compteurs requièrent des valeurs brutes de deux exemples, certains types de compteurs requièrent des horodateurs, et certains types de compteurs requièrent des valeurs brutes de plusieurs compteurs. Par exemple :

- `PERF_COUNTER_LARGE_RAWCOUNT` est une valeur brute de 64 bits qui ne nécessite aucun traitement. Il convient pour les valeurs à un point dans le temps, telles que « octets de mémoire en cours d’utilisation ».
- `PERF_COUNTER_RAWCOUNT_HEX` est une valeur brute de 32 bits qui requiert uniquement une mise en forme hexadécimale simple. Il convient à un point dans le temps ou à des informations d’identification telles que « Flags » ou « adresse de base ».
- `PERF_COUNTER_BULK_COUNT` est une valeur brute de 64 bits qui indique le nombre d’événements et est utilisée pour calculer la vitesse à laquelle les événements se produisent. Pour être utile, ce type de compteur requiert deux exemples qui sont séparés dans le temps. La valeur mise en forme est le taux d’événements, c’est-à-dire le nombre de fois où l’événement s’est produit par seconde sur l’intervalle entre les deux échantillons. À partir de deux exemples `s0` et `s1` , la valeur mise en forme (taux d’événements) est calculée sous la forme `(s1.EventCount - s0.EventCount)/(s1.TimestampInSeconds - s0.TimestampInSeconds)` .

Les fournisseurs doivent se comporter comme s’ils étaient sans État. par exemple, la collecte de données à partir d’un CounterSet ne doit pas affecter l’état du fournisseur. Par exemple, un fournisseur ne doit pas réinitialiser les valeurs de compteur à 0 lorsqu’un CounterSet est collecté et qu’il ne doit pas utiliser l’horodateur d’une collection précédente pour ajuster les valeurs de la collection actuelle. Au lieu de cela, il doit fournir des valeurs de compteur brutes simples avec des types exacts afin que le consommateur puisse calculer des statistiques utiles en fonction des valeurs brutes et de leurs horodateurs.

## <a name="performance-api-architecture"></a>Architecture de l’API de performances

![les applications de compteur de Performance appellent des api Windows qui appellent des fournisseurs pour obtenir des données de performances.](images/architecture.png)

Les consommateurs des compteurs de performances sont les suivants :

- [Applications fournies par Microsoft](performance-counters-tools.md) , telles que le gestionnaire des tâches, les moniteur de ressource, l’analyseur de performances et les typeperf.exe.
- Surfaces d’API de haut niveau fournies par Microsoft qui exposent des données de compteurs de performances telles que les [classes de performance WMI](/windows/desktop/WmiSdk/monitoring-performance-data).
- Vos propres applications ou scripts qui utilisent des [API de consommateur de compteur de performance](consuming-counter-data.md).

La plupart des consommateurs de compteurs de performances utilisent des API de [PDH.dll](using-the-pdh-functions-to-consume-counter-data.md) pour collecter des données de performances. PDH gère de nombreux aspects complexes de la collecte des compteurs de performances, tels que l’analyse des requêtes, la mise en correspondance des instances sur plusieurs échantillons et le calcul des valeurs mises en forme à partir des données de compteur brutes. L’implémentation PDH utilise les API du registre lors de l’utilisation des données d’un fournisseur v1 et utilise les API de consommateur v2 lors de l’utilisation de données à partir d’un fournisseur v2.

Certains anciens consommateurs de compteurs de performances utilisent les [API du Registre](using-the-registry-functions-to-consume-counter-data.md) pour collecter les données de performances à partir de la `HKEY_PERFORMANCE_DATA` clé de Registre spéciale. Cela n’est pas recommandé pour le nouveau code, car le traitement des données à partir du Registre est complexe et sujet aux erreurs. L’implémentation de l’API du Registre prend directement en charge la collecte de données à partir des fournisseurs v1. Il prend indirectement en charge la collecte de données à partir de fournisseurs v2 via une couche de traduction qui utilise les API de consommateur v2.

Certains consommateurs de compteur de performance utilisent les [fonctions de consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md) pour accéder directement aux données à partir de fournisseurs v2. Cela est plus complexe que l’utilisation de données à l’aide des API PDH, mais cette approche peut être utile si les API PDH ne peuvent pas être utilisées en raison de problèmes de performances ou de dépendance. L’implémentation de PerfLib v2 prend directement en charge la collecte de données à partir de fournisseurs v2. Elle ne prend pas en charge la collecte de données à partir de fournisseurs v1.

> [!NOTE]
> Windows OneCore n’inclut pas PDH.dll et n’inclut pas la prise en charge de l’utilisation des données des compteurs de performances via les api du registre. les consommateurs qui s’exécutent sur OneCore doivent utiliser les fonctions de consommateur de PerfLib V2.

Les fournisseurs v1 sont implémentés en tant que DLL de fournisseur chargé dans le processus consommateur. L’implémentation de l’API du Registre gère le chargement de la DLL du fournisseur, l’appel de la DLL pour collecter les données de performances et le déchargement de la DLL, le cas échéant. la DLL du fournisseur est responsable de la [collecte des données de performances selon les besoins](communicating-with-your-application.md), par exemple en utilisant les api de Windows normales, RPC, les canaux nommés, la mémoire partagée ou d’autres mécanismes de communication entre processus.

les fournisseurs V2 sont implémentés sous la forme d’un programme en mode utilisateur (souvent un service Windows) ou d’un pilote en mode noyau. En général, le code du fournisseur de données de performances est intégré directement dans un composant existant (par exemple, le pilote ou le service signale des statistiques sur lui-même). L’implémentation de PerfLib v2 gère les demandes et les réponses via l’extension du noyau PCW.sys, de sorte que le fournisseur n’a généralement pas besoin d’implémenter de communication interprocessus pour fournir les données de performances.

> [!NOTE]
> Windows Les API et les outils du compteur de performances incluent une prise en charge limitée de l’accès aux compteurs de performances à partir d’autres ordinateurs via le Registre distant (pour les fournisseurs v1) et RPC (pour les fournisseurs v2). Cette prise en charge est souvent difficile à utiliser en termes de contrôles d’authentification (les outils et les API peuvent uniquement s’authentifier en tant qu’utilisateur actuel), ainsi qu’en termes de [configuration du système](accessing-remote-counter-data.md) (les points de terminaison et les services nécessaires sont désactivés par défaut). Dans de nombreux cas, il est préférable d’accéder aux compteurs de performance des systèmes distants via [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) plutôt qu’à l’aide de la prise en charge intégrée de l’accès à distance.

## <a name="developer-audience"></a>Développeurs concernés

Les compteurs de performances sont souvent utilisés par les administrateurs pour identifier les problèmes de performances ou le comportement anormal des systèmes, par les développeurs pour étudier l’utilisation des ressources des composants logiciels et par les utilisateurs individuels pour comprendre comment les programmes se comportent sur leur système. L’utilisation peut se faire via des outils d’interface utilisateur graphique tels que le gestionnaire des tâches ou l’analyseur de performances, des outils en ligne de commande comme typeperf.exe ou logman.exe, via des scripts via WMI et PowerShell, ou via des API C/C++ et .NET.

Les fournisseurs de compteurs de performances sont généralement implémentés en tant que pilotes en mode noyau ou services en mode utilisateur. Les fournisseurs de compteurs de performances sont généralement écrits en C ou C++.

## <a name="run-time-requirements"></a>Conditions d’exécution

Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.

Pour plus d’informations sur l’historique des versions, consultez [Nouveautés](performance-counters-what-s-new.md).

## <a name="see-also"></a>Voir aussi

[Using Performance Counters](using-performance-counters.md)

[Référence des compteurs de performance](performance-counters-reference.md)
