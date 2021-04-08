---
title: Impact de la sécurité sur les opérations dans Active Directory Domain Services
description: Active Directory Domain Services utiliser le contrôle d’accès pour accorder ou refuser l’accès aux objets, aux propriétés et aux opérations en fonction de l’identité de l’utilisateur qui effectue la tentative d’accès.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Effets de sécurité dans Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839306"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a><span data-ttu-id="b6ca6-104">Impact de la sécurité sur les opérations dans Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="b6ca6-104">How Security Affects Operations in Active Directory Domain Services</span></span>

<span data-ttu-id="b6ca6-105">Active Directory Domain Services utiliser le contrôle d’accès pour accorder ou refuser l’accès aux objets, aux propriétés et aux opérations en fonction de l’identité de l’utilisateur qui effectue la tentative d’accès.</span><span class="sxs-lookup"><span data-stu-id="b6ca6-105">Active Directory Domain Services use access control to grant or deny access to objects, properties, and operations based on the identity of the user performing the access attempt.</span></span> <span data-ttu-id="b6ca6-106">Lorsque votre application est liée à l’annuaire, elle est liée à des informations d’identification spécifiques de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6ca6-106">When your application binds to the directory, it binds with specific user credentials.</span></span> <span data-ttu-id="b6ca6-107">Une fois authentifiés, ces informations d’identification déterminent le contexte de sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="b6ca6-107">When authenticated, these credentials determine your application's security context.</span></span> <span data-ttu-id="b6ca6-108">Indépendamment du fait que les informations d’identification correspondent à celles de l’utilisateur connecté, d’un utilisateur spécifié, d’un compte de service, d’un compte d’ordinateur ou d’un utilisateur non authentifié (invité/tout le monde), le serveur de Active Directory vérifie le droit de l’utilisateur d’accéder à un objet avant l’exécution d’une opération sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="b6ca6-108">Regardless of whether the credentials are those of the logged-on user, a specified user, a service account, a computer account, or an unauthenticated user (Guest/Everyone), the Active Directory server verifies the user's right to access an object before any operation is performed on that object.</span></span> <span data-ttu-id="b6ca6-109">L’utilisateur peut ou non avoir accès à un objet particulier, à ses enfants, à ses propriétés ou à ses opérations sur cet objet, ce qui signifie que votre application doit gérer les erreurs potentielles provoquées par l’accès refusé.</span><span class="sxs-lookup"><span data-stu-id="b6ca6-109">The user may, or may not, have access to a particular object, its children, its properties, or operations on that object, which means that your application must handle the potential errors caused by denied access.</span></span>

<span data-ttu-id="b6ca6-110">Pour plus d’informations sur les contextes de sécurité et les effets du contrôle d’accès sur diverses opérations, consultez :</span><span class="sxs-lookup"><span data-stu-id="b6ca6-110">For more information about security contexts and the effects of access control on various operations, see:</span></span>

-   [<span data-ttu-id="b6ca6-111">Opérations de Access Control et de lecture</span><span class="sxs-lookup"><span data-stu-id="b6ca6-111">Access Control and Read Operations</span></span>](access-control-and-read-operations.md)
-   [<span data-ttu-id="b6ca6-112">Opérations d’Access Control et d’écriture</span><span class="sxs-lookup"><span data-stu-id="b6ca6-112">Access Control and Write Operations</span></span>](access-control-and-write-operations.md)
-   [<span data-ttu-id="b6ca6-113">Access Control et création d’objets</span><span class="sxs-lookup"><span data-stu-id="b6ca6-113">Access Control and Object Creation</span></span>](access-control-and-object-creation.md)
-   [<span data-ttu-id="b6ca6-114">Access Control et suppression d’objets</span><span class="sxs-lookup"><span data-stu-id="b6ca6-114">Access Control and Object Deletion</span></span>](access-control-and-object-deletion.md)

 

 




