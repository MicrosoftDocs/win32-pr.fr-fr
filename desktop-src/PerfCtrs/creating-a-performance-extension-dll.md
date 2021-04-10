---
description: Un fournisseur est une DLL de performance qui fournit des données de compteur aux consommateurs.
ms.assetid: bbb777fe-b97e-4777-b797-ec8525065610
title: Création d’une DLL d’extension de performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d397f1581454aca1b25c447b35f250eefd215f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865125"
---
# <a name="creating-a-performance-extension-dll"></a>Création d’une DLL d’extension de performance

> [!IMPORTANT]
> En raison des limitations de performances et de fiabilité significatives, la méthode permettant de fournir des données de compteurs de performances que cette rubrique décrit peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md) pour la création de nouveaux compteurs de performances et la migration des compteurs de performances existants afin d’utiliser également cette méthode.

Un [fournisseur v1](providing-counter-data.md) utilise une dll de performance qui fournit des données de compteur aux consommateurs. La DLL de performance doit exporter les fonctions [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)), [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc)et [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) . En général, vous utilisez un fichier de définition de module (. def) pour exporter les fonctions à partir de la DLL. Le système appelle ces fonctions lorsqu’un consommateur interroge des données de performances.

La première fois qu’un consommateur appelle [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa), ou si le consommateur utilise la fonction [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) ou [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistrya) pour ouvrir `HKEY_PERFORMANCE_DATA` , le système appelle la fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) pour chaque fournisseur [inscrit](adding-performance-counters.md) sur l’ordinateur. L’exception est si le fournisseur spécifie la liste d’objets qu’il prend en charge dans la `[objects]` section de. Fichier INI. Dans ce cas, le système appelle le fournisseur uniquement si l’un des objets interrogés correspond à un objet de la liste.

La fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) donne à chaque fournisseur la possibilité d’initialiser ses structures de données de performances. Ensuite, si la fonction **OpenPerformanceData** retourne avec succès, le système appelle la fonction [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) du fournisseur. Les appels suivants à [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) provoquent l’appel de la fonction **CollectPerformanceData** par le système.

Lorsque le consommateur termine la collecte des données de performances, il spécifie `HKEY_PERFORMANCE_DATA` dans un appel à la fonction [**échec RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) . Cela amène le système à appeler la fonction [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) pour chaque fournisseur. Les fournisseurs sont ensuite déchargés.

Plusieurs consommateurs peuvent collecter des données de performances en même temps. Le système appelle les fonctions [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) et [**ClosePerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_close_proc) une seule fois chaque fois que la dll est chargée ou déchargée.

> [!Note]
> Veillez à inclure extern "C" dans votre code C++ pour empêcher le compilateur d’ajouter des décorations à vos noms de fonction. dans le cas contraire, le système risque de ne pas trouver vos fonctions.

> [!Note]
> Si une erreur se produit lors du chargement de votre DLL de performance, de la recherche de vos fonctions ou de l’appel de vos fonctions, le système désactive le fournisseur pour les collections suivantes au sein du même processus. En outre, si cela se produit lors de l’exécution dans un processus privilégié, le système ajoute une valeur de **désactivation des compteurs de performances** à votre clé de **performance** pour empêcher le fournisseur d’être chargé à l’avenir.

Pour plus d’informations sur l’écriture d’une DLL de performance, consultez les rubriques suivantes :

- [Implémentation de la fonction OpenPerformanceData](implementing-openperformancedata.md)
- [Implémentation de la fonction CollectPerformanceData](implementing-collectperformancedata.md)
- [Gestion des erreurs dans la DLL](error-handling-in-the-dll.md)
- [Restriction de l’accès aux DLL d’extension de performance](restricting-access-to-performance-extension--dlls.md)
- [Exemples de DLL de performance](performance-dll-samples.md)
