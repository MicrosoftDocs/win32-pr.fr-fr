---
description: Les éléments d’API suivants sont utilisés avec les profils utilisateur.
title: Référence des profils utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d5d4c4f585eda66674059f402dbd73f106a3e4f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973727"
---
# <a name="user-profiles-reference"></a><span data-ttu-id="7ae91-103">Référence des profils utilisateur</span><span class="sxs-lookup"><span data-stu-id="7ae91-103">User Profiles Reference</span></span>

<span data-ttu-id="7ae91-104">Les éléments d’API suivants sont utilisés avec les profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ae91-104">The following API elements are used with user profiles.</span></span>

## <a name="functions"></a><span data-ttu-id="7ae91-105">Fonctions</span><span class="sxs-lookup"><span data-stu-id="7ae91-105">Functions</span></span>



| <span data-ttu-id="7ae91-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="7ae91-106">Function</span></span>                                                                   | <span data-ttu-id="7ae91-107">Description</span><span class="sxs-lookup"><span data-stu-id="7ae91-107">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ae91-108">**CreateEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="7ae91-108">**CreateEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | <span data-ttu-id="7ae91-109">Récupère les variables d’environnement pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae91-109">Retrieves the environment variables for the specified user.</span></span>                                                   |
| [<span data-ttu-id="7ae91-110">**CreateProfile**</span><span class="sxs-lookup"><span data-stu-id="7ae91-110">**CreateProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | <span data-ttu-id="7ae91-111">Crée un nouveau profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ae91-111">Creates a new user profile.</span></span> <span data-ttu-id="7ae91-112">(Windows Vista et versions ultérieures uniquement.)</span><span class="sxs-lookup"><span data-stu-id="7ae91-112">(Windows Vista and later only.)</span></span>                                                   |
| [<span data-ttu-id="7ae91-113">**DeleteProfile**</span><span class="sxs-lookup"><span data-stu-id="7ae91-113">**DeleteProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | <span data-ttu-id="7ae91-114">Supprime le profil utilisateur et tous les paramètres liés à l’utilisateur de l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae91-114">Deletes the user profile and all user-related settings from the specified computer.</span></span>                           |
| [<span data-ttu-id="7ae91-115">**DestroyEnvironmentBlock**</span><span class="sxs-lookup"><span data-stu-id="7ae91-115">**DestroyEnvironmentBlock**</span></span>](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | <span data-ttu-id="7ae91-116">Libère les variables d’environnement créées par la fonction [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) .</span><span class="sxs-lookup"><span data-stu-id="7ae91-116">Frees environment variables created by the [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) function.</span></span> |
| [<span data-ttu-id="7ae91-117">**ExpandEnvironmentStringsForUser**</span><span class="sxs-lookup"><span data-stu-id="7ae91-117">**ExpandEnvironmentStringsForUser**</span></span>](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | <span data-ttu-id="7ae91-118">Développe la chaîne source à l’aide du bloc d’environnement établi pour l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae91-118">Expands the source string by using the environment block established for the specified user.</span></span>                  |
| [<span data-ttu-id="7ae91-119">**GetAllUsersProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="7ae91-119">**GetAllUsersProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | <span data-ttu-id="7ae91-120">Récupère le chemin d’accès à la racine du profil tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7ae91-120">Retrieves the path to the root of the All Users profile.</span></span>                                                      |
| [<span data-ttu-id="7ae91-121">**GetDefaultUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="7ae91-121">**GetDefaultUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | <span data-ttu-id="7ae91-122">Récupère le chemin d’accès à la racine du profil utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ae91-122">Retrieves the path to the root of the Default User profile.</span></span>                                                   |
| [<span data-ttu-id="7ae91-123">**GetProfilesDirectory**</span><span class="sxs-lookup"><span data-stu-id="7ae91-123">**GetProfilesDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | <span data-ttu-id="7ae91-124">Récupère le chemin d’accès au répertoire racine dans lequel tous les profils utilisateur sont stockés.</span><span class="sxs-lookup"><span data-stu-id="7ae91-124">Retrieves the path to the root directory where all user profiles are stored.</span></span>                                  |
| [<span data-ttu-id="7ae91-125">**GetProfileType**</span><span class="sxs-lookup"><span data-stu-id="7ae91-125">**GetProfileType**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | <span data-ttu-id="7ae91-126">Récupère le type de profil chargé pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7ae91-126">Retrieves the type of profile loaded for the current user.</span></span>                                                    |
| [<span data-ttu-id="7ae91-127">**GetUserProfileDirectory**</span><span class="sxs-lookup"><span data-stu-id="7ae91-127">**GetUserProfileDirectory**</span></span>](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | <span data-ttu-id="7ae91-128">Récupère le chemin d’accès au répertoire racine du profil de l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae91-128">Retrieves the path to the root directory of the specified user's profile.</span></span>                                     |
| [<span data-ttu-id="7ae91-129">**LoadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="7ae91-129">**LoadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | <span data-ttu-id="7ae91-130">Charge le profil de l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7ae91-130">Loads the specified user's profile.</span></span>                                                                           |
| [<span data-ttu-id="7ae91-131">**UnloadUserProfile**</span><span class="sxs-lookup"><span data-stu-id="7ae91-131">**UnloadUserProfile**</span></span>](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | <span data-ttu-id="7ae91-132">Décharge le profil d’un utilisateur qui a été chargé par la fonction [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="7ae91-132">Unloads a user's profile that was loaded by the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span>          |



 

<span data-ttu-id="7ae91-133">La fonction [**CreateUserProfileEx**](createuserprofileex.md) n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7ae91-133">The [**CreateUserProfileEx**](createuserprofileex.md) function is not supported.</span></span>

## <a name="structures"></a><span data-ttu-id="7ae91-134">Structures</span><span class="sxs-lookup"><span data-stu-id="7ae91-134">Structures</span></span>



| <span data-ttu-id="7ae91-135">Structure</span><span class="sxs-lookup"><span data-stu-id="7ae91-135">Structure</span></span>                          | <span data-ttu-id="7ae91-136">Description</span><span class="sxs-lookup"><span data-stu-id="7ae91-136">Description</span></span>                                |
|------------------------------------|--------------------------------------------|
| [<span data-ttu-id="7ae91-137">**PROFILEINFO**</span><span class="sxs-lookup"><span data-stu-id="7ae91-137">**PROFILEINFO**</span></span>](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | <span data-ttu-id="7ae91-138">Contient des informations sur un profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ae91-138">Contains information about a user profile.</span></span> |



 

 

 



