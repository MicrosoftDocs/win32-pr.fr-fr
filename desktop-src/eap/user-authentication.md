---
title: Authentification des utilisateurs
description: Le protocole d’authentification lui-même peut authentifier l’utilisateur via PEAP (Protected EAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3f5d377163f2519d97de847d8d14b5bd96925577a8133988adf8fbf950b283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978369"
---
# <a name="user-authentication"></a>Authentification des utilisateurs

Le protocole d’authentification lui-même peut authentifier l’utilisateur via PEAP (Protected EAP). il existe également deux fournisseurs d’authentification intégrés au système d’exploitation : Windows l’authentification de domaine (accessible via les Services d’annuaire) et RADIUS (Remote Access Dial-In User Service).

Dans le cas où RADIUS est le fournisseur d’authentification, le plug-in EAP est installé sur le serveur RADIUS plutôt que sur le serveur de point d’accès sans fil (AP), tel qu’un serveur RAS. Le serveur AP transmet les paquets EAP directement du client au service d’authentification sur le serveur RADIUS. Le serveur AP ne traite aucune des informations contenues dans les paquets EAP, mais il doit accepter les clés de chiffrement générées PEAP côté serveur, à pleine puissance (256 bits) pour créer la connexion sécurisée.

 

 




