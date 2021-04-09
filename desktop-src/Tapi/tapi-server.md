---
description: Le serveur TAPI (TAPISRV) est le référentiel central des données de téléphonie sur un ordinateur utilisateur.
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: Serveur TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866913"
---
# <a name="tapi-server"></a>Serveur TAPI

Le serveur TAPI (TAPISRV) est le référentiel central des données de téléphonie sur un ordinateur utilisateur. Ce processus de service effectue le suivi des ressources de téléphonie locales et distantes, des applications inscrites pour gérer les demandes de téléphonie assistées et des fonctions asynchrones en attente, et il permet également une interface cohérente avec les fournisseurs de services de téléphonie (TSPs). Pour plus d’informations et pour obtenir un diagramme illustrant la relation du serveur TAPI avec d’autres composants et une vue d’ensemble de leurs rôles, consultez [modèle de programmation Microsoft](microsoft-telephony-programming-model.md)pour la téléphonie.

Pour les ordinateurs qui exécutent les systèmes d’exploitation Windows Server 2003, Windows XP et Windows 2000, TAPISRV s’exécute dans le contexte de Svchost.exe. Pour les ordinateurs fonctionnant sous Windows NT, il s’exécute en tant que processus de service distinct. Quand une application charge une DLL TAPI dans son espace de processus et effectue une opération d’initialisation, la DLL établit une liaison RPC avec le serveur TAPI. Le serveur TAPI charge les fournisseurs de services téléphoniques (TSPs) dans son espace de processus. Quel que soit le nombre d’applications qui accèdent aux appareils d’un fournisseur donné, une seule instance d’un TSP donné existera.

 

 



