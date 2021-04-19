---
description: Vous pouvez affecter des privilèges aux comptes en utilisant le composant logiciel enfichable MMC (Microsoft Management Console) de la stratégie de sécurité locale (secpol. msc) ou en appelant la fonction LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Attribution de privilèges à un compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530126"
---
# <a name="assigning-privileges-to-an-account"></a>Attribution de privilèges à un compte

Vous pouvez affecter des privilèges aux comptes en utilisant le composant logiciel enfichable MMC (Microsoft Management Console) de la stratégie de sécurité locale (secpol. msc) ou en appelant la fonction [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .

L’attribution d’un privilège à un compte n’affecte pas les jetons utilisateur existants. Un utilisateur doit se déconnecter puis se reconnecter pour obtenir un jeton d’accès avec le privilège qui vient d’être attribué.

Pour affecter des privilèges à l’aide du composant logiciel enfichable MMC stratégie de sécurité locale, modifiez la liste des utilisateurs pour chaque privilège répertorié sous **paramètres de sécurité/stratégies locales/attribution des droits utilisateur**.

 

 
