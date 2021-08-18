---
description: Le serveur TAPI (TAPISRV) est le référentiel central des données de téléphonie sur un ordinateur utilisateur.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Serveur TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19eb335ddef68f5f4cc588e34edab4931ad8be1e5e1d768e07a142989afe2291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002677"
---
# <a name="tapi-server"></a>Serveur TAPI

Le serveur TAPI (TAPISRV) est le référentiel central des données de téléphonie sur un ordinateur utilisateur. Ce processus de service effectue le suivi des ressources de téléphonie locales et distantes, des applications inscrites pour gérer les demandes de téléphonie assistées et des fonctions asynchrones en attente, et il permet également une interface cohérente avec les fournisseurs de services de téléphonie (TSPs). Pour plus d’informations et pour obtenir un diagramme illustrant la relation du serveur TAPI avec d’autres composants et une vue d’ensemble de leurs rôles, consultez [modèle de programmation Microsoft](microsoft-telephony-programming-model.md)pour la téléphonie.

pour les ordinateurs qui exécutent les systèmes d’exploitation Windows Server 2003, Windows XP et Windows 2000, TAPISRV s’exécute dans le contexte de Svchost.exe. Pour les ordinateurs qui exécutent sur Windows NT, il s’exécute en tant que processus de service distinct. Quand une application charge une DLL TAPI dans son espace de processus et effectue une opération d’initialisation, la DLL établit une liaison RPC avec le serveur TAPI. Le serveur TAPI charge les fournisseurs de services téléphoniques (TSPs) dans son espace de processus. Quel que soit le nombre d’applications qui accèdent aux appareils d’un fournisseur donné, une seule instance d’un TSP donné existera.

 

 



