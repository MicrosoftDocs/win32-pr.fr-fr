---
description: Dans l’exemple suivant, un socket multipoint est décrit fréquemment en définissant son rôle dans l’un des deux plans (contrôle ou données).
ms.assetid: 34f639e2-9363-4f3f-a8de-b7c5d12618c9
title: Sémantique pour joindre des feuilles multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df12683838fbad89f717b08d7a19802f24556761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520502"
---
# <a name="semantics-for-joining-multipoint-leaves"></a>Sémantique pour joindre des feuilles multipoint

Dans l’exemple suivant, un socket multipoint est décrit fréquemment en définissant son rôle dans l’un des deux plans (contrôle ou données). Il est important de comprendre que ce même socket a un rôle dans l’autre plan, mais cela n’est pas mentionné afin de conserver les références courtes. Par exemple, lorsqu’une référence est faite à un « \_ Socket racine c », il peut s’agir d’une \_ racine racine/d \_ ou d’un \_ Socket feuille c racine/d \_ .

Dans les schémas de plan de contrôle enracinés, de nouveaux nœuds terminaux sont ajoutés à une session multipoint dans l’une ou l’autre des deux méthodes. Dans la première méthode, la racine utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour établir une connexion avec un nœud terminal et l’inviter à devenir participant. Sur le nœud terminal, l’application pair doit avoir créé un \_ Socket feuille c et utilisé [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) pour le définir en mode écoute. Le nœud terminal reçoit une \_ indication FD Accept lorsqu’il est invité à rejoindre la session et signale sa volonté de s’y joindre en appelant [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). L’application racine reçoit ensuite une \_ indication FD Connect lorsque l’opération de **jointure** est terminée.

Dans la deuxième méthode, les rôles sont fondamentalement inversés. L’application racine crée un \_ Socket racine c et le définit en mode d’écoute. Un nœud feuille souhaitant rejoindre la session crée un \_ Socket feuille c et utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) pour initier la connexion et demander des admission. L’application racine reçoit le FD \_ Accept quand une requête admission entrante arrive et admet le nœud terminal en appelant [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept). Le nœud terminal reçoit FD \_ Connect lorsqu’il a été admis.

Dans un plan de contrôle sans racine, où tous les nœuds sont des \_ feuilles c, le [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) est utilisé pour initier l’inclusion d’un nœud dans une session multipoint existante. Une \_ indication FD Connect est fournie lorsque la jointure est terminée et que le descripteur de socket retourné est utilisable dans la session multipoint. Dans le cas de la multidiffusion IP, cela correspond à l' \_ option IP ajouter \_ un socket d’appartenance.

(Les lecteurs connaissant l’utilisation de la multidiffusion IP du protocole UDP sans connexion peuvent être concernés par la sémantique orientée connexion présentée ici. En particulier, la notion d’utilisation de [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) sur un socket UDP et l’attente d’une \_ indication FD Connect peut être troublantes. Toutefois, l’application d’une sémantique orientée connexion à des protocoles sans connexion est beaucoup plus importante. Elle est autorisée et parfois utile, par exemple, pour appeler la fonction de [**connexion**](/windows/desktop/api/Winsock2/nf-winsock2-connect) standard sur un socket UDP. Le résultat général de l’application de la sémantique orientée connexion aux sockets sans connexion est une restriction dans la manière dont ces Sockets peuvent être utilisés, et c’est également le cas ici. Un socket UDP utilisé dans **WSAJoinLeaf** présente certaines restrictions et attend une \_ indication FD Connect (qui, dans ce cas, indique simplement que le message IGMP correspondant a été envoyé) est une limite de ce type.)

Par conséquent, il existe trois instances où une application utilise [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) en tant que :

-   Racine multipoint et invitation à une nouvelle feuille pour rejoindre la session
-   Feuille effectuant une demande admission à une session multipoint enracinée
-   Feuille de recherche de admission dans une session multipoint sans racine (par exemple, la multidiffusion IP)

 

 



