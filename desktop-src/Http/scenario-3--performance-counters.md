---
title: Scénario 3-compteurs de performance
description: Les compteurs de performances mesurent les quantités d’informations ou de données, en fonction du nombre, de la taille, de la durée et du taux de données demandées ou reçues.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92afacf959c72735adea25c3ace60c8ae032da66394dda6731fdab913407e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950718"
---
# <a name="scenario-3-performance-counters"></a>Scénario 3 : compteurs de performances

Les compteurs de performances mesurent les quantités d’informations ou de données, en fonction du nombre, de la taille, de la durée et du taux de données demandées ou reçues. Vous ne devez pas vous attendre à obtenir la liste des détails d’un compteur, par exemple une liste de messages d’erreur. Utilisez plutôt des compteurs de performances pour connaître les quantités, telles que le nombre de messages d’erreur depuis le démarrage ou la fréquence à laquelle les messages d’erreur sont générés.

## <a name="performance-counters-for-httpsys"></a>Compteurs de performances pour HTTP.sys

à compter de Windows Vista et Windows Server 2008, HTTP.sys dispose des compteurs de métriques de performances suivants pour vous aider à surveiller, diagnostiquer et planifier la capacité des serveurs web : le composant de l’API du serveur HTTP contient les compteurs de performances suivants pour vous aider à surveiller, diagnostiquer et planifier la capacité des serveurs web :

- Compteurs de service HTTP :
  - Nombre d’URI dans le cache, ajoutés depuis le démarrage, supprimé depuis le démarrage et nombre de vidages du cache
  - Présences dans le cache/seconde et échecs dans le cache/seconde
- Groupes d’URL de service HTTP :
  - Taux d’envoi des données, taux de réception des données, octets transférés (envoyés et reçus)
  - Nombre maximal de connexions, taux de tentatives de connexion, taux pour les demandes d’extraction et d’en-tête et nombre total de demandes
- Files d’attente de demandes de service HTTP :
  - Nombre de demandes dans la file d’attente, âge des requêtes les plus anciennes dans la file d’attente (âge de la dernière demande dans la file d’attente)
  - Taux d’arrivées de demande dans la file d’attente, taux de rejet, nombre total de demandes rejetées, taux d’accès au cache

**Accès aux compteurs de performance**

1.  Tapez **Perfmon** à l’invite de commandes pour démarrer la console de diagnostic des performances.
2.  Sélectionnez **Analyseur de performances** dans le contrôle d’arborescence, puis ouvrez l' **Ajouter des compteurs** en cliquant sur **+** .
3.  À partir de **Ajouter des compteurs** , sélectionnez l’un des trois compteurs de performances : **service http**, **files d’attente de requêtes de service http** ou **groupes d’URL de service http**.
4.  Pour afficher les compteurs des ensembles de compteurs **files d’attente de requêtes de service http** et **groupes d’URL de service http** , sélectionnez **instances** , puis cliquez sur **Ajouter** et sur **OK**. Pour afficher les compteurs du service HTTP, sélectionnez l’ensemble de compteurs dans le volet gauche, puis cliquez sur **Ajouter**.

> [!Note]  
> Une seule instance des compteurs de l’API du serveur HTTP existe par ordinateur, car ces compteurs représentent l’État à l’ensemble du composant. Avec les instances de compteurs de performance de groupe d’URL, l’ID d’instance (pour le compteur de performance) correspond à l’ID de groupe d’URL. L’ID de groupe d’URL peut être affiché en exécutant **netsh http show ServiceState**. Avec des instances de compteurs de performance de files d’attente de demandes, le nom d’instance correspond au nom de la file d’attente de demandes. Le nom de la file d’attente des demandes (s’il en existe un) peut être affiché par le même **netsh http show ServiceState**. Toutefois, certaines applications serveur peuvent avoir des files d’attente de demandes sans nom qui ne peuvent pas être mises en correspondance avec un ID d’instance de compteur de performance.

 

 

 




