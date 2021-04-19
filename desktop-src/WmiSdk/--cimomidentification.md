---
description: Décrit l’installation locale de WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Classe __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530599"
---
# <a name="__cimomidentification-class"></a><span data-ttu-id="761f2-103">\_\_CIMOMIdentification, classe</span><span class="sxs-lookup"><span data-stu-id="761f2-103">\_\_CIMOMIdentification class</span></span>

<span data-ttu-id="761f2-104">La classe système **\_ \_ CIMOMIdentification** décrit l’installation locale de WMI.</span><span class="sxs-lookup"><span data-stu-id="761f2-104">The **\_\_CIMOMIdentification** system class describes the local installation of WMI.</span></span> <span data-ttu-id="761f2-105">Il s’agit d’une classe singleton. Il n’existe qu’une seule instance.</span><span class="sxs-lookup"><span data-stu-id="761f2-105">This is a singleton class; there is only one instance.</span></span> <span data-ttu-id="761f2-106">La classe **\_ \_ CIMOMIdentification** est disponible uniquement dans les espaces de noms **root** et **root \\ par défaut** .</span><span class="sxs-lookup"><span data-stu-id="761f2-106">The **\_\_CIMOMIdentification** class is available only in the **Root** and **Root\\Default** namespaces.</span></span> <span data-ttu-id="761f2-107">Les utilisateurs interrogent l’instance pour obtenir des informations sur l’installation de WMI.</span><span class="sxs-lookup"><span data-stu-id="761f2-107">Users query for the instance to obtain information about the WMI installation.</span></span>

<span data-ttu-id="761f2-108">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="761f2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="761f2-109">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="761f2-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="761f2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="761f2-110">Syntax</span></span>

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a><span data-ttu-id="761f2-111">Membres</span><span class="sxs-lookup"><span data-stu-id="761f2-111">Members</span></span>

<span data-ttu-id="761f2-112">La classe **\_ \_ CIMOMIdentification** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="761f2-112">The **\_\_CIMOMIdentification** class has these types of members:</span></span>

-   [<span data-ttu-id="761f2-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="761f2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="761f2-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="761f2-114">Properties</span></span>

<span data-ttu-id="761f2-115">La classe **\_ \_ CIMOMIdentification** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="761f2-115">The **\_\_CIMOMIdentification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="761f2-116">**SetupDateTime**</span><span class="sxs-lookup"><span data-stu-id="761f2-116">**SetupDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="761f2-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="761f2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="761f2-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="761f2-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="761f2-119">Date et heure de l’installation.</span><span class="sxs-lookup"><span data-stu-id="761f2-119">Date and time of installation.</span></span> <span data-ttu-id="761f2-120">Cette propriété est vide après l’installation du système d’exploitation pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="761f2-120">This property is empty after the operating system is installed for the first time.</span></span>

<span data-ttu-id="761f2-121">Si le référentiel WMI a été supprimé, puis recréé, cette propriété contient la date et l’heure de la création du dépôt.</span><span class="sxs-lookup"><span data-stu-id="761f2-121">If the WMI repository has been deleted and then created again, this property contains the date and time that the repository is created again.</span></span>

</dd> <dt>

<span data-ttu-id="761f2-122">**VersionCurrentlyRunning**</span><span class="sxs-lookup"><span data-stu-id="761f2-122">**VersionCurrentlyRunning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="761f2-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="761f2-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="761f2-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="761f2-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="761f2-125">Indique la version de l’image réelle contenant le service WMI qui a créé le référentiel Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="761f2-125">Indicates the version of the actual image containing the WMI service that created the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="761f2-126">Étant donné que le format de référentiel peut changer d’une version à l’autre de WMI, cette propriété autorise les futures mises à niveau de WMI pour déterminer si la base de données doit être mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="761f2-126">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="761f2-127">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="761f2-127">The format is:</span></span>

<span data-ttu-id="761f2-128">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="761f2-128">"1.00.183.0000"</span></span>

<span data-ttu-id="761f2-129">où le premier chiffre est la version principale, les deux chiffres suivants sont des versions mineures, et les trois chiffres suivants sont le numéro de Build.</span><span class="sxs-lookup"><span data-stu-id="761f2-129">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="761f2-130">Les chiffres restants ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="761f2-130">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="761f2-131">**VersionUsedToCreateDB**</span><span class="sxs-lookup"><span data-stu-id="761f2-131">**VersionUsedToCreateDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="761f2-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="761f2-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="761f2-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="761f2-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="761f2-134">Indique la version de l’image réelle contenant le service WMI qui a créé le référentiel CIM.</span><span class="sxs-lookup"><span data-stu-id="761f2-134">Indicates the version of the actual image containing the WMI service that created the CIM repository.</span></span> <span data-ttu-id="761f2-135">Étant donné que le format de référentiel peut changer d’une version à l’autre de WMI, cette propriété autorise les futures mises à niveau de WMI pour déterminer si la base de données doit être mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="761f2-135">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="761f2-136">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="761f2-136">The format is:</span></span>

<span data-ttu-id="761f2-137">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="761f2-137">"1.00.183.0000"</span></span>

<span data-ttu-id="761f2-138">où le premier chiffre est la version principale, les deux chiffres suivants sont des versions mineures, et les trois chiffres suivants sont le numéro de Build.</span><span class="sxs-lookup"><span data-stu-id="761f2-138">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="761f2-139">Les chiffres restants ne sont pas utilisés.</span><span class="sxs-lookup"><span data-stu-id="761f2-139">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="761f2-140">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="761f2-140">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="761f2-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="761f2-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="761f2-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="761f2-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="761f2-143">Répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="761f2-143">Installation directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="761f2-144">Notes</span><span class="sxs-lookup"><span data-stu-id="761f2-144">Remarks</span></span>

<span data-ttu-id="761f2-145">La classe **\_ \_ CIMOMIdentification** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="761f2-145">The **\_\_CIMOMIdentification** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

## <a name="examples"></a><span data-ttu-id="761f2-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="761f2-146">Examples</span></span>

<span data-ttu-id="761f2-147">L’exemple de code VBScript suivant décrit comment afficher les informations d’identification du modèle d’objet CIM et provient de l’exemple de répertoire situé dans \\ \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ Scripting.</span><span class="sxs-lookup"><span data-stu-id="761f2-147">The following VBScript code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



<span data-ttu-id="761f2-148">L’exemple de code perl suivant décrit comment afficher les informations d’identification du modèle d’objet CIM et provient de l’exemple de répertoire situé dans \\ \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ sysmgmt \\ WMI \\ Scripting.</span><span class="sxs-lookup"><span data-stu-id="761f2-148">The following Perl code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="761f2-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="761f2-149">Requirements</span></span>



| <span data-ttu-id="761f2-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="761f2-150">Requirement</span></span> | <span data-ttu-id="761f2-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="761f2-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="761f2-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="761f2-152">Minimum supported client</span></span><br/> | <span data-ttu-id="761f2-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="761f2-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="761f2-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="761f2-154">Minimum supported server</span></span><br/> | <span data-ttu-id="761f2-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="761f2-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="761f2-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="761f2-156">Namespace</span></span><br/>                | <span data-ttu-id="761f2-157">Root</span><span class="sxs-lookup"><span data-stu-id="761f2-157">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="761f2-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="761f2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="761f2-159">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="761f2-159">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="761f2-160">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="761f2-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

