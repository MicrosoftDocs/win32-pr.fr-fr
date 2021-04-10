---
title: Suppression d’un client d’une interface
description: Pour supprimer un client, tel qu’un protocole de routage, d’une interface particulière, utilisez MprAdminInterfaceTransportGetInfo ou MprConfigInterfaceTransportGetInfo pour récupérer toutes les informations client pour l’interface.
ms.assetid: 22fd7233-a242-49c2-8c26-59b415c73af2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585a37920b59f47a0c933427d7218d08a61bed9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940125"
---
# <a name="deleting-a-client-from-an-interface"></a>Suppression d’un client d’une interface

Pour supprimer un client, tel qu’un protocole de routage, d’une interface particulière, utilisez [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) ou [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) pour récupérer toutes les informations client pour l’interface. Utilisez [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove) pour supprimer le bloc d’informations du client à supprimer. Utilisez ensuite [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd) pour ajouter un bloc de longueur zéro pour le client à supprimer. Enfin, utilisez [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) ou [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) pour enregistrer les informations sur le routeur ou le registre en cours d’exécution.

Si le gestionnaire de routeur reçoit un bloc d’informations d’interface de longueur nulle pour un client, il sait supprimer ce client de l’interface. Le gestionnaire de routeur supprime le client en appelant l’implémentation du client de [**DeleteInterface**](/windows/desktop/api/Routprot/nc-routprot-pdelete_interface). Notez la différence importante entre le passage d’un en-tête d’informations qui ne contient pas de bloc d’informations pour un client et le passage d’un en-tête d’informations qui contient un bloc d’informations de longueur nulle pour le client. Dans le premier cas, le gestionnaire de routage n’entreprend aucune action en ce qui concerne le client. Dans le deuxième cas, le gestionnaire de routeur supprime le client de l’interface.

 

 




