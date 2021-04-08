---
title: Rôle du gestionnaire de listes de réseaux
description: Rôle du gestionnaire de listes de réseaux
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840825"
---
# <a name="the-role-of-network-list-manager"></a>Rôle du gestionnaire de listes de réseaux

Avant Windows XP et Windows Server 2003, les applications devaient appeler un certain nombre d’API non liées pour obtenir des données sur les attributs réseau tels que l’adresse IP, le contrôleur de domaine ou le système DNS (Domain Name System). À compter de Windows XP et de Windows Server 2003, l’API Winsock de sensibilisation à l’emplacement réseau offre un ensemble limité de fonctionnalités d’emplacement réseau. Dans Windows Server 2008 et Windows Vista, le service de reconnaissance réseau capture les attributs réseau dans un emplacement unique et permet aux applications d’interroger et de récupérer des réseaux et des attributs spécifiques. Le gestionnaire de listes de réseaux remplace les fonctionnalités de l’API Winsock précédente (disponible en tant que fournisseur d’espace de noms Winsock) tout en conservant la compatibilité avec les anciennes applications à l’aide de l’API Winsock.

 

 




