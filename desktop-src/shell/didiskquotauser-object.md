---
description: Permet à un client de gérer les paramètres de quota de disque global d’un volume NTFS. Cet objet rend les fonctionnalités essentielles de l’interface DIDiskQuotaUser disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.
title: Objet DIDiskQuotaUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843240"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="c6001-104">Objet DIDiskQuotaUser</span><span class="sxs-lookup"><span data-stu-id="c6001-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="c6001-105">Permet à un client de gérer les paramètres de quota de disque global d’un volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="c6001-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="c6001-106">Cet objet rend les fonctionnalités essentielles de l’interface **DIDiskQuotaUser** disponibles pour les scripts et les applications basées sur Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c6001-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="c6001-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c6001-107">Members</span></span>

<span data-ttu-id="c6001-108">L’objet **DIDiskQuotaUser** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c6001-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="c6001-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c6001-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c6001-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c6001-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c6001-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c6001-111">Methods</span></span>

<span data-ttu-id="c6001-112">L’objet **DIDiskQuotaUser** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c6001-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="c6001-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="c6001-113">Method</span></span>                                           | <span data-ttu-id="c6001-114">Description</span><span class="sxs-lookup"><span data-stu-id="c6001-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="c6001-115">**Invalidate**</span><span class="sxs-lookup"><span data-stu-id="c6001-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="c6001-116">Efface les informations utilisateur mises en cache de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c6001-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c6001-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c6001-117">Properties</span></span>

<span data-ttu-id="c6001-118">L’objet **DIDiskQuotaUser** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c6001-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="c6001-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="c6001-119">Property</span></span>                                                                        | <span data-ttu-id="c6001-120">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c6001-120">Access type</span></span>           | <span data-ttu-id="c6001-121">Description</span><span class="sxs-lookup"><span data-stu-id="c6001-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6001-122">**AccountContainerName**</span><span class="sxs-lookup"><span data-stu-id="c6001-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="c6001-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-123">Read-only</span></span><br/>  | <span data-ttu-id="c6001-124">Obtient le nom du conteneur de compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="c6001-125">**AccountStatus**</span><span class="sxs-lookup"><span data-stu-id="c6001-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="c6001-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-126">Read-only</span></span><br/>  | <span data-ttu-id="c6001-127">Obtient l’état du compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="c6001-128">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="c6001-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="c6001-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-129">Read-only</span></span><br/>  | <span data-ttu-id="c6001-130">Obtient le nom complet de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="c6001-131">**ID**</span><span class="sxs-lookup"><span data-stu-id="c6001-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="c6001-132">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-132">Read-only</span></span><br/>  | <span data-ttu-id="c6001-133">Obtient un ID qui identifie de façon unique l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="c6001-134">**LogonName**</span><span class="sxs-lookup"><span data-stu-id="c6001-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="c6001-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-135">Read-only</span></span><br/>  | <span data-ttu-id="c6001-136">Obtient le nom du compte d’ouverture de session de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="c6001-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="c6001-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="c6001-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c6001-138">Read/write</span></span><br/> | <span data-ttu-id="c6001-139">Définit ou obtient la [**limite de quota**](diskquotacontrol-object.md)actuelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="c6001-140">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="c6001-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="c6001-141">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-141">Read-only</span></span><br/>  | <span data-ttu-id="c6001-142">Obtient la [**limite de quota**](diskquotacontrol-object.md) actuelle de l’utilisateur sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="c6001-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="c6001-143">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="c6001-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="c6001-144">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c6001-144">Read/write</span></span><br/> | <span data-ttu-id="c6001-145">Définit ou obtient le seuil d’avertissement de l’utilisateur, en octets.</span><span class="sxs-lookup"><span data-stu-id="c6001-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="c6001-146">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="c6001-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="c6001-147">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-147">Read-only</span></span><br/>  | <span data-ttu-id="c6001-148">Obtient le seuil d’avertissement de l’utilisateur sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="c6001-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="c6001-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="c6001-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="c6001-150">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-150">Read-only</span></span><br/>  | <span data-ttu-id="c6001-151">Obtient l’utilisation actuelle du disque de l’utilisateur, en octets.</span><span class="sxs-lookup"><span data-stu-id="c6001-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="c6001-152">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="c6001-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="c6001-153">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c6001-153">Read-only</span></span><br/>  | <span data-ttu-id="c6001-154">Obtient l’utilisation du disque actuel de l’utilisateur sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="c6001-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="c6001-155">Notes</span><span class="sxs-lookup"><span data-stu-id="c6001-155">Remarks</span></span>

