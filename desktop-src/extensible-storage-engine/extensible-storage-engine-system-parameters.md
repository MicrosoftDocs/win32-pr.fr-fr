---
description: 'En savoir plus sur : paramètres système du moteur de stockage extensible'
title: Paramètres système du moteur de stockage extensible
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527988"
---
# <a name="extensible-storage-engine-system-parameters"></a>Paramètres système du moteur de stockage extensible


_**S’applique à :** Windows | Serveur Windows_

## <a name="extensible-storage-engine-system-parameters"></a>Paramètres système du moteur de stockage extensible

Les constantes suivantes sont utilisées comme valeurs pour le paramètre *paramid* des fonctions [JetGetSystemParameter](./jetgetsystemparameter-function.md) et [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

  - [Paramètres de sauvegarde et de restauration](./backup-and-restore-parameters.md)

  - [Paramètres de rappel](./callback-parameters.md)

  - [Paramètres de base de données](./database-parameters.md)

  - [Paramètres du cache de base de données](./database-cache-parameters.md)

  - [Paramètres de gestion des erreurs](./error-handling-parameters.md)

  - [Paramètres du journal des événements](./event-log-parameters.md)

  - [Paramètres d’e/s](./i-o-parameters.md)

  - [Paramètres d’index](./index-parameters.md)

  - [Paramètres d’information](./informational-parameters.md)

  - [Paramètres méta](./meta-parameters.md)

  - [Paramètres de ressource](./resource-parameters.md)

  - [Paramètres de base de données temporaires](./temporary-database-parameters.md)

  - [Paramètres du journal des transactions](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a>Format de description de paramètre système

Chaque paramètre système est décrit en utilisant le format suivant :

JET_paramX

Description du paramètre système JET_paramX.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Valeur par défaut du paramètre.</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Type de données du paramètre.</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>Valeurs autorisées pour le paramètre.</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Le paramètre est-il global ou par instance ?</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Le paramètre peut-il être défini si des instances existent ?</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Le paramètre peut-il être défini lors de son initialisation ?</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Le paramètre affecte-t-il les fichiers sur le disque ?</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Le paramètre affecte-t-il la fiabilité du moteur ?</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Le paramètre affecte-t-il les performances du moteur ?</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Le paramètre affecte-t-il les ressources du moteur ?</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>Les versions de Windows qui prennent en charge le paramètre.</p></td>
</tr>
</tbody>
</table>
