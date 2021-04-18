---
title: Mode de tunnel
description: Le scénario de stratégie IPsec en mode tunnel est utilisé pour appliquer la protection du mode de tunnel IPsec pour tout le trafic correspondant entre deux points de terminaison de tunnel.
ms.assetid: 170046c5-28ec-4341-89e2-93494bf9c6b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75fdecb7f959a2f95aae2649a6e3f8f94def9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310693"
---
# <a name="tunnel-mode"></a>Mode de tunnel

Le scénario de stratégie IPsec en mode tunnel est utilisé pour appliquer la protection du mode de tunnel IPsec pour tout le trafic correspondant entre deux points de terminaison de tunnel.

Ce scénario de stratégie est généralement utilisé pour protéger le trafic entre plusieurs sous-réseaux de succursales, lorsqu’il est transféré entre les passerelles correspondantes sur Internet. Il peut également être utilisé pour sécuriser la communication de bout en bout entre deux ordinateurs hôtes, également appelés tunnels point à point.

Pour implémenter une stratégie de mode de tunnel à l’aide de la plateforme de filtrage Windows (WFP), appelez la fonction [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) qui instancie les filtres de mode de tunnel appropriés aux couches appropriées pour le compte de l’appelant. L’appelant doit spécifier le mode principal, les contextes de fournisseur en mode rapide et les conditions de filtre qui décrivent le trafic qui doit être sécurisé à l’intérieur du tunnel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code : utilisation du mode de tunnel](using-tunnel-mode.md)
</dt> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




