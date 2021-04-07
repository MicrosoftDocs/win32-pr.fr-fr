---
title: La délégation
description: La délégation est l’une des fonctionnalités de sécurité les plus importantes de Active Directory Domain Services.
ms.assetid: ab8740c9-f5a2-40cc-abce-0ef80c3fca7a
ms.tgt_platform: multiple
keywords:
- AD de délégation
- sécurité AD, délégation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26be1f9350c664d289832874994e2b3ba2e696c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939649"
---
# <a name="delegation"></a><span data-ttu-id="ae60a-105">La délégation</span><span class="sxs-lookup"><span data-stu-id="ae60a-105">Delegation</span></span>

<span data-ttu-id="ae60a-106">La *délégation* est l’une des fonctionnalités de sécurité les plus importantes de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ae60a-106">*Delegation* is one of the most important security features of Active Directory Domain Services.</span></span> <span data-ttu-id="ae60a-107">La délégation permet à une autorité administrative plus élevée d’accorder des droits d’administration spécifiques pour des conteneurs et des sous-arbres à des individus et des groupes.</span><span class="sxs-lookup"><span data-stu-id="ae60a-107">Delegation enables a higher administrative authority to grant specific administrative rights for containers and subtrees to individuals and groups.</span></span> <span data-ttu-id="ae60a-108">Les administrateurs de domaine, avec une autorité étendue sur de grands segments d’utilisateurs, ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ae60a-108">Domain administrators, with broad authority over large segments of users, are no longer required.</span></span>

<span data-ttu-id="ae60a-109">Une entrée du contrôle d’accès peut accorder des droits d’administration spécifiques pour les objets d’un conteneur à un utilisateur ou à un groupe.</span><span class="sxs-lookup"><span data-stu-id="ae60a-109">An ACE can grant specific administrative rights for the objects in a container to a user or group.</span></span> <span data-ttu-id="ae60a-110">Des droits sont accordés pour des opérations spécifiques sur des classes d’objets spécifiques utilisant des ACE dans la liste de contrôle d’accès du conteneur.</span><span class="sxs-lookup"><span data-stu-id="ae60a-110">Rights are granted for specific operations on specific object classes using ACEs in the container's ACL.</span></span> <span data-ttu-id="ae60a-111">Par exemple, pour permettre à un utilisateur nommé « utilisateur 1 » d’être administrateur de l’unité d’organisation comptabilité d’entreprise, ajoutez des ACE à la liste de contrôle d’accès sur « comptabilité d’entreprise » comme suit :</span><span class="sxs-lookup"><span data-stu-id="ae60a-111">For example, to enable a user named "user 1" to be an administrator of the "Corporate Accounting" organizational unit, add ACEs to the ACL on "Corporate Accounting" as follows:</span></span>

<span data-ttu-id="ae60a-112">« utilisateur 1 »; Licence Créer, modifier, supprimer ; utilisateur de classe objet « utilisateur 1 »; Licence Créer, modifier, supprimer ; objet-classe groupe « utilisateur 1 »; Licence Écriture ; utilisateur de classe d’objet ; Mot de passe d’attribut»</span><span class="sxs-lookup"><span data-stu-id="ae60a-112">""user 1";Grant ;Create, Modify, Delete;Object-Class User"user 1";Grant ;Create, Modify, Delete;Object-Class Group"user 1";Grant ;Write;Object-Class User; Attribute Password"</span></span>

<span data-ttu-id="ae60a-113">Désormais, l’utilisateur 1 peut créer des utilisateurs et des groupes dans la comptabilité d’entreprise et définir les mots de passe pour les utilisateurs existants, mais l’utilisateur 1 ne peut pas créer d’autres classes d’objets et ne peut pas affecter les utilisateurs dans d’autres conteneurs, sauf si, bien sûr, l’utilisateur 1 est autorisé à accéder aux autres conteneurs par les ACE.</span><span class="sxs-lookup"><span data-stu-id="ae60a-113">Now, user 1 can create new users and groups in Corporate Accounting and set the passwords on existing users, but user 1 cannot create any other object classes and cannot affect users in any other containers, unless, of course, user 1 is granted that access by ACEs on the other containers.</span></span>

 

 




