---
description: L’API du gestionnaire d’identité de l’homologue utilise les fonctions suivantes.
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Fonctions du gestionnaire d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea56df6500239141038f76ba312b84148581f8f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009235"
---
# <a name="identity-manager-functions"></a>Fonctions du gestionnaire d’identité

L’API du gestionnaire d’identité de l’homologue utilise les fonctions suivantes.



| Fonction                                                           | Description                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | Crée un nouveau nom basé sur le nom existant de l’identité d’homologue et du classifieur spécifiés. Toutefois, une nouvelle identité n’est pas créée par un appel à [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername).                                                                                                     |
| [**PeerEnumGroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | Crée et retourne un handle d’énumération d’homologue utilisé pour énumérer tous les groupes homologues associés à une identité d’homologue spécifique.                                                                                                                                                                          |
| [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | Crée et retourne un handle d’énumération d’homologue utilisé pour énumérer toutes les identités d’homologue qui appartiennent à un utilisateur spécifique.                                                                                                                                                                                |
| [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | Libère une énumération, par exemple, un enregistrement ou une énumération de membre, et libère toutes les ressources associées à l’énumération.                                                                                                                                                                   |
| [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | Libère un bloc de données et le retourne au pool de mémoire.                                                                                                                                                                                                                                         |
| [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | Retourne le nombre d’éléments dans une énumération d’homologues.                                                                                                                                                                                                                                                    |
| [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | Retourne un nombre spécifique d’éléments à partir d’une énumération d’homologues.                                                                                                                                                                                                                                            |
| [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | Crée une nouvelle identité d’homologue et retourne son nom. Le nom de l’identité de l’homologue doit être passé dans tous les appels suivants au gestionnaire d’identité de l’homologue, au regroupement d’homologues ou aux fonctions PNRP qui fonctionnent pour le compte de l’identité de l’homologue. Le nom d’identité de l’homologue spécifie l’identité de l’homologue utilisée. |
| [**PeerIdentityDelete**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | Supprime une identité d’homologue. Cela comprend la suppression de tous les certificats, clés privées et informations de groupe associées à une identité d’homologue spécifiée.                                                                                                                                                   |
| [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | Permet à un utilisateur d’exporter une identité d’homologue. L’utilisateur peut ensuite transférer l’identité de l’homologue vers un autre ordinateur.                                                                                                                                                                                       |
| [**PeerIdentityGetCryptKey**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         | Récupère un handle vers un fournisseur de services de chiffrement (CSP).                                                                                                                                                                                                                                          |
| [**PeerIdentityGetDefault**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | Récupère le nom d’homologue par défaut défini pour l’utilisateur actuel.                                                                                                                                                                                                                                              |
| [**PeerIdentityGetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | Retourne le nom convivial de l’identité de l’homologue.                                                                                                                                                                                                                                                        |
| [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | Retourne une description de l’identité de l’homologue, qui peut ensuite être passée à des tiers et utilisée pour inviter une identité d’homologue dans un groupe homologue. Ces informations sont retournées sous forme de fragment XML.                                                                                                           |
| [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | Importe une identité d’homologue. Si l’identité de l’homologue existe sur un ordinateur, l' **homologue \_ E \_ \_ existe déjà** est retourné.                                                                                                                                                                                        |
| [**PeerIdentitySetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | Modifie le nom convivial d’une identité d’homologue spécifiée. Le nom convivial est le nom explicite.                                                                                                                                                                                                |



 

 

 



