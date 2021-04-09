---
description: Sécurité des composants en file d’attente
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: Sécurité des composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b51592f6216d7380e877f2cd582a277f1583b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111026"
---
# <a name="queued-components-security"></a>Sécurité des composants en file d’attente

Lorsqu’un client effectue un appel de méthode à un objet mis en file d’attente, l’appel est en fait effectué à l’enregistreur, qui le configure dans le cadre d’un message sur le serveur. L’écouteur lit le message à partir de la file d’attente et le transmet au lecteur. Le lecteur appelle le composant serveur réel et effectue le même appel de méthode. Le composant serveur doit observer le contexte de l’appel de sécurité du client (et non le contexte de l’appel de sécurité du lecteur) lorsque le joueur effectue l’appel de la méthode. L’enregistreur marshale le contexte de l’appel de sécurité du client dans le message, et le lecteur le démarshale sur le serveur avant d’effectuer l’appel de la méthode. En ce qui concerne l’objet serveur, il n’existe aucune différence dans le contexte de sécurité entre un appel direct du client et un appel indirect du joueur. En particulier, les méthodes appelées s’exécutent avec les privilèges de l’expéditeur.

Un composant COM+ mis en file d’attente prend en charge la sémantique de sécurité basée sur les rôles, tout comme les autres composants conçus pour être utilisés avec les applications COM+. Les composants d’une application en file d’attente peuvent donc utiliser les interfaces de programmation pour découvrir l’appartenance au rôle de leur appelant ([**ISecurityCallContext :: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) ou un utilisateur spécifique ([**ISecurityCallContext :: IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)). Il est recommandé que tous les composants en file d’attente présentant un impact potentiel sur la sécurité utilisent ces interfaces pour vérifier explicitement les informations d’identification de l’expéditeur.

L’identité de l’appelant est l’identité associée à un appel de méthode. L’identité de l’appelant est utilisée par la sécurité basée sur les rôles et est présente dans le contexte de l’appel de sécurité. Dans les composants en file d’attente, l’identité de l’appelant est représentée sous forme de données dans le message de Message Queuing. Message Queuing authentifie l’identité de l’expéditeur du message. Lorsque l’identité de l’appelant et l’identité de l’expéditeur du message sont identiques, Message Queuing authentifie le message et l’appelant. Il s’agit du cas habituel.

> [!Note]  
> Les composants COM+ en file d’attente ne prennent pas en charge la sécurité de type emprunt d’identité, ce qui permet à un serveur d’obtenir un jeton d’accès correspondant à l’identité du client et de l’utiliser pour effectuer des vérifications de contrôle d’accès ou pour agir dans le contexte de sécurité du client.

 

Lorsque l’appelant d’un composant en file d’attente interagit avec le composant par le biais d’un enregistreur out-of-process, les identités de l’appelant et de l’expéditeur du message (enregistreur) peuvent être différentes. Dans ce cas, les composants COM+ en file d’attente vérifient que l’expéditeur du message est membre du rôle d’utilisateur approuvé QC sur le serveur. En outre, l’enregistreur out-of-process requiert un certificat d’authentification, car il est authentifié par Message Queuing.

Les membres du rôle d’utilisateur approuvé QC sont autorisés à spécifier une identité arbitraire, ce qui signifie qu’un membre malveillant peut exécuter un appel de composant mis en file d’attente avec des privilèges élevés. Par conséquent, il est recommandé de conserver le nombre d’utilisateurs à un minimum absolu.

En raison du risque d’une attaque sophistiquée associée à un mécanisme qui propage l’identité sur un réseau, ainsi que le risque d’une attaque par déni de service simple en inondant les files d’attente avec des demandes non exécutables, il est recommandé de déployer le service composants en file d’attente COM+ uniquement sur un réseau d’hôtes approuvés, par exemple sur un réseau privé ou un réseau privé virtuel ou derrière un pare-feu configuré de manière appropriée.

Les composants COM+ en file d’attente s’exécutent sur DCOM. vous pouvez ainsi protéger l’intégrité et le secret des appels de méthode en file d’attente en sélectionnant **confidentialité du paquet** comme **niveau d’authentification des appels** sous l’onglet **sécurité** de la feuille de **Propriétés** de votre application en file d’attente.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité COM+](com--security.md)
</dt> <dt>

[Limitations de sécurité en mode groupe de travail](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[Spécification du protocole d’authentification](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



