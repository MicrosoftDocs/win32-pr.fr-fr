---
description: Utilisé pour sécuriser des parties individuelles d’une application dans un environnement verrouillé. Il peut être utilisé avec l’installation des fichiers, les clés de Registre et les dossiers créés.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Table LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524636"
---
# <a name="lockpermissions-table"></a><span data-ttu-id="ff03c-104">Table LockPermissions</span><span class="sxs-lookup"><span data-stu-id="ff03c-104">LockPermissions Table</span></span>

<span data-ttu-id="ff03c-105">La table LockPermissions est utilisée pour sécuriser des parties individuelles d’une application dans un environnement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="ff03c-105">The LockPermissions Table is used to secure individual portions of an application in a locked-down environment.</span></span> <span data-ttu-id="ff03c-106">Il peut être utilisé avec l’installation des fichiers, les clés de Registre et les dossiers créés.</span><span class="sxs-lookup"><span data-stu-id="ff03c-106">It can be used with the installation of files, registry keys, and created folders.</span></span>

<span data-ttu-id="ff03c-107">Un package destiné à être installé dans Windows Server 2008 R2 ou Windows 7 doit utiliser la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) au lieu de la table LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="ff03c-107">A package intended for installation in Windows Server 2008 R2 or Windows 7 should use the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) rather than the LockPermissions Table.</span></span> <span data-ttu-id="ff03c-108">Windows Installer versions antérieures à Windows Installer 5,0 ignorent la table MsiLockPermissionsEx.</span><span class="sxs-lookup"><span data-stu-id="ff03c-108">Windows Installer versions earlier than Windows Installer 5.0 ignore the MsiLockPermissionsEx Table.</span></span> <span data-ttu-id="ff03c-109">Windows Installer 5,0 peut installer un package qui contient la table LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="ff03c-109">Windows Installer 5.0 can install an package that contains the LockPermissions Table.</span></span> <span data-ttu-id="ff03c-110">À compter de Windows Installer 5,0, l’installation d’un package qui contient à la fois la table MsiLockPermissionsEx et la table LockPermissions échoue et retourne Windows Installer message d’erreur 1941.</span><span class="sxs-lookup"><span data-stu-id="ff03c-110">Beginning with Windows Installer 5.0, installation of a package that contains both the MsiLockPermissionsEx Table and the LockPermissions Table fails and returns Windows Installer error message 1941.</span></span>

<span data-ttu-id="ff03c-111">La table LockPermissions contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="ff03c-111">The LockPermissions Table has the following columns.</span></span>



