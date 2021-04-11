---
description: La \_ classe ClusterShare Win32 représente une ressource partagée sur un cluster.
ms.assetid: 6c8b40e3-431f-4728-a389-affbc04b8415
ms.tgt_platform: multiple
title: Classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare
- Win32_ClusterShare.Caption
- Win32_ClusterShare.Description
- Win32_ClusterShare.InstallDate
- Win32_ClusterShare.Status
- Win32_ClusterShare.AccessMask
- Win32_ClusterShare.AllowMaximum
- Win32_ClusterShare.MaximumAllowed
- Win32_ClusterShare.Name
- Win32_ClusterShare.Path
- Win32_ClusterShare.Type
- Win32_ClusterShare.ServerName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccff6ad8d99692d066728c99dd74ab07640af4fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111238"
---
# <a name="win32_clustershare-class"></a><span data-ttu-id="2cd16-103">\_Classe ClusterShare Win32</span><span class="sxs-lookup"><span data-stu-id="2cd16-103">Win32\_ClusterShare class</span></span>

<span data-ttu-id="2cd16-104">\[La classe **Win32 \_ ClusterShare** est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="2cd16-104">\[The **Win32\_ClusterShare** class is deprecated.</span></span> <span data-ttu-id="2cd16-105">Utilisez les classes de [**\_ SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) de [**\_ partage msft**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) et msft à la place.\]</span><span class="sxs-lookup"><span data-stu-id="2cd16-105">Please use the [**MSFT\_FileShare**](/previous-versions/windows/desktop/stormgmt/msft-fileshare) and [**MSFT\_SMFileShare**](/previous-versions/windows/desktop/msftstrgmanprov/msft-smfileshare) classes instead.\]</span></span>

<span data-ttu-id="2cd16-106">La \_ classe ClusterShare Win32 représente une ressource partagée sur un cluster.</span><span class="sxs-lookup"><span data-stu-id="2cd16-106">The Win32\_ClusterShare class represents a shared resource on a cluster.</span></span>

