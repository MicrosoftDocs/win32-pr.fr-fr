---
description: Un profil utilisateur obligatoire est un type spécial de profil utilisateur itinérant préconfiguré que les administrateurs peuvent utiliser pour spécifier des paramètres pour les utilisateurs.
title: Profils utilisateur obligatoires
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 744d35e92a279c5d8a8e8b239fa64bb1960e011a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524423"
---
# <a name="mandatory-user-profiles"></a><span data-ttu-id="76a78-103">Profils utilisateur obligatoires</span><span class="sxs-lookup"><span data-stu-id="76a78-103">Mandatory User Profiles</span></span>

<span data-ttu-id="76a78-104">Un profil utilisateur obligatoire est un type spécial de [profil utilisateur itinérant](roaming-user-profiles.md) préconfiguré que les administrateurs peuvent utiliser pour spécifier des paramètres pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="76a78-104">A mandatory user profile is a special type of pre-configured [roaming user profile](roaming-user-profiles.md) that administrators can use to specify settings for users.</span></span> <span data-ttu-id="76a78-105">Avec les profils utilisateur obligatoires, un utilisateur peut modifier son bureau, mais les modifications ne sont pas enregistrées lorsque l’utilisateur se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="76a78-105">With mandatory user profiles, a user can modify his or her desktop, but the changes are not saved when the user logs off.</span></span> <span data-ttu-id="76a78-106">La prochaine fois que l’utilisateur ouvre une session, le profil utilisateur obligatoire créé par l’administrateur est téléchargé.</span><span class="sxs-lookup"><span data-stu-id="76a78-106">The next time the user logs on, the mandatory user profile created by the administrator is downloaded.</span></span> <span data-ttu-id="76a78-107">Il existe deux types de profils obligatoires : les profils *obligatoires normaux* et les profils *Super obligatoires* .</span><span class="sxs-lookup"><span data-stu-id="76a78-107">There are two types of mandatory profiles: *normal mandatory* profiles and *super-mandatory* profiles.</span></span>

<span data-ttu-id="76a78-108">Les profils utilisateur deviennent des profils obligatoires lorsque l’administrateur renomme le fichier NTuser. dat (la ruche du registre) sur le serveur en NTuser. Man.</span><span class="sxs-lookup"><span data-stu-id="76a78-108">User profiles become mandatory profiles when the administrator renames the NTuser.dat file (the registry hive) on the server to NTuser.man.</span></span> <span data-ttu-id="76a78-109">L’extension. Man fait en sorte que le profil utilisateur soit un profil en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="76a78-109">The .man extension causes the user profile to be a read-only profile.</span></span>

<span data-ttu-id="76a78-110">Les profils utilisateur deviennent *Super obligatoires* lorsque le nom du dossier du chemin d’accès du profil se termine par. Man ; par exemple, le \\ \\ partage de serveur \\ \\ mandatoryprofile. Man \\ .</span><span class="sxs-lookup"><span data-stu-id="76a78-110">User profiles become *super-mandatory* when the folder name of the profile path ends in .man; for example, \\\\server\\share\\mandatoryprofile.man\\.</span></span>

<span data-ttu-id="76a78-111">Les profils utilisateur Super obligatoires sont similaires aux profils obligatoires normaux, à l’exception près que les utilisateurs qui ont des profils Super obligatoires ne peuvent pas ouvrir une session lorsque le serveur qui stocke le profil obligatoire n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="76a78-111">Super-mandatory user profiles are similar to normal mandatory profiles, with the exception that users who have super-mandatory profiles cannot log on when the server that stores the mandatory profile is unavailable.</span></span> <span data-ttu-id="76a78-112">Les utilisateurs avec des profils obligatoires normaux peuvent se connecter avec la copie mise en cache localement du profil obligatoire.</span><span class="sxs-lookup"><span data-stu-id="76a78-112">Users with normal mandatory profiles can log on with the locally cached copy of the mandatory profile.</span></span>

<span data-ttu-id="76a78-113">Seuls les administrateurs système peuvent apporter des modifications aux profils utilisateur obligatoires.</span><span class="sxs-lookup"><span data-stu-id="76a78-113">Only system administrators can make changes to mandatory user profiles.</span></span>

 

 



