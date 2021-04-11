---
description: Le service DDE réseau est utilisé pour initier et maintenir les connexions réseau nécessaires aux conversations DDE entre les applications qui s’exécutent sur des ordinateurs différents d’un réseau.
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: À propos de DDE réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319010"
---
# <a name="about-network-dde"></a>À propos de DDE réseau

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Le service DDE réseau est utilisé pour initier et maintenir les connexions réseau nécessaires aux conversations DDE entre les applications qui s’exécutent sur des ordinateurs différents d’un réseau. Une *conversation* DDE est l’interaction entre les applications client et serveur. Vous utilisez le DDE réseau avec DDE et la bibliothèque de gestion DDE (DDEML) dans votre application.

DDE est une forme de communication interprocessus qui utilise la mémoire partagée pour échanger des données entre des applications. Les applications peuvent utiliser DDE pour les transferts de données à usage unique ou pour les échanges en cours et la mise à jour des données. Pour plus d’informations sur les échanges de données, consultez [échange dynamique de données](../dataxchg/dynamic-data-exchange.md).

DDEML simplifie la tâche d’ajout de la fonctionnalité DDE à une application. Au lieu d’envoyer, de publier et de traiter des messages DDE directement, une application utilise les fonctions fournies par le DDEML pour gérer les conversations DDE. Pour plus d’informations sur DDEML, consultez [bibliothèque de gestion des échange dynamique de données](../dataxchg/dynamic-data-exchange-management-library.md).

## <a name="network-dde-files"></a>Fichiers DDE réseau

Pour utiliser les éléments d’API du DDE réseau, vous devez inclure le fichier d’en-tête NDDEApi. h dans vos fichiers sources et inclure le fichier NDDEApi. lib sur la ligne de votre lien. Vous devez également vous assurer que le fichier NDDEApi.dll est chargé.

Pour plus d'informations, voir les rubriques suivantes :

-   [Agent DDE réseau](network-dde-agent.md)
-   [Partages DDE](dde-shares.md)
-   [Partages et sécurité approuvés](trusted-shares-and-security.md)
-   [Gestion des partages DDE](managing-dde-shares.md)

 

 
