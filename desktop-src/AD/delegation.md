---
title: La délégation
description: La délégation est l’une des fonctionnalités de sécurité les plus importantes de Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- AD de délégation
- sécurité AD, délégation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939649"
---
# <a name="delegation"></a>La délégation

La *délégation* est l’une des fonctionnalités de sécurité les plus importantes de Active Directory Domain Services. La délégation permet à une autorité administrative plus élevée d’accorder des droits d’administration spécifiques pour des conteneurs et des sous-arbres à des individus et des groupes. Les administrateurs de domaine, avec une autorité étendue sur de grands segments d’utilisateurs, ne sont plus nécessaires.

Une entrée du contrôle d’accès peut accorder des droits d’administration spécifiques pour les objets d’un conteneur à un utilisateur ou à un groupe. Des droits sont accordés pour des opérations spécifiques sur des classes d’objets spécifiques utilisant des ACE dans la liste de contrôle d’accès du conteneur. Par exemple, pour permettre à un utilisateur nommé « utilisateur 1 » d’être administrateur de l’unité d’organisation comptabilité d’entreprise, ajoutez des ACE à la liste de contrôle d’accès sur « comptabilité d’entreprise » comme suit :

« utilisateur 1 »; Licence Créer, modifier, supprimer ; utilisateur de classe objet « utilisateur 1 »; Licence Créer, modifier, supprimer ; objet-classe groupe « utilisateur 1 »; Licence Écriture ; utilisateur de classe d’objet ; Mot de passe d’attribut»

Désormais, l’utilisateur 1 peut créer des utilisateurs et des groupes dans la comptabilité d’entreprise et définir les mots de passe pour les utilisateurs existants, mais l’utilisateur 1 ne peut pas créer d’autres classes d’objets et ne peut pas affecter les utilisateurs dans d’autres conteneurs, sauf si, bien sûr, l’utilisateur 1 est autorisé à accéder aux autres conteneurs par les ACE.

 

 




