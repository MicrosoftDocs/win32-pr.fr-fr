---
description: Le système utilise les informations de configuration pour déterminer comment démarrer le service.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Configuration du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525822"
---
# <a name="service-configuration"></a>Configuration du service

Le système utilise les informations de configuration pour déterminer comment démarrer le service. Les informations de configuration incluent également le nom complet du service et sa description. Par exemple, pour le service DHCP, vous pouvez utiliser le nom d’affichage « service Dynamic Host Configuration Protocol » et la description « fournit des adresses Internet pour l’ordinateur sur votre réseau ».

Pour modifier les informations de configuration d’un objet de service, un programme de configuration utilise la fonction [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) . Pour obtenir un exemple, consultez [modification d’une configuration de service](changing-a-service-configuration.md).

Pour récupérer les informations de configuration d’un objet de service, le programme de configuration utilise la fonction [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) ou [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) . Pour obtenir un exemple, consultez [interrogation de la configuration d’un service](querying-a-service-s-configuration.md).

Les fonctions de configuration du service [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) et [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) prennent en charge l’utilisation de déclencheurs pour contrôler le démarrage du service.

Pour modifier le descripteur de sécurité pour un objet SCManager ou un objet de service, un programme de configuration utilise la fonction [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Pour récupérer une copie du descripteur de sécurité, le programme de configuration utilise la fonction [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration d’un service à l’aide de SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
