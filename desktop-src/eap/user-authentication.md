---
title: Authentification utilisateur
description: Le protocole d’authentification lui-même peut authentifier l’utilisateur via PEAP (Protected EAP).
ms.assetid: 7e0ff5e3-3274-4b52-8c53-101ad01e3034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10de1d08a0daffe7fb415c3eab4ba939afa9387
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679246"
---
# <a name="user-authentication"></a>Authentification utilisateur

Le protocole d’authentification lui-même peut authentifier l’utilisateur via PEAP (Protected EAP). Il existe également deux fournisseurs d’authentification intégrés au système d’exploitation : l’authentification de domaine Windows (accessible via les services d’annuaire) et le service RADIUS (Remote Access Dial-in User Service).

Dans le cas où RADIUS est le fournisseur d’authentification, le plug-in EAP est installé sur le serveur RADIUS plutôt que sur le serveur de point d’accès sans fil (AP), tel qu’un serveur RAS. Le serveur AP transmet les paquets EAP directement du client au service d’authentification sur le serveur RADIUS. Le serveur AP ne traite aucune des informations contenues dans les paquets EAP, mais il doit accepter les clés de chiffrement générées PEAP côté serveur, à pleine puissance (256 bits) pour créer la connexion sécurisée.

 

 




