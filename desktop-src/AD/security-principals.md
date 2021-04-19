---
title: Principaux de sécurité
description: Dans Windows 2000, un principal de sécurité est un utilisateur, un groupe ou un ordinateur \ 8212 ; entité que le système de sécurité reconnaît.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- principaux de sécurité AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510389"
---
# <a name="security-principals"></a><span data-ttu-id="f8b8c-104">Principaux de sécurité</span><span class="sxs-lookup"><span data-stu-id="f8b8c-104">Security Principals</span></span>

<span data-ttu-id="f8b8c-105">Dans Windows 2000, un principal de sécurité est un utilisateur, un groupe ou un ordinateur, une entité que le système de sécurité reconnaît.</span><span class="sxs-lookup"><span data-stu-id="f8b8c-105">In Windows 2000, a security principal is a user, group, or computer — an entity that the security system recognizes.</span></span> <span data-ttu-id="f8b8c-106">Cela comprend les utilisateurs humains et les processus autonomes.</span><span class="sxs-lookup"><span data-stu-id="f8b8c-106">This includes human users as well as autonomous processes.</span></span> <span data-ttu-id="f8b8c-107">Strictement parlant, le système de sécurité ne peut pas déterminer la différence entre les utilisateurs qui sont connectés et les processus en cours d’exécution sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f8b8c-107">Strictly speaking, the security system cannot tell the difference between users who are logged in and processes running on the computer.</span></span> <span data-ttu-id="f8b8c-108">Il voit à la fois comme entités de sécurité avec des noms de principal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f8b8c-108">It sees both as security principals with security principal names.</span></span>

<span data-ttu-id="f8b8c-109">Les utilisateurs, les groupes et les ordinateurs sont créés et stockés en tant qu’objets dans Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f8b8c-109">Users, groups, and computers are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="f8b8c-110">Il existe également des principaux de sécurité connus qui représentent des identités spéciales définies par le système de sécurité de Windows 2000, telles que tout le monde, système local, principal Self, utilisateur authentifié, propriétaire créateur, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="f8b8c-110">There are also well-known security principals that represent special identities defined by the Windows 2000 security system, such as Everyone, Local System, Principal Self, Authenticated User, Creator Owner, and so on.</span></span> <span data-ttu-id="f8b8c-111">Les objets représentant les principaux de sécurité connus, tels que Anonymous Logon, sont stockés dans le conteneur WellKnown Security principals sous le conteneur Configuration.</span><span class="sxs-lookup"><span data-stu-id="f8b8c-111">Objects representing the well-known security principals, such as Anonymous Logon, are stored in the WellKnown Security Principals container beneath the Configuration container.</span></span>

 

 




