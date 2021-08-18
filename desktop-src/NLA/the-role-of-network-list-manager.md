---
title: Rôle du gestionnaire de listes de réseaux
description: Rôle du gestionnaire de listes de réseaux
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec37d0cf157b87bf43fe12e9aa3a33eb316b7800474dd75ef3a6d4e23bb6189d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780489"
---
# <a name="the-role-of-network-list-manager"></a>Rôle du gestionnaire de listes de réseaux

avant Windows XP et Windows Server 2003, les applications devaient appeler un certain nombre d’api non liées pour obtenir des données sur les attributs réseau, tels que l’adresse IP, le contrôleur de domaine ou le système DNS (domain Name System). depuis Windows XP et Windows Server 2003, l’API Winsock network location awareness a proposé un ensemble limité de fonctionnalités d’emplacement réseau. dans Windows Server 2008 et Windows Vista, le service de sensibilisation du réseau capture les attributs réseau dans un emplacement unique et permet aux applications d’interroger et de récupérer des réseaux et des attributs spécifiques. Le gestionnaire de listes de réseaux remplace les fonctionnalités de l’API Winsock précédente (disponible en tant que fournisseur d’espace de noms Winsock) tout en conservant la compatibilité avec les anciennes applications à l’aide de l’API Winsock.

 

 




