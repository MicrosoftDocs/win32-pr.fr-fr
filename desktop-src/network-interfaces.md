---
description: cette rubrique décrit les concepts de l’interface réseau de haut niveau sur Windows, notamment leur identification dans le code et leurs propriétés.
ms.assetid: CB01B5ED-C9DB-410B-8C98-E30D9A680847
title: Interfaces réseau
ms.topic: article
ms.date: 06/29/2018
ms.openlocfilehash: d74c875b579a34464190ca039e0176b8c01bef671b0ea6c24581023a49988645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825454"
---
# <a name="network-interfaces"></a>Interfaces réseau

cette rubrique décrit les concepts de l’interface réseau de haut niveau sur Windows, notamment leur identification dans le code et leurs propriétés. 

> [!IMPORTANT]
> cette rubrique est destinée à un public de développement, à la fois pour les applications de réseau de bureau Windows et les pilotes réseau en mode noyau. Toutefois, certaines informations présentées ici peuvent également être utiles pour les administrateurs système qui gèrent des interfaces réseau via des applets de commande PowerShell.

## <a name="overview"></a>Vue d’ensemble

Une *interface réseau* est le point où deux éléments de l’équipement réseau ou les couches de protocole se connectent. En règle générale, il est représenté par une carte d’interface réseau (NIC) physique pour la connexion entre un ordinateur et un réseau privé ou public. Toutefois, il peut également prendre la forme d’un composant logiciel uniquement, tel que l’interface de bouclage ( `127.0.0.1` pour IPv4 ou `::1` pour IPv6).

