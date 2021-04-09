---
description: La \_ classe de partage Win32 représente une ressource partagée sur un système informatique exécutant Windows. Il peut s’agir d’un lecteur de disque, d’une imprimante, d’une communication entre processus ou d’un autre appareil partageable. Pour plus d’informations sur la récupération des classes WMI, consultez récupération d’une classe.
ms.assetid: 2d47b726-a0fe-47f3-9e96-d1d507655e56
ms.tgt_platform: multiple
title: Classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share
- Win32_Share.Caption
- Win32_Share.Description
- Win32_Share.InstallDate
- Win32_Share.Status
- Win32_Share.AccessMask
- Win32_Share.AllowMaximum
- Win32_Share.MaximumAllowed
- Win32_Share.Name
- Win32_Share.Path
- Win32_Share.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e871880da5aa9819de4a9eaaf3c6f074bd198d23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111203"
---
# <a name="win32_share-class"></a><span data-ttu-id="ab5ce-105">\_Classe de partage Win32</span><span class="sxs-lookup"><span data-stu-id="ab5ce-105">Win32\_Share class</span></span>

<span data-ttu-id="ab5ce-106">La classe de **\_ partage Win32** représente une ressource partagée sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-106">The **Win32\_Share** class represents a shared resource on a computer system running Windows.</span></span> <span data-ttu-id="ab5ce-107">Il peut s’agir d’un lecteur de disque, d’une imprimante, d’une communication entre processus ou d’un autre appareil partageable.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-107">This may be a disk drive, printer, interprocess communication, or other sharable device.</span></span> <span data-ttu-id="ab5ce-108">Pour plus d’informations sur la récupération des classes WMI, consultez [récupération d’une classe](../wmisdk/retrieving-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="ab5ce-108">For more information about retrieving WMI classes, see [Retrieving a Class](../wmisdk/retrieving-a-class.md).</span></span>

<span data-ttu-id="ab5ce-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ab5ce-110">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5ce-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab5ce-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D6-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), AMENDMENT]
class Win32_Share : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="ab5ce-112">Membres</span><span class="sxs-lookup"><span data-stu-id="ab5ce-112">Members</span></span>

<span data-ttu-id="ab5ce-113">La classe de **\_ partage Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ab5ce-113">The **Win32\_Share** class has these types of members:</span></span>

-   [<span data-ttu-id="ab5ce-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ab5ce-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ab5ce-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab5ce-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ab5ce-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ab5ce-116">Methods</span></span>

<span data-ttu-id="ab5ce-117">La classe de **\_ partage Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-117">The **Win32\_Share** class has these methods.</span></span>



| <span data-ttu-id="ab5ce-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="ab5ce-118">Method</span></span>                                                             | <span data-ttu-id="ab5ce-119">Description</span><span class="sxs-lookup"><span data-stu-id="ab5ce-119">Description</span></span>                                                                                                                                                                                                         |
|:-------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab5ce-120">**Créés**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-120">**Create**</span></span>](create-method-in-class-win32-share.md)               | <span data-ttu-id="ab5ce-121">Méthode de classe qui initie le partage pour une ressource de serveur.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-121">Class method that initiates sharing for a server resource.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="ab5ce-122">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-122">**Delete**</span></span>](delete-method-in-class-win32-share.md)               | <span data-ttu-id="ab5ce-123">Méthode de classe qui supprime un nom de partage de la liste des ressources partagées d’un serveur, en déconnectant les connexions à la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-123">Class method that deletes a share name from a server's list of shared resources, disconnecting connections to the shared resource.</span></span><br/>                                                                       |
| [<span data-ttu-id="ab5ce-124">**GetAccessMask**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-124">**GetAccessMask**</span></span>](getaccessmask-method-in-class-win32-share.md) | <span data-ttu-id="ab5ce-125">Retourne les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-125">Returns the access rights to the share held by the user or group on whose behalf the instance is returned.</span></span> <span data-ttu-id="ab5ce-126">Vous devez utiliser cette méthode à la place de la propriété **AccessMask** , qui est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-126">You should use this method in place of the **AccessMask** property, which is always **NULL**.</span></span><br/> |
| [<span data-ttu-id="ab5ce-127">**SetShareInfo**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-127">**SetShareInfo**</span></span>](setshareinfo-method-in-class-win32-share.md)   | <span data-ttu-id="ab5ce-128">Méthode de classe qui définit les paramètres d’une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-128">Class method that sets the parameters of a shared resource.</span></span><br/>                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="ab5ce-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab5ce-129">Properties</span></span>

<span data-ttu-id="ab5ce-130">La classe de **\_ partage Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-130">The **Win32\_Share** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab5ce-131">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-131">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-134">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-134">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-135">Cette propriété est obsolète et n’est plus utilisée.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-135">This property is obsolete and is no longer used.</span></span> <span data-ttu-id="ab5ce-136">Utilisez la méthode [**Win32 \_ share. GetAccessMask**](getaccessmask-method-in-class-win32-share.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-136">Use the [**Win32\_Share.GetAccessMask**](getaccessmask-method-in-class-win32-share.md) method instead.</span></span> <span data-ttu-id="ab5ce-137">La valeur de la propriété **AccessMask** est définie sur **null** par WMI.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-137">The value of the **AccessMask** property is set to **null** by WMI.</span></span> <span data-ttu-id="ab5ce-138">Pour plus d’informations sur la définition de l’accès lors de la création d’un partage, consultez la méthode [**Create**](create-method-in-class-win32-share.md) .</span><span class="sxs-lookup"><span data-stu-id="ab5ce-138">For more information about setting access when a share is created, see the [**Create**](create-method-in-class-win32-share.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-139">**AllowMaximum**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-139">**AllowMaximum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-142">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-143">Le nombre d’utilisateurs simultanés pour cette ressource a été limité.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-143">Number of concurrent users for this resource has been limited.</span></span> <span data-ttu-id="ab5ce-144">Si la valeur est **true**, la valeur de la propriété **MaximumAllowed** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-144">If **True**, the value in the **MaximumAllowed** property is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-148">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-149">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-149">A short textual description of the object.</span></span>

<span data-ttu-id="ab5ce-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab5ce-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-151">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-154">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-154">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-155">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-155">A textual description of the object.</span></span>

<span data-ttu-id="ab5ce-156">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab5ce-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-158">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-160">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-160">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-161">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-161">Indicates when the object was installed.</span></span> <span data-ttu-id="ab5ce-162">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-162">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ab5ce-163">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab5ce-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-164">**MaximumAllowed**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-164">**MaximumAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-167">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ Max \_ uses")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-167">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_max\_uses")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-168">Limite du nombre maximal d’utilisateurs autorisés à utiliser cette ressource simultanément.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-168">Limit on the maximum number of users allowed to use this resource concurrently.</span></span> <span data-ttu-id="ab5ce-169">La valeur est valide uniquement si la propriété **AllowMaximum** est définie sur **false**.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-169">The value is only valid if the **AllowMaximum** property is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-170">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-170">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-173">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**remplacement**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api partagent les \| [**\_ informations \_ 1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1) \| shi1 \_ NetName")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-173">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_1**](/windows/win32/api/lmshare/ns-lmshare-share_info_1)\|shi1\_netname")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-174">Alias donné à un chemin d’accès configuré en tant que partage sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-174">Alias given to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="ab5ce-175">Windows 2008 exemple : « \\ SERVEUR01 \\ public »-windows Server 2008 nécessite que vous détrouviez l’UNC dans le nom.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-175">Windows 2008 example: "\\SERVER01\\public" - Windows Server 2008 requires that you place the UNC in the name.</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-176">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-176">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-179">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ path")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-179">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_path")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-180">Chemin d’accès local du partage Windows.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-180">Local path of the Windows share.</span></span>