<span data-ttu-id="c6001-156">Chaque utilisateur sur le volume qui est géré par l’objet [**DiskQuotaControl**](diskquotacontrol-object.md) est associé à un objet **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="c6001-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="c6001-157">Cet objet permet à un client de gérer les paramètres d’un utilisateur individuel.</span><span class="sxs-lookup"><span data-stu-id="c6001-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="c6001-158">Il existe plusieurs façons d’obtenir l’objet **DIDiskQuotaUser** d’un utilisateur :</span><span class="sxs-lookup"><span data-stu-id="c6001-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="c6001-159">Les objets **DIDiskQuotaUser** pour tous les utilisateurs avec quotas sur le volume sont exposés en tant que collection et peuvent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="c6001-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="c6001-160">Vous trouverez ci-dessous une discussion sur l’énumération des objets **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="c6001-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="c6001-161">Lorsque vous ajoutez un nouvel utilisateur, la méthode [**adduser**](diskquotacontrol-adduser.md) retourne l’objet **DIDiskQuotaUser** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="c6001-162">Si vous avez le nom de l’utilisateur, la méthode [**FindUser**](diskquotacontrol-finduser.md) retourne l’objet **DIDiskQuotaUser** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c6001-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="c6001-163">Énumération des utilisateurs du quota de disque</span><span class="sxs-lookup"><span data-stu-id="c6001-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="c6001-164">Les objets **DIDiskQuotaUser** pour tous les utilisateurs avec un quota sur le volume sont exposés en tant que collection.</span><span class="sxs-lookup"><span data-stu-id="c6001-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="c6001-165">L’objet [**DiskQuotaControl**](diskquotacontrol-object.md) exporte une méthode d’énumérateur standard qui vous permet d’énumérer la collection d’objets **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="c6001-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="c6001-166">La procédure suivante montre comment effectuer l’énumération avec Microsoft JScript (compatible avec la spécification du langage ECMA 262).</span><span class="sxs-lookup"><span data-stu-id="c6001-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="c6001-167">Vous pouvez utiliser une procédure similaire avec Visual Basic ou Microsoft Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c6001-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="c6001-168">Créez un nouvel objet [**DiskQuotaControl**](diskquotacontrol-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c6001-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="c6001-169">Initialisez-le avec [**Initialize**](diskquotacontrol-initialize.md).</span><span class="sxs-lookup"><span data-stu-id="c6001-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="c6001-170">Créez un nouvel objet **énumérateur** JScript.</span><span class="sxs-lookup"><span data-stu-id="c6001-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="c6001-171">Utilisez une boucle **for** pour énumérer les objets **DIDiskQuotaUser** .</span><span class="sxs-lookup"><span data-stu-id="c6001-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="c6001-172">Il n’est pas nécessaire de définir une valeur de départ.</span><span class="sxs-lookup"><span data-stu-id="c6001-172">There is no need to set a starting value.</span></span> <span data-ttu-id="c6001-173">La méthode **MoveNext** de l’objet Enumerator indique à la méthode **Item** de retourner l’objet **DIDiskQuotaUser** suivant.</span><span class="sxs-lookup"><span data-stu-id="c6001-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="c6001-174">La méthode **atEnd** retourne la **valeur false** lorsque vous atteignez la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="c6001-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="c6001-175">Si nécessaire, utilisez l’objet **DIDiskQuotaUser** retourné par la méthode **Item** de l’énumérateur pour récupérer ou définir une ou plusieurs des propriétés de quota de disque de l’utilisateur associé.</span><span class="sxs-lookup"><span data-stu-id="c6001-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="c6001-176">Le fragment de code suivant montre comment énumérer les objets **DIDiskQuotaUser** avec JScript.</span><span class="sxs-lookup"><span data-stu-id="c6001-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="c6001-177">L’argument de **\_ nom de volume** qui est passé à la fonction **EnumUsers** est une valeur de chaîne contenant un nom de volume tel que « C : \\ \\ ».</span><span class="sxs-lookup"><span data-stu-id="c6001-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a><span data-ttu-id="c6001-178">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c6001-178">Requirements</span></span>



| <span data-ttu-id="c6001-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6001-179">Requirement</span></span> | <span data-ttu-id="c6001-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6001-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6001-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6001-181">Minimum supported client</span></span><br/> | <span data-ttu-id="c6001-182">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6001-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6001-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6001-183">Minimum supported server</span></span><br/> | <span data-ttu-id="c6001-184">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6001-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c6001-185">DLL</span><span class="sxs-lookup"><span data-stu-id="c6001-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6001-186"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c6001-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6001-187">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6001-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6001-188">**Objet Shell**</span><span class="sxs-lookup"><span data-stu-id="c6001-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




