---
description: Vous pouvez utiliser les fonctions de Registre pour collecter les données de performances.
ms.assetid: feac7b8d-1dee-462c-89dc-bec1ba045da2
title: Utilisation des fonctions de Registre pour consommer des données de compteur
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ce2a4ba9992510cb296b037cfd98965410c48939
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519704"
---
# <a name="using-the-registry-functions-to-consume-counter-data"></a>Utilisation des fonctions de Registre pour consommer des données de compteur

Utilisez les [fonctions de Registre](/windows/desktop/SysInfo/registry-functions) pour collecter les données de performances à partir de la `HKEY_PERFORMANCE_DATA` clé de Registre spéciale.

Les données de performances ne sont pas réellement stockées dans le registre. L’appel des fonctions de Registre provoque la collecte des données par le système à partir du fournisseur de données de performances approprié.

> [!Note]
> Normalement, vous ne devez pas utiliser les fonctions de Registre pour consommer des données de compteur. Au lieu de cela, vous devez [utiliser les fonctions d’assistance des données de performance (PDH)](using-the-pdh-functions-to-consume-counter-data.md). Les fonctions PDH sont plus faciles à utiliser et évitent de nombreux problèmes de performances et de fiabilité qui peuvent se produire par le biais d’une utilisation incorrecte des fonctions de registre.

> [!Note]
> Vous ne pouvez pas utiliser les fonctions de Registre si vous écrivez des applications Windows OneCore. Utilisez plutôt des [fonctions de consommateur de Perflib v2](using-the-perflib-functions-to-consume-counter-data.md).

Les fonctions de Registre sont l’API de bas niveau pour la collecte de données à partir de **fournisseurs v1**. Les fonctions de Registre prennent également en charge la collecte de données à partir de **fournisseurs v2** via une couche de traduction qui appelle les [fonctions de consommateur v2](using-the-perflib-functions-to-consume-counter-data.md).

Pour obtenir les données de performances du système local, appelez la fonction [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexw) . Utilisez `HKEY_PERFORMANCE_DATA` comme clé. Le premier appel ouvre la clé. Vous n’avez pas besoin d’ouvrir explicitement la clé.

Pour obtenir des données de performances à partir d’un système distant, appelez la fonction [**RegConnectRegistry**](/windows/desktop/api/winreg/nf-winreg-regconnectregistryw) . Utilisez le nom d’ordinateur du système distant et utilisez-le `HKEY_PERFORMANCE_DATA` comme clé. Cet appel récupère une clé représentant les données de performances du système distant. Utilisez cette clé plutôt que `HKEY_PERFORMANCE_DATA` la clé pour récupérer les données.

Veillez à utiliser la fonction [**échec RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey) pour fermer le descripteur de la clé lorsque vous avez fini d’obtenir les données de performances. Cela est important pour les cas locaux et distants :

- `RegCloseKey(HKEY_PERFORMANCE_DATA)` ne ferme pas réellement un handle de Registre, mais efface toutes les données mises en cache et libère les dll de performance chargées.
- `RegCloseKey(hkeyRemotePerformanceData)` ferme le descripteur du registre de l’ordinateur distant.

> [!IMPORTANT]
> N’appelez pas `RegCloseKey(HKEY_PERFORMANCE_DATA)` pendant `DLL_PROCESS_DETACH` .

Vous utilisez le `lpValueName` paramètre de la fonction [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) pour indiquer les informations à récupérer. Le tableau suivant répertorie les valeurs que vous pouvez spécifier pour `lpValueName` . Notez que les chaînes de valeur ne respectent pas la casse.

|Valeur|Description
|-----|-----------
|`Global`| Récupère les données de performances de tous les objets de performance inscrits sur l’ordinateur, à l’exception de ceux inclus dans la `Costly` catégorie.
|`OLD_Global`| **Windows Vista et versions ultérieures :** Récupère les données de performances de tous les objets de performance **v1** inscrits sur l’ordinateur, à l’exception de ceux inclus dans la `Costly` catégorie. Utilisez-le à la place de `Global` pour éviter de collecter des données de fournisseur v2 inutiles Lorsque vous savez que les données d’intérêt proviennent d’un fournisseur v1.
|`n1 n2 ...`| Récupère des données de performances pour un ou plusieurs objets de performance. Spécifiez l’index décimal associé à chaque objet que vous souhaitez récupérer dans une liste séparée par des espaces. Par exemple, si vous souhaitez récupérer des objets système et de mémoire et que vous avez déterminé que les index des chaînes de nom correspondantes sont 2 et 4, spécifiez la chaîne `"2 4"` . Notez que la requête peut retourner un nombre différent d’objets que celui que vous avez demandé. Cela peut se produire si l’objet spécifié n’est pas disponible, si l’objet spécifié dépend d’un autre type d’objet ou si un fournisseur retourne des données qui n’ont pas été demandées directement. Par exemple, les threads dépendent des processus. par conséquent, si vous demandez des données à partir de l' `Thread` objet, les résultats incluront les données de l' `Process` objet.
|`Counter n`| Récupère les chaînes de nom pour l’identificateur de langue spécifié, par exemple l’anglais pour `Counter 9` . Utilisez les chaînes de nom retournées pour Rechercher l’index correspondant à un nom donné ou pour rechercher le nom correspondant à un index donné. Pour plus d’informations [, consultez récupération des noms de compteur et du texte d’aide](retrieving-counter-names-and-help-text.md) . Notez que la liste retournée inclut à la fois des noms d’objet (CounterSet) et des noms de compteurs. il n’existe aucun moyen simple de déterminer si un nom est un nom d’objet ou un nom de compteur.
|`Help n`| Récupère les chaînes d’aide pour l’identificateur de langue spécifié, par exemple l’anglais pour `Help 9` . Utilisez les chaînes d’aide retournées pour rechercher les descriptions correspondant aux index de l’objet (CounterSet) ou de l’aide du compteur. Pour plus d’informations [, consultez récupération des noms de compteur et du texte d’aide](retrieving-counter-names-and-help-text.md) .
|`Costly`| **Déconseillé :** Récupère des données de performances pour les types d’objets dont les données sont coûteuses à collecter en termes de temps processeur ou d’utilisation de la mémoire. Cette collecte peut prendre plusieurs minutes sur un ordinateur lourdement chargé. Vous devez effectuer la collecte sur un thread de travail si votre application doit répondre à l’utilisateur pendant la collecte de données.

Pour plus d’informations sur le format des données de performance retournées par le registre, consultez [format des données de performances](performance-data-format.md).

Pour obtenir un exemple qui récupère les noms et les descriptions des compteurs inscrits sur l’ordinateur, consultez [extraction des noms de compteur et du texte d’aide](retrieving-counter-names-and-help-text.md).

Pour obtenir un exemple qui accède aux composants des données de performances, consultez [affichage des noms d’objet, d’instance et de compteur](displaying-object-instance-and-counter-names.md).

Pour obtenir un exemple qui récupère, calcule et imprime des valeurs de compteur, consultez [récupération des données de compteur](retrieving-counter-data.md) et calcul des valeurs de [compteur](calculating-counter-values.md).
