---
description: Si un ordinateur exécute Windows 2000 Server ou une version ultérieure sur un réseau, les utilisateurs peuvent stocker leurs profils sur le serveur. Ces profils sont appelés profils utilisateur itinérants.
title: Profils utilisateur itinérants
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973342"
---
# <a name="roaming-user-profiles"></a><span data-ttu-id="7cc14-104">Profils utilisateur itinérants</span><span class="sxs-lookup"><span data-stu-id="7cc14-104">Roaming User Profiles</span></span>

<span data-ttu-id="7cc14-105">Si un ordinateur exécute Windows 2000 Server ou une version ultérieure sur un réseau, les utilisateurs peuvent stocker leurs profils sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7cc14-105">If a computer is running Windows 2000 Server or later on a network, users can store their profiles on the server.</span></span> <span data-ttu-id="7cc14-106">Ces profils sont appelés *profils utilisateur itinérants*.</span><span class="sxs-lookup"><span data-stu-id="7cc14-106">These profiles are called *roaming user profiles*.</span></span>

<span data-ttu-id="7cc14-107">Les profils utilisateur itinérants présentent les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="7cc14-107">Roaming user profiles have the following advantages:</span></span>

-   <span data-ttu-id="7cc14-108">Disponibilité automatique des ressources.</span><span class="sxs-lookup"><span data-stu-id="7cc14-108">Automatic resource availability.</span></span> <span data-ttu-id="7cc14-109">Le profil unique d’un utilisateur est automatiquement disponible lorsqu’il se connecte à un ordinateur sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="7cc14-109">A user's unique profile is automatically available when he or she logs on to any computer on the network.</span></span> <span data-ttu-id="7cc14-110">Les utilisateurs n’ont pas besoin de créer un profil sur chaque ordinateur qu’ils utilisent sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="7cc14-110">Users do not need to create a profile on each computer they use on a network.</span></span>
-   <span data-ttu-id="7cc14-111">Remplacement et sauvegarde de l’ordinateur simplifiés.</span><span class="sxs-lookup"><span data-stu-id="7cc14-111">Simplified computer replacement and backup.</span></span> <span data-ttu-id="7cc14-112">Lorsque l’ordinateur d’un utilisateur doit être remplacé, il peut être remplacé facilement, car toutes les informations de profil de l’utilisateur sont conservées séparément sur le réseau, indépendamment d’un ordinateur individuel.</span><span class="sxs-lookup"><span data-stu-id="7cc14-112">When a user's computer must be replaced, it can be replaced easily because all of the user's profile information is maintained separately on the network, independent of an individual computer.</span></span> <span data-ttu-id="7cc14-113">Lorsque l’utilisateur ouvre une session sur le nouvel ordinateur pour la première fois, la copie sur le serveur du profil de l’utilisateur est copiée sur le nouvel ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7cc14-113">When the user logs on to the new computer for the first time, the server copy of the user's profile is copied to the new computer.</span></span>

<span data-ttu-id="7cc14-114">Le profil de l’utilisateur n’est pas chargé automatiquement lorsque l’utilisateur a ouvert une session à l’aide de la fonction [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="7cc14-114">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="7cc14-115">Pour charger un profil utilisateur itinérant par programme, utilisez la fonction [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="7cc14-115">To load a roaming user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="7cc14-116">Pour décharger un profil utilisateur itinérant chargé par **LoadUserProfile**, appelez la fonction [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="7cc14-116">To unload a roaming user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
