---
title: Filtrage avec état ALE
description: Les filtres installés au niveau des couches d’application de la couche application (ALE) de la plateforme de filtrage Windows (WFP) effectuent un filtrage réseau avec état.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031237"
---
# <a name="ale-stateful-filtering"></a>Filtrage avec état ALE

Les filtres installés au niveau des couches d’application de la couche application (ALE) de la plateforme de filtrage Windows (WFP) effectuent un filtrage réseau avec état. Un *fluide ALE* est utilisé comme base pour le filtrage avec état ALE.

Un flux ALE est un moyen de classer le trafic réseau en le regroupant en fonction d’une adresse IP source, d’une adresse IP de destination, d’un port source, d’un port de destination et d’un protocole. Un fluide ALE peut être générique, autrement dit un ou plusieurs des descripteurs peuvent correspondre à tout (ou caractère générique \* ). Par exemple, un workflow générique UDP ALE est décrit en tant qu’adresse IP source = \* , adresse IP de destination = \* , port source = \* , port de destination = \* et protocole = UDP.

Une fois qu’une connexion est autorisée (les connexions entrantes sont autorisées au niveau de la couche FWPM d’authentification ALE de la couche et des connexions sortantes au niveau de la couche FWPM d’authentification ALE de la couche **\_ \_ ALE \_ \_ \_ v {4 \| 6}** ), un fluide ALE est créé de telle sorte que, en excluant une modification de stratégie, tous les paquets, entrants et sortants, qui appartiennent au même fluide ALE sont autorisés automatiquement. [**\_ \_ \_ \_ \_ \_ \|**](management-filtering-layer-identifiers-.md) Étant donné qu’une modification de stratégie peut nécessiter le blocage des connexions précédemment autorisées, les flux ALE doivent être [réautorisés](ale-re-authorization.md) lorsqu’une modification de stratégie se produit.

Le filtrage avec état ALE réduit considérablement le nombre de classifications requises en classant uniquement le premier paquet qui appartient à un fluide ALE. Par comparaison, le filtrage sans état requiert la classification de chaque paquet qui traverse le réseau.

Un fluide ALE est associé à une direction, qui est la direction du premier paquet du fluide. Cela permet d’obtenir des stratégies plus flexibles, en autorisant les connexions initiées entrantes à avoir des stratégies différentes des connexions sortantes initiées.

## <a name="tcp-ale-flow"></a>Flow TCP ALE

Un flux ALE pour le trafic TCP est identifié par cinq tuples de TCP/IP (adresse IP source, adresse IP de destination, port source, port de destination et protocole).

Un flot TCP ALE a la même durée de vie qu’un socket TCP connecté. Un socket TCP connecté peut être un socket créé à l’aide de [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) ou un socket créé à la suite d’un appel [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .

ALE gère une relation un-à-un entre un fluide TCP ALE et un bloc de contrôle TCP (TCB).

## <a name="udp-ale-flow"></a>Flow PEA UDP

> [!Note]  
> Les protocoles qui ne sont pas TCP ou ICMP sont traités comme UDP.

 

Un flux ALE pour le trafic UDP est identifié par cinq tuples de TCP/IP (adresse IP source, adresse IP de destination, port source, port de destination et protocole).

Un workflow UDP ALE est créé sur la base d’un socket UDP et représente l’homologue distant avec lequel l’application communique. Un homologue distant est identifié par un tuple (adresse IP de destination et port de destination).

Il existe une relation un-à-plusieurs entre un socket UDP et les homologues distants avec lesquels il communique.

Lorsque le socket UDP local est fermé, tous les flux ALE qui lui sont associés sont supprimés.

En l’absence de fermetures de sockets, les flux ALE de monodiffusion UDP ont un délai d’inactivité [configurable](ale-flow-customization.md) qui a pour valeur par défaut 60 secondes. Si aucun paquet n’est envoyé ou reçu dans cette fenêtre, le Flow ALE sera supprimé. Ce délai d’attente par défaut est progressivement réduit lorsque le nombre de flux ALE atteint un certain seuil.

## <a name="icmp-ale-flow"></a>Trafic de la ALE ALE

Un flux ALE pour le trafic ICMP est identifié par le code à six tuples (adresse IP source, adresse IP de destination, type ICMP, code ICMP, protocole et ID ICMP). L’ID ICMP fait partie du flux ALE uniquement pour le trafic ICMP d’écho/réponse.

En l’absence de fermetures de sockets, les flux ALE de monodiffusion ICMP ont un délai d’inactivité [configurable](ale-flow-customization.md) qui a pour valeur par défaut 60 secondes. Si aucun paquet n’est envoyé ou reçu dans cette fenêtre, le Flow ALE sera supprimé. Ce délai d’attente par défaut est progressivement réduit lorsque le nombre de flux ALE atteint un certain seuil.

Seuls les messages ICMP sans erreur sont indiqués aux couches ALE. Les messages d’erreur ICMP peuvent être inspectés au niveau des \_ couches d’erreurs ICMP.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Application de la couche application (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Couches ALE](ale-layers.md)
</dt> <dt>

[Trafic de diffusion/multidiffusion ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Réautorisation ALE](ale-re-authorization.md)
</dt> <dt>

[Personnalisation du fluide ALE](ale-flow-customization.md)
</dt> <dt>

[Flux de paquets TCP](tcp-packet-flows.md)
</dt> <dt>

[Flux de paquets UDP](udp-packet-flows.md)
</dt> <dt>

[Fonctions Winsock](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 