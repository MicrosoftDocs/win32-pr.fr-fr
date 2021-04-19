---
title: Connexion automatique RAS
description: Une fonctionnalité appelée \ 0034 ; connexion par défaut \ 0034 ; a été ajouté au système dans Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Numérotation automatique, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543406"
---
# <a name="ras-autodial"></a>Connexion automatique RAS

Une fonctionnalité appelée « connexion par défaut » a été ajoutée au système dans Windows XP. En cas d’échec de tentative de connexion, le système recherche une correspondance explicite (pour le nom Winsock ou le nom de partage) dans la base de données si ce n’est pas le cas, il compose la connexion par défaut, le cas échéant.

**Windows 2000 :** Lorsqu’une tentative de connexion à une adresse réseau échoue parce que l’ordinateur hôte est inaccessible, la fonctionnalité de numérotation automatique peut démarrer automatiquement une opération de connexion à distance. Pour ce faire, AutoDial effectue une recherche dans sa base de données d’adresses réseau afin de trouver une entrée de l’annuaire téléphonique qu’il peut utiliser pour établir la connexion.

**Windows NT 4,0 :  ** RAS conserve une base de données des noms Winsock et/ou des noms de partage que vous avez atteints avec succès alors qu’une connexion RAS/VPN était active. Plus tard, en cas d’échec d’une tentative de connexion Winsock ou de partage, le système vérifie cette base de données et offre à la fois la connexion stockée.

 

 




