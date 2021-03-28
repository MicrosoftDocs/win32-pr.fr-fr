---
description: Le système crée automatiquement un profil utilisateur local pour chaque utilisateur quand l’utilisateur ouvre une session sur l’ordinateur pour la première fois. Le système conserve automatiquement les paramètres de l’environnement de travail de chaque utilisateur dans un profil utilisateur sur l’ordinateur local.
title: Profils utilisateur locaux
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973379"
---
# <a name="local-user-profiles"></a><span data-ttu-id="dd640-104">Profils utilisateur locaux</span><span class="sxs-lookup"><span data-stu-id="dd640-104">Local User Profiles</span></span>

<span data-ttu-id="dd640-105">La sécurité Windows nécessite un profil utilisateur pour chaque compte d’utilisateur sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dd640-105">Windows security requires a user profile for each user account on a computer.</span></span> <span data-ttu-id="dd640-106">Le système crée automatiquement un *profil utilisateur local* pour chaque utilisateur quand l’utilisateur ouvre une session sur l’ordinateur pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="dd640-106">The system automatically creates a *local user profile* for each user when the user logs on to the computer for the first time.</span></span> <span data-ttu-id="dd640-107">Le système conserve automatiquement les paramètres de l’environnement de travail de chaque utilisateur dans un profil utilisateur sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="dd640-107">The system automatically maintains the settings for each user's work environment in a user profile on the local computer.</span></span>

<span data-ttu-id="dd640-108">Windows Vista et versions ultérieures : les profils utilisateur sont gérés à l’aide de l’élément **comptes d’utilisateur** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="dd640-108">Windows Vista and later: User profiles are managed through the **User Accounts** control panel item.</span></span>

<span data-ttu-id="dd640-109">Windows 2000 et Windows XP : pour copier ou supprimer un profil utilisateur, sélectionnez **système** dans le panneau de configuration, puis l’onglet **avancé** , puis le bouton **paramètres** dans la zone **profil utilisateur** .</span><span class="sxs-lookup"><span data-stu-id="dd640-109">Windows 2000 and Windows XP: To copy or delete a user profile, select **System** from the Control Panel, then the **Advanced** tab, and then the **Settings** button in the **User Profile** area.</span></span>

<span data-ttu-id="dd640-110">Le profil de l’utilisateur n’est pas chargé automatiquement lorsque l’utilisateur a ouvert une session à l’aide de la fonction [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) .</span><span class="sxs-lookup"><span data-stu-id="dd640-110">The user's profile is not loaded automatically when the user is logged on using the [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) function.</span></span> <span data-ttu-id="dd640-111">Pour charger un profil utilisateur par programme, utilisez la fonction [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .</span><span class="sxs-lookup"><span data-stu-id="dd640-111">To load a user profile programmatically, use the [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) function.</span></span> <span data-ttu-id="dd640-112">Pour décharger un profil utilisateur chargé par **LoadUserProfile**, appelez la fonction [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .</span><span class="sxs-lookup"><span data-stu-id="dd640-112">To unload a user profile loaded by **LoadUserProfile**, call the [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) function.</span></span>

 

 
