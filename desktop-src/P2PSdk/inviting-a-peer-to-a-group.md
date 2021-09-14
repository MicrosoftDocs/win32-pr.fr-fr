---
description: Cette rubrique décrit le processus d’invitation d’un pair à joindre un groupe homologue à l’aide des API de regroupement pair.
ms.assetid: 6afcbfec-b1df-45cd-8a43-221dfe5d8c33
title: Invitation d’un pair à un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68b1e8852f58387d424944d4a8821f56b5e11e8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009225"
---
# <a name="inviting-a-peer-to-a-group"></a>Invitation d’un pair à un groupe

Cette rubrique décrit le processus d’invitation d’un pair à joindre un groupe homologue à l’aide des API de regroupement pair.

Un groupe homologue requiert des informations d’identification valides pour participer. Les informations d’identification sont délivrées en dehors d’un groupe sous la forme d’invitations, ou directement aux membres d’un groupe lorsque des mises à jour des informations d’identification sont nécessaires.

## <a name="group-member-certificates"></a>Certificats de membre de groupe

Un groupe homologue est créé lorsqu’une application effectue un appel à [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate).

Pour participer à un groupe pair, chaque homologue doit avoir une identité d’homologue. Appelez [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities) jusqu’à ce que toutes les identités d’homologue définies pour l’homologue aient été retournées, puis sélectionnez celle qui doit être utilisée. Si une identité d’homologue n’existe pas, créez-en une en appelant [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).

Chaque identité d’homologue est associée à un ensemble spécifique d’informations d’identification qui peuvent être utilisées pour prouver l’appartenance à un groupe homologue lors de la connexion, ainsi que lors de la publication d’enregistrements ou de l’invitation de membres supplémentaires. Ces informations d’identification sont représentées sous forme de chaînes de [certificats X. 509](https://www.ietf.org/rfc/rfc2511.txt) appelés « certificats d’appartenance au groupe » (GMC).

Pour créer le GMC pour une identité d’homologue, vous devez d’abord obtenir sa clé publique. Cette clé est obtenue en appelant [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) sur l’invitation potentielle et en passant son identité d’homologue. Cette fonction renvoie un certificat encodé en base 64 (IDC) qui contient la clé publique RSA utilisée pour créer le GMC pour l’identité de l’homologue (entre autres choses), encapsulée dans un objet BLOB XML, au format suivant :

``` syntax
<PEERIDENTITYINFO VERSION="1.0">
     <IDC xmlns:dt="urn:schemas-microsoft-com:datatypes" dt:dt="bin.base64">
          <!-- Base-64 encoded certificate  -->
     </IDC>
</PEERIDENTITYINFO>
```

Cette chaîne peut être passée à [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), qui retourne une invitation qui contient le GMC pour cette identité d’homologue. L’invitation doit être passée à l’invité à l’aide d’un processus différent, tel que le courrier électronique, FTP ou un partage de fichiers sécurisé.

L’IDC lui-même peut également être placé dans une nouvelle structure d’informations sur les [**\_ informations d’identification \_ de l’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) et être passé à [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials), ce qui génère de la même manière une invitation.

Notez que les applications ne sont pas autorisées à ajouter des balises dans la balise **PEERIDENTITYINFO** ou à modifier ce fragment XML de quelque manière que ce soit. Les applications sont autorisées à incorporer ce fragment XML dans d’autres documents XML, mais doivent supprimer toutes les données XML spécifiques à l’application avant de passer ce fragment aux fonctions [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) ou [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) .

Les GMCs membres sont émis par les administrateurs et le créateur du groupe homologue. Les membres doivent obtenir de nouvelles GMCs avec des durées de vie étendues de leur GMCs avant que le délai d’expiration soit écoulé. L’administrateur du groupe homologue émet des informations d’identification mises à jour en appelant [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) avec les informations d’identification existantes pour cet homologue.

La structure des [**\_ \_ informations d’identification de l’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) contient les données de base sur l’état d’appartenance d’un homologue, y compris la clé publique pour leur GMC. Les informations d’identification nouvellement émises peuvent être publiées dans le groupe homologue en définissant l' \_ indicateur des informations d’identification du magasin du groupe homologue \_ \_ dans l’appel à [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Lorsque le destinataire des nouvelles informations d’identification rejoint le groupe homologue, les informations d’identification existantes sont mises à jour par l’infrastructure de regroupement pair.

## <a name="issuing-an-invitation"></a>Émission d’une invitation

Un membre est invité à rejoindre le groupe homologue de l’une des deux manières suivantes :

-   Un administrateur de groupe homologue appelle [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation), en transmettant la chaîne XML des informations d’identité obtenue de l’invitation potentielle via un mécanisme hors bande commun, tel qu’un e-mail ou une session de messagerie instantanée. L’invitation est également transmise par un processus ou un mécanisme externe à l’homologue, qui le recevra finalement sous la forme d’une chaîne XML ou d’un fichier texte.
-   Un administrateur de groupe homologue appelle [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Pour utiliser cette fonction, l’homologue doit déjà avoir publié les informations d’appartenance au groupe homologue ([**\_ membre homologue**](/windows/desktop/api/P2P/ns-p2p-peer_member)) ou disposer d’une clé publique disponible (de la paire de clés RSA utilisée pour créer l’identité de sujet). Dans le premier cas, la structure des [**\_ \_ informations d’identification de l’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) requise pour **PeerGroupIssueCredentials** peut être obtenue à partir de la structure de **\_ membre homologue** . dans ce dernier cas, une nouvelle structure **\_ d' \_ informations d’informations d’identification de pair** peut être remplie avec la clé publique.

Une fois la chaîne d’invitation reçue, l’homologue la transmet à [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) pour joindre le groupe homologue. Si l’appel à **PeerGroupJoin** réussit, l’homologue peut ensuite ouvrir le groupe homologue en appelant [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen).

## <a name="parsing-an-invitation"></a>Analyse d’une invitation

Si vous le souhaitez, vous pouvez analyser une invitation en appelant [**PeerGroupParseInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupparseinvitation), qui retourne une structure d' [**\_ \_ informations d’invitation d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_invitation_info) . Les champs de la structure peuvent être facilement obtenus à des fins d’affichage.

 

 



