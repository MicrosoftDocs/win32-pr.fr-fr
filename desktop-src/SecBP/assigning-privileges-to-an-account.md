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
# <a name="assigning-privileges-to-an-account"></a><span data-ttu-id="a387c-103">Attribution de privilèges à un compte</span><span class="sxs-lookup"><span data-stu-id="a387c-103">Assigning Privileges to an Account</span></span>

<span data-ttu-id="a387c-104">Vous pouvez affecter des privilèges aux comptes en utilisant le composant logiciel enfichable MMC (Microsoft Management Console) de la stratégie de sécurité locale (secpol. msc) ou en appelant la fonction [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .</span><span class="sxs-lookup"><span data-stu-id="a387c-104">You can assign privileges to accounts either by using the Local Security Policy Microsoft Management Console (MMC) snap-in (Secpol.msc) or by calling the [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) function.</span></span>

<span data-ttu-id="a387c-105">L’attribution d’un privilège à un compte n’affecte pas les jetons utilisateur existants.</span><span class="sxs-lookup"><span data-stu-id="a387c-105">Assigning a privilege to an account does not affect existing user tokens.</span></span> <span data-ttu-id="a387c-106">Un utilisateur doit se déconnecter puis se reconnecter pour obtenir un jeton d’accès avec le privilège qui vient d’être attribué.</span><span class="sxs-lookup"><span data-stu-id="a387c-106">A user must log off and then log back on to get an access token with the newly assigned privilege.</span></span>

<span data-ttu-id="a387c-107">Pour affecter des privilèges à l’aide du composant logiciel enfichable MMC stratégie de sécurité locale, modifiez la liste des utilisateurs pour chaque privilège répertorié sous **paramètres de sécurité/stratégies locales/attribution des droits utilisateur**.</span><span class="sxs-lookup"><span data-stu-id="a387c-107">To assign privileges by using the Local Security Policy MMC snap-in, edit the list of users for each privilege listed under **Security Settings/Local Policies/User Rights Assignment**.</span></span>

 

 