<span data-ttu-id="ab5ce-181">Exemple : « C : \\ Program Files »</span><span class="sxs-lookup"><span data-stu-id="ab5ce-181">Example: "C:\\Program Files"</span></span>

</dd> <dt>

<span data-ttu-id="ab5ce-182">**État**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-182">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-185">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-185">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-186">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-186">String that indicates the current status of the object.</span></span> <span data-ttu-id="ab5ce-187">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-187">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="ab5ce-188">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="ab5ce-188">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="ab5ce-189">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="ab5ce-189">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="ab5ce-190">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="ab5ce-190">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ab5ce-191">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-191">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ab5ce-192">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-192">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ab5ce-193">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab5ce-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="ab5ce-194">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab5ce-194">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="ab5ce-195">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-195">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="ab5ce-196">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-196">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="ab5ce-197">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-197">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ab5ce-198">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-198">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="ab5ce-199">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-199">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="ab5ce-200">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-200">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="ab5ce-201">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-201">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="ab5ce-202">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-202">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="ab5ce-203">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-203">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="ab5ce-204">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-204">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="ab5ce-205">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-205">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="ab5ce-206">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-206">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ab5ce-207">**Type**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-207">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab5ce-208">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ab5ce-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab5ce-210">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("les \| structures de gestion de réseau win32api \| [**partagent les \_ informations \_ 502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502) \| shi502 \_ type")</span><span class="sxs-lookup"><span data-stu-id="ab5ce-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Network Management Structures\|[**SHARE\_INFO\_502**](/windows/win32/api/lmshare/ns-lmshare-share_info_502)\|shi502\_type")</span></span>
</dt> </dl>

<span data-ttu-id="ab5ce-211">Type de ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-211">Type of resource being shared.</span></span> <span data-ttu-id="ab5ce-212">Les types sont les suivants : lecteurs de disque, files d’attente à l’impression, communications interprocessus (IPC) et périphériques généraux.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-212">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="ab5ce-213">**Lecteur de disque** (0)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-213">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="ab5ce-214">**File d’attente** à l’impression (1)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-214">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="ab5ce-215">**Appareil** (2)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-215">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="ab5ce-216">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-216">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="ab5ce-217">**Administrateur de lecteur de disque** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-217">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="ab5ce-218">**Administrateur de file d’attente** à l’impression (2147483649)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-218">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="ab5ce-219">**Administrateur d’appareil** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-219">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="ab5ce-220">**Administrateur IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="ab5ce-220">**IPC Admin** (2147483651)</span></span>


