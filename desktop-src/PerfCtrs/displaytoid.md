---
description: La table DisplayToID lie la chaîne conviviale affichée par le moniteur système au GUID stocké dans les autres tables.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519117"
---
# <a name="displaytoid"></a>DisplayToID

La table **DisplayToID** lie la chaîne conviviale affichée par le moniteur système au GUID stocké dans les autres tables.

La table **DisplayToID** définit les champs suivants :

-   **GUID :** Identificateur unique généré pour un journal. Ce champ est la clé primaire de cette table.
-   **RunId :** Réservé à un usage interne.
-   **DisplayString :** Nom du fichier journal tel qu’il s’affiche dans le moniteur système.
-   **LogStartTime :** Heure de début du processus de journalisation au format aaaa-mm-jj hh : mm : SS : nnn.
-   **LogStopTime :** Heure d’arrêt du processus de journalisation au format aaaa-mm-jj hh : mm : SS : nnn. Il est possible de différencier plusieurs fichiers journaux ayant la même valeur **DisplayString** à l’aide de la valeur de ce champ et des champs **LogStartTime** . Les valeurs des champs **LogStartTime** et **LogStopTime** permettent également d’accéder rapidement à la durée totale de collecte.
-   **NumberOfRecords :** Nombre d’échantillons stockés dans la table pour chaque collection de journaux.
-   **MinutesToUTC :** Valeur utilisée pour convertir les données de ligne stockées en heure UTC en heure locale.
-   **TimeZoneName :** Nom du fuseau horaire dans lequel les données ont été collectées. Si vous collectez ou que vous avez reconnecté des données à partir d’un fichier collecté sur des systèmes dans votre propre fuseau horaire, ce champ indique l’emplacement.

**Remarque**  Avant Windows Vista, les ensembles de collecteurs de données étaient stockés dans le registre à l’adresse

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services \\ SysmonLog \\ journaux des requêtes**

. Les champs listés ci-dessus ne correspondent pas aux valeurs du Registre. Pour Windows Vista, les ensembles de collecteurs de données ne sont pas stockés dans le registre.

 

 



