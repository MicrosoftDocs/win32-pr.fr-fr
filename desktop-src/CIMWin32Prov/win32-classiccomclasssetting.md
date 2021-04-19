---
description: Représente les paramètres d’un composant COM (Component Object Model).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515790"
---
# <a name="win32_classiccomclasssetting-class"></a><span data-ttu-id="90593-103">\_Classe ClassicCOMClassSetting Win32</span><span class="sxs-lookup"><span data-stu-id="90593-103">Win32\_ClassicCOMClassSetting class</span></span>

<span data-ttu-id="90593-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ClassicCOMClassSetting** représente les paramètres d’un composant COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="90593-104">The **Win32\_ClassicCOMClassSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a Component Object Model (COM) component.</span></span>

<span data-ttu-id="90593-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="90593-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="90593-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="90593-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90593-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90593-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a><span data-ttu-id="90593-108">Membres</span><span class="sxs-lookup"><span data-stu-id="90593-108">Members</span></span>

<span data-ttu-id="90593-109">La classe **Win32 \_ ClassicCOMClassSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="90593-109">The **Win32\_ClassicCOMClassSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="90593-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90593-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90593-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="90593-111">Properties</span></span>

<span data-ttu-id="90593-112">La classe **Win32 \_ ClassicCOMClassSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="90593-112">The **Win32\_ClassicCOMClassSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90593-113">**AppID**</span><span class="sxs-lookup"><span data-stu-id="90593-113">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-116">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[AppID\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-117">Identificateur global unique (GUID) de l’application COM utilisant ce composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-117">Globally unique identifier (GUID) for the COM application using this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="90593-118">**AutoConvertToClsid**</span><span class="sxs-lookup"><span data-stu-id="90593-118">**AutoConvertToClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-121">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AutoConvertTo \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoConvertTo\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-122">GUID de la classe COM vers laquelle ce composant COM sera automatiquement converti.</span><span class="sxs-lookup"><span data-stu-id="90593-122">GUID of the COM class to which this COM component will automatically be converted.</span></span>

</dd> <dt>

<span data-ttu-id="90593-123">**AutoTreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="90593-123">**AutoTreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-126">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ autotraitéas \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-126">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AutoTreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-127">GUID du composant COM qui émulera automatiquement les instances de cette classe.</span><span class="sxs-lookup"><span data-stu-id="90593-127">GUID for the COM component that will automatically emulate instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="90593-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="90593-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-131">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="90593-131">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="90593-132">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="90593-132">Short textual description of the current object.</span></span>

<span data-ttu-id="90593-133">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="90593-133">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="90593-134">**ComponentId**</span><span class="sxs-lookup"><span data-stu-id="90593-134">**ComponentId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-137">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machines \\ \\ \\ \\ \\ \\ CLSID \\ \\ {GUID} \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-138">GUID de ce composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-138">GUID of this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="90593-139">**Contrôle**</span><span class="sxs-lookup"><span data-stu-id="90593-139">**Control**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-140">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="90593-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90593-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-142">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classe \\ \\ CLSID \\ \\ {GUID} \\ \\ Control")</span><span class="sxs-lookup"><span data-stu-id="90593-142">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Control")</span></span>
</dt> </dl>

<span data-ttu-id="90593-143">Le composant COM est un contrôle OLE.</span><span class="sxs-lookup"><span data-stu-id="90593-143">COM component is an OLE control.</span></span>

</dd> <dt>

<span data-ttu-id="90593-144">**DefaultIcon**</span><span class="sxs-lookup"><span data-stu-id="90593-144">**DefaultIcon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-147">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\DefaultIcon\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-148">Chemin d’accès au fichier exécutable et à l’identificateur de ressource de l’icône par défaut utilisée par la classe.</span><span class="sxs-lookup"><span data-stu-id="90593-148">Path to the executable file and resource identifier of the default icon used by the class.</span></span>

</dd> <dt>

<span data-ttu-id="90593-149">**Description**</span><span class="sxs-lookup"><span data-stu-id="90593-149">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90593-152">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="90593-152">Textual description of the current object.</span></span>

