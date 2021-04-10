---
description: Échange client/serveur
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Échange client/serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114943"
---
# <a name="clientserver-exchange"></a>Échange client/serveur

Une fois qu’un utilisateur a un ticket vers un serveur, le client de station de travail peut établir une session de communication sécurisée avec ce serveur.

**Pour établir une session de communication sécurisée avec un serveur**

1.  Le client envoie au serveur un message de type KRB \_ AP \_ req (demande d’application Kerberos). Ce message contient un message d’authentificateur chiffré avec la clé envoyée par le [*Centre de distribution de clés*](/windows/desktop/SecGloss/k-gly) (KDC) pour la session avec le serveur, le ticket pour les sessions avec le serveur et un indicateur qui indique si le client demande une authentification mutuelle. La définition de l’indicateur qui demande l’authentification mutuelle est l’une des options de configuration de [*Kerberos*](/windows/desktop/SecGloss/k-gly). L’utilisateur n’est jamais invité à utiliser l’authentification mutuelle.
2.  Le serveur reçoit une \_ demande KRB AP \_ , déchiffre le ticket, puis extrait les données d’autorisation de l’utilisateur et la [*clé de session*](/windows/desktop/SecGloss/s-gly).
3.  Le serveur utilise la clé de session du ticket pour déchiffrer le message de l’authentificateur de l’utilisateur et évalue l’horodatage à l’intérieur de.
4.  Si le message de l’authentificateur est valide, le serveur vérifie l’indicateur d’authentification mutuelle dans la demande du client.
5.  Si l’indicateur d’authentification mutuelle est défini, le serveur utilise la clé de session pour chiffrer l’heure à partir du message de l’authentificateur de l’utilisateur et retourne le résultat dans un message de type KRB \_ AP \_ Rep (réponse de l’application Kerberos).
6.  Lorsque le client reçoit un \_ \_ REP AP, il déchiffre le message de l’authentificateur du serveur avec la clé de session qu’il partage avec le serveur et compare l’heure renvoyée par le service à l’heure de son message d’authentificateur d’origine. S’ils correspondent, le client est assuré que le service est authentique et que la connexion se poursuit.

 

 
