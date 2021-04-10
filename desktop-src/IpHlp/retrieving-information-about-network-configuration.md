---
description: L’assistance IP fournit des informations sur la configuration réseau de l’ordinateur local.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Récupération d’informations sur la configuration réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952893"
---
# <a name="retrieving-information-about-network-configuration"></a>Récupération d’informations sur la configuration réseau

L’assistance IP fournit des informations sur la configuration réseau de l’ordinateur local. Pour récupérer des informations de configuration générales, utilisez la fonction [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Cette fonction retourne des informations qui ne sont pas spécifiques à un adaptateur ou une interface particulier. Par exemple, **GetNetworkParams** retourne la liste des serveurs DNS utilisés par l’ordinateur local.

-   Pour obtenir des exemples de code impliquant des [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , consultez [extraction d’informations à l’aide de GetNetworkParams](retrieving-information-using-getnetworkparams.md).

 

 



