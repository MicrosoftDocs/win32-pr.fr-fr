---
title: Classe Win32_RDMSPublishedApplication
description: Gère une application publiée.
ms.assetid: 7a529f1d-1aaf-42fb-8469-92d38a7b0ffc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSPublishedApplication de la classe Services Bureau à distance
- Win32_RDMSPublishedApplication de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSPublishedApplication
- Win32_RDMSPublishedApplication.AppAlias
- Win32_RDMSPublishedApplication.PoolName
- Win32_RDMSPublishedApplication.DisplayName
- Win32_RDMSPublishedApplication.ShowInPortal
- Win32_RDMSPublishedApplication.SecurityDescriptor
- Win32_RDMSPublishedApplication.AppPath
- Win32_RDMSPublishedApplication.VirtualPath
- Win32_RDMSPublishedApplication.CommandLineSetting
- Win32_RDMSPublishedApplication.RequiredCommandLine
- Win32_RDMSPublishedApplication.Folder
- Win32_RDMSPublishedApplication.IconPath
- Win32_RDMSPublishedApplication.IconIndex
- Win32_RDMSPublishedApplication.IconContents
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb003faf5e51c9da1f46f23c5f8d6b5ae977987c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317426"
---
# <a name="win32_rdmspublishedapplication-class"></a><span data-ttu-id="7bd50-105">\_Classe RDMSPublishedApplication Win32</span><span class="sxs-lookup"><span data-stu-id="7bd50-105">Win32\_RDMSPublishedApplication class</span></span>

<span data-ttu-id="7bd50-106">Gère une application publiée.</span><span class="sxs-lookup"><span data-stu-id="7bd50-106">Manages a published application.</span></span>

<span data-ttu-id="7bd50-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="7bd50-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd50-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bd50-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSPublishedApplication
{
  string  AppAlias;
  string  PoolName;
  string  DisplayName;
  boolean ShowInPortal;
  string  SecurityDescriptor;
  string  AppPath;
  string  VirtualPath;
  uint32  CommandLineSetting;
  string  RequiredCommandLine;
  string  Folder;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
};
```

## <a name="members"></a><span data-ttu-id="7bd50-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7bd50-109">Members</span></span>

<span data-ttu-id="7bd50-110">La classe **Win32 \_ RDMSPublishedApplication** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7bd50-110">The **Win32\_RDMSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="7bd50-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bd50-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bd50-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7bd50-112">Properties</span></span>

<span data-ttu-id="7bd50-113">La classe **Win32 \_ RDMSPublishedApplication** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7bd50-113">The **Win32\_RDMSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bd50-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="7bd50-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-117">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bd50-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-118">Obtient et définit l’alias de l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-118">Gets and sets the alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-119">**AppPath**</span><span class="sxs-lookup"><span data-stu-id="7bd50-119">**AppPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-122">Obtient et définit le chemin d’accès à l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-122">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-123">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="7bd50-123">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-124">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bd50-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-126">Obtient et définit le paramètre de ligne de commande pour l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-126">Gets and sets the command line setting for the application.</span></span>

<span data-ttu-id="7bd50-127">Cette propriété peut prendre les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="7bd50-127">This property can be set to one of the following values:</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="7bd50-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="7bd50-128"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7bd50-129">N’autorisez pas les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7bd50-129">Do not allow command line arguments.</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="7bd50-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Autoriser** (1)</span><span class="sxs-lookup"><span data-stu-id="7bd50-130"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7bd50-131">Autorisez les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7bd50-131">Allow command line arguments.</span></span>

</dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="7bd50-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Exiger** (2)</span><span class="sxs-lookup"><span data-stu-id="7bd50-132"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7bd50-133">Exiger des arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7bd50-133">Require command line arguments.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7bd50-134">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="7bd50-134">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-137">Obtient et définit le nom complet de l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-137">Gets and sets the display name of the application.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-138">**Folder**</span><span class="sxs-lookup"><span data-stu-id="7bd50-138">**Folder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-141">Obtient et définit le chemin d’accès à l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-141">Gets and sets the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-142">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="7bd50-142">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-143">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7bd50-143">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-145">Obtient et définit un tableau qui contient l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-145">Gets and sets an array that contains the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-146">**IndexIcône**</span><span class="sxs-lookup"><span data-stu-id="7bd50-146">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="7bd50-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-149">Obtient et définit l’index de l’icône de l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-149">Gets and sets the index for the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-150">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="7bd50-150">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-153">Obtient et définit le chemin d’accès à l’icône pour cette application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-153">Gets and sets the path to the icon for this application.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-154">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="7bd50-154">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-157">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bd50-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-158">Obtient et définit le nom du pool d’applications de l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-158">Gets and sets the name of the application pool of the application.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-159">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="7bd50-159">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-161">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-161">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-162">Obtient et définit les arguments de ligne de commande requis pour l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-162">Gets and sets the command line arguments that are required for the application</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="7bd50-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-166">Qualificateurs : [ **facultatif**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7bd50-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-167">Obtient et définit le descripteur de sécurité qui contrôle l’accès à l’application, au format SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="7bd50-167">Gets and sets the security descriptor that controls access to the application, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-168">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="7bd50-168">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-169">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7bd50-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-171">Indique s’il faut afficher l’application dans les Accès web Terminal Services (TS Accès web).</span><span class="sxs-lookup"><span data-stu-id="7bd50-171">Indicates whether to display the application in Terminal Services Web Access (TS Web Access).</span></span> <span data-ttu-id="7bd50-172">**True** pour afficher l’application dans les accès Web TS ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="7bd50-172">**TRUE** to display the application in TS Web Access; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="7bd50-173">**VirtualPath**</span><span class="sxs-lookup"><span data-stu-id="7bd50-173">**VirtualPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bd50-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7bd50-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bd50-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7bd50-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7bd50-176">Obtient et définit le chemin d’accès virtuel à l’application.</span><span class="sxs-lookup"><span data-stu-id="7bd50-176">Gets and sets the virtual path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bd50-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bd50-177">Requirements</span></span>



| <span data-ttu-id="7bd50-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bd50-178">Requirement</span></span> | <span data-ttu-id="7bd50-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bd50-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd50-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bd50-180">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd50-181">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bd50-181">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7bd50-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bd50-182">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd50-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7bd50-183">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7bd50-184">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7bd50-184">Namespace</span></span><br/>                | <span data-ttu-id="7bd50-185">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="7bd50-185">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7bd50-186">MOF</span><span class="sxs-lookup"><span data-stu-id="7bd50-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bd50-187"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bd50-187"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bd50-188">DLL</span><span class="sxs-lookup"><span data-stu-id="7bd50-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bd50-189"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd50-189"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7bd50-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bd50-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd50-191">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="7bd50-191">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

