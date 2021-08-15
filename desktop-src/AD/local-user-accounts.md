---
title: Utilisation d’un compte d’utilisateur local en tant que compte d’ouverture de session de service
description: Un compte d’utilisateur local (format de nom \ 0034 ;. \\ Nom d’utilisateur \ 0034 ;) existe uniquement dans la base de données SAM de l’ordinateur hôte ; Il n’a pas d’objet utilisateur dans Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a6d536b83675cc3d4fa9c23db01d8f4137fff228bf72444bec7164a51068ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186854"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>Utilisation d’un compte d’utilisateur local en tant que compte d’ouverture de session de service

Un compte d’utilisateur local (format de nom : ". \\ *Username*") existe uniquement dans la base de données Sam de l’ordinateur hôte ; Il n’a pas d’objet utilisateur dans Active Directory Domain Services. Cela signifie qu’un compte local ne peut pas être authentifié par le domaine. Par conséquent, un service qui s’exécute dans le contexte de sécurité d’un compte d’utilisateur local n’a pas accès aux ressources réseau (sauf s’il s’agit d’un utilisateur anonyme) et il ne peut pas prendre en charge l’authentification mutuelle Kerberos dans laquelle le service est authentifié par ses clients. Pour ces raisons, les comptes d’utilisateur locaux sont généralement inappropriés pour les services d’annuaire. Côté plus, les bogues dans le service ne peuvent pas endommager le système. Si votre service peut s’exécuter sous ces limites, il doit le faire.

 

 




