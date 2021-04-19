---
title: Utilisation d’un compte d’utilisateur de domaine en tant que compte d’ouverture de session de service
description: Un compte d’utilisateur de domaine permet au service de tirer pleinement parti des fonctionnalités de sécurité du service de Windows et de Microsoft Active Directory Domain Services.
ms.assetid: 03c486fd-faec-450c-9348-314680eb73cb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.custom: contperf-fy21q3
ms.openlocfilehash: f482359eb8445cacef12c46716ecde662a95d46d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106537298"
---
# <a name="using-a-domain-user-account-as-a-service-logon-account"></a>Utilisation d’un compte d’utilisateur de domaine en tant que compte d’ouverture de session de service

Un compte d’utilisateur de domaine permet au service de tirer pleinement parti des fonctionnalités de sécurité du service de Windows et de Microsoft Active Directory Domain Services. Le service dispose de tout accès local et réseau accordé au compte, ou à tous les groupes dont le compte est membre. Le service peut prendre en charge l’authentification mutuelle Kerberos.

> [!Note]  
> La documentation suivante est destinée aux développeurs. Si vous êtes un utilisateur final à la recherche d’informations sur un message d’erreur impliquant des comptes d’utilisateur de domaine, consultez les forums de la [communauté Microsoft](https://answers.microsoft.com). Pour plus d’informations sur la gestion des comptes d’utilisateur de domaine, voir [TechNet](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754217(v=ws.11)).

L’avantage de l’utilisation d’un compte d’utilisateur de domaine est que les actions du service sont limitées par les droits d’accès et les privilèges associés au compte. Contrairement `LocalSystem` à un service, les bogues dans un service de compte d’utilisateur ne peuvent pas endommager le système. Si le service est compromis par une attaque de sécurité, il est isolé des opérations que le système autorise l’exécution du compte d’utilisateur. En même temps, les clients qui exécutent à différents niveaux de privilège peuvent se connecter au service, ce qui permet au service d’emprunter l’identité d’un client pour effectuer des opérations sensibles.

Le compte d’utilisateur d’un service ne doit pas être membre d’un groupe d’administrateurs local, de domaine ou d’entreprise. Si votre service a besoin de privilèges d’administrateur local, exécutez-le sous le `LocalSystem` compte. Pour les opérations qui requièrent des privilèges d’administrateur de domaine, exécutez-les en empruntant l’identité du contexte de sécurité d’une application cliente.

Une instance de service qui utilise un compte d’utilisateur de domaine nécessite une action administrative périodique pour gérer le mot de passe du compte. Le gestionnaire de contrôle des services (SCM) sur l’ordinateur hôte d’une instance de service met en cache le mot de passe du compte pour une utilisation dans la journalisation du service. Lorsque vous modifiez le mot de passe du compte, vous devez également mettre à jour le mot de passe mis en cache sur l’ordinateur hôte sur lequel le service est installé. Pour plus d’informations et pour obtenir un exemple de code, consultez [modification du mot de passe sur le compte d’utilisateur d’un service](changing-the-password-on-a-serviceampaposs-user-account.md). Vous pouvez éviter la maintenance régulière en laissant le mot de passe inchangé, mais cela augmenterait la probabilité d’une attaque de mot de passe sur le compte de service. Sachez que même si le SCM stocke le mot de passe dans une partie sécurisée du Registre, il est néanmoins soumis à des attaques.

Un compte d’utilisateur de domaine a deux formats de nom : le nom unique de l’objet utilisateur dans le répertoire et le <domain> \\ <username> format «» utilisé par le gestionnaire de contrôle des services locaux. Pour plus d’informations et pour obtenir un exemple de code qui convertit d’un format à l’autre, consultez [conversion de formats de nom de compte de domaine](converting-domain-account-name-formats.md).

 

 