| <span data-ttu-id="ff03c-112">Colonne</span><span class="sxs-lookup"><span data-stu-id="ff03c-112">Column</span></span>     | <span data-ttu-id="ff03c-113">Type</span><span class="sxs-lookup"><span data-stu-id="ff03c-113">Type</span></span>                               | <span data-ttu-id="ff03c-114">Clé</span><span class="sxs-lookup"><span data-stu-id="ff03c-114">Key</span></span> | <span data-ttu-id="ff03c-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="ff03c-115">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="ff03c-116">LockObject</span><span class="sxs-lookup"><span data-stu-id="ff03c-116">LockObject</span></span> | [<span data-ttu-id="ff03c-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="ff03c-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="ff03c-118">O</span><span class="sxs-lookup"><span data-stu-id="ff03c-118">Y</span></span>   | <span data-ttu-id="ff03c-119">N</span><span class="sxs-lookup"><span data-stu-id="ff03c-119">N</span></span>        |
| <span data-ttu-id="ff03c-120">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="ff03c-120">Table</span></span>      | [<span data-ttu-id="ff03c-121">Text</span><span class="sxs-lookup"><span data-stu-id="ff03c-121">Text</span></span>](text.md)                   | <span data-ttu-id="ff03c-122">O</span><span class="sxs-lookup"><span data-stu-id="ff03c-122">Y</span></span>   | <span data-ttu-id="ff03c-123">N</span><span class="sxs-lookup"><span data-stu-id="ff03c-123">N</span></span>        |
| <span data-ttu-id="ff03c-124">Domain</span><span class="sxs-lookup"><span data-stu-id="ff03c-124">Domain</span></span>     | [<span data-ttu-id="ff03c-125">Correct</span><span class="sxs-lookup"><span data-stu-id="ff03c-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="ff03c-126">O</span><span class="sxs-lookup"><span data-stu-id="ff03c-126">Y</span></span>   | <span data-ttu-id="ff03c-127">O</span><span class="sxs-lookup"><span data-stu-id="ff03c-127">Y</span></span>        |
| <span data-ttu-id="ff03c-128">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="ff03c-128">User</span></span>       | [<span data-ttu-id="ff03c-129">Correct</span><span class="sxs-lookup"><span data-stu-id="ff03c-129">Formatted</span></span>](formatted.md)         | <span data-ttu-id="ff03c-130">O</span><span class="sxs-lookup"><span data-stu-id="ff03c-130">Y</span></span>   | <span data-ttu-id="ff03c-131">N</span><span class="sxs-lookup"><span data-stu-id="ff03c-131">N</span></span>        |
| <span data-ttu-id="ff03c-132">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ff03c-132">Permission</span></span> | [<span data-ttu-id="ff03c-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="ff03c-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="ff03c-134">N</span><span class="sxs-lookup"><span data-stu-id="ff03c-134">N</span></span>   | <span data-ttu-id="ff03c-135">O</span><span class="sxs-lookup"><span data-stu-id="ff03c-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ff03c-136">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ff03c-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ff03c-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="ff03c-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="ff03c-138">Cette colonne et la colonne de table spécifient ensemble le fichier, le répertoire ou la clé de Registre à sécuriser.</span><span class="sxs-lookup"><span data-stu-id="ff03c-138">This column and the Table column together specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="ff03c-139">La colonne LockObject est une clé étrangère qui pointe vers la clé primaire de la table spécifiée par la colonne de table.</span><span class="sxs-lookup"><span data-stu-id="ff03c-139">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="ff03c-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="ff03c-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="ff03c-141">Cette colonne et la colonne LockObject spécifient le fichier, le répertoire ou la clé de Registre à sécuriser.</span><span class="sxs-lookup"><span data-stu-id="ff03c-141">This column and the LockObject column specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="ff03c-142">Dans la colonne table, entrez file, Registry ou CreateFolder pour spécifier un LockObject listé dans la table [file](file-table.md), la table [Registry](registry-table.md)ou [CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff03c-142">In the Table column, enter File, Registry, or CreateFolder to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), or [CreateFolder Table](createfolder-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="ff03c-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span><span class="sxs-lookup"><span data-stu-id="ff03c-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span></span>
</dt> <dd>

<span data-ttu-id="ff03c-144">Colonne qui identifie le domaine de l’utilisateur pour lequel les autorisations doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="ff03c-144">The column that identifies the domain of the user for which permissions are to be set.</span></span> <span data-ttu-id="ff03c-145">Il s’agit du nom d’un ordinateur autonome ou d’un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="ff03c-145">This is the name of a stand-alone machine or a domain name.</span></span> <span data-ttu-id="ff03c-146">Le type de données de la colonne est [mis en forme](formatted.md)et vous pouvez utiliser la chaîne \[ % UserDomain \] dans ce champ pour obtenir la valeur de la variable d’environnement UserDomain pour le domaine actuel.</span><span class="sxs-lookup"><span data-stu-id="ff03c-146">The column data type is [Formatted](formatted.md), and you may use the string \[%USERDOMAIN\] in this field to get the value of the USERDOMAIN environment variable for the current domain.</span></span> <span data-ttu-id="ff03c-147">Pour faire en sorte que tout autre domaine requiert l’utilisation d' [actions personnalisées](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ff03c-147">To get any other domain requires using [Custom Actions](custom-actions.md).</span></span> <span data-ttu-id="ff03c-148">Pour plus d’informations, consultez le tableau des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="ff03c-148">For more information, see the Custom Action Table.</span></span>

</dd> <dt>

<span data-ttu-id="ff03c-149"><span id="User"></span><span id="user"></span><span id="USER"></span>Utilisateur</span><span class="sxs-lookup"><span data-stu-id="ff03c-149"><span id="User"></span><span id="user"></span><span id="USER"></span>User</span></span>
</dt> <dd>

<span data-ttu-id="ff03c-150">Colonne qui identifie le nom localisé de l’utilisateur pour lequel les autorisations doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="ff03c-150">The column that identifies the localized name of the user for which permissions are to be set.</span></span> <span data-ttu-id="ff03c-151">Ce nom doit se trouver sur l’ordinateur ou le domaine.</span><span class="sxs-lookup"><span data-stu-id="ff03c-151">This name must be located on the machine or domain.</span></span> <span data-ttu-id="ff03c-152">L’installation échoue si l’ordinateur ou le contrôleur de domaine ne reconnaît pas la combinaison de domaine et d’utilisateur, ou si l’identificateur de sécurité (SID) de l’utilisateur ne peut pas être récupéré.</span><span class="sxs-lookup"><span data-stu-id="ff03c-152">The installation fails if the machine or domain controller does not recognize the domain and user combination or if the user's security identifier (SID) cannot be retrieved.</span></span> <span data-ttu-id="ff03c-153">Plusieurs utilisateurs peuvent être spécifiés pour un seul LockObject.</span><span class="sxs-lookup"><span data-stu-id="ff03c-153">Multiple users can be specified for a single LockObject.</span></span>

<span data-ttu-id="ff03c-154">Les noms d’utilisateur courants « tout le monde » et « administrateurs » peuvent être entrés en anglais et mappés à des SID connus.</span><span class="sxs-lookup"><span data-stu-id="ff03c-154">The common user names "Everyone" and "Administrators" may be entered in English and are mapped to well-known SIDs.</span></span> <span data-ttu-id="ff03c-155">LocalSystem reçoit un contrôle total sur tous les descripteurs de sécurité créés par le biais de la table LockPermissions.</span><span class="sxs-lookup"><span data-stu-id="ff03c-155">LocalSystem is given full control in all security descriptors created through the LockPermissions Table.</span></span> <span data-ttu-id="ff03c-156">Vous pouvez utiliser la propriété [**ComputerName**](computername.md), la propriété [**LogonUser**](logonuser.md) ou la [**propriété UserName**](username.md) dans ce champ pour accéder à l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="ff03c-156">You can use the [**ComputerName Property**](computername.md), [**LogonUser Property**](logonuser.md) or [**USERNAME Property**](username.md) in this field to get the current user.</span></span> <span data-ttu-id="ff03c-157">Une action personnalisée est nécessaire pour entrer le nom localisé d’un autre utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="ff03c-157">A custom action is required to enter the localized name of any other user or group.</span></span>

<span data-ttu-id="ff03c-158">Vous pouvez utiliser plusieurs enregistrements avec des entrées de données et des entrées de table identiques (mais différentes entrées utilisateur) pour spécifier des listes de contrôle d’accès pour plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ff03c-158">You can use multiple records with identical LockObject and Table entries (but different User entries) to specify access control lists for multiple users.</span></span>

</dd> <dt>

<span data-ttu-id="ff03c-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Autorisées</span><span class="sxs-lookup"><span data-stu-id="ff03c-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permission</span></span>
</dt> <dd>

<span data-ttu-id="ff03c-160">Colonne qui identifie la description entière des privilèges système.</span><span class="sxs-lookup"><span data-stu-id="ff03c-160">The column that identifies the integer description of system privileges.</span></span> <span data-ttu-id="ff03c-161">Les éléments suivants fournissent les valeurs les plus couramment utilisées (une liste complète existe dans Winnt. h).</span><span class="sxs-lookup"><span data-stu-id="ff03c-161">The following gives the most commonly used values (a complete list exists in Winnt.h).</span></span>



| <span data-ttu-id="ff03c-162">Privilège</span><span class="sxs-lookup"><span data-stu-id="ff03c-162">Privilege</span></span>                                                              | <span data-ttu-id="ff03c-163">Description</span><span class="sxs-lookup"><span data-stu-id="ff03c-163">Description</span></span>                     |
|------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="ff03c-164">GÉNÉRIQUE \_ tout</span><span class="sxs-lookup"><span data-stu-id="ff03c-164">GENERIC\_ALL</span></span><br/> <span data-ttu-id="ff03c-165">0X10000000</span><span class="sxs-lookup"><span data-stu-id="ff03c-165">0X10000000</span></span><br/> <span data-ttu-id="ff03c-166">268435456</span><span class="sxs-lookup"><span data-stu-id="ff03c-166">268435456</span></span><br/>     | <span data-ttu-id="ff03c-167">Accès en lecture, écriture et exécution</span><span class="sxs-lookup"><span data-stu-id="ff03c-167">Read, write, and execute access</span></span> |
| <span data-ttu-id="ff03c-168">\_Exécution générique</span><span class="sxs-lookup"><span data-stu-id="ff03c-168">GENERIC\_EXECUTE</span></span><br/> <span data-ttu-id="ff03c-169">0X20000000</span><span class="sxs-lookup"><span data-stu-id="ff03c-169">0X20000000</span></span><br/> <span data-ttu-id="ff03c-170">536870912</span><span class="sxs-lookup"><span data-stu-id="ff03c-170">536870912</span></span><br/> | <span data-ttu-id="ff03c-171">Exécuter l’accès</span><span class="sxs-lookup"><span data-stu-id="ff03c-171">Execute access</span></span>                  |
| <span data-ttu-id="ff03c-172">\_écriture générique</span><span class="sxs-lookup"><span data-stu-id="ff03c-172">GENERIC\_WRITE</span></span><br/> <span data-ttu-id="ff03c-173">0X40000000</span><span class="sxs-lookup"><span data-stu-id="ff03c-173">0X40000000</span></span><br/> <span data-ttu-id="ff03c-174">1073741824</span><span class="sxs-lookup"><span data-stu-id="ff03c-174">1073741824</span></span><br/>  | <span data-ttu-id="ff03c-175">Accès en écriture</span><span class="sxs-lookup"><span data-stu-id="ff03c-175">Write access</span></span>                    |



 

<span data-ttu-id="ff03c-176">Vous ne pouvez pas spécifier une \_ lecture générique dans la colonne autorisation.</span><span class="sxs-lookup"><span data-stu-id="ff03c-176">You cannot specify GENERIC\_READ in the Permission column.</span></span> <span data-ttu-id="ff03c-177">Toute tentative d’opération échouera.</span><span class="sxs-lookup"><span data-stu-id="ff03c-177">Attempting to do so will fail.</span></span> <span data-ttu-id="ff03c-178">Au lieu de cela, vous devez spécifier une valeur telle que \_ lecture clé ou fichier \_ générique \_ lecture.</span><span class="sxs-lookup"><span data-stu-id="ff03c-178">Instead, you must specify a value such as KEY\_READ or FILE\_GENERIC\_READ.</span></span>

<span data-ttu-id="ff03c-179">La valeur null entrée dans cette colonne est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ff03c-179">Null entered in this column is reserved for future use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff03c-180">Notes</span><span class="sxs-lookup"><span data-stu-id="ff03c-180">Remarks</span></span>

<span data-ttu-id="ff03c-181">Les actions [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md)et [CreateFolders](createfolders-action.md) dans les [*tables de séquence*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ff03c-181">The [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md), and [CreateFolders](createfolders-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="ff03c-182">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ff03c-182">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="ff03c-183">L’autorisation ne peut être définie que dans la table LockPermissions pour les utilisateurs qui existent déjà sur l’ordinateur ou le domaine.</span><span class="sxs-lookup"><span data-stu-id="ff03c-183">Permission can only be set in the LockPermissions Table for users that already exist on the computer or domain.</span></span> <span data-ttu-id="ff03c-184">Une tentative de définition d’autorisations pour un utilisateur inconnu entraîne l’échec de l’installation, même si ce compte d’utilisateur est créé lors de l’installation par une action personnalisée différée.</span><span class="sxs-lookup"><span data-stu-id="ff03c-184">An attempt to set permissions for an unknown user causes the installation to fail, even if that user account is created during the installation by a deferred custom action.</span></span>

<span data-ttu-id="ff03c-185">Il est recommandé que le groupe local de l’administrateur système soit inclus dans toutes les listes de contrôle d’accès (ACL).</span><span class="sxs-lookup"><span data-stu-id="ff03c-185">It is recommended that the system administrator's local group be included in all access control lists (ACL).</span></span> <span data-ttu-id="ff03c-186">Cela permet de s’assurer que l’administrateur système peut accéder aux objets et les gérer.</span><span class="sxs-lookup"><span data-stu-id="ff03c-186">This ensures that the system administrator can access and maintain objects.</span></span>

<span data-ttu-id="ff03c-187">Chaque fichier, clé de registre ou répertoire figurant dans la table LockPermissions reçoit un descripteur de sécurité explicite, qu’il remplace ou non un objet existant.</span><span class="sxs-lookup"><span data-stu-id="ff03c-187">Every file, registry key, or directory that is listed in the LockPermissions Table receives an explicit security descriptor, whether it replaces an existing object or not.</span></span> <span data-ttu-id="ff03c-188">Le Windows Installer tente de préserver la sécurité sur les objets qui existent déjà sur le système.</span><span class="sxs-lookup"><span data-stu-id="ff03c-188">The Windows Installer attempts to preserve the security on objects that already exist on the system.</span></span> <span data-ttu-id="ff03c-189">Si un objet n’est pas listé dans la table LockPermissions et remplace un objet existant, le remplacement obtient les paramètres de sécurité de l’objet qu’il remplace.</span><span class="sxs-lookup"><span data-stu-id="ff03c-189">If an object is not listed in the LockPermissions Table, and replaces an existing object, the replacement gets the security settings of the object that it replaces.</span></span>

<span data-ttu-id="ff03c-190">Si un objet n’est pas listé dans la table LockPermissions et qu’il ne remplace pas un objet existant, il ne reçoit pas de descripteur de sécurité explicite.</span><span class="sxs-lookup"><span data-stu-id="ff03c-190">If an object is not listed in the LockPermissions Table, and does not replace an existing object, it receives no explicit security descriptor.</span></span> <span data-ttu-id="ff03c-191">L’accès au nouvel objet est basé sur les attributs de son objet parent ou conteneur.</span><span class="sxs-lookup"><span data-stu-id="ff03c-191">The access to the new object is based on the attributes of its parent or container object.</span></span> <span data-ttu-id="ff03c-192">Si un objet n’est pas listé dans le tableau et remplace un objet sans descripteur de sécurité explicite, l’accès au nouvel objet est basé sur les attributs de son objet parent ou conteneur.</span><span class="sxs-lookup"><span data-stu-id="ff03c-192">If an object is not listed in the table, and replaces an object with no explicit security descriptor, the access to the new object is based on the attributes of its parent or container object.</span></span>

<span data-ttu-id="ff03c-193">L’Windows Installer définit la propriété [**UserSid**](usersid.md) sur l’identificateur de sécurité (SID) ou l’utilisateur qui exécute l’installation.</span><span class="sxs-lookup"><span data-stu-id="ff03c-193">The Windows Installer sets the [**UserSID**](usersid.md) property to the security identifier (SID) or the user running the installation.</span></span>

## <a name="validation"></a><span data-ttu-id="ff03c-194">Validation</span><span class="sxs-lookup"><span data-stu-id="ff03c-194">Validation</span></span>

<dl>

[<span data-ttu-id="ff03c-195">ICE03</span><span class="sxs-lookup"><span data-stu-id="ff03c-195">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ff03c-196">ICE06</span><span class="sxs-lookup"><span data-stu-id="ff03c-196">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ff03c-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="ff03c-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="ff03c-198">ICE55</span><span class="sxs-lookup"><span data-stu-id="ff03c-198">ICE55</span></span>](ice55.md)  
</dl>

 

 




