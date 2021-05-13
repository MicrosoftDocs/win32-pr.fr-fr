---
description: Permet à un administrateur de gérer les propriétés de quota de disque d’un volume.
title: Objet DiskQuotaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841550"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="b48b5-103">Objet DiskQuotaControl</span><span class="sxs-lookup"><span data-stu-id="b48b5-103">DiskQuotaControl object</span></span>

<span data-ttu-id="b48b5-104">Permet à un administrateur de gérer les propriétés de quota de disque d’un volume.</span><span class="sxs-lookup"><span data-stu-id="b48b5-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="b48b5-105">Le système de fichiers NTFS permet à un administrateur de gérer l’utilisation du disque sur un volume partagé en allouant une quantité d’espace disque spécifiée ou une *limite de quota* à chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b48b5-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="b48b5-106">Vous pouvez utiliser cet objet pour définir la limite de quota par défaut qui sera automatiquement affectée à tous les nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b48b5-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="b48b5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b48b5-107">Members</span></span>

<span data-ttu-id="b48b5-108">L’objet **DiskQuotaControl** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b48b5-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="b48b5-109">Événements</span><span class="sxs-lookup"><span data-stu-id="b48b5-109">Events</span></span>](#events)
-   [<span data-ttu-id="b48b5-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b48b5-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b48b5-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b48b5-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="b48b5-112">Événements</span><span class="sxs-lookup"><span data-stu-id="b48b5-112">Events</span></span>

<span data-ttu-id="b48b5-113">L’objet **DiskQuotaControl** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="b48b5-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="b48b5-114">Événement</span><span class="sxs-lookup"><span data-stu-id="b48b5-114">Event</span></span>                                                           | <span data-ttu-id="b48b5-115">Description</span><span class="sxs-lookup"><span data-stu-id="b48b5-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b48b5-116">**OnUserNameChanged**</span><span class="sxs-lookup"><span data-stu-id="b48b5-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="b48b5-117">Se produit lorsque les informations de nom d’un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) ont été résolues.</span><span class="sxs-lookup"><span data-stu-id="b48b5-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="b48b5-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b48b5-118">Methods</span></span>

<span data-ttu-id="b48b5-119">L’objet **DiskQuotaControl** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b48b5-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="b48b5-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="b48b5-120">Method</span></span>                                                                                    | <span data-ttu-id="b48b5-121">Description</span><span class="sxs-lookup"><span data-stu-id="b48b5-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b48b5-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="b48b5-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="b48b5-123">Affecte un quota de disque autre que celui par défaut à un nouvel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b48b5-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="b48b5-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="b48b5-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="b48b5-125">Supprime un utilisateur du volume.</span><span class="sxs-lookup"><span data-stu-id="b48b5-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="b48b5-126">**FindUser**</span><span class="sxs-lookup"><span data-stu-id="b48b5-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="b48b5-127">Recherche l’entrée d’un utilisateur, par son nom, dans le fichier de quota du volume.</span><span class="sxs-lookup"><span data-stu-id="b48b5-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="b48b5-128">**GiveUserNameResolutionPriority**</span><span class="sxs-lookup"><span data-stu-id="b48b5-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="b48b5-129">Place l’objet utilisateur spécifié en regard de la résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="b48b5-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="b48b5-130">**Initialiser**</span><span class="sxs-lookup"><span data-stu-id="b48b5-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="b48b5-131">Ouvre un volume spécifié et initialise son objet de contrôle de quota.</span><span class="sxs-lookup"><span data-stu-id="b48b5-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="b48b5-132">**InvalidateSidNameCache**</span><span class="sxs-lookup"><span data-stu-id="b48b5-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="b48b5-133">Invalide le cache du nom d’utilisateur de l’ID de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b48b5-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="b48b5-134">**ShutdownNameResolution**</span><span class="sxs-lookup"><span data-stu-id="b48b5-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="b48b5-135">Arrête le thread de résolution de nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b48b5-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="b48b5-136">**TranslateLogonNameToSID**</span><span class="sxs-lookup"><span data-stu-id="b48b5-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="b48b5-137">Convertit un nom d’ouverture de session en ID de sécurité de l’utilisateur correspondant au format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="b48b5-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b48b5-138">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b48b5-138">Properties</span></span>

<span data-ttu-id="b48b5-139">L’objet **DiskQuotaControl** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b48b5-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="b48b5-140">Propriété</span><span class="sxs-lookup"><span data-stu-id="b48b5-140">Property</span></span>                                                                                   | <span data-ttu-id="b48b5-141">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b48b5-141">Access type</span></span>           | <span data-ttu-id="b48b5-142">Description</span><span class="sxs-lookup"><span data-stu-id="b48b5-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b48b5-143">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="b48b5-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="b48b5-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b48b5-144">Read/write</span></span><br/> | <span data-ttu-id="b48b5-145">Définit ou obtient la limite de quota par défaut.</span><span class="sxs-lookup"><span data-stu-id="b48b5-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="b48b5-146">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="b48b5-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="b48b5-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b48b5-147">Read-only</span></span><br/>  | <span data-ttu-id="b48b5-148">Obtient la limite de quota par défaut sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="b48b5-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="b48b5-149">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="b48b5-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="b48b5-150">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b48b5-150">Read/write</span></span><br/> | <span data-ttu-id="b48b5-151">Définit ou obtient le seuil de quota par défaut.</span><span class="sxs-lookup"><span data-stu-id="b48b5-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="b48b5-152">**DefaultQuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="b48b5-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="b48b5-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b48b5-153">Read-only</span></span><br/>  | <span data-ttu-id="b48b5-154">Obtient le seuil de quota par défaut sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="b48b5-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="b48b5-155">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="b48b5-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="b48b5-156">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b48b5-156">Read/write</span></span><br/> | <span data-ttu-id="b48b5-157">Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse sa limite de quota affectée.</span><span class="sxs-lookup"><span data-stu-id="b48b5-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="b48b5-158">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="b48b5-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="b48b5-159">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b48b5-159">Read/write</span></span><br/> | <span data-ttu-id="b48b5-160">Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse son seuil de quota attribué.</span><span class="sxs-lookup"><span data-stu-id="b48b5-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="b48b5-161">**QuotaFileIncomplete**</span><span class="sxs-lookup"><span data-stu-id="b48b5-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="b48b5-162">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b48b5-162">Read-only</span></span><br/>  | <span data-ttu-id="b48b5-163">Obtient une valeur booléenne qui indique si le fichier de quota du volume est terminé.</span><span class="sxs-lookup"><span data-stu-id="b48b5-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="b48b5-164">**QuotaFileRebuilding**</span><span class="sxs-lookup"><span data-stu-id="b48b5-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="b48b5-165">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b48b5-165">Read-only</span></span><br/>  | <span data-ttu-id="b48b5-166">Obtient une valeur booléenne qui indique si le fichier de quota du volume est en cours de reconstruction.</span><span class="sxs-lookup"><span data-stu-id="b48b5-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="b48b5-167">**QuotaState**</span><span class="sxs-lookup"><span data-stu-id="b48b5-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="b48b5-168">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b48b5-168">Read/write</span></span><br/> | <span data-ttu-id="b48b5-169">Définit ou obtient l’état des quotas de disque du volume.</span><span class="sxs-lookup"><span data-stu-id="b48b5-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="b48b5-170">**UserNameResolution**</span><span class="sxs-lookup"><span data-stu-id="b48b5-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="b48b5-171">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b48b5-171">Read/write</span></span><br/> | <span data-ttu-id="b48b5-172">Définit ou obtient une valeur qui contrôle la façon dont le SID de l’utilisateur est résolu en noms d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b48b5-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="b48b5-173">Notes</span><span class="sxs-lookup"><span data-stu-id="b48b5-173">Remarks</span></span>

<span data-ttu-id="b48b5-174">Un administrateur peut utiliser l’objet **DiskQuotaControl** pour effectuer un certain nombre de tâches, y compris les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="b48b5-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="b48b5-175">Activation et désactivation du système de quota de disque du volume.</span><span class="sxs-lookup"><span data-stu-id="b48b5-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="b48b5-176">Obtention de l’état du système de quota sur le volume.</span><span class="sxs-lookup"><span data-stu-id="b48b5-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="b48b5-177">Refus de l’espace disque aux utilisateurs dépassant leur limite de quota.</span><span class="sxs-lookup"><span data-stu-id="b48b5-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="b48b5-178">Spécification du seuil d’avertissement et des valeurs de limite de quota par défaut qui seront affectés aux nouveaux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b48b5-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="b48b5-179">Ajout et suppression d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b48b5-179">Adding and removing users.</span></span>

<span data-ttu-id="b48b5-180">L’objet **DiskQuotaControl** vous permet de définir des valeurs globales par défaut pour le volume pour les propriétés telles que les limites de quota.</span><span class="sxs-lookup"><span data-stu-id="b48b5-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="b48b5-181">Toutefois, chaque utilisateur est représenté par un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) qui peut être utilisé pour spécifier des paramètres de quota individuels.</span><span class="sxs-lookup"><span data-stu-id="b48b5-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="b48b5-182">Il existe plusieurs façons d’obtenir l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="b48b5-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="b48b5-183">Les objets [**DIDiskQuotaUser**](didiskquotauser-object.md) pour tous les utilisateurs avec quotas sur le volume sont exposés en tant que collection et peuvent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="b48b5-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="b48b5-184">Pour plus d’informations sur l’énumération des objets **DIDiskQuotaUser** , consultez la section **énumération des quotas de disque** pour les utilisateurs dans la section Notes de **DIDiskQuotaUser**.</span><span class="sxs-lookup"><span data-stu-id="b48b5-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="b48b5-185">Lorsque vous ajoutez un nouvel utilisateur, la méthode [**adduser**](diskquotacontrol-adduser.md) retourne l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b48b5-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="b48b5-186">Si vous avez le nom de l’utilisateur, la méthode [**FindUser**](diskquotacontrol-finduser.md) retourne l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b48b5-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="b48b5-187">Cet objet rend les fonctionnalités essentielles de l’interface IDiskQuotaControl disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b48b5-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48b5-188">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b48b5-188">Requirements</span></span>



| <span data-ttu-id="b48b5-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b48b5-189">Requirement</span></span> | <span data-ttu-id="b48b5-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="b48b5-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b48b5-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b48b5-191">Minimum supported client</span></span><br/> | <span data-ttu-id="b48b5-192">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b48b5-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b48b5-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b48b5-193">Minimum supported server</span></span><br/> | <span data-ttu-id="b48b5-194">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b48b5-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b48b5-195">DLL</span><span class="sxs-lookup"><span data-stu-id="b48b5-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b48b5-196"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b48b5-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b48b5-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b48b5-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48b5-198">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="b48b5-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




