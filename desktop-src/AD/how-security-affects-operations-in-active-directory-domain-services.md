---
title: Impact de la sécurité sur les opérations dans Active Directory Domain Services
description: Active Directory Domain Services utiliser le contrôle d’accès pour accorder ou refuser l’accès aux objets, aux propriétés et aux opérations en fonction de l’identité de l’utilisateur qui effectue la tentative d’accès.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Effets de sécurité dans Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8f5599afbc8552f9708fcfa953a069f429a152c4f0fff37546ffb7d9f6b809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188204"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Impact de la sécurité sur les opérations dans Active Directory Domain Services

Active Directory Domain Services utiliser le contrôle d’accès pour accorder ou refuser l’accès aux objets, aux propriétés et aux opérations en fonction de l’identité de l’utilisateur qui effectue la tentative d’accès. Lorsque votre application est liée à l’annuaire, elle est liée à des informations d’identification spécifiques de l’utilisateur. Une fois authentifiés, ces informations d’identification déterminent le contexte de sécurité de votre application. Indépendamment du fait que les informations d’identification correspondent à celles de l’utilisateur connecté, d’un utilisateur spécifié, d’un compte de service, d’un compte d’ordinateur ou d’un utilisateur non authentifié (invité/tout le monde), le serveur de Active Directory vérifie le droit de l’utilisateur d’accéder à un objet avant l’exécution d’une opération sur cet objet. L’utilisateur peut ou non avoir accès à un objet particulier, à ses enfants, à ses propriétés ou à ses opérations sur cet objet, ce qui signifie que votre application doit gérer les erreurs potentielles provoquées par l’accès refusé.

Pour plus d’informations sur les contextes de sécurité et les effets du contrôle d’accès sur diverses opérations, consultez :

-   [Opérations de Access Control et de lecture](access-control-and-read-operations.md)
-   [Opérations d’Access Control et d’écriture](access-control-and-write-operations.md)
-   [Access Control et création d’objets](access-control-and-object-creation.md)
-   [Access Control et suppression d’objets](access-control-and-object-deletion.md)

 

 