Les interfaces réseau sont définies par l’IETF (Internet Engineering Task Force) dans la [norme RFC 2863](https://tools.ietf.org/html/rfc2863) et ne sont pas censées être définies par Windows. Pour obtenir des questions détaillées sur la signification des identificateurs d’interface réseau, tels que **ifIndex**, consultez les définitions de l’IETF. le reste de cette rubrique traite des détails d’implémentation spécifiques à Windows.

## <a name="network-interface-identifiers-and-properties"></a>Identificateurs et propriétés de l’interface réseau

sur Windows, une interface réseau peut être identifiée de différentes façons. Certains de ces identificateurs sont utilisés pour distinguer les interfaces réseau les unes des autres, mais tous les identificateurs ne sont pas adaptés à cette tâche en raison de leurs propriétés différentes. En règle générale, les interfaces réseau sont identifiées par une adresse réseau à des composants externes. Par exemple, il peut s’agir d’un ID de nœud et d’un numéro de port, ou simplement d’un ID de nœud unique. 

Dans le code, une interface réseau peut être identifiée de plusieurs façons. Le tableau suivant détaille les façons dont une interface réseau peut être identifiée ainsi que les propriétés associées. Nous vous recommandons d’utiliser le GUID d’interface (**ifGuid**) pour la programmation, sauf si une API spécifique requiert un identificateur d’interface réseau différent.

> [!NOTE]
> Dans le tableau suivant, les cellules en **gras** représentent une propriété qui est souhaitable pour les programmeurs de mise en réseau.

| Identificateur | Taille | Est unique sur le système | Est unique dans le monde | Est prévisible | Sera recyclé si la carte réseau est supprimée | Persiste entre les redémarrages | Les utilisateurs finaux peuvent modifier à tout moment | Les pilotes peuvent être modifiés à tout moment | Familiarité générale avec les utilisateurs finaux | Est toujours présent |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **ifIndex** | **4 octets** | **Oui** | Non | Non | Oui | Non<sup>1</sup> | **Non** | **Non** | **Certains**<sup>2</sup> | **Oui** |
| **NetLuid** | **8 octets** | **Oui** | Non | Non | Oui | **Oui** | **Non** | **Non** | Non | **Oui** |
| **ifGuid** | **16 octets** | **Oui** | **Généralement**<sup>3</sup> | Non | **Non** | **Oui** | **Non** | **Non** | Non | **Oui** |
| **ifAlias** | 514 octets | **Oui pour les cartes réseau**<sup>4</sup> | Non | Parfois<sup>5</sup> | Oui | **Oui** | Oui | **Non** | **Oui** | **Généralement**<sup>4</sup> |
| **ifDescr** | 514 octets | En général<sup>6</sup> | Non | Non | Oui | **Oui** | **Non** | Oui | **Oui** | **Trouve** |
| **ifPhysAddress (adresse MAC)**| 0 à 32 octets | Généralement, pour les cartes réseau | **Généralement, pour les cartes réseau** | **Oui** | **Lié au matériel** | **Oui** | **Non** | **Non** | **Oui** | **Généralement** <sup>7</sup> |
| **ID d’instance PnP** | Jusqu’à 400 octets | **Oui** | Non | Non | Oui | **Oui** | **Non** | **Non** | Non | **Généralement, pour les cartes réseau**<sup>8</sup> |
| **Emplacement PnP (numéro d’emplacement PCI)** | Jusqu’à 400 octets | **Oui** | Non | **Oui** | Oui | **Oui** | **Non** | **Non** | Que | Parfois<sup>8, 9</sup> |

Remarques pour le tableau précédent :

1. Il n’est pas garanti que les **IfIndexes** soient stables entre les redémarrages, même s’ils reçoivent souvent la même valeur que le démarrage précédent. Par conséquent, il n’est pas recommandé que les pilotes utilisent **ifIndex** , sauf si cela est requis par une API.
2. Certaines `netsh` commandes prennent `ifIndex` , ou `index` , en tant qu’entrée. Par conséquent, certains utilisateurs administratifs sont familiarisés avec la propriété **ifIndex** s’ils utilisent `netsh` fréquemment la commande.
3. Si un ordinateur est cloné ou mis en image, certains GUID peuvent être identiques. En outre, certaines interfaces réseau spéciales, telles que l’interface Teredo intégrée, peuvent avoir le même GUID sur tous les ordinateurs.
4. NetCfg garantit qu’un **ifAlias** est une chaîne non vide et qu’il est unique parmi toutes les cartes réseau. Toutefois, le fournisseur d’interface NDIS ne le fait pas. Thererfore, il est possible de trouver des interfaces réseau spéciales avec des noms en double ou vides. Cela s’affiche le plus souvent avec les équipes LBFO.
5. Uniquement si le microprogramme prend en charge un nom de périphérique cohérent. Typcically, les serveurs disposent de cette fonctionnalité.
6. NetCfg attribue des **ifDescrs** uniques à toutes les interfaces réseau. Toutefois, les pilotes peuvent appeler une API pour remplacer **ifDescr** par n’importe quelle valeur, y compris un autre qui n’est pas unique. Certains packages de logiciels tiers le font.
7. Tous les types de supports n’ont pas d’adresse MAC. Par exemple, certains tunnels n’ont pas ce concept et publient simplement un tableau d’octets de longueur nulle en tant qu’adresse réseau.
8. Uniquement présent sur les interfaces réseau qui sont sauvegardées par un périphérique PnP. Par exemple, les interfaces de bouclage, les interfaces de filtre légère, les interfaces fournies par un fournisseur d’interface NDIS et certaines cartes réseau intégrées spéciales n’ont pas de périphériques PnP qui les sauvegardent.
9. Seuls certains bus PnP prennent en charge un ID d’emplacement PnP. Les bus PCI et USB intégrés sont, contrairement aux appareils énumérés à l’origine.

## <a name="visibility-to-developers"></a>Visibilité pour les développeurs

Dans le tableau précédent, toutes les propriétés, à l’exception des propriétés Plug-and-Play (PnP), sont visibles par les applications de bureau en mode utilisateur et les pilotes en mode noyau via un en-tête partagé (Netioapi. h). Les propriétés PnP sont visibles via l’en-tête Devpkey. h et sont utilisées par les applications de bureau en mode utilisateur et les pilotes en mode noyau. Par exemple, consultez la documentation [DEVPKEY](/windows-hardware/drivers/install/devpkey-device-instanceid) .

L’API [d’assistance IP](/windows/desktop/IpHlp/ip-helper-start-page) est également disponible pour les applications de bureau en mode utilisateur et les pilotes en mode noyau.

La surface de l’API UWP expose uniquement la propriété [ifGuid](/uwp/api/windows.networking.connectivity.networkadapter.networkadapterid) directement. Toutefois, les développeurs d’applications UWP peuvent importer la fonction [**GetIfTable2**](/windows/desktop/api/netioapi/nf-netioapi-getiftable2) à l’aide de P/Invoke s’ils sont tenus d’accéder à d’autres propriétés de l’interface réseau.

## <a name="related-topics"></a>Rubriques connexes

Pour plus d’informations sur les définitions MIB (Management Information base) des interfaces réseau, consultez [RFC 2863](https://tools.ietf.org/html/rfc2863).

Pour les interfaces réseau NDIS dans les pilotes réseau, consultez [NDIS Network Interfaces](/windows-hardware/drivers/network/ndis-network-interfaces2).

Pour obtenir des informations de référence sur l’API Netioapi. h, consultez l' [en-tête Netioapi. h](/windows/desktop/api/netioapi/).
