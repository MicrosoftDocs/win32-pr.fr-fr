---
title: Définition des descripteurs de sécurité sur les nouveaux objets d’annuaire
description: Lorsque vous créez un objet dans Active Directory Domain Services, vous pouvez créer explicitement un descripteur de sécurité, puis définir ce descripteur de sécurité en tant que propriété nTSecurityDescriptor de l’objet.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- objets AD, comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire
- descripteurs de sécurité Active Directory, comment définir sur de nouveaux objets d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7858d08944e93165b4a1a63ef7d845ee646dc648
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462855"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Définition des descripteurs de sécurité sur les nouveaux objets d’annuaire

Lorsque vous créez un objet dans Active Directory Domain Services, vous pouvez créer explicitement un descripteur de sécurité, puis définir ce descripteur de sécurité en tant que propriété **ntSecurityDescriptor** de l’objet. Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet d’annuaire](creating-a-security-descriptor-for-a-new-directory-object.md).

Active Directory Domain Services Utilisez les règles suivantes pour définir la liste DACL dans le descripteur de sécurité du nouvel objet :

-   Si vous spécifiez explicitement un descripteur de sécurité lorsque vous créez l’objet, le système fusionne toutes les entrées de contrôle d’accès héritées de l’objet parent dans la liste DACL spécifiée, sauf si le bit **\_ \_ protégé par la liste** de contrôle d’accès discrétionnaire est défini dans les bits de contrôle du descripteur de sécurité.
-   Si vous ne spécifiez pas de descripteur de sécurité, le système génère la liste DACL de l’objet en fusionnant toutes les ACE pouvant être héritées de l’objet parent dans la liste DACL par défaut de l’objet **classSchema** pour la classe de l’objet.
-   Si le schéma n’a pas de DACL par défaut, la liste DACL de l’objet est la DACL par défaut du jeton principal ou d’emprunt d’identité du créateur.
-   S’il n’existe pas d’ACL spécifiée, héritée ou par défaut, le système crée l’objet sans DACL, ce qui permet à tout le monde d’accéder entièrement à l’objet.

Le système utilise un algorithme similaire pour générer une liste SACL pour un objet de service d’annuaire.

Le propriétaire et le groupe principal du descripteur de sécurité du nouvel objet sont définis sur les valeurs que vous spécifiez dans la propriété **ntSecurityDescriptor** lors de la création de l’objet. Si vous ne définissez pas ces valeurs, Active Directory Domain Services Utilisez les règles indiquées dans le tableau suivant pour les définir.



| Règle          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Propriétaire         | Le propriétaire d’un descripteur de sécurité par défaut est défini sur le SID du propriétaire par défaut à partir du jeton principal ou d’emprunt d’identité du processus de création. Pour la plupart des utilisateurs, le SID du propriétaire par défaut est le même que le SID qui identifie le compte de l’utilisateur. N’oubliez pas que pour les utilisateurs qui sont membres du groupe Administrateurs intégré, le système définit automatiquement le SID du propriétaire par défaut dans le jeton d’accès au groupe administrateurs. par conséquent, les objets créés par un membre du groupe administrateurs sont généralement détenus par le groupe administrateurs. Pour récupérer ou définir le propriétaire par défaut dans un jeton d’accès, appelez la fonction [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) ou [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) avec la structure du [**\_ propriétaire du jeton**](/windows/desktop/api/winnt/ns-winnt-token_owner) . |
| Groupe principal | Le groupe principal dans un descripteur de sécurité par défaut est défini sur le groupe principal par défaut à partir du jeton principal ou d’emprunt d’identité du créateur. N’oubliez pas que le groupe principal n’est pas utilisé dans le contexte de Active Directory Domain Services.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Pour plus d’informations sur l’héritage des entrées du contrôle d’accès, consultez [héritage et délégation de l’administration](inheritance-and-delegation-of-administration.md).

Pour plus d’informations sur les descripteurs de sécurité par défaut dans le schéma, consultez descripteur de [sécurité par défaut](default-security-descriptor.md).

Pour plus d’informations sur les objets **classSchema** , consultez [Active Directory schéma](active-directory-schema.md).

 

 