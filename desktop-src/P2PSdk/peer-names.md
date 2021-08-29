---
description: Les noms d’homologues sont utilisés par le protocole PNRP (Peer Name Resolution Protocol), le gestionnaire d’identité homologue et l’infrastructure de regroupement d’homologues.
ms.assetid: b0d78b17-6f48-4294-b8a2-8fcc1a7f8ef1
title: Noms de pairs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3587cb27a0d47ebedb60e7987b035a0486e0b67e46fad12fe4673e490268be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775859"
---
# <a name="peer-names"></a>Noms de pairs

Les noms d’homologues sont utilisés par le protocole PNRP (Peer Name Resolution Protocol), le gestionnaire d’identité homologue et l’infrastructure de regroupement d’homologues. Les noms d’homologues sont des noms stables pour les ressources telles que les ordinateurs, les utilisateurs, les groupes ou les services. PNRP utilise des noms d’homologues pour identifier les nœuds d’un réseau pair à pair.

> [!Note]  
> Un point de terminaison utilisé par l’infrastructure homologue est en fait un tuple qui se compose d’une adresse IPv4 ou IPv6, d’un port et d’un protocole (TCP ou UDP). Un nom d’homologue peut avoir plusieurs tuples.

 

Un nom d’homologue est une chaîne de texte au format suivant :

-   « Authority. classifier »

La valeur d’une autorité varie selon que le nom est sécurisé ou non. Le classifieur d’un nom d’homologue est une chaîne. Un classifieur peut être n’importe quel nom qui contient 150 caractères UNICODE ou moins. Les noms d’homologues sont sensibles à la casse et peuvent être inscrits comme sécurisés ou non sécurisés. La liste suivante répertorie quelques exemples de noms d’homologues :

-   « 0. MyUnsecuredPeerName »
-   « 0. JohnDoe. Games »
-   "6520c005f63fc1864b7d8f3cabebd4916ae7f33d. JohnDoe

## <a name="secure-peer-names"></a>Noms d’homologues sécurisés

Pour un nom sécurisé, l’autorité est le hachage SHA (Secure Hash Algorithm) de la clé publique du nom d’homologue et génère une chaîne hexadécimale de 40 caractères. Un nom d’homologue sécurisé peut uniquement être inscrit avec PNRP par le propriétaire ou le délégué du propriétaire du nom d’homologue. Un nom d’homologue sécurisé doit être créé en appelant [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).

## <a name="unsecured-peer-names"></a>Noms d’homologues non sécurisés

Pour un nom non sécurisé, l’autorité est égale à zéro (0) et le classifieur est la seule partie significative du nom d’homologue, qui crée un nom d’homologue non sécurisé sans [identité](identity-manager-api.md)associée. Les noms d’homologues non sécurisés sont utilisés dans l’inscription et la résolution de noms PNRP. Les noms d’homologues non sécurisés permettent d’inscrire et de résoudre des ressources qui ne nécessitent pas de résolution de noms sécurisée. Toutefois, tout nœud peut publier n’importe quel nom non sécurisé. Les applications concernées par la sécurité doivent s’assurer qu’elles sont robustes et sécurisées dans leur consommation de noms d’homologues non sécurisés.

> [!Note]  
> Tout le monde peut inscrire un nom d’homologue non sécurisé avec PNRP.

 

## <a name="pnrp-and-the-nearest-peer-name-instance"></a>PNRP et l’instance de nom d’homologue la plus proche

Il peut y avoir plusieurs instances d’un nom d’homologue. Lorsque vous utilisez [PNRP](pnrp-namespace-provider-api.md) pour résoudre un nom d’homologue, il existe un concept d’instance de nom d’homologue le **plus proche** , ce qui signifie que le nom a un emplacement de service le plus proche du membre **sahint** spécifié dans [**PNRPINFO \_ v1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) ou [**PNRPINFO \_ v2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85)). Si aucun indicateur n’est fourni, le plus proche de l’une des adresses IP locales.

 

 
