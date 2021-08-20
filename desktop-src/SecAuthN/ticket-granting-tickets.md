---
description: Au fur et à mesure que le protocole Kerberos était conçu à l’origine, une clé principale pour un utilisateur était dérivée d’un mot de passe fourni par l’utilisateur.
ms.assetid: b8fcb68d-751e-4495-ab92-8b70c96aaa7a
title: Tickets de Ticket-Granting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd56ef05ce2ea9149b9bd35ef17dc684973f7125026f474e5a8dd3d1d14ff4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916381"
---
# <a name="ticket-granting-tickets"></a>Tickets de Ticket-Granting

Au fur et à mesure que le [*protocole Kerberos*](../secgloss/k-gly.md) était conçu à l’origine, une clé principale pour un utilisateur était dérivée d’un mot de passe fourni par l’utilisateur. Lorsqu’un utilisateur a ouvert une session, le client Kerberos sur la station de travail de l’utilisateur a accepté le mot de passe de l’utilisateur et l’a converti en clé de chiffrement en passant le texte par le biais d’une fonction de [*hachage*](../secgloss/h-gly.md) unidirectionnelle. Le hachage résultant était la [*clé principale*](../secgloss/m-gly.md)de l’utilisateur. Le client a utilisé cette *clé principale* pour déchiffrer les [*clés de session*](../secgloss/s-gly.md) reçues du KDC.

Le problème avec la conception Kerberos d’origine est que le client a besoin de la clé principale de l’utilisateur chaque fois qu’il déchiffre une clé de session à partir du KDC. Autrement dit, soit le client doit demander le mot de passe au début de chaque échange client/serveur, soit le client doit stocker la clé de l’utilisateur sur la station de travail. Les interruptions fréquentes de l’utilisateur sont trop intrusives. Le stockage de la clé sur les risques de la station de travail compromettre une clé dérivée du mot de passe de l’utilisateur, qui est une clé à long terme.

La solution du protocole Kerberos à ce problème est que le client récupère une clé temporaire auprès du KDC. Cette clé temporaire est correcte uniquement pour cette [*session de connexion*](../secgloss/l-gly.md). Lorsqu’un utilisateur ouvre une session, le client demande un ticket au KDC de la même manière qu’un ticket pour un autre service. Le centre de distribution de clés répond en créant une clé de session de connexion et un ticket pour un serveur spécial, le service d’accord de tickets complet du KDC. Une copie de la clé de session de connexion est incorporée dans le ticket et le ticket est chiffré avec la clé principale du KDC. Une autre copie de la clé de session de connexion est chiffrée avec la clé principale de l’utilisateur dérivée du mot de passe d’ouverture de session de l’utilisateur. Le ticket et la clé de session chiffrée sont envoyés au client.

Lorsque le client reçoit la réponse du KDC, il déchiffre la clé de session de connexion avec la clé principale de l’utilisateur dérivée du mot de passe de l’utilisateur. Le client n’a plus besoin de la clé dérivée du mot de passe de l’utilisateur, car le client utilise désormais la clé de session de connexion pour déchiffrer sa copie de la clé de session du serveur qu’il obtient du KDC. Le client stocke la clé de session de connexion dans son cache de tickets, ainsi que son ticket pour le service d’accord de ticket complet du KDC.

Le ticket du service d’accord de ticket complet est appelé ticket TGT (Ticket-Granting Ticket). Lorsque le client demande un ticket au centre de gestion de clés pour un serveur, il présente les [*informations d’identification*](../secgloss/c-gly.md) sous la forme d’un message d’authentificateur et d’un ticket, dans ce cas un TGT, de la même manière qu’il présente des informations d’identification à un autre service. Le service d’accord de tickets ouvre le ticket TGT avec sa clé principale, extrait la clé de session de connexion pour ce client et utilise la clé de session de connexion pour chiffrer la copie du client d’une clé de session pour le serveur.

 

 
