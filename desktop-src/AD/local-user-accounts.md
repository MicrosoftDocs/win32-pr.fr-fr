---
title: Utilisation d’un compte d’utilisateur local en tant que compte d’ouverture de session de service
description: Un compte d’utilisateur local (format de nom \ 0034 ;. \\ Nom d’utilisateur \ 0034 ;) existe uniquement dans la base de données SAM de l’ordinateur hôte ; Il n’a pas d’objet utilisateur dans Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100593"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>Utilisation d’un compte d’utilisateur local en tant que compte d’ouverture de session de service

Un compte d’utilisateur local (format de nom : ". \\ *Username*") existe uniquement dans la base de données Sam de l’ordinateur hôte ; Il n’a pas d’objet utilisateur dans Active Directory Domain Services. Cela signifie qu’un compte local ne peut pas être authentifié par le domaine. Par conséquent, un service qui s’exécute dans le contexte de sécurité d’un compte d’utilisateur local n’a pas accès aux ressources réseau (sauf s’il s’agit d’un utilisateur anonyme) et il ne peut pas prendre en charge l’authentification mutuelle Kerberos dans laquelle le service est authentifié par ses clients. Pour ces raisons, les comptes d’utilisateur locaux sont généralement inappropriés pour les services d’annuaire. Côté plus, les bogues dans le service ne peuvent pas endommager le système. Si votre service peut s’exécuter sous ces limites, il doit le faire.

 

 




