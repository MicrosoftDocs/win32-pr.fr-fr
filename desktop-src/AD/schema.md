---
title: Schéma (AD DS)
description: Active Directory schéma est implémenté comme un ensemble d’instances de classes d’objets stockées dans le répertoire.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "103679457"
---
# <a name="schema-ad-ds"></a><span data-ttu-id="c8f99-104">Schéma (AD DS)</span><span class="sxs-lookup"><span data-stu-id="c8f99-104">Schema (AD DS)</span></span>

<span data-ttu-id="c8f99-105">Active Directory schéma est implémenté comme un ensemble d’instances de classes d’objets stockées dans le répertoire.</span><span class="sxs-lookup"><span data-stu-id="c8f99-105">Active Directory schema is implemented as a set of object class instances stored in the directory.</span></span> <span data-ttu-id="c8f99-106">Cela est très différent de nombreux répertoires qui ont un schéma, mais le stocke sous la forme d’un fichier texte lu au démarrage.</span><span class="sxs-lookup"><span data-stu-id="c8f99-106">This is very different than many directories that have a schema but store it as a text file read at startup.</span></span> <span data-ttu-id="c8f99-107">Le stockage du schéma dans l’annuaire présente de nombreux avantages.</span><span class="sxs-lookup"><span data-stu-id="c8f99-107">Storing the schema in the directory has many advantages.</span></span> <span data-ttu-id="c8f99-108">Par exemple, les applications utilisateur peuvent la lire pour découvrir les objets et les propriétés disponibles.</span><span class="sxs-lookup"><span data-stu-id="c8f99-108">For example, user applications can read it to discover what objects and properties are available.</span></span>

<span data-ttu-id="c8f99-109">Active Directory schéma peut être mis à jour de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="c8f99-109">Active Directory schema can be updated dynamically.</span></span> <span data-ttu-id="c8f99-110">Autrement dit, une application peut étendre le schéma avec de nouveaux attributs et classes et utiliser les extensions immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c8f99-110">That is, an application can extend the schema with new attributes and classes and use the extensions immediately.</span></span> <span data-ttu-id="c8f99-111">Les mises à jour de schéma sont effectuées en créant ou en modifiant les objets de schéma stockés dans l’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c8f99-111">Schema updates are accomplished by creating or modifying the schema objects stored in the directory.</span></span> <span data-ttu-id="c8f99-112">Comme chaque objet dans Active Directory, les listes de contrôle d’accès (ACL) protègent les objets de schéma, de sorte que les utilisateurs autorisés peuvent modifier le schéma.</span><span class="sxs-lookup"><span data-stu-id="c8f99-112">Like every object in Active Directory, access-control lists (ACLs) protect schema objects, so authorized users only may alter the schema.</span></span>

<span data-ttu-id="c8f99-113">Pour plus d’informations, consultez [Active Directory le schéma](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="c8f99-113">For more information, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 




