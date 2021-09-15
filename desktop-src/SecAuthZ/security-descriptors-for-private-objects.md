---
description: Pour créer un descripteur de sécurité, un serveur protégé peut utiliser la même procédure que celle qu’une application utiliserait pour créer un descripteur de sécurité pour un objet sécurisable.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descripteurs de sécurité pour les objets privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c40dc5c4e9f0a3d0e641874153d2862d038a19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413470"
---
# <a name="security-descriptors-for-private-objects"></a>Descripteurs de sécurité pour les objets privés

Pour créer un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly), un serveur protégé peut utiliser la même procédure que celle qu’une application utiliserait pour créer un descripteur de sécurité pour un objet sécurisable. Pour obtenir un exemple de code, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md). Une application serveur protégée peut également appeler la fonction [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) pour effectuer cette opération. Si un pointeur vers un [*descripteur de sécurité auto-relatif*](/windows/desktop/SecGloss/s-gly) existant est fourni à **BuildSecurityDescriptor**, il génère le nouveau descripteur de sécurité avec les informations provenant de ce descripteur de sécurité fusionnées avec les nouvelles informations de contrôle d’accès passées comme paramètres dans l’appel de fonction. Le propriétaire et le groupe sont éventuellement spécifiés par les structures de [**tiers de confiance**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) transmises à la fonction. Le descripteur de sécurité créé par **BuildSecurityDescriptor** est au format *auto-relatif* .

en outre, l’API Windows fournit un ensemble de fonctions pour fusionner les informations de sécurité du client avec les informations héritées du descripteur de sécurité pour un objet parent ou à partir d’un descripteur de sécurité par défaut. Les fonctions [**CreatePrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity), [**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity), [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)et [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) permettent de récupérer des informations par défaut à partir d’un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly), de prendre en charge l’héritage et de manipuler des parties spécifiques du descripteur de sécurité. Cela peut être utile lorsqu’un client crée un objet privé dans une hiérarchie d’objets sécurisés. Par exemple, vous pouvez utiliser la fonction **CreatePrivateObjectSecurity** pour créer un descripteur de sécurité qui contenait des ACE spécifiées par le client, des ACE héritées d’un objet parent et le propriétaire par défaut à partir du jeton d’accès de création du client. Alors que [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) crée des descripteurs de sécurité à partir des informations de contrôle d’accès passées dans l’appel de fonction ou à partir d’un descripteur de sécurité existant, **CreatePrivateObjectSecurity** crée un descripteur de sécurité uniquement à partir des informations contenues dans les descripteurs de sécurité existants.

La fonction [**LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) obtient les informations de descripteur de sécurité à partir d’un [*descripteur de sécurité auto-relatif*](/windows/desktop/SecGloss/s-gly)existant. Ces informations incluent la spécification du propriétaire et du groupe, le nombre d’entrées de du SACL ou DACL, ainsi que la liste des ACE dans la liste SACL ou DACL.

 

 