<span data-ttu-id="2cd16-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="2cd16-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd16-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2cd16-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_ClusterShare : Win32_Share
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   AccessMask;
  boolean  AllowMaximum;
  uint32   MaximumAllowed;
  string   Name;
  string   Path;
  uint32   Type;
  string   ServerName;
};
```

## <a name="members"></a><span data-ttu-id="2cd16-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2cd16-109">Members</span></span>

<span data-ttu-id="2cd16-110">La classe **Win32 \_ ClusterShare** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2cd16-110">The **Win32\_ClusterShare** class has these types of members:</span></span>

-   [<span data-ttu-id="2cd16-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2cd16-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="2cd16-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2cd16-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2cd16-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2cd16-113">Methods</span></span>

<span data-ttu-id="2cd16-114">La classe **Win32 \_ ClusterShare** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2cd16-114">The **Win32\_ClusterShare** class has these methods.</span></span>



| <span data-ttu-id="2cd16-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="2cd16-115">Method</span></span>                                                    | <span data-ttu-id="2cd16-116">Description</span><span class="sxs-lookup"><span data-stu-id="2cd16-116">Description</span></span>                                                      |
|:----------------------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="2cd16-117">**Créés**</span><span class="sxs-lookup"><span data-stu-id="2cd16-117">**Create**</span></span>](create-win32-clustershare.md)               | <span data-ttu-id="2cd16-118">Crée une instance **de \_ ClusterShare Win32** .</span><span class="sxs-lookup"><span data-stu-id="2cd16-118">Creates a new **Win32\_ClusterShare** instance.</span></span><br/>       |
| [<span data-ttu-id="2cd16-119">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="2cd16-119">**Delete**</span></span>](delete-win32-clustershare.md)               | <span data-ttu-id="2cd16-120">Supprime une instance **de \_ ClusterShare Win32** .</span><span class="sxs-lookup"><span data-stu-id="2cd16-120">Deletes a **Win32\_ClusterShare** instance.</span></span><br/>           |
| [<span data-ttu-id="2cd16-121">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="2cd16-121">**GetAccessMask**</span></span>](getaccessmask-win32-clustershare.md) | <span data-ttu-id="2cd16-122">Retourne une bitmap avec les droits d’accès au partage.</span><span class="sxs-lookup"><span data-stu-id="2cd16-122">Returns a bitmap with the access rights to the share.</span></span><br/> |
| [<span data-ttu-id="2cd16-123">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="2cd16-123">**SetShareInfo**</span></span>](setshareinfo-win32-clustershare.md)   | <span data-ttu-id="2cd16-124">Définit les paramètres de la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="2cd16-124">Sets the parameters of the shared resource.</span></span><br/>           |



 

### <a name="properties"></a><span data-ttu-id="2cd16-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2cd16-125">Properties</span></span>

<span data-ttu-id="2cd16-126">La classe **Win32 \_ ClusterShare** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2cd16-126">The **Win32\_ClusterShare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cd16-127">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="2cd16-127">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cd16-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-130">Qualificateurs : [ **déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2cd16-130">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-131">Cette propriété est obsolète et n’est plus utilisée.</span><span class="sxs-lookup"><span data-stu-id="2cd16-131">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="2cd16-132">Utilisez la méthode [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="2cd16-132">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="2cd16-133">La valeur de la propriété **AccessMask** est définie sur **null** par WMI.</span><span class="sxs-lookup"><span data-stu-id="2cd16-133">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="2cd16-134">Pour plus d’informations sur la définition de l’accès lors de la création d’un partage, consultez la méthode [**Create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd16-134">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

<span data-ttu-id="2cd16-135">Cette propriété est héritée [**du \_ partage Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-135">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-136">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="2cd16-136">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2cd16-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="2cd16-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-140">Le nombre d’utilisateurs simultanés pour cette ressource a été limité.</span><span class="sxs-lookup"><span data-stu-id="2cd16-140">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="2cd16-141">Si la valeur est **true**, la valeur de la propriété **MaximumAllowed** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="2cd16-141">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

<span data-ttu-id="2cd16-142">Cette propriété est héritée [**du \_ partage Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-142">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-143">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2cd16-143">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2cd16-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-146">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-147">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2cd16-147">A short textual description of the object.</span></span>

<span data-ttu-id="2cd16-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-149">**Description**</span><span class="sxs-lookup"><span data-stu-id="2cd16-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2cd16-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-152">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="2cd16-152">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-153">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2cd16-153">A textual description of the object.</span></span>

<span data-ttu-id="2cd16-154">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-155">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2cd16-155">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-156">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2cd16-156">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-158">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="2cd16-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-159">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="2cd16-159">Indicates when the object was installed.</span></span> <span data-ttu-id="2cd16-160">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="2cd16-160">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2cd16-161">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-162">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="2cd16-162">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-163">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cd16-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-164">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-165">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="2cd16-165">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-166">Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément.</span><span class="sxs-lookup"><span data-stu-id="2cd16-166">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="2cd16-167">La valeur est valide uniquement si la propriété **AllowMaximum** est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="2cd16-167">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

<span data-ttu-id="2cd16-168">Cette propriété est héritée [**du \_ partage Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-168">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-169">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2cd16-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-170">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2cd16-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-172">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Network Management structures \| [**share \_ information \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="2cd16-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/desktop/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-173">Alias donné à un chemin d’accès configuré en tant que partage sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd16-173">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="2cd16-174">Windows 2008 exemple : « \\ SERVEUR01 \\ public »-windows Server 2008 nécessite que vous détrouviez l’UNC dans le nom.</span><span class="sxs-lookup"><span data-stu-id="2cd16-174">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

<span data-ttu-id="2cd16-175">Cette propriété est héritée [**du \_ partage Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-175">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-176">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="2cd16-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2cd16-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-179">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="2cd16-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-180">Chemin d’accès local du partage Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd16-180">Local path of the Windows share.</span></span>

<span data-ttu-id="2cd16-181">Exemple : « C : \\ Program Files »</span><span class="sxs-lookup"><span data-stu-id="2cd16-181">Example: "C:\\Program Files"</span></span>

<span data-ttu-id="2cd16-182">Cette propriété est héritée [**du \_ partage Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-182">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-183">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="2cd16-183">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2cd16-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-186">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("servername"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("structures de \| gestion de réseau win32api \| [**share \_ info \_ 503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503) \| shi503 \_ ServerName")</span><span class="sxs-lookup"><span data-stu-id="2cd16-186">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ServerName"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_503**](/windows/desktop/api/lmshare/ns-lmshare-share_info_503)\|shi503\_servername")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-187">Serveur de cluster sur lequel le partage est hébergé.</span><span class="sxs-lookup"><span data-stu-id="2cd16-187">The cluster server on which the share is hosted.</span></span>

</dd> <dt>

<span data-ttu-id="2cd16-188">**État**</span><span class="sxs-lookup"><span data-stu-id="2cd16-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2cd16-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-191">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="2cd16-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-192">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="2cd16-192">String that indicates the current status of the object.</span></span> <span data-ttu-id="2cd16-193">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="2cd16-193">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2cd16-194">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="2cd16-194">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2cd16-195">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="2cd16-195">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2cd16-196">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="2cd16-196">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2cd16-197">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="2cd16-197">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2cd16-198">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="2cd16-198">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2cd16-199">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2cd16-200">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cd16-200">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2cd16-201">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-201">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2cd16-202">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-202">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2cd16-203">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-203">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2cd16-204">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="2cd16-204">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2cd16-205">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-205">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2cd16-206">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-206">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2cd16-207">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-207">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2cd16-208">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-208">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2cd16-209">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-209">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2cd16-210">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-210">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2cd16-211">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-211">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2cd16-212">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="2cd16-212">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2cd16-213">**Type**</span><span class="sxs-lookup"><span data-stu-id="2cd16-213">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cd16-214">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2cd16-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2cd16-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cd16-216">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")</span><span class="sxs-lookup"><span data-stu-id="2cd16-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/desktop/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="2cd16-217">Type de ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="2cd16-217">Type of resource being shared.</span></span> <span data-ttu-id="2cd16-218">Les types sont les suivants : lecteurs de disque, files d’attente à l’impression, communications interprocessus (IPC) et périphériques généraux.</span><span class="sxs-lookup"><span data-stu-id="2cd16-218">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<span data-ttu-id="2cd16-219">Cette propriété est héritée [**du \_ partage Win32**](win32-share.md).</span><span class="sxs-lookup"><span data-stu-id="2cd16-219">This property is inherited from [**Win32\_Share**](win32-share.md).</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="2cd16-220">**Lecteur de disque** (0)</span><span class="sxs-lookup"><span data-stu-id="2cd16-220">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="2cd16-221">**File d’attente** à l’impression (1)</span><span class="sxs-lookup"><span data-stu-id="2cd16-221">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="2cd16-222">**Appareil** (2)</span><span class="sxs-lookup"><span data-stu-id="2cd16-222">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="2cd16-223">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="2cd16-223">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="2cd16-224">**Administrateur de lecteur de disque** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="2cd16-224">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="2cd16-225">**Administrateur de file d’attente** à l’impression (2147483649)</span><span class="sxs-lookup"><span data-stu-id="2cd16-225">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="2cd16-226">**Administrateur d’appareil** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="2cd16-226">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="2cd16-227">**Administrateur IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="2cd16-227">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="2cd16-228"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2cd16-228"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2cd16-229">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2cd16-229">Requirements</span></span>



| <span data-ttu-id="2cd16-230">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2cd16-230">Requirement</span></span> | <span data-ttu-id="2cd16-231">Valeur</span><span class="sxs-lookup"><span data-stu-id="2cd16-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd16-232">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cd16-232">Minimum supported client</span></span><br/> | <span data-ttu-id="2cd16-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2cd16-233">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="2cd16-234">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cd16-234">Minimum supported server</span></span><br/> | <span data-ttu-id="2cd16-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2cd16-235">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2cd16-236">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2cd16-236">Namespace</span></span><br/>                | <span data-ttu-id="2cd16-237">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="2cd16-237">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2cd16-238">MOF</span><span class="sxs-lookup"><span data-stu-id="2cd16-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cd16-239"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cd16-239"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cd16-240">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd16-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cd16-241"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd16-241"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd16-242">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2cd16-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd16-243">**\_Partage Win32**</span><span class="sxs-lookup"><span data-stu-id="2cd16-243">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

