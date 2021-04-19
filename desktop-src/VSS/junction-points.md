---
description: Dans Windows Vista et Windows Server 2008, les emplacements par défaut des données utilisateur et des données système ont changé.
ms.assetid: 78679851-91f5-447f-8580-12cbf0323fb8
title: Points de jonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f1823c67e2c6b95ae366b7604054b47305062e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518197"
---
# <a name="junction-points"></a><span data-ttu-id="dd7cc-103">Points de jonction</span><span class="sxs-lookup"><span data-stu-id="dd7cc-103">Junction Points</span></span>

<span data-ttu-id="dd7cc-104">Dans Windows Vista et Windows Server 2008, les emplacements par défaut des données utilisateur et des données système ont changé.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-104">In Windows Vista and Windows Server 2008, the default locations for user data and system data have changed.</span></span> <span data-ttu-id="dd7cc-105">Par exemple, les données utilisateur précédemment stockées dans le répertoire% SystemDrive% \\ Documents and Settings sont maintenant stockées dans le répertoire% SystemDrive% \\ users.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-105">For example, user data that was previously stored in the %SystemDrive%\\Documents and Settings directory is now stored in the %SystemDrive%\\Users directory.</span></span> <span data-ttu-id="dd7cc-106">Pour la compatibilité descendante, les anciens emplacements ont des points de jonction qui pointent vers les nouveaux emplacements.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-106">For backward compatibility, the old locations have junction points that point to the new locations.</span></span> <span data-ttu-id="dd7cc-107">Par exemple, C : \\ Documents and Settings est maintenant un point de jonction qui pointe vers C : \\ users.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-107">For example, C:\\Documents and Settings is now a junction point that points to C:\\Users.</span></span> <span data-ttu-id="dd7cc-108">Les applications de sauvegarde doivent être en charge de la sauvegarde et de la restauration des points de jonction.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-108">Backup applications must be capable of backing up and restoring junction points.</span></span>

<span data-ttu-id="dd7cc-109">Ces points de jonction peuvent être identifiés comme suit :</span><span class="sxs-lookup"><span data-stu-id="dd7cc-109">These junction points can be identified as follows:</span></span>

-   <span data-ttu-id="dd7cc-110">Ils disposent du point d’analyse, de l’attribut de fichier \_ \_ \_ \_ \_ masqué et des \_ attributs de fichier \_ système d’attribut de fichier définis.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-110">They have the FILE\_ATTRIBUTE\_REPARSE\_POINT, FILE\_ATTRIBUTE\_HIDDEN, and FILE\_ATTRIBUTE\_SYSTEM file attributes set.</span></span>
-   <span data-ttu-id="dd7cc-111">Ils ont également leurs listes de contrôle d’accès (ACL) définies pour refuser l’accès en lecture à tout le monde.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-111">They also have their access control lists (ACLs) set to deny read access to everyone.</span></span>

<span data-ttu-id="dd7cc-112">Les applications qui appellent un chemin d’accès spécifique peuvent traverser ces points de jonction s’ils ont les autorisations requises.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-112">Applications that call out a specific path can traverse these junction points if they have the required permissions.</span></span> <span data-ttu-id="dd7cc-113">Toutefois, toute tentative d’énumération du contenu des points de jonction entraîne des échecs.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-113">However, attempts to enumerate the contents of the junction points will result in failures.</span></span> <span data-ttu-id="dd7cc-114">Il est important que les applications de sauvegarde ne traversent pas ces points de jonction ou ne tentent pas de sauvegarder les données sous elles, pour deux raisons :</span><span class="sxs-lookup"><span data-stu-id="dd7cc-114">It is important that backup applications do not traverse these junction points, or attempt to backup data under them, for two reasons:</span></span>

-   <span data-ttu-id="dd7cc-115">Cela peut entraîner l’application de sauvegarde à sauvegarder les mêmes données plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-115">Doing so can cause the backup application to back up the same data more than once.</span></span>
-   <span data-ttu-id="dd7cc-116">Cela peut également entraîner des cycles (références circulaires).</span><span class="sxs-lookup"><span data-stu-id="dd7cc-116">It can also lead to cycles (circular references).</span></span>

## <a name="per-user-junctions-and-system-junctions"></a><span data-ttu-id="dd7cc-117">Jonctions de Per-User et jonctions système</span><span class="sxs-lookup"><span data-stu-id="dd7cc-117">Per-User Junctions and System Junctions</span></span>

<span data-ttu-id="dd7cc-118">Les points de jonction utilisés pour assurer la virtualisation des fichiers et du Registre dans Windows Vista et Windows Server 2008 peuvent être divisés en deux classes : jonctions par utilisateur et jonctions système.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-118">The junction points that are used to provide file and registry virtualization in Windows Vista and Windows Server 2008 can be divided into two classes: per-user junctions and system junctions.</span></span>

<span data-ttu-id="dd7cc-119">Les jonctions par utilisateur sont créées dans chaque profil d’utilisateur individuel pour fournir une compatibilité descendante pour les applications utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-119">Per-user junctions are created inside each individual user's profile to provide backward compatibility for user applications.</span></span> <span data-ttu-id="dd7cc-120">Le point de jonction sur C : \\ Users \\ *username* \\ My documents qui pointe vers c : \\ Users \\ *username* \\ documents est un exemple de jonction par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-120">The junction point at C:\\Users\\*username*\\My Documents that points to C:\\Users\\*username*\\Documents is an example of a per-user junction.</span></span> <span data-ttu-id="dd7cc-121">Les jonctions par utilisateur sont créées par le service de profil lors de la création du profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-121">Per-user junctions are created by the Profile service when the user's profile is created.</span></span>

<span data-ttu-id="dd7cc-122">Les autres jonctions sont des jonctions système qui ne se trouvent pas dans le \\ répertoire du *nom d’utilisateur* de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-122">The other junctions are system junctions that do not reside under the Users\\*username* directory.</span></span> <span data-ttu-id="dd7cc-123">Voici quelques exemples de jonctions système :</span><span class="sxs-lookup"><span data-stu-id="dd7cc-123">Examples of system junctions include:</span></span>

-   <span data-ttu-id="dd7cc-124">Documents et paramètres</span><span class="sxs-lookup"><span data-stu-id="dd7cc-124">Documents and Settings</span></span>
-   <span data-ttu-id="dd7cc-125">Jonctions dans tous les profils utilisateur, public et utilisateur par défaut</span><span class="sxs-lookup"><span data-stu-id="dd7cc-125">Junctions within the All Users, Public, and Default User profiles</span></span>

<span data-ttu-id="dd7cc-126">Les jonctions système sont créées par userenv.dll quand elles sont appelées par l’accueil de Windows (également appelé ordinateur out-of-Box-Experience, ou mOOBE).</span><span class="sxs-lookup"><span data-stu-id="dd7cc-126">System junctions are created by userenv.dll when it is invoked by Windows Welcome (also called the machine out-of-box-experience, or mOOBE).</span></span>

> [!Note]  
> <span data-ttu-id="dd7cc-127">Si l’utilisateur change la langue du système dans une langue autre que l’anglais, les points de jonction système et par utilisateur sont créés avec des noms localisés.</span><span class="sxs-lookup"><span data-stu-id="dd7cc-127">If the user changes the system language to a language other than English, the per-user and system junction points will be created with localized names.</span></span>

 

 

 



