---
description: Les partages DDE sont des ressources de machine.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Partages DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e3416235f78e48c68b7d2e35c7ac042f8ff5d6eac79cc2471efa5ea12d82b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602119"
---
# <a name="dde-shares"></a>Partages DDE

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Les partages DDE sont des ressources de machine. Ils sont similaires aux partages de fichiers, car ils permettent de contrôler l’accès à une ressource. Avec les partages de fichiers, la ressource est un fichier. Avec les partages DDE, la ressource est des données échangées dynamiquement. Le type de données échangées est déterminé par l’application serveur qui fournit les données et l’application cliente qui demande les données.

Le serveur appelle la fonction [**NDdeShareAdd**](nddeshareadd.md) pour créer le partage DDE, qui est stocké dans le gestionnaire de base de données du partage DDE (DSDM).

Le client démarre la conversation DDE en se connectant au partage DDE. Le client doit appeler la fonction [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) pour initialiser Ddeml et appeler la fonction [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) pour se connecter au partage DDE. Dans l’appel **DdeConnect** , le client spécifie le nom du service comme suit :

\\\\*Nom de l’ordinateur* \\ NDDE $

où *nom_ordinateur* est le nom de l’ordinateur qui exécute l’application serveur. NDDE $ indique que la rubrique fournie à [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) est le nom de partage DDE sur l’ordinateur distant nommé *ComputerName*.

Il existe trois types de partages DDE : ancien style, nouveau style et statique. Il est courant de prendre uniquement en charge le type statique. Les noms des partages statiques utilisent la Convention suivante : *Nom_Partage*$.

 

 
