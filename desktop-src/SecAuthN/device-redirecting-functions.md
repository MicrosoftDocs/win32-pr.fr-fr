---
description: Les fonctions de redirection de l’appareil redirigent les périphériques MS-DOS standard, les lettres de lecteur et les ports LPT. Cela permet aux applications qui s’exécutent sur le système d’utiliser les appareils et d’accéder au réseau de manière totalement transparente.
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Fonctions Device-Redirecting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577f8d108b6bfdeb01f786478cd736e6c84cc83d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121210"
---
# <a name="device-redirecting-functions"></a>Fonctions Device-Redirecting

Les fonctions de redirection de l’appareil redirigent les périphériques MS-DOS standard, les lettres de lecteur et les ports LPT. Cela permet aux applications qui s’exécutent sur le système d’utiliser les appareils et d’accéder au réseau de manière totalement transparente.



| Fonction                                                         | Description                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | Redirige ou connecte un appareil local à une ressource réseau.<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | Effectue la même action que [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection), mais permet à l’utilisateur de spécifier quelle fenêtre doit posséder toutes les boîtes de dialogue et comment la connexion doit être établie.<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | Interrompt une connexion réseau. Les modifications sont mémorisées si un appareil est déconnecté, sauf si la connexion est une connexion sans appareil.<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | Retourne des informations sur une connexion.<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | Retourne des informations sur une connexion, même si la connexion est actuellement déconnectée.<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | Retourne les informations de performance relatives à une connexion.<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | Retourne le nom universel local ou distant, au format spécifié lors de l’appel de la fonction.<br/>                                                                                            |



 

 

 




