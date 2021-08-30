---
description: 'en savoir plus sur : paramètres système du moteur de Stockage Extensible'
title: paramètres système du moteur de Stockage Extensible
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
ms.openlocfilehash: 6d51d8c918b9c6dfc8f4dde652bbabe7fe3c17ae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475565"
---
# <a name="extensible-storage-engine-system-parameters"></a>paramètres système du moteur de Stockage Extensible


_**S’applique à :** Windows | Windows Serveurs_

## <a name="extensible-storage-engine-system-parameters"></a>paramètres système du moteur de Stockage Extensible

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


| | | <p>Valeur par défaut :</p> | <p>Valeur par défaut du paramètre.</p> | | <p>Tapez :</p> | <p>Type de données du paramètre.</p> | | <p>Plage valide :</p> | <p>Valeurs autorisées pour le paramètre.</p> | | <p>Étendue :</p> | <p>Le paramètre est-il global ou par instance ?</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Le paramètre peut-il être défini si des instances existent ?</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Le paramètre peut-il être défini lors de son initialisation ?</p> | | <p>Affecte la disposition physique :</p> | <p>Le paramètre affecte-t-il les fichiers sur le disque ?</p> | | <p>Affecte la fiabilité :</p> | <p>Le paramètre affecte-t-il la fiabilité du moteur ?</p> | | <p>Affecte les performances :</p> | <p>Le paramètre affecte-t-il les performances du moteur ?</p> | | <p>Affecte les ressources :</p> | <p>Le paramètre affecte-t-il les ressources du moteur ?</p> | | <p>Disponibilité :</p> | <p>les versions de Windows qui prennent en charge le paramètre.</p> | 