<span data-ttu-id="90593-153">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="90593-153">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="90593-154">**InprocHandler**</span><span class="sxs-lookup"><span data-stu-id="90593-154">**InprocHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-157">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-158">Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’un gestionnaire personnalisé 16 bits pour le composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-158">Full path including filename or only filename to a 16-bit custom handler for the COM component.</span></span> <span data-ttu-id="90593-159">Le fournisseur ne retourne pas toujours le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="90593-159">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="90593-160">**InprocHandler32**</span><span class="sxs-lookup"><span data-stu-id="90593-160">**InprocHandler32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-163">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocHandler32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-164">Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’un gestionnaire personnalisé 32 bits pour le composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-164">Full path including filename or only filename to a 32-bit custom handler for the COM component.</span></span> <span data-ttu-id="90593-165">Le fournisseur ne retourne pas toujours le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="90593-165">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="90593-166">**InprocServer**</span><span class="sxs-lookup"><span data-stu-id="90593-166">**InprocServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-169">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-170">Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’une DLL de serveur in-process 16 bits pour ce composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-170">Full path including filename or only filename to a 16-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="90593-171">Le fournisseur ne retourne pas toujours le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="90593-171">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="90593-172">**InprocServer32**</span><span class="sxs-lookup"><span data-stu-id="90593-172">**InprocServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-175">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-176">Chemin complet incluant le nom de fichier ou uniquement le nom de fichier d’une DLL de serveur in-process 32 bits pour ce composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-176">Full path including filename or only filename to a 32-bit in-process server DLL for this COM component.</span></span> <span data-ttu-id="90593-177">Le fournisseur ne retourne pas toujours le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="90593-177">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="90593-178">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="90593-178">**Insertable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-179">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="90593-179">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90593-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-181">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")</span><span class="sxs-lookup"><span data-stu-id="90593-181">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Insertable")</span></span>
</dt> </dl>

<span data-ttu-id="90593-182">Le composant COM peut être inséré dans des applications de conteneur OLE.</span><span class="sxs-lookup"><span data-stu-id="90593-182">COM component can be inserted into OLE container applications.</span></span>

</dd> <dt>

<span data-ttu-id="90593-183">**JavaClass**</span><span class="sxs-lookup"><span data-stu-id="90593-183">**JavaClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="90593-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="90593-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-186">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] »)</span><span class="sxs-lookup"><span data-stu-id="90593-186">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[JavaClass\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-187">Le composant COM est un composant Java.</span><span class="sxs-lookup"><span data-stu-id="90593-187">COM component is a Java component.</span></span>

</dd> <dt>

<span data-ttu-id="90593-188">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="90593-188">**LocalServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-191">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-191">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-192">Chemin d’accès complet incluant le nom de fichier ou uniquement le nom de fichier d’une application serveur locale 16 bits.</span><span class="sxs-lookup"><span data-stu-id="90593-192">Full path including filename or only filename to a 16-bit local server application.</span></span> <span data-ttu-id="90593-193">Le fournisseur ne retourne pas toujours le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="90593-193">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="90593-194">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="90593-194">**LocalServer32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-197">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-197">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\LocalServer32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-198">Chemin d’accès complet incluant le nom de fichier ou uniquement le nom de fichier d’une application serveur locale 32 bits.</span><span class="sxs-lookup"><span data-stu-id="90593-198">Full path including filename or only filename to a 32-bit local server application.</span></span> <span data-ttu-id="90593-199">Le fournisseur ne retourne pas toujours le chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="90593-199">The provider does not always return the full path.</span></span>

</dd> <dt>

<span data-ttu-id="90593-200">**LongDisplayName**</span><span class="sxs-lookup"><span data-stu-id="90593-200">**LongDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-203">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\3\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-204">Nom complet de l’application COM.</span><span class="sxs-lookup"><span data-stu-id="90593-204">Full name of the COM application.</span></span> <span data-ttu-id="90593-205">Elle est utilisée dans des zones telles que le champ **résultats** de la boîte de dialogue **OLE Collage spécial** .</span><span class="sxs-lookup"><span data-stu-id="90593-205">It is used in areas such as the **Results** field of the **OLE Paste Special** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="90593-206">**ProgId**</span><span class="sxs-lookup"><span data-stu-id="90593-206">**ProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-209">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-209">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ProgID\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-210">Identificateur programmatique associé au composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-210">Programmatic identifier associated with the COM component.</span></span> <span data-ttu-id="90593-211">Le format d’un ProgID est <fournisseur. <version du composant. <.</span><span class="sxs-lookup"><span data-stu-id="90593-211">The format of a ProgID is <Vendor.<Component.<Version.</span></span> <span data-ttu-id="90593-212">Il n’est pas garanti que cet identificateur soit unique.</span><span class="sxs-lookup"><span data-stu-id="90593-212">This identifier is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="90593-213">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="90593-213">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-214">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-216">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="90593-216">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="90593-217">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="90593-217">Identifier by which the current object is known.</span></span>

