---
description: Les groupes homologues requièrent que chaque membre possède un certificat spécifique, appelé certificat de membre de groupe (GMC).
ms.assetid: 3966d4eb-4504-4b1e-9c9f-6eab7751d7ed
title: Fonctionnement de la sécurité de groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d272e9a0567c6edc300a52cfa206305253ec5a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009243"
---
# <a name="how-group-security-works"></a>Fonctionnement de la sécurité de groupe

Les groupes homologues requièrent que chaque membre possède un certificat spécifique, appelé certificat de membre de groupe (GMC). Le certificat GMC garantit que tous les enregistrements échangés entre les pairs sont signés numériquement. La clé publique d’un homologue est contenue dans les structures qui sont passées dans le cadre de la communication entre les homologues, y compris les [**\_ \_ informations d’identification de l’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info).

Un GMC peut être émis dans une chaîne. Par exemple, un créateur peut émettre un GMC pour l’administrateur A, qui peut émettre un GMC à l’administrateur B, qui peut émettre un GMC pour le membre M. La chaîne GMC obtenue est : Creator->A->B->M, dont la longueur est égale à 4. La longueur de chaîne est importante, car elle ne peut pas être supérieure à 24. Si le 24 administrateur d’une chaîne tente d’émettre un GMC à un membre, [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) ou [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) retourne une chaîne d’homologue \_ E \_ \_ trop \_ longue.

Un GMC peut également être émis en appelant [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials). Un GMC implique l’appartenance de l’utilisateur au groupe pour lequel le GMC est émis, et peut avoir une durée de vie limitée ou infinie. L’activité des membres du groupe ne peut pas être plus longue que la durée de vie spécifiée dans GMC.

> [!Note]  
> Une durée de vie infinie de GMC est actuellement définie à 1000 ans.

 

L’activité des membres du groupe est limitée par la durée de vie GMC et comprend les éléments suivants :

-   **Opérations d’enregistrement** : un homologue ne peut pas publier d’informations dans un groupe après l’expiration de l’appartenance à un groupe, ou publier des enregistrements dont la durée de vie est plus longue que la durée de vie de l’appartenance au groupe de l’homologue.
-   **Opérations d’appartenance** -un administrateur de groupe ne peut pas émettre une appartenance qui a une durée de vie supérieure à la date spécifiée dans l’appartenance à un administrateur de groupe. Par exemple, si un administrateur a 500 heures restantes à sa durée de vie GMC, toutes les appartenances émises doivent être inférieures à 500 heures.

Comme un membre du groupe ne peut pas avoir une durée de vie plus longue que l’administrateur qui invite ce membre du groupe, il est recommandé de définir la durée de vie GMC d’un administrateur comme étant infinie ou pour une durée de vie très longue. Par défaut, le créateur du groupe a une durée de vie infinie.

## <a name="renewing-group-membership"></a>Renouvellement de l’appartenance à un groupe

Pour renouveler les informations d’identification d’un administrateur ou d’un membre dont la durée de vie GMC est prête à expirer, vous disposez des deux options suivantes :

-   Appelez [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) et transmettez l’identité du membre dont la durée de vie est prête à expirer. Si les informations d’identification sont spécifiées comme **null** et que les informations d’appartenance de l’homologue sont disponibles pour le groupe, la durée de renouvellement est définie sur la même durée que celle spécifiée dans les informations d’identification du membre précédemment publiées. Si une autre période de durée doit être spécifiée, une nouvelle structure [**\_ d' \_ informations d’identification d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) doit être fournie et contient la nouvelle durée de vie, puis une nouvelle GMC est publiée pour le membre.

    La fonction [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials) prend éventuellement l' \_ \_ indicateur des informations d’identification du magasin du groupe homologue \_ , qui publie automatiquement les nouvelles informations d’identification du membre dans la base de données du groupe. Lorsque le membre se connecte au groupe la prochaine fois, pour la première fois ou après une mise hors connexion, le membre obtient le GMC mis à jour de la base de données.

-   Appelez [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) pour transmettre l’identité du membre dont la durée de vie GMC est prête à expirer. Si l’expiration spécifiée dans l’invitation est **null**, la durée de vie du GMC est la même que celle de l’administrateur GMC qui émet l’appartenance. Si le créateur spécifie l’expiration comme **null**, un GMC avec une durée de vie infinie est émis.

    Si un homologue reçoit un GMC qui expire avant la valeur de durée de vie de présence, les adresses de l’homologue ne sont pas disponibles dans les structures de [**\_ membres homologues**](/windows/desktop/api/P2P/ns-p2p-peer_member) retournées dans l’énumération lancée par un appel à [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Cela se produit parce que les informations de présence ne sont pas publiées dans ce cas, même si l’indicateur de présence de désactivation d’HOMOLOGUe \_ \_ n’est pas défini.

 

 



