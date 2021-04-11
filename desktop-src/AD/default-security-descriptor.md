---
title: Descripteur de sécurité par défaut
description: Avec Active Directory Domain Services, vous pouvez également spécifier la sécurité par défaut pour chaque type d’objet.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descripteur de sécurité par défaut AD
- descripteurs de sécurité Active Directory, par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031025"
---
# <a name="default-security-descriptor"></a>Descripteur de sécurité par défaut

Avec Active Directory Domain Services, vous pouvez également spécifier la sécurité par défaut pour chaque type d’objet. Cela est spécifié dans l’attribut [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de la définition de l’objet [**classSchema**](/windows/desktop/ADSchema/c-classschema) dans le [schéma Active Directory](active-directory-schema.md). Ce descripteur de sécurité est utilisé pour fournir la protection par défaut sur l’objet si aucun descripteur de sécurité n’est spécifié lors de la création de l’objet.

> [!Note]  
> Les entrées du descripteur de sécurité par défaut sont gérées comme si elles avaient été spécifiées dans le cadre de la création de l’objet. Par conséquent, les ACE par défaut sont placées avant les ACE héritées et les remplacent, le cas échéant. Pour plus d’informations, consultez [ordre des entrées de commande dans une liste DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

Le [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) est spécifié dans un format de chaîne spécial à l’aide du langage SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ). Deux fonctions peuvent être utilisées pour convertir le format binaire du descripteur de sécurité en format de chaîne et vice versa. Ces fonctions sont les suivantes :

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [Convertstringsecuritydescriptortosecuritydescriptor a](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Pour plus d’informations et pour connaître les descripteurs de sécurité par défaut des classes d’objets prédéfinies, consultez les pages de référence de la classe dans la référence de schéma Active Directory de la [référence de Active Directory Domain Services](active-directory-domain-services-reference.md).

Pour plus d’informations et pour obtenir un exemple de code qui lit ou modifie la propriété [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) d’une classe d’objet, consultez [lecture du DefaultSecurityDescriptor pour une classe d’objet](reading-the-defaultsecuritydescriptor-for-an-object-class.md) et [modification de DefaultSecurityDescriptor pour une classe d’objet](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).

 

 