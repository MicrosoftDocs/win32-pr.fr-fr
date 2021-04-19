---
description: La table MsiLockPermissionsEx peut être utilisée pour sécuriser les services, les fichiers, les clés de Registre et les dossiers créés.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Table MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536407"
---
# <a name="msilockpermissionsex-table"></a><span data-ttu-id="49ecf-103">Table MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="49ecf-103">MsiLockPermissionsEx Table</span></span>

<span data-ttu-id="49ecf-104">La table MsiLockPermissionsEx peut être utilisée pour sécuriser les services, les fichiers, les clés de Registre et les dossiers créés.</span><span class="sxs-lookup"><span data-stu-id="49ecf-104">The MsiLockPermissionsEx Table can be used to secure services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="49ecf-105">Un package ne doit pas contenir à la fois la table MsiLockPermissionsEx et la [table LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="49ecf-105">A package should not contain both the MsiLockPermissionsEx Table and the [LockPermissions Table](lockpermissions-table.md).</span></span>

<span data-ttu-id="49ecf-106">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="49ecf-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="49ecf-107">Ce tableau est recommandé pour les packages destinés à une installation avec Windows Installer 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="49ecf-107">This table is recommended for packages intended for installation with Windows Installer 5.0 or later.</span></span>

<span data-ttu-id="49ecf-108">La table MsiLockPermissionsEx contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="49ecf-108">The MsiLockPermissionsEx Table has the following columns.</span></span>



| <span data-ttu-id="49ecf-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="49ecf-109">Column</span></span>               | <span data-ttu-id="49ecf-110">Type</span><span class="sxs-lookup"><span data-stu-id="49ecf-110">Type</span></span>                                       | <span data-ttu-id="49ecf-111">Clé</span><span class="sxs-lookup"><span data-stu-id="49ecf-111">Key</span></span> | <span data-ttu-id="49ecf-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="49ecf-112">Nullable</span></span> |
|----------------------|--------------------------------------------|-----|----------|
| <span data-ttu-id="49ecf-113">MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="49ecf-113">MsiLockPermissionsEx</span></span> | [<span data-ttu-id="49ecf-114">Text</span><span class="sxs-lookup"><span data-stu-id="49ecf-114">Text</span></span>](text.md)                           | <span data-ttu-id="49ecf-115">O</span><span class="sxs-lookup"><span data-stu-id="49ecf-115">Y</span></span>   | <span data-ttu-id="49ecf-116">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-116">N</span></span>        |
| <span data-ttu-id="49ecf-117">LockObject</span><span class="sxs-lookup"><span data-stu-id="49ecf-117">LockObject</span></span>           | [<span data-ttu-id="49ecf-118">Identificateur</span><span class="sxs-lookup"><span data-stu-id="49ecf-118">Identifier</span></span>](identifier.md)               | <span data-ttu-id="49ecf-119">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-119">N</span></span>   | <span data-ttu-id="49ecf-120">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-120">N</span></span>        |
| <span data-ttu-id="49ecf-121">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="49ecf-121">Table</span></span>                | [<span data-ttu-id="49ecf-122">Text</span><span class="sxs-lookup"><span data-stu-id="49ecf-122">Text</span></span>](text.md)                           | <span data-ttu-id="49ecf-123">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-123">N</span></span>   | <span data-ttu-id="49ecf-124">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-124">N</span></span>        |
| <span data-ttu-id="49ecf-125">SDDLText</span><span class="sxs-lookup"><span data-stu-id="49ecf-125">SDDLText</span></span>             | [<span data-ttu-id="49ecf-126">FormattedSDDLText</span><span class="sxs-lookup"><span data-stu-id="49ecf-126">FormattedSDDLText</span></span>](formattedsddltext.md) | <span data-ttu-id="49ecf-127">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-127">N</span></span>   | <span data-ttu-id="49ecf-128">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-128">N</span></span>        |
| <span data-ttu-id="49ecf-129">Condition</span><span class="sxs-lookup"><span data-stu-id="49ecf-129">Condition</span></span>            | [<span data-ttu-id="49ecf-130">Condition</span><span class="sxs-lookup"><span data-stu-id="49ecf-130">Condition</span></span>](condition.md)                 | <span data-ttu-id="49ecf-131">N</span><span class="sxs-lookup"><span data-stu-id="49ecf-131">N</span></span>   | <span data-ttu-id="49ecf-132">O</span><span class="sxs-lookup"><span data-stu-id="49ecf-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="49ecf-133">Colonnes</span><span class="sxs-lookup"><span data-stu-id="49ecf-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="49ecf-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="49ecf-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span></span>
</dt> <dd>

<span data-ttu-id="49ecf-135">Il s’agit de la clé primaire de cette table.</span><span class="sxs-lookup"><span data-stu-id="49ecf-135">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="49ecf-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="49ecf-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="49ecf-137">Cette colonne et la colonne de table spécifient ensemble le fichier, le répertoire, la clé de registre ou le service qui doit être sécurisé.</span><span class="sxs-lookup"><span data-stu-id="49ecf-137">This column and the Table column together specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="49ecf-138">La colonne LockObject est une clé étrangère qui pointe vers la clé primaire de la table spécifiée par la colonne de table.</span><span class="sxs-lookup"><span data-stu-id="49ecf-138">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="49ecf-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="49ecf-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="49ecf-140">Cette colonne et la colonne LockObject spécifient le fichier, le répertoire, la clé de registre ou le service qui doit être sécurisé.</span><span class="sxs-lookup"><span data-stu-id="49ecf-140">This column and the LockObject column specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="49ecf-141">Dans la colonne table, entrez file, Registry, CreateFolder ou ServiceInstall pour spécifier un LockObject listé dans la table [file](file-table.md), la [table Registry](registry-table.md), la [table CreateFolder](createfolder-table.md)ou la [table ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="49ecf-141">In the Table column, enter File, Registry, CreateFolder, or ServiceInstall to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), [CreateFolder Table](createfolder-table.md), or [ServiceInstall Table](serviceinstall-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="49ecf-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span><span class="sxs-lookup"><span data-stu-id="49ecf-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span></span>
</dt> <dd>

<span data-ttu-id="49ecf-143">Entrez la chaîne SDDL pour indiquer les autorisations à appliquer à l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="49ecf-143">Enter the SDDL string to indicate permissions to apply to selected object.</span></span> <span data-ttu-id="49ecf-144">Le SDDL doit être fourni au [format de chaîne de descripteur de sécurité](../secauthz/security-descriptor-string-format.md).</span><span class="sxs-lookup"><span data-stu-id="49ecf-144">The SDDL must be provided in [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span>

<span data-ttu-id="49ecf-145">Cela ne prend pas en charge les propriétés privées ou publiques.</span><span class="sxs-lookup"><span data-stu-id="49ecf-145">This does not support private or public properties.</span></span>

</dd> <dt>

<span data-ttu-id="49ecf-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="49ecf-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="49ecf-147">Cette colonne contient une expression conditionnelle utilisée pour déterminer s’il faut appliquer l’autorisation spécifiée.</span><span class="sxs-lookup"><span data-stu-id="49ecf-147">This column contains a conditional expression used to determine whether to apply the specified permission.</span></span> <span data-ttu-id="49ecf-148">Si la condition prend la **valeur false**, l’autorisation n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="49ecf-148">If the condition evaluates to **FALSE**, the permission is not applied.</span></span> <span data-ttu-id="49ecf-149">Si la condition prend la **valeur true**, l’autorisation est appliquée.</span><span class="sxs-lookup"><span data-stu-id="49ecf-149">If the condition evaluates to **TRUE**, the permission is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49ecf-150">Notes</span><span class="sxs-lookup"><span data-stu-id="49ecf-150">Remarks</span></span>

<span data-ttu-id="49ecf-151">Pour plus d’informations sur la sécurisation des services, des fichiers, des clés de Registre et des dossiers créés, consultez [sécurisation des ressources](securing-resources-.md).</span><span class="sxs-lookup"><span data-stu-id="49ecf-151">See [Securing Resources](securing-resources-.md)for more information about securing services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="49ecf-152">Utilisez la table MsiLockPermissionsEx pour sécuriser les objets d’un compte d’utilisateur en cours de création au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="49ecf-152">Use the MsiLockPermissionsEx Table to secure objects for a user account that is being created during the installation.</span></span> <span data-ttu-id="49ecf-153">Le compte d’utilisateur doit déjà exister lorsque l’installation sécurise l’objet.</span><span class="sxs-lookup"><span data-stu-id="49ecf-153">The user account must already exist when the installation secures the object.</span></span> <span data-ttu-id="49ecf-154">Créez le compte d’utilisateur avant d’installer le fichier, la clé de Registre, le dossier ou le service sécurisé.</span><span class="sxs-lookup"><span data-stu-id="49ecf-154">Create the user account before installing the file, registry key, folder or service being secured.</span></span>

<span data-ttu-id="49ecf-155">Si une paire LockObject et table dans cette table possède plusieurs expressions conditionnelles qui ont la valeur true, l’installation échoue et Windows Installer retourne un message d’erreur 1942.</span><span class="sxs-lookup"><span data-stu-id="49ecf-155">If a LockObject and Table pair in this table has more than one conditional expression that evaluates to true, the installation fails and Windows Installer returns an error message 1942.</span></span>

<span data-ttu-id="49ecf-156">Si la chaîne [FormattedSDDLText](formattedsddltext.md) dans le champ SDDLText ne peut pas être résolue en une chaîne SDDL valide, l’installation échoue et Windows Installer retourne un message d’erreur 1943.</span><span class="sxs-lookup"><span data-stu-id="49ecf-156">If the [FormattedSDDLText](formattedsddltext.md) string in the SDDLText field cannot be resolved into a valid SDDL string, the installation fails and Windows Installer returns an error message 1943.</span></span>

<span data-ttu-id="49ecf-157">Si l’utilisateur ne dispose pas de privilèges suffisants pour définir le descripteur de sécurité spécifié par le champ SDDLText sur un fichier ou un dossier, l’installation échoue et Windows Installer renvoie un message d’erreur 1926.</span><span class="sxs-lookup"><span data-stu-id="49ecf-157">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a file or folder, the installation fails and Windows Installer returns an error message 1926.</span></span>

<span data-ttu-id="49ecf-158">Si l’utilisateur ne dispose pas de privilèges suffisants pour définir le descripteur de sécurité spécifié par le champ SDDLText sur une clé de Registre, l’installation échoue et Windows Installer renvoie un message d’erreur 1401.</span><span class="sxs-lookup"><span data-stu-id="49ecf-158">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a registry key, the installation fails and Windows Installer returns an error message 1401.</span></span>

<span data-ttu-id="49ecf-159">Si l’utilisateur ne dispose pas de privilèges suffisants pour définir le descripteur de sécurité spécifié par le champ SDDLText sur un service, l’installation échoue et Windows Installer renvoie un message d’erreur 1944.</span><span class="sxs-lookup"><span data-stu-id="49ecf-159">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a service, the installation fails and Windows Installer returns an error message 1944.</span></span>

## <a name="validation"></a><span data-ttu-id="49ecf-160">Validation</span><span class="sxs-lookup"><span data-stu-id="49ecf-160">Validation</span></span>

<dl>

[<span data-ttu-id="49ecf-161">ICE104</span><span class="sxs-lookup"><span data-stu-id="49ecf-161">ICE104</span></span>](ice-104.md)  
[<span data-ttu-id="49ecf-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="49ecf-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="49ecf-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="49ecf-163">ICE06</span></span>](ice06.md)  
</dl>

 

 
