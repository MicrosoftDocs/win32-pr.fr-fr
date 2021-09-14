---
title: Fonctionnement des fonctions de gestion de routeur
description: Les sections suivantes décrivent les différents types de fonctions de gestion de routeur et ce que vous devez savoir pour les utiliser efficacement.
ms.assetid: 2f6831f2-39be-43b1-80bd-9a36c0f8a2af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b1891bc55b80a18a6d0dd928044da1e0e9709
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123518"
---
# <a name="understanding-router-management-functions"></a>Fonctionnement des fonctions de gestion de routeur

Les sections suivantes décrivent les différents types de fonctions de gestion de routeur et ce que vous devez savoir pour les utiliser efficacement.

Toutes les fonctions de gestion de routeur requièrent des privilèges d’administrateur. Un utilisateur du groupe utilisateurs avec pouvoir ne dispose pas des privilèges suffisants pour utiliser les fonctions de gestion de routeur.

## <a name="the-different-classes-of-router-management-functions"></a>Les différentes classes de fonctions de gestion de routeur

Les fonctions de gestion de routeur peuvent être divisées en fonctions d’administration et fonctions de configuration. Les [fonctions d’administration](router-administration-functions.md) ont un préfixe MprAdmin et les [fonctions de configuration](router-configuration-functions.md) ont un préfixe MprConfig. Malgré l’attribution de noms, les deux ensembles de fonctions sont utilisés pour la gestion de routeur. Les fonctions MprAdmin fonctionnent directement sur le routeur en cours d’exécution. Les fonctions MprConfig ont des fonctionnalités similaires, mais fonctionnent sur la configuration du routeur stockée dans le registre. Les deux types de fonctions passent des [blocs d’informations](router-information-functions.md).

Les fonctions de gestion de routeur peuvent également être divisées en fonction des composants du routeur qu’ils gèrent : les interfaces, les gestionnaires de routeur ou les clients du gestionnaire de routeur.

Les [fonctions](router-interface-functions.md) de l’interface du routeur ont un préfixe MprAdminInterface ou MprConfigInterface. Utilisez ces fonctions pour accéder aux interfaces. Les [fonctions du gestionnaire de routeur](router-manager-transport-functions.md) ont le préfixe MprAdminTransport ou MprConfigTransport. Utilisez ces fonctions pour accéder aux gestionnaires de routeur. Enfin, les [fonctions du client du gestionnaire de routeur](router-manager-client-interfacetransport-functions.md) ont un préfixe MprAdminInterfaceTransport ou MprConfigInterfaceTransport. Utilisez ces fonctions pour accéder aux clients qui s’exécutent sur le routeur.

Les [fonctions MprAdminMib](/windows/desktop/RRAS/about-router-management-with-mib)sont un sous-ensemble de fonctions MprAdmin. Ils fonctionnent également sur l’itinéraire en cours d’exécution seul. Toutefois, ces fonctions ne transmettent pas de blocs d’informations. Ces fonctions offrent une plus grande souplesse au concepteur de protocoles, en particulier pour la récupération des informations de non-configuration, telles que les statistiques.

## <a name="ensuring-that-changes-occur-immediately-and-are-persistent"></a>S’assurer que les modifications se produisent immédiatement et sont persistantes

Un développeur peut apporter des modifications à la configuration du routeur directement à l’aide des [fonctions de configuration du routeur](router-configuration-functions.md). Toutefois, toutes les modifications apportées à la configuration ne prennent pas effet tant que le routeur n’est pas redémarré, car il s’agit de la seule fois où DIM lit la configuration dans le registre.

Un développeur peut apporter des modifications au routeur en cours d’exécution à l’aide des [fonctions d’administration du routeur](router-administration-functions.md). Toutefois, ces modifications ne sont pas persistantes : dans la mesure où elles n’ont pas été écrites dans le registre, elles sont perdues si le routeur est redémarré.

Pour apporter des modifications immédiates et persistantes, un développeur doit utiliser les fonctions d’administration de routeur et de configuration de routeur. Si le routeur n’est pas en cours d’exécution, le développeur doit uniquement appeler les fonctions de configuration de routeur appropriées.

Pour interroger les informations du routeur en cours d’exécution, utilisez les fonctions d’administration du routeur. Si le routeur n’est pas en cours d’exécution, interrogez les informations à l’aide des fonctions de configuration du routeur.

Les fonctions [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) et [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) prennent en charge la structure [**MPR \_ interface \_ 2**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_2) . Toutefois, [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate) et [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo) ne le font pas. Pour créer une interface de connexion à la demande qui est persistante après un redémarrage, appelez **MprAdminInterfaceCreate** avec l' **\_ interface MPR \_ 2**, puis appelez **MprConfigInterfaceCreate** avec [**MPR \_ interface \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) ou [**MPR \_ interface \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_1). De même, pour apporter des modifications persistantes à une interface de connexion à la demande, appelez **MprAdminInterfaceSetInfo** avec l' **\_ interface MPR \_ 2**, puis appelez **MprConfigInterfaceSetInfo** avec **MPR \_ interface \_ 0** ou **MPR \_ interface \_ 1**.

## <a name="using-router-administration-and-configuration-functions-remotely"></a>Utilisation des fonctions d’administration et de configuration de routeur à distance

La plupart des fonctions d’administration et de configuration de routeur peuvent être appelées sur un ordinateur autre que celui qui est administré. Ces fonctions prennent comme paramètre, un handle vers le service de routeur ou la configuration à administrer. Les fonctions d’administration utilisent RPC (appel de procédure distante) pour communiquer avec le service de routage spécifié par le descripteur. Les fonctions de configuration écrivent et lisent dans le registre de l’ordinateur spécifié par le descripteur.

Pour administrer le service de routage sur un ordinateur distant, appelez d’abord [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning) pour vérifier que le service est en cours d’exécution. Appelez ensuite [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect) pour obtenir le descripteur. Si le service de routeur n’est pas en cours d’exécution sur l’ordinateur distant, tous les appels d’administration de routeur (MprAdmin) échouent.

Pour apporter des modifications à la configuration du routeur sur un ordinateur distant, obtenez un handle en appelant la fonction [**MprConfigServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigserverconnect) .

 

 