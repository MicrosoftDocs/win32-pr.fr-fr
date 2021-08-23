---
description: Explique comment modifier des privilèges dans un jeton à l’aide des fonctions AdjustTokenPrivileges et CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Modification des privilèges dans un jeton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c511ca66c5d4739057f5ea75cae589ee97e849f659002a612e7d22fd6be8eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622749"
---
# <a name="changing-privileges-in-a-token"></a>Modification des privilèges dans un jeton

Vous pouvez modifier les privilèges dans un jeton principal ou un jeton d’emprunt d’identité de deux manières :

-   Activez ou désactivez les privilèges à l’aide de la fonction [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .
-   Limitez ou supprimez des privilèges à l’aide de la fonction [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) ne peut pas ajouter ou supprimer des privilèges du jeton. Il peut uniquement activer des privilèges existants qui sont actuellement désactivés ou désactiver des privilèges existants actuellement activés. Pour obtenir des exemples, consultez [activation et désactivation des privilèges en C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Pour affecter des privilèges à un compte d’utilisateur, consultez [attribution de privilèges à un compte](assigning-privileges-to-an-account.md).

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) dispose de fonctionnalités plus étendues, comme suit :

-   Suppression d’un privilège. Notez que la suppression d’un privilège n’est pas la même que la désactivation d’un. Une fois qu’un privilège a été supprimé d’un jeton, il ne peut pas être remis.
-   Attachement de l’attribut de refus uniquement aux sid dans le jeton. Cela a pour effet d’interdire des groupes ou des comptes spécifiques, par exemple, en refusant au groupe tout le monde de supprimer l’accès à un fichier particulier. Pour plus d’informations sur la restriction des SID, consultez [attributs SID dans un jeton d’accès](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).
-   Spécification d’une liste de sid restreints dans le jeton. Pour plus d’informations sur la restriction des SID, consultez [jetons restreints](/windows/desktop/SecAuthZ/restricted-tokens).

 

 