<span data-ttu-id="ab5ce-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ab5ce-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="ab5ce-222">Notes</span><span class="sxs-lookup"><span data-stu-id="ab5ce-222">Remarks</span></span>

<span data-ttu-id="ab5ce-223">La classe de **\_ partage Win32** est dérivée de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="ab5ce-223">The **Win32\_Share** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="ab5ce-224">La méthode Create de cette classe est une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-224">The Create method in this class is a static method.</span></span> <span data-ttu-id="ab5ce-225">Les méthodes **Delete**, **GetAccessMask** et **SetShareInfo** sont toutes des méthodes d’instance.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-225">The **Delete**, **GetAccessMask** and **SetShareInfo** methods are all instance methods.</span></span>

<span data-ttu-id="ab5ce-226">Selon vos autorisations de sécurité, vous risquez de ne pas pouvoir récupérer toutes les propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-226">Depending on your security permissions, you may not be able to retrieve all of the properties of this class.</span></span> <span data-ttu-id="ab5ce-227">Par exemple, les propriétés **AllowMaximum**, **MaximumAllowed**, **path** et **type** peuvent retourner la valeur null.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-227">For example, **AllowMaximum**, **MaximumAllowed**, **Path**, and **Type** properties may return null.</span></span> <span data-ttu-id="ab5ce-228">En règle générale, les utilisateurs avec pouvoir et les administrateurs peuvent récupérer toutes les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-228">Generally speaking, Power Users and Administrators will be able to retrieve all property values.</span></span>

## <a name="examples"></a><span data-ttu-id="ab5ce-229">Exemples</span><span class="sxs-lookup"><span data-stu-id="ab5ce-229">Examples</span></span>

<span data-ttu-id="ab5ce-230">L'[exemple de code](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) du centre de scripts suivant répertorie tous les partages sur un ordinateur et répertorie toutes les autorisations de partage pour chaque partage.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-230">The following Script Center[code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/List-Share-Permissions-83f8c419) lists all shares on a computer, and list all the share permissions for each share.</span></span>

<span data-ttu-id="ab5ce-231">Les [informations de partage obtenir des informations similaires à celles de Win32 \_ share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell Sample interrogent \_ le partage Win32 et fournissent les résultats.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-231">The [Get Share Information similar to Win32\_Share](https://Gallery.TechNet.Microsoft.Com/Get-Share-Information-5cc71b2c) PowerShell sample queries Win32\_Share and provides the results.</span></span>

<span data-ttu-id="ab5ce-232">L’exemple PowerShell suivant affiche les partages sur le système local.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-232">The following PowerShell sample displays the shares on the local system.</span></span>


```PowerShell
$shares = Get-WMIObject -class Win32_share
"Shares on : {0}" -f $((gwmi win32_computersystem).name)
$shares | sort name | ft -auto
```



<span data-ttu-id="ab5ce-233">Sinon, si vous souhaitez filtrer plus précisément, vous pouvez utiliser l’extrait de code PowerShell suivant :</span><span class="sxs-lookup"><span data-stu-id="ab5ce-233">Alternately, if you wish to filter more precisely, you can use the following PowerShell snippet:</span></span>


```PowerShell
gwmi -q "SELECT * FROM Win32_Share WHERE Name != 'ADMIN$' AND Name != 'IPC$'"
```



<span data-ttu-id="ab5ce-234">L’exemple VBScript suivant affiche les partages sur le système local.</span><span class="sxs-lookup"><span data-stu-id="ab5ce-234">The Following VBScript sample displays the shares on the local system.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_Share")


For Each objItem in colItems 
 Wscript.Echo "Name: " & objItem.Name
 Wscript.Echo "Caption: " & objItem.Caption & "=" & objItem.Path
Next
```



## <a name="requirements"></a><span data-ttu-id="ab5ce-235">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab5ce-235">Requirements</span></span>



| <span data-ttu-id="ab5ce-236">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab5ce-236">Requirement</span></span> | <span data-ttu-id="ab5ce-237">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab5ce-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5ce-238">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab5ce-238">Minimum supported client</span></span><br/> | <span data-ttu-id="ab5ce-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab5ce-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab5ce-240">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab5ce-240">Minimum supported server</span></span><br/> | <span data-ttu-id="ab5ce-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab5ce-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab5ce-242">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ab5ce-242">Namespace</span></span><br/>                | <span data-ttu-id="ab5ce-243">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ab5ce-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab5ce-244">MOF</span><span class="sxs-lookup"><span data-stu-id="ab5ce-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab5ce-245"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab5ce-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab5ce-246">DLL</span><span class="sxs-lookup"><span data-stu-id="ab5ce-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab5ce-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab5ce-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab5ce-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab5ce-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5ce-249">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ab5ce-249">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="ab5ce-250">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ab5ce-250">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="ab5ce-251">Tâches WMI : fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="ab5ce-251">WMI Tasks: Files and Folders</span></span>](../wmisdk/wmi-tasks--files-and-folders.md)
</dt> </dl>

 

 
