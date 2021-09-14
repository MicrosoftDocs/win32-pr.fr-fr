---
description: L’assistance IP fournit des informations sur la configuration réseau de l’ordinateur local.
ms.assetid: 6135dca5-00c8-4ed4-bb89-7c99abeb7c7c
title: Récupération d’informations sur la configuration réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a6860b329ba7c69575be1dfeaaa2e19c57558f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094558"
---
# <a name="retrieving-information-about-network-configuration"></a>Récupération d’informations sur la configuration réseau

L’assistance IP fournit des informations sur la configuration réseau de l’ordinateur local. Pour récupérer des informations de configuration générales, utilisez la fonction [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) . Cette fonction retourne des informations qui ne sont pas spécifiques à un adaptateur ou une interface particulier. Par exemple, **GetNetworkParams** retourne la liste des serveurs DNS utilisés par l’ordinateur local.

-   Pour obtenir des exemples de code impliquant des [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) , consultez [extraction d’informations à l’aide de GetNetworkParams](retrieving-information-using-getnetworkparams.md).

 

 