<span data-ttu-id="90593-218">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="90593-218">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="90593-219">**ShortDisplayName**</span><span class="sxs-lookup"><span data-stu-id="90593-219">**ShortDisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-222">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-222">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\AuxUserType\\\\2\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-223">Nom abrégé de l’application COM (utilisé dans les menus et les fenêtres contextuelles).</span><span class="sxs-lookup"><span data-stu-id="90593-223">Short name of the COM application (used in menus and pop-ups).</span></span>

</dd> <dt>

<span data-ttu-id="90593-224">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="90593-224">**ThreadingModel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-227">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] »)</span><span class="sxs-lookup"><span data-stu-id="90593-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\InprocServer32\[ThreadingModel\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-228">Modèle de thread utilisé par les classes COM in-process.</span><span class="sxs-lookup"><span data-stu-id="90593-228">Threading model used by in-process COM classes.</span></span> <span data-ttu-id="90593-229">Si cette propriété a la **valeur null**, aucun modèle de thread n’est utilisé.</span><span class="sxs-lookup"><span data-stu-id="90593-229">If this property is **NULL**, then no threading model is used.</span></span> <span data-ttu-id="90593-230">Le composant est créé sur le thread principal du client et les appels d’autres threads sont marshalés vers ce thread.</span><span class="sxs-lookup"><span data-stu-id="90593-230">The component is created on the main thread of the client and calls from other threads are marshaled to this thread.</span></span>

<span data-ttu-id="90593-231">Le modèle Apartment spécifie que les composants peuvent être entrés par un et un seul thread.</span><span class="sxs-lookup"><span data-stu-id="90593-231">The Apartment model specifies that components may be entered by one and only one thread.</span></span> <span data-ttu-id="90593-232">Les données communes détenues par ces types de serveurs d’objets doivent être protégées contre les collisions de threads, car le serveur d’objets prend en charge plusieurs composants.</span><span class="sxs-lookup"><span data-stu-id="90593-232">Common data held by these types of object servers must be protected against thread collisions because the object server supports multiple components.</span></span> <span data-ttu-id="90593-233">Chaque composant peut être entré simultanément par différents threads.</span><span class="sxs-lookup"><span data-stu-id="90593-233">Each component can be entered simultaneously by different threads.</span></span>

<span data-ttu-id="90593-234">Le modèle gratuit spécifie que les composants n’imposent aucune restriction sur les threads ou le nombre de threads qui peuvent accéder à l’objet.</span><span class="sxs-lookup"><span data-stu-id="90593-234">The Free model specifies that components place no restrictions on which threads or how many threads can enter the object.</span></span> <span data-ttu-id="90593-235">L’objet ne peut pas contenir de données spécifiques aux threads et doit protéger ses données d’un accès simultané par plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="90593-235">The object cannot contain thread-specific data and must protect its data from simultaneous access by multiple threads.</span></span> <span data-ttu-id="90593-236">Toutefois, les composants à threads libres ne sont pas accessibles directement aux threads cloisonnés, et les appels à ces derniers sont marshalés à partir du cloisonnement du client.</span><span class="sxs-lookup"><span data-stu-id="90593-236">Free-threaded components however, cannot be accessed by apartment threads directly, and calls to them are marshaled across from the client apartment.</span></span>

<span data-ttu-id="90593-237">Lorsque les deux sont spécifiés, les composants peuvent être utilisés en mode thread cloisonné ou thread libre.</span><span class="sxs-lookup"><span data-stu-id="90593-237">When Both is specified, components can be used in either apartment-threaded or free-threaded modes.</span></span> <span data-ttu-id="90593-238">Ces composants peuvent être entrés par plusieurs threads, protéger leurs données contre les collisions de threads et ne contiennent pas de données spécifiques aux threads.</span><span class="sxs-lookup"><span data-stu-id="90593-238">These components can be entered by multiple threads, protect their data from thread collisions, and do not contain thread-specific data.</span></span>

<span data-ttu-id="90593-239">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="90593-239">The values are:</span></span>

<dl> <dd><span data-ttu-id="90593-240">STA</span><span class="sxs-lookup"><span data-stu-id="90593-240">"Apartment"</span></span></dd> <dd><span data-ttu-id="90593-241">Gratuit</span><span class="sxs-lookup"><span data-stu-id="90593-241">"Free"</span></span></dd> <dd><span data-ttu-id="90593-242">Versions</span><span class="sxs-lookup"><span data-stu-id="90593-242">"Both"</span></span></dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

<span data-ttu-id="90593-243">**Cloisonnement** (« Apartment »)</span><span class="sxs-lookup"><span data-stu-id="90593-243">**Apartment** ("Apartment")</span></span>


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

<span data-ttu-id="90593-244">**Gratuit** (« gratuit »)</span><span class="sxs-lookup"><span data-stu-id="90593-244">**Free** ("Free")</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="90593-245">**Les deux** (« les deux »)</span><span class="sxs-lookup"><span data-stu-id="90593-245">**Both** ("Both")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="90593-246">**ToolBoxBitmap32**</span><span class="sxs-lookup"><span data-stu-id="90593-246">**ToolBoxBitmap32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-249">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolboxBitmap32 \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\ToolBoxBitmap32\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-250">Nom de module et identificateur de ressource pour une petite image bitmap (16x16) utilisée pour la face d’un bouton de barre d’outils ou de boîte à outils.</span><span class="sxs-lookup"><span data-stu-id="90593-250">Module name and resource identifier for a small (16x16) bitmap used for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="90593-251">Utilisé lorsque le composant COM est un contrôle OLE ou ActiveX.</span><span class="sxs-lookup"><span data-stu-id="90593-251">Used when the COM component is an OLE or ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="90593-252">**TreatAsClsid**</span><span class="sxs-lookup"><span data-stu-id="90593-252">**TreatAsClsid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-253">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-254">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-255">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TreatAs \[ par défaut \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-255">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TreatAs\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-256">GUID d’un composant COM qui peut émuler des instances de ce composant.</span><span class="sxs-lookup"><span data-stu-id="90593-256">GUID of a COM component that can emulate instances of this component.</span></span>

</dd> <dt>

<span data-ttu-id="90593-257">**TypeLibraryId**</span><span class="sxs-lookup"><span data-stu-id="90593-257">**TypeLibraryId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-260">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-260">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\TypeLib\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-261">GUID de la bibliothèque de types pour ce composant COM.</span><span class="sxs-lookup"><span data-stu-id="90593-261">GUID for the type library for this COM component.</span></span>

</dd> <dt>

<span data-ttu-id="90593-262">**Version**</span><span class="sxs-lookup"><span data-stu-id="90593-262">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-263">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-264">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-265">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ Software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ version \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-265">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\Version\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-266">Numéro de version de cette classe COM.</span><span class="sxs-lookup"><span data-stu-id="90593-266">Version number of this COM class.</span></span>

</dd> <dt>

<span data-ttu-id="90593-267">**VersionIndependentProgId**</span><span class="sxs-lookup"><span data-stu-id="90593-267">**VersionIndependentProgId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90593-268">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="90593-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="90593-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="90593-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90593-270">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgID \[ default \] ")</span><span class="sxs-lookup"><span data-stu-id="90593-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\CLSID\\\\{GUID}\\\\VersionIndependentProgId\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="90593-271">Identificateur de programme cohérent pour toutes les versions du même programme.</span><span class="sxs-lookup"><span data-stu-id="90593-271">Program identifier that is consistent for all versions of the same program.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90593-272">Notes</span><span class="sxs-lookup"><span data-stu-id="90593-272">Remarks</span></span>

<span data-ttu-id="90593-273">La classe **Win32 \_ ClassicCOMClassSetting** est dérivée de la [**\_ comdéfinition Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="90593-273">The **Win32\_ClassicCOMClassSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90593-274">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90593-274">Requirements</span></span>



| <span data-ttu-id="90593-275">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90593-275">Requirement</span></span> | <span data-ttu-id="90593-276">Valeur</span><span class="sxs-lookup"><span data-stu-id="90593-276">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90593-277">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90593-277">Minimum supported client</span></span><br/> | <span data-ttu-id="90593-278">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90593-278">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90593-279">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90593-279">Minimum supported server</span></span><br/> | <span data-ttu-id="90593-280">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90593-280">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90593-281">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="90593-281">Namespace</span></span><br/>                | <span data-ttu-id="90593-282">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="90593-282">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90593-283">MOF</span><span class="sxs-lookup"><span data-stu-id="90593-283">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90593-284"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90593-284"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90593-285">DLL</span><span class="sxs-lookup"><span data-stu-id="90593-285">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90593-286"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90593-286"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90593-287">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90593-287">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90593-288">**Configuration de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="90593-288">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="90593-289">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="90593-289">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

