---
description: L’interface IInstallationBehavior définit les propriétés suivantes.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Propriétés IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951233"
---
# <a name="iinstallationbehavior-properties"></a>Propriétés IInstallationBehavior

L’interface [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) définit les propriétés suivantes.



| Propriété                                                                                 | Description                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanRequestUserInput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Obtient une valeur booléenne thast indique si l’installation ou la désinstallation d’une mise à jour peut demander une entrée d’utilisateur.                                                        |
| [**Impact**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Obtient une énumération [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) qui indique comment l’installation ou la désinstallation de la mise à jour affecte l’ordinateur.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Obtient une énumération [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) qui spécifie le comportement de redémarrage qui se produit lorsque vous installez ou désinstallez la mise à jour. |
| [**RequiresNetworkConnectivity**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Obtient une valeur booléenne qui indique si l’installation ou la désinstallation d’une mise à jour requiert une connectivité réseau.                                                     |



 

 

 



