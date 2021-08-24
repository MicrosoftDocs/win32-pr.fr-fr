---
title: Tunnel Mode
description: le scénario de stratégie ipsec en mode Tunnel est utilisé pour appliquer la protection du mode de Tunnel ipsec pour tout le trafic correspondant entre deux points de terminaison de tunnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac16de0dc01bc37e0e4f4b997d00d19339de021ffce66a0d3cf6957addbe90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639069"
---
# <a name="tunnel-mode"></a>Tunnel Mode

le scénario de stratégie ipsec en mode Tunnel est utilisé pour appliquer la protection du mode de Tunnel ipsec pour tout le trafic correspondant entre deux points de terminaison de tunnel.

Ce scénario de stratégie est généralement utilisé pour protéger le trafic entre plusieurs sous-réseaux de succursales, lorsqu’il est transféré entre les passerelles correspondantes sur Internet. Il peut également être utilisé pour sécuriser la communication de bout en bout entre deux ordinateurs hôtes, également appelés tunnels point à point.

pour implémenter la stratégie de mode de Tunnel à l’aide de la plateforme de filtrage Windows (WFP), appelez la fonction [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) qui instancie les filtres de mode de Tunnel appropriés aux couches appropriées pour le compte de l’appelant. L’appelant doit spécifier le mode principal, les contextes de fournisseur en mode rapide et les conditions de filtre qui décrivent le trafic qui doit être sécurisé à l’intérieur du tunnel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[exemple de code : utilisation du Mode Tunnel](using-tunnel-mode.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




