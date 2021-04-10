---
title: Modification des Interface-Specific et des informations globales pour les clients
description: Pour modifier les informations d’interface d’un client spécifique, par exemple NAT, utilisez d’abord le \ 0034 ; GetInfo \ 0034 ; fonction permettant de récupérer les informations actuelles.
ms.assetid: 208e356b-328e-416d-881c-732fed460ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c8f2ef3c37d75db1cc7686a67108530b16b28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939964"
---
# <a name="changing-interface-specific-and-global-information-for-clients"></a>Modification des Interface-Specific et des informations globales pour les clients

Pour modifier les informations d’interface d’un client spécifique, par exemple NAT, utilisez d’abord la fonction « GetInfo » appropriée pour récupérer les informations actuelles. Si le routeur est en cours d’exécution, utilisez [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). Si le routeur n’est pas en cours d’exécution, utilisez [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo). Cet appel récupère les informations pour tous les clients qui s’exécutent sur l’interface spécifiée. Par exemple, si OSPF et RIP s’exécutent sur une interface particulière, cet appel récupère les informations d’interface pour les deux. Utilisez la fonction [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind) pour localiser le bloc d’informations qui correspond au client que vous souhaitez modifier. Utilisez ensuite la fonction [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset) pour effectuer les modifications. Enfin, utilisez [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) ou [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) pour apporter les modifications au routeur en cours d’exécution ou à la configuration du routeur dans le registre.

Les informations sur les clients globaux sont des informations qui ne sont pas spécifiques à une interface particulière sur laquelle le client s’exécute. Utilisez une procédure similaire pour modifier les informations globales pour un client spécifique. Tout d’abord, récupérez les informations globales pour tous les clients à l’aide de [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo) ou [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo). Utilisez ensuite les fonctions MprInfo pour modifier les informations. Enfin, utilisez les fonctions [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo) ou [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo) pour enregistrer les informations modifiées à nouveau sur le routeur ou le registre en cours d’exécution.

Les appels aux fonctions d’administration précédentes passent par le gestionnaire d’interface dynamique (DIM) et finissent par traduire en appels du gestionnaire de routeur aux clients eux-mêmes. Tous les clients, qu’ils soient ou non des protocoles de routage, doivent être conformes à l’interface décrite dans la section [interface de protocole du routeur](about-routing-protocol-interface.md). Dans le cadre de cette interface, le protocole de routage doit prendre en charge les fonctions suivantes (parmi d’autres) :

-   [**GetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_global_info)
-   [**SetGlobalInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_global_info)
-   [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info)
-   [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info)

Le gestionnaire de routeur appelle les fonctions [**GetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pget_interface_info) pour chacun des clients afin de recueillir les informations retournées à partir d’un appel à [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo). De même, lorsque le gestionnaire de routeur reçoit des informations mises à jour via l’appel [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) , il utilise les fonctions [**SetInterfaceInfo**](/windows/desktop/api/Routprot/nc-routprot-pset_interface_info) pour mettre à jour les informations d’interface de chacun des clients.

 

 




