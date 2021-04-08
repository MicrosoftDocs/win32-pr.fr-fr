---
title: Référence de l’interface de protocole de routage
description: Cette documentation décrit les fonctions et les structures utilisées pour implémenter un protocole de routage en tant que DLL en mode utilisateur.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Routage et accès à distance service RRAS, interface de protocole de routage, référence
- Routage de l’interface de protocole RRAS, référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839981"
---
# <a name="routing-protocol-interface-reference"></a>Référence de l’interface de protocole de routage

Cette documentation décrit les fonctions et les structures utilisées pour implémenter un protocole de routage en tant que DLL en mode utilisateur.

MPR50 doit être défini dans le fichier Make pour le protocole de routage.

La macro de **\_ \_ liaison IP (x) sizeof** calcule la taille, en octets, d’une structure d’informations de [**\_ \_ liaison \_ d’adaptateur IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) qui contient le nombre d’adresses IP.

Ces éléments de référence sont décrits dans les rubriques suivantes :

-   [Fonctions de l’interface de protocole de routage](routing-protocol-interface-functions.md)
-   [Structures de l’interface de protocole de routage](routing-protocol-interface-structures.md)
-   [Gestion des tables de services IPX](ipx-service-table-management.md)

 

 




