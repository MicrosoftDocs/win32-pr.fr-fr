---
title: Application de la couche application (ALE)
description: ALE est un ensemble de couches en mode noyau de plateforme de filtrage Windows (WFP) qui sont utilisées pour le filtrage avec état.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d74db5fdc231569f65c3b25cb630b306111aa5d6a7e3eb7faad743a5f74db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069469"
---
# <a name="application-layer-enforcement-ale"></a>Application de la couche application (ALE)

ALE est un ensemble de couches en mode noyau de plateforme de filtrage Windows (WFP) qui sont utilisées pour le filtrage avec état.

Le filtrage avec État assure le suivi de l’état des connexions réseau et autorise uniquement les paquets qui correspondent à un état de connexion connu. Par exemple, le filtrage avec état d’une connexion TCP lancée à partir d’un pare-feu peut autoriser uniquement les paquets entrants qui correspondent aux paquets sortants précédents envoyés par le tiers protégé.

Les filtres dans les couches ALE autorisent la création de connexions entrantes et sortantes, les affectations de port, les opérations de socket telles que [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), la création de sockets bruts et le mode de proximité.

Le trafic au niveau des couches ALE est classé par opération par connexion ou par socket. Sur les couches non ALE, les filtres peuvent uniquement classer le trafic par paquet.

Les couches ALE sont les seules couches WFP où le trafic réseau peut être filtré en fonction de l’identité de l’application (à l’aide d’un nom de fichier normalisé) et en fonction de l’identité de l’utilisateur, à l’aide d’un descripteur de sécurité. (Voir FLT \_ \_informations de nom \_ de fichier dans la documentation du Kit de pilotes Windows (WDK), pour plus d’informations sur les noms de fichiers normalisés.)

En outre, quand IPsec est utilisé pour sécuriser la connexion, le filtrage au niveau des couches ALE peut également être effectué sur l’identité de l’ordinateur distant et sur l’identité de l’utilisateur distant. Les identités de l’ordinateur distant et de l’utilisateur sont obtenues à partir des informations d’identification utilisées lors de la création d’une session IPsec.

Pour cette raison, les stratégies qui appliquent (par exemple, « administrateur ») et/ou l’application (par exemple, « Internet Explorer ») sont autorisées à effectuer les opérations de réseau mentionnées ci-dessus sont créées au niveau des couches ALE.

ALE fournit la mise en application pour les stratégies telles que « autoriser Windows Messenger à accéder au réseau tout en bloquant toutes les autres applications ». Dans un tel exemple, lorsque l’application « Messenger » se connecte sur le réseau, ALE interrompt l’événement, détermine qu’elle a été lancée par Messenger et interroge le moteur de filtre WFP pour déterminer si le socket doit être autorisé à continuer.

> [!Note]  
> En raison de la nature des véritables sockets à deux adresses IP, les classifications au niveau de la couche ALE d’IPv4 peuvent ne pas se produire. Cela est dû à la conception, car pour toutes les intentions et les objectifs, le socket est un socket IPv6. Pour voir le trafic v4 pour un tel Socket, créez des filtres au niveau de la couche V6 à l’aide de l’adresse mappée IPv6.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

[Filtrage avec état ALE](ale-stateful-filtering.md)
</dt> <dt>

[Trafic de diffusion/multidiffusion ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Réautorisation ALE](ale-re-authorization.md)
</dt> <dt>

[personnalisation de la Flow ALE](ale-flow-customization.md)
</dt> </dl>

 

 