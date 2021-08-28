---
title: Informations d’authentification utilisateur
description: Le service du gestionnaire de connexions d’accès à distance sur l’ordinateur client envoie un nom d’utilisateur et un mot de passe au serveur RAS sur l’ordinateur distant.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f347cd9f42106619f2558bdcbc677c961b4fae749912c92dd32ac2c8096f6fd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127809"
---
# <a name="user-authentication-information"></a>Informations d’authentification utilisateur

Le service du gestionnaire de connexions d’accès à distance sur l’ordinateur client envoie un nom d’utilisateur et un mot de passe au serveur RAS sur l’ordinateur distant. Avant d’établir une connexion, le serveur distant utilise ces informations pour authentifier l’utilisateur. Par défaut, le gestionnaire de connexions d’accès à distance envoie le nom d’utilisateur et le mot de passe de l’utilisateur actuellement connecté. Le client RAS peut utiliser la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) spécifiée dans l’appel de [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour spécifier un nom d’utilisateur et un mot de passe différents.

Si le serveur distant ne parvient pas à authentifier l’utilisateur avec les informations spécifiées, il peut autoriser l’opération de connexion à passer à l' [état suspendu](paused-states.md) pour permettre au client RAS de collecter différentes données d’authentification de l’utilisateur.

 

 