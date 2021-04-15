---
title: Authentification (AD DS)
description: Chaque objet dans Active Directory Domain Services possède un descripteur de sécurité unique qui définit les autorisations d’accès requises pour lire ou mettre à jour l’objet ou ses propriétés individuelles.
ms.assetid: a4a663d3-b0f3-4993-a74e-9e4f896e8c95
ms.tgt_platform: multiple
keywords:
- Active Directory, utilisation de, liaison, authentification
- liaison de l’authentification Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80bbca4604a99011d3198eaf6b3e871cd3f84c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462935"
---
# <a name="authentication-ad-ds"></a><span data-ttu-id="e2ba1-105">Authentification (AD DS)</span><span class="sxs-lookup"><span data-stu-id="e2ba1-105">Authentication (AD DS)</span></span>

<span data-ttu-id="e2ba1-106">Chaque objet dans Active Directory Domain Services possède un descripteur de sécurité unique qui définit les autorisations d’accès requises pour lire ou mettre à jour l’objet ou ses propriétés individuelles.</span><span class="sxs-lookup"><span data-stu-id="e2ba1-106">Every object in Active Directory Domain Services has a unique security descriptor that defines the access permissions that are required to read or update the object or its individual properties.</span></span> <span data-ttu-id="e2ba1-107">Les privilèges d’accès sont déterminés par les droits accordés au compte d’un utilisateur ou aux appartenances à un groupe.</span><span class="sxs-lookup"><span data-stu-id="e2ba1-107">Access privileges are determined by the rights granted to a user's account or group memberships.</span></span>

<span data-ttu-id="e2ba1-108">Quand une application est liée à un objet dans l’annuaire, les privilèges d’accès de l’application à cet objet sont basés sur le contexte utilisateur spécifié pendant l’opération de liaison.</span><span class="sxs-lookup"><span data-stu-id="e2ba1-108">When an application binds to an object in the directory, the access privileges that the application has to that object are based on the user context specified during the bind operation.</span></span> <span data-ttu-id="e2ba1-109">Pour les fonctions de liaison et les méthodes [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject :: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), une application peut utiliser implicitement les informations d’identification de l’appelant, spécifier explicitement les informations d’identification d’un compte d’utilisateur ou utiliser un contexte utilisateur non authentifié (invité).</span><span class="sxs-lookup"><span data-stu-id="e2ba1-109">For the binding functions and methods [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject), [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject), **GetObject**, [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject), an application can implicitly use the credentials of the caller, explicitly specify the credentials of a user account, or use an unauthenticated user context (Guest).</span></span>

 

 