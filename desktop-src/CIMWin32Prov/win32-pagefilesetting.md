---
description: Le \_ PageFileSetting Win32&\# 8194 ; La classe WMI représente les paramètres d’un fichier d’échange.
ms.assetid: 22190ede-1db6-4d69-ae74-63d10977cc78
ms.tgt_platform: multiple
title: Classe Win32_PageFileSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileSetting
- Win32_PageFileSetting.Caption
- Win32_PageFileSetting.Description
- Win32_PageFileSetting.SettingID
- Win32_PageFileSetting.InitialSize
- Win32_PageFileSetting.MaximumSize
- Win32_PageFileSetting.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3ec2fa36e31cf9075f218f31d3063e3a298b8ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515794"
---
# <a name="win32_pagefilesetting-class"></a><span data-ttu-id="f7000-103">\_Classe PageFileSetting Win32</span><span class="sxs-lookup"><span data-stu-id="f7000-103">Win32\_PageFileSetting class</span></span>

<span data-ttu-id="f7000-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ PageFileSetting** représente les paramètres d’un fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="f7000-104">The **Win32\_PageFileSetting** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings of a page file.</span></span> <span data-ttu-id="f7000-105">Les informations contenues dans les objets instanciés à partir de cette classe spécifient les paramètres du fichier d’échange utilisés lors de la création du fichier au démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="f7000-105">Information contained within objects instantiated from this class specify the page file parameters used when the file is created at system startup.</span></span> <span data-ttu-id="f7000-106">Les propriétés de cette classe peuvent être modifiées et différées jusqu’au démarrage.</span><span class="sxs-lookup"><span data-stu-id="f7000-106">The properties in this class can be modified and deferred until startup.</span></span> <span data-ttu-id="f7000-107">Ces paramètres sont différents de l’état d’exécution d’un fichier d’échange exprimé via la classe associée [**Win32 \_ PageFileUsage**](win32-pagefileusage.md).</span><span class="sxs-lookup"><span data-stu-id="f7000-107">These settings are different from the run-time state of a page file expressed through the associated class [**Win32\_PageFileUsage**](win32-pagefileusage.md).</span></span>

<span data-ttu-id="f7000-108">Pour créer une instance de cette classe, activez le privilège **SeCreatePagefilePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="f7000-108">To create an instance of this class, enable the **SeCreatePagefilePrivilege** privilege.</span></span> <span data-ttu-id="f7000-109">Pour plus d’informations, consultez [**constantes de privilège**](../wmisdk/privilege-constants.md) et [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f7000-109">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span>

<span data-ttu-id="f7000-110">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f7000-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f7000-111">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="f7000-111">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7000-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7000-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeCreatePagefilePrivilege"), UUID("{514A9270-C856-11D2-B364-00105A1f77A1}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_PageFileSetting : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 InitialSize;
  uint32 MaximumSize;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="f7000-113">Membres</span><span class="sxs-lookup"><span data-stu-id="f7000-113">Members</span></span>

<span data-ttu-id="f7000-114">La classe **Win32 \_ PageFileSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f7000-114">The **Win32\_PageFileSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f7000-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7000-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7000-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7000-116">Properties</span></span>

<span data-ttu-id="f7000-117">La classe **Win32 \_ PageFileSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f7000-117">The **Win32\_PageFileSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7000-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f7000-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7000-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7000-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7000-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7000-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7000-121">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="f7000-121">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f7000-122">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="f7000-122">Short textual description of the current object.</span></span>

<span data-ttu-id="f7000-123">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f7000-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7000-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="f7000-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7000-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7000-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7000-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7000-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f7000-127">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="f7000-127">Textual description of the current object.</span></span>

<span data-ttu-id="f7000-128">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f7000-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7000-129">**InitialSize**</span><span class="sxs-lookup"><span data-stu-id="f7000-129">**InitialSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7000-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7000-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7000-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f7000-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f7000-132">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ \| PagingFiles »), [**Units**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)</span><span class="sxs-lookup"><span data-stu-id="f7000-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7000-133">Taille initiale du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="f7000-133">Initial size of the page file.</span></span>

<span data-ttu-id="f7000-134">Exemple : 139</span><span class="sxs-lookup"><span data-stu-id="f7000-134">Example: 139</span></span>

</dd> <dt>

<span data-ttu-id="f7000-135">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="f7000-135">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7000-136">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7000-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f7000-137">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f7000-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f7000-138">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ \| PagingFiles »), [**Units**](../wmisdk/standard-qualifiers.md) (« mégaoctets »)</span><span class="sxs-lookup"><span data-stu-id="f7000-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Memory Management\|PagingFiles"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="f7000-139">Taille maximale du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="f7000-139">Maximum size of the page file.</span></span>

<span data-ttu-id="f7000-140">Exemple : 178</span><span class="sxs-lookup"><span data-stu-id="f7000-140">Example: 178</span></span>

</dd> <dt>

<span data-ttu-id="f7000-141">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f7000-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7000-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7000-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7000-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f7000-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f7000-144">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="f7000-144">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="f7000-145">Chemin d’accès et nom de fichier du fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="f7000-145">Path and file name of the page file.</span></span>

<span data-ttu-id="f7000-146">Exemple : « C : \\PAGEFILE.SYS »</span><span class="sxs-lookup"><span data-stu-id="f7000-146">Example: "C:\\PAGEFILE.SYS"</span></span>

</dd> <dt>

<span data-ttu-id="f7000-147">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="f7000-147">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7000-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7000-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7000-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7000-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7000-150">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="f7000-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7000-151">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="f7000-151">Identifier by which the current object is known.</span></span>

<span data-ttu-id="f7000-152">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f7000-152">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7000-153">Notes</span><span class="sxs-lookup"><span data-stu-id="f7000-153">Remarks</span></span>

<span data-ttu-id="f7000-154">La classe **Win32 \_ PageFileSetting** est dérivée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="f7000-154">The **Win32\_PageFileSetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7000-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7000-155">Requirements</span></span>



| <span data-ttu-id="f7000-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7000-156">Requirement</span></span> | <span data-ttu-id="f7000-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7000-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7000-158">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7000-158">Minimum supported client</span></span><br/> | <span data-ttu-id="f7000-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7000-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7000-160">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7000-160">Minimum supported server</span></span><br/> | <span data-ttu-id="f7000-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7000-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7000-162">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7000-162">Namespace</span></span><br/>                | <span data-ttu-id="f7000-163">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f7000-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7000-164">MOF</span><span class="sxs-lookup"><span data-stu-id="f7000-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7000-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7000-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7000-166">DLL</span><span class="sxs-lookup"><span data-stu-id="f7000-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7000-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7000-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7000-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7000-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7000-169">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="f7000-169">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="f7000-170">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f7000-170">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
