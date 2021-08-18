---
title: Référence de l’interface de protocole de routage
description: Cette documentation décrit les fonctions et les structures utilisées pour implémenter un protocole de routage en tant que DLL en mode utilisateur.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Routage et accès à distance service RRAS, interface de protocole de routage, référence
- Routage de l’interface de protocole RRAS, référence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0196a5cbad8919a07a6e9a19ee5f7848eb6378ad2c56f7f0977125e5e79133a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027349"
---
# <a name="routing-protocol-interface-reference"></a>Référence de l’interface de protocole de routage

Cette documentation décrit les fonctions et les structures utilisées pour implémenter un protocole de routage en tant que DLL en mode utilisateur.

MPR50 doit être défini dans le fichier Make pour le protocole de routage.

La macro de **\_ \_ liaison IP (x) sizeof** calcule la taille, en octets, d’une structure d’informations de [**\_ \_ liaison \_ d’adaptateur IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) qui contient le nombre d’adresses IP.

Ces éléments de référence sont décrits dans les rubriques suivantes :

-   [Fonctions de l’interface de protocole de routage](routing-protocol-interface-functions.md)
-   [Structures de l’interface de protocole de routage](routing-protocol-interface-structures.md)
-   [Gestion des tables de services IPX](ipx-service-table-management.md)

 

 




