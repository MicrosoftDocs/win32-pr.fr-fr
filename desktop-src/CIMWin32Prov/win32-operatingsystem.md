---
description: Représente un système d’exploitation Windows installé sur un ordinateur.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201108"
---
# <a name="win32_operatingsystem-class"></a><span data-ttu-id="92c7c-103">\_Classe Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="92c7c-103">Win32\_OperatingSystem class</span></span>

<span data-ttu-id="92c7c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ OperatingSystem** représente un système d’exploitation Windows installé sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-104">The **Win32\_OperatingSystem** [WMI class](../wmisdk/retrieving-a-class.md) represents a Windows-based operating system installed on a computer.</span></span>

<span data-ttu-id="92c7c-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="92c7c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="92c7c-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="92c7c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c7c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92c7c-107">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a><span data-ttu-id="92c7c-108">Membres</span><span class="sxs-lookup"><span data-stu-id="92c7c-108">Members</span></span>

<span data-ttu-id="92c7c-109">La classe **Win32 \_ OperatingSystem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="92c7c-109">The **Win32\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="92c7c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92c7c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="92c7c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92c7c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="92c7c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="92c7c-112">Methods</span></span>

<span data-ttu-id="92c7c-113">La classe **Win32 \_ OperatingSystem** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="92c7c-113">The **Win32\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="92c7c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="92c7c-114">Method</span></span>                                                                                     | <span data-ttu-id="92c7c-115">Description</span><span class="sxs-lookup"><span data-stu-id="92c7c-115">Description</span></span>                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92c7c-116">**Reboot**</span><span class="sxs-lookup"><span data-stu-id="92c7c-116">**Reboot**</span></span>](reboot-method-in-class-win32-operatingsystem.md)                             | <span data-ttu-id="92c7c-117">Arrête puis redémarre le système informatique.</span><span class="sxs-lookup"><span data-stu-id="92c7c-117">Shuts down and then restarts the computer system.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="92c7c-118">**SetDateTime**</span><span class="sxs-lookup"><span data-stu-id="92c7c-118">**SetDateTime**</span></span>](setdatetime-method-in-class-win32-operatingsystem.md)                   | <span data-ttu-id="92c7c-119">Autorise la définition de la date et de l’heure de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-119">Allows the computer date and time to be set.</span></span><br/>                                                                                                                                                                                                                |
| [<span data-ttu-id="92c7c-120">**Correct**</span><span class="sxs-lookup"><span data-stu-id="92c7c-120">**Shutdown**</span></span>](shutdown-method-in-class-win32-operatingsystem.md)                         | <span data-ttu-id="92c7c-121">Décharge les programmes et les dll jusqu’au point où il est possible de mettre hors tension l’ordinateur en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="92c7c-121">Unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="92c7c-122">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="92c7c-122">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)               | <span data-ttu-id="92c7c-123">Fournit l’ensemble complet d’options d’arrêt prises en charge par les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="92c7c-123">Provides the full set of shutdown options supported by Windows operating systems.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="92c7c-124">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="92c7c-124">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | <span data-ttu-id="92c7c-125">Fournit le même ensemble d’options d’arrêt prises en charge par la méthode [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) dans **Win32 \_ OperatingSystem**, mais vous permet également de spécifier des commentaires, une raison d’arrêt ou un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="92c7c-125">Provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in **Win32\_OperatingSystem**, but also allows you to specify comments, a reason for shutdown, or a timeout.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="92c7c-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="92c7c-126">Properties</span></span>

<span data-ttu-id="92c7c-127">La classe **Win32 \_ OperatingSystem** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="92c7c-127">The **Win32\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="92c7c-128">**BootDevice**</span><span class="sxs-lookup"><span data-stu-id="92c7c-128">**BootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-131">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| lecteur \_ Map \_ info \| btInt13Unit »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-132">Nom du lecteur de disque à partir duquel le système d’exploitation Windows démarre.</span><span class="sxs-lookup"><span data-stu-id="92c7c-132">Name of the disk drive from which the Windows operating system starts.</span></span>

<span data-ttu-id="92c7c-133">Exemple : « \\ \\ Harddisk0 d’appareil \\ »</span><span class="sxs-lookup"><span data-stu-id="92c7c-133">Example: "\\\\Device\\Harddisk0"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-134">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="92c7c-134">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-137">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")</span><span class="sxs-lookup"><span data-stu-id="92c7c-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwBuildNumber")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-138">Numéro de build d’un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-138">Build number of an operating system.</span></span> <span data-ttu-id="92c7c-139">Il peut être utilisé pour obtenir des informations de version plus précises que les numéros de version de produit.</span><span class="sxs-lookup"><span data-stu-id="92c7c-139">It can be used for more precise version information than product release version numbers.</span></span>

<span data-ttu-id="92c7c-140">Exemple : « 1381 »</span><span class="sxs-lookup"><span data-stu-id="92c7c-140">Example: "1381"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-141">**BuildType**</span><span class="sxs-lookup"><span data-stu-id="92c7c-141">**BuildType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-142">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-144">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType")</span><span class="sxs-lookup"><span data-stu-id="92c7c-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|CurrentType")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-145">Type de build utilisé pour un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-145">Type of build used for an operating system.</span></span>

<span data-ttu-id="92c7c-146">Exemples : « version commerciale », « version contrôlée »»</span><span class="sxs-lookup"><span data-stu-id="92c7c-146">Examples: ""retail build"", ""checked build""</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-147">**Caption**</span><span class="sxs-lookup"><span data-stu-id="92c7c-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-150">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-151">Brève description de l’objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="92c7c-151">Short description of the object—a one-line string.</span></span> <span data-ttu-id="92c7c-152">La chaîne comprend la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-152">The string includes the operating system version.</span></span> <span data-ttu-id="92c7c-153">Par exemple, « Microsoft Windows 7 entreprise ».</span><span class="sxs-lookup"><span data-stu-id="92c7c-153">For example, "Microsoft Windows 7 Enterprise ".</span></span> <span data-ttu-id="92c7c-154">Cette propriété peut être localisée.</span><span class="sxs-lookup"><span data-stu-id="92c7c-154">This property can be localized.</span></span>

<span data-ttu-id="92c7c-155">**Windows Vista et Windows 7 :** Cette propriété peut contenir des caractères de fin.</span><span class="sxs-lookup"><span data-stu-id="92c7c-155">**Windows Vista and Windows 7:** This property may contain trailing characters.</span></span> <span data-ttu-id="92c7c-156">Par exemple, la chaîne « Microsoft Windows 7 entreprise » (espace de fin inclus) peut être nécessaire pour récupérer des informations à l’aide de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="92c7c-156">For example, the string "Microsoft Windows 7 Enterprise " (trailing space included) may be necessary to retrieve information using this property.</span></span>

<span data-ttu-id="92c7c-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-158">**Codes**</span><span class="sxs-lookup"><span data-stu-id="92c7c-158">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-161">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| fonctions de prise en charge linguistique nationale \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ IDEFAULTANSICODEPAGE")</span><span class="sxs-lookup"><span data-stu-id="92c7c-161">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_IDEFAULTANSICODEPAGE")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-162">Valeur de page de codes utilisée par un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-162">Code page value an operating system uses.</span></span> <span data-ttu-id="92c7c-163">Une page de codes contient une table de caractères qu’un système d’exploitation utilise pour traduire des chaînes pour différentes langues.</span><span class="sxs-lookup"><span data-stu-id="92c7c-163">A code page contains a character table that an operating system uses to translate strings for different languages.</span></span> <span data-ttu-id="92c7c-164">Le American National Standards Institute (ANSI) répertorie les valeurs qui représentent des pages de codes définies.</span><span class="sxs-lookup"><span data-stu-id="92c7c-164">The American National Standards Institute (ANSI) lists values that represent defined code pages.</span></span> <span data-ttu-id="92c7c-165">Si un système d’exploitation n’utilise pas de page de codes ANSI, ce membre a la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="92c7c-165">If an operating system does not use an ANSI code page, this member is set to 0 (zero).</span></span> <span data-ttu-id="92c7c-166">La **chaîne du** Codeet peut utiliser six caractères au maximum pour définir la valeur de la page de codes.</span><span class="sxs-lookup"><span data-stu-id="92c7c-166">The **CodeSet** string can use a maximum of six characters to define the code page value.</span></span>

<span data-ttu-id="92c7c-167">Exemple : « 1255 »</span><span class="sxs-lookup"><span data-stu-id="92c7c-167">Example: "1255"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-168">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="92c7c-168">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-171">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ ICOUNTRY")</span><span class="sxs-lookup"><span data-stu-id="92c7c-171">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ICOUNTRY")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-172">Code du pays ou de la région utilisé par un système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-172">Code for the country/region that an operating system uses.</span></span> <span data-ttu-id="92c7c-173">Les valeurs sont basées sur des préfixes de numérotation téléphonique internationaux, également appelées codes pays/région IBM.</span><span class="sxs-lookup"><span data-stu-id="92c7c-173">Values are based on international phone dialing prefixes—also referred to as IBM country/region codes.</span></span> <span data-ttu-id="92c7c-174">Cette propriété peut utiliser six caractères au maximum pour définir la valeur du code de pays/région.</span><span class="sxs-lookup"><span data-stu-id="92c7c-174">This property can use a maximum of six characters to define the country/region code value.</span></span>

<span data-ttu-id="92c7c-175">Exemple : « 1 » (États-Unis)</span><span class="sxs-lookup"><span data-stu-id="92c7c-175">Example: "1" (United States)</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="92c7c-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-179">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="92c7c-179">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-180">Nom de la première classe concrète qui apparaît dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="92c7c-180">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="92c7c-181">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, cette propriété permet d’identifier toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="92c7c-181">When used with other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="92c7c-182">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-182">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-183">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="92c7c-183">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-186">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="92c7c-186">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-187">Nom de la classe de création du système d’étendue de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-187">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="92c7c-188">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-188">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-189">**CSDVersion**</span><span class="sxs-lookup"><span data-stu-id="92c7c-189">**CSDVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-190">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-192">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")</span><span class="sxs-lookup"><span data-stu-id="92c7c-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**szCSDVersion**")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-193">Chaîne terminée par le caractère **null** qui indique la dernière Service Pack installée sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-193">**NULL**-terminated string that indicates the latest service pack installed on a computer.</span></span> <span data-ttu-id="92c7c-194">Si aucun Service Pack n’est installé, la chaîne est **null**.</span><span class="sxs-lookup"><span data-stu-id="92c7c-194">If no service pack is installed, the string is **NULL**.</span></span>

<span data-ttu-id="92c7c-195">Exemple : « Service Pack 3 »</span><span class="sxs-lookup"><span data-stu-id="92c7c-195">Example: "Service Pack 3"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-196">**CSName**</span><span class="sxs-lookup"><span data-stu-id="92c7c-196">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-197">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-198">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-199">Qualificateurs : [**propagé**](../wmisdk/standard-qualifiers.md) ("[**CIM CIM \_**](cim-computersystem.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="92c7c-199">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-200">Nom du système informatique d’étendue.</span><span class="sxs-lookup"><span data-stu-id="92c7c-200">Name of the scoping computer system.</span></span>

<span data-ttu-id="92c7c-201">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-201">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-202">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="92c7c-202">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-203">Type de données : **sint16**</span><span class="sxs-lookup"><span data-stu-id="92c7c-203">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-205">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-205">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-206">Nombre, en minutes, un système d’exploitation est décalé par rapport à l’heure GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="92c7c-206">Number, in minutes, an operating system is offset from Greenwich mean time (GMT).</span></span> <span data-ttu-id="92c7c-207">Le nombre est positif, négatif ou égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="92c7c-207">The number is positive, negative, or zero.</span></span>

<span data-ttu-id="92c7c-208">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-208">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-209">**DataExecutionPrevention \_ 32BitApplications**</span><span class="sxs-lookup"><span data-stu-id="92c7c-209">**DataExecutionPrevention\_32BitApplications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-210">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-212">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-213">Lorsque la fonctionnalité matérielle de prévention de l’exécution des données est disponible, cette propriété indique que la fonctionnalité est configurée pour fonctionner pour les applications 32 bits si la **valeur est true**.</span><span class="sxs-lookup"><span data-stu-id="92c7c-213">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for 32-bit applications if **True**.</span></span> <span data-ttu-id="92c7c-214">Sur les ordinateurs 64 bits, la fonctionnalité de prévention de l’exécution des données est configurée dans le magasin [données de configuration de démarrage (BCD) (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) et les propriétés dans **Win32 \_ OperatingSystem** sont définies en conséquence.</span><span class="sxs-lookup"><span data-stu-id="92c7c-214">On 64-bit computers, the data execution prevention feature is configured in the [Boot Configuration Data (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-215">**DataExecutionPrevention \_ disponibles**</span><span class="sxs-lookup"><span data-stu-id="92c7c-215">**DataExecutionPrevention\_Available**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-216">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-217">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-218">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-219">La prévention de l’exécution des données est une fonctionnalité matérielle permettant d’empêcher les attaques par dépassement de mémoire tampon en arrêtant l’exécution du code sur les pages de mémoire de type de données.</span><span class="sxs-lookup"><span data-stu-id="92c7c-219">Data execution prevention is a hardware feature to prevent buffer overrun attacks by stopping the execution of code on data-type memory pages.</span></span> <span data-ttu-id="92c7c-220">Si la **valeur est true**, cette fonctionnalité est disponible.</span><span class="sxs-lookup"><span data-stu-id="92c7c-220">If **True**, then this feature is available.</span></span> <span data-ttu-id="92c7c-221">Sur les ordinateurs 64 bits, la fonctionnalité de prévention de l’exécution des données est configurée dans le magasin BCD et les propriétés dans **Win32 \_ OperatingSystem** sont définies en conséquence.</span><span class="sxs-lookup"><span data-stu-id="92c7c-221">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-222">**\_Pilotes DataExecutionPrevention**</span><span class="sxs-lookup"><span data-stu-id="92c7c-222">**DataExecutionPrevention\_Drivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-223">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-224">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-225">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-226">Lorsque la fonctionnalité matérielle de prévention de l’exécution des données est disponible, cette propriété indique que la fonctionnalité est configurée pour fonctionner pour les pilotes si la **valeur est true**.</span><span class="sxs-lookup"><span data-stu-id="92c7c-226">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for drivers if **True**.</span></span> <span data-ttu-id="92c7c-227">Sur les ordinateurs 64 bits, la fonctionnalité de prévention de l’exécution des données est configurée dans le magasin BCD et les propriétés dans **Win32 \_ OperatingSystem** sont définies en conséquence.</span><span class="sxs-lookup"><span data-stu-id="92c7c-227">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-228">**DataExecutionPrevention \_ SupportPolicy**</span><span class="sxs-lookup"><span data-stu-id="92c7c-228">**DataExecutionPrevention\_SupportPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-229">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="92c7c-229">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-231">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-232">Indique quel paramètre de prévention de l’exécution des données (DEP) est appliqué.</span><span class="sxs-lookup"><span data-stu-id="92c7c-232">Indicates which Data Execution Prevention (DEP) setting is applied.</span></span> <span data-ttu-id="92c7c-233">Le paramètre DEP spécifie dans quelle mesure DEP s’applique aux applications 32 bits sur le système.</span><span class="sxs-lookup"><span data-stu-id="92c7c-233">The DEP setting specifies the extent to which DEP applies to 32-bit applications on the system.</span></span> <span data-ttu-id="92c7c-234">DEP est toujours appliqué au noyau Windows.</span><span class="sxs-lookup"><span data-stu-id="92c7c-234">DEP is always applied to the Windows kernel.</span></span>

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span data-ttu-id="92c7c-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Toujours désactivé** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-236">DEP est désactivé pour toutes les applications 32 bits sur l’ordinateur sans exceptions.</span><span class="sxs-lookup"><span data-stu-id="92c7c-236">DEP is turned off for all 32-bit applications on the computer with no exceptions.</span></span> <span data-ttu-id="92c7c-237">Ce paramètre n’est pas disponible pour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-237">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span data-ttu-id="92c7c-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-239">DEP est activé pour toutes les applications 32 bits sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-239">DEP is enabled for all 32-bit applications on the computer.</span></span> <span data-ttu-id="92c7c-240">Ce paramètre n’est pas disponible pour l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-240">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span data-ttu-id="92c7c-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Accepter** (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt In** (2)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-242">DEP est activé pour un nombre limité de fichiers binaires, le noyau et tous les services Windows.</span><span class="sxs-lookup"><span data-stu-id="92c7c-242">DEP is enabled for a limited number of binaries, the kernel, and all Windows-based services.</span></span> <span data-ttu-id="92c7c-243">Toutefois, elle est désactivée par défaut pour toutes les applications 32 bits.</span><span class="sxs-lookup"><span data-stu-id="92c7c-243">However, it is off by default for all 32-bit applications.</span></span> <span data-ttu-id="92c7c-244">Un utilisateur ou un administrateur doit choisir explicitement le **Always on** ou le paramètre d' **annulation** avant que DEP puisse être appliqué aux applications 32 bits.</span><span class="sxs-lookup"><span data-stu-id="92c7c-244">A user or administrator must explicitly choose either the **Always On** or the **Opt Out** setting before DEP can be applied to 32-bit applications.</span></span>

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span data-ttu-id="92c7c-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Refuser** (3)</span><span class="sxs-lookup"><span data-stu-id="92c7c-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Opt Out** (3)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-246">DEP est activé par défaut pour toutes les applications 32 bits.</span><span class="sxs-lookup"><span data-stu-id="92c7c-246">DEP is enabled by default for all 32-bit applications.</span></span> <span data-ttu-id="92c7c-247">Un utilisateur ou un administrateur peut supprimer explicitement la prise en charge d’une application 32 bits en ajoutant l’application à une liste d’exceptions.</span><span class="sxs-lookup"><span data-stu-id="92c7c-247">A user or administrator can explicitly remove support for a 32-bit application by adding the application to an exceptions list.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-248">**Déboguer**</span><span class="sxs-lookup"><span data-stu-id="92c7c-248">**Debug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-249">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-251">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ debug")</span><span class="sxs-lookup"><span data-stu-id="92c7c-251">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)\|SM\_DEBUG")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-252">Le système d’exploitation est une version (débogage) vérifiée.</span><span class="sxs-lookup"><span data-stu-id="92c7c-252">Operating system is a checked (debug) build.</span></span> <span data-ttu-id="92c7c-253">Si la **valeur est true**, la version de débogage est installée.</span><span class="sxs-lookup"><span data-stu-id="92c7c-253">If **True**, the debugging version is installed.</span></span> <span data-ttu-id="92c7c-254">Les builds vérifiées permettent de vérifier les erreurs, la vérification des arguments et le code de débogage du système.</span><span class="sxs-lookup"><span data-stu-id="92c7c-254">Checked builds provide error checking, argument verification, and system debugging code.</span></span> <span data-ttu-id="92c7c-255">Du code supplémentaire dans un fichier binaire vérifié génère un message d’erreur du débogueur du noyau et s’arrête dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-255">Additional code in a checked binary generates a kernel debugger error message and breaks into the debugger.</span></span> <span data-ttu-id="92c7c-256">Cela permet de déterminer immédiatement la cause et l’emplacement de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-256">This helps immediately determine the cause and location of the error.</span></span> <span data-ttu-id="92c7c-257">Les performances peuvent être affectées dans une build vérifiée en raison du code supplémentaire qui est exécuté.</span><span class="sxs-lookup"><span data-stu-id="92c7c-257">Performance may be affected in a checked build due to the additional code that is executed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-258">**Description**</span><span class="sxs-lookup"><span data-stu-id="92c7c-258">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-259">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-260">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="92c7c-260">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-261">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="92c7c-261">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-262">Description du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="92c7c-262">Description of the Windows operating system.</span></span> <span data-ttu-id="92c7c-263">Certaines interfaces utilisateur, par exemple, celles qui autorisent la modification de cette description, limitent sa longueur à 48 caractères.</span><span class="sxs-lookup"><span data-stu-id="92c7c-263">Some user interfaces for example, those that allow editing of this description, limit its length to 48 characters.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-264">**Graphique**</span><span class="sxs-lookup"><span data-stu-id="92c7c-264">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-265">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-266">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-267">Si la **valeur est true**, le système d’exploitation est distribué sur plusieurs nœuds système de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-267">If **True**, the operating system is distributed across several computer system nodes.</span></span> <span data-ttu-id="92c7c-268">Dans ce cas, ces nœuds doivent être regroupés en tant que cluster.</span><span class="sxs-lookup"><span data-stu-id="92c7c-268">If so, these nodes should be grouped as a cluster.</span></span>

<span data-ttu-id="92c7c-269">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-269">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-270">**EncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="92c7c-270">**EncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-271">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-271">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-273">Niveau de chiffrement pour les transactions sécurisées : 40 bits, 128 bits ou *n*-bit.</span><span class="sxs-lookup"><span data-stu-id="92c7c-273">Encryption level for secure transactions: 40-bit, 128-bit, or *n*-bit.</span></span>

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

<span data-ttu-id="92c7c-274">**40 bits** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-274">**40-bit** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

<span data-ttu-id="92c7c-275">**128** bits (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-275">**128-bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

<span data-ttu-id="92c7c-276">**n** bits (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-276">**n-bit** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-277">**ForegroundApplicationBoost**</span><span class="sxs-lookup"><span data-stu-id="92c7c-277">**ForegroundApplicationBoost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-278">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="92c7c-278">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-279">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="92c7c-279">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-280">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="92c7c-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-281">Une augmentation de la priorité est accordée à l’application de premier plan.</span><span class="sxs-lookup"><span data-stu-id="92c7c-281">Increase in priority is given to the foreground application.</span></span> <span data-ttu-id="92c7c-282">L’amélioration de l’application est implémentée en donnant à une application plus de tranches de temps d’exécution (longueurs de Quantum).</span><span class="sxs-lookup"><span data-stu-id="92c7c-282">Application boost is implemented by giving an application more execution time slices (quantum lengths).</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="92c7c-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-284">Le système augmente la longueur de quantum de 6.</span><span class="sxs-lookup"><span data-stu-id="92c7c-284">The system boosts the quantum length by 6.</span></span>

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="92c7c-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-286">Le système augmente la longueur de quantum de 12.</span><span class="sxs-lookup"><span data-stu-id="92c7c-286">The system boosts the quantum length by 12.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="92c7c-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-288">Le système augmente la longueur de quantum de 18.</span><span class="sxs-lookup"><span data-stu-id="92c7c-288">The system boosts the quantum length by 18.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-289">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="92c7c-289">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-290">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-291">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-292">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-292">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-293">Nombre, en kilo-octets, de la mémoire physique actuellement inutilisée et disponible.</span><span class="sxs-lookup"><span data-stu-id="92c7c-293">Number, in kilobytes, of physical memory currently unused and available.</span></span>

<span data-ttu-id="92c7c-294">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-294">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-295">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-295">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-296">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="92c7c-296">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-297">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-298">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-299">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Paramètres de mémoire système DMTF \| 001,4»), [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-300">Nombre, en kilo-octets, qui peut être mappé dans les fichiers de pagination du système d’exploitation sans entraîner le remplacement de toutes les autres pages.</span><span class="sxs-lookup"><span data-stu-id="92c7c-300">Number, in kilobytes, that can be mapped into the operating system paging files without causing any other pages to be swapped out.</span></span>

<span data-ttu-id="92c7c-301">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-302">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-302">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-303">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="92c7c-303">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-304">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-306">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-306">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-307">Nombre, en kilo-octets, de la mémoire virtuelle actuellement inutilisée et disponible.</span><span class="sxs-lookup"><span data-stu-id="92c7c-307">Number, in kilobytes, of virtual memory currently unused and available.</span></span>

<span data-ttu-id="92c7c-308">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-309">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-309">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="92c7c-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-311">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92c7c-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-313">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="92c7c-313">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-314">L’objet date a été installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-314">Date object was installed.</span></span> <span data-ttu-id="92c7c-315">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-315">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="92c7c-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-317">**LargeSystemCache**</span><span class="sxs-lookup"><span data-stu-id="92c7c-317">**LargeSystemCache**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-318">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-319">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-320">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="92c7c-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-321">Cette propriété est obsolète et n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="92c7c-321">This property is obsolete and not supported.</span></span>

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span data-ttu-id="92c7c-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimiser pour les applications** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimize for Applications** (0)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-323">Optimiser la mémoire pour les applications.</span><span class="sxs-lookup"><span data-stu-id="92c7c-323">Optimize memory for applications.</span></span>

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span data-ttu-id="92c7c-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimiser pour les performances du système** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimize for System Performance** (1)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-325">Optimiser la mémoire pour les performances du système.</span><span class="sxs-lookup"><span data-stu-id="92c7c-325">Optimize memory for system performance.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-326">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="92c7c-326">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-327">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92c7c-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-328">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-329">Date et heure du dernier redémarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-329">Date and time the operating system was last restarted.</span></span>

<span data-ttu-id="92c7c-330">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-330">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-331">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="92c7c-331">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-332">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="92c7c-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-334">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. hrSystemDate "," MIF. \|Informations générales sur DMTF \| 001,6»)</span><span class="sxs-lookup"><span data-stu-id="92c7c-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-335">Version du système d’exploitation de la date et de l’heure locales.</span><span class="sxs-lookup"><span data-stu-id="92c7c-335">Operating system version of the local date and time-of-day.</span></span>

<span data-ttu-id="92c7c-336">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-336">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-337">**Paramètres régionaux**</span><span class="sxs-lookup"><span data-stu-id="92c7c-337">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-338">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-339">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-340">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ ILANGUAGE")</span><span class="sxs-lookup"><span data-stu-id="92c7c-340">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ILANGUAGE")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-341">Identificateur de langue utilisé par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-341">Language identifier used by the operating system.</span></span> <span data-ttu-id="92c7c-342">Un identificateur de langue est une abréviation numérique internationale standard pour un pays ou une région.</span><span class="sxs-lookup"><span data-stu-id="92c7c-342">A language identifier is a standard international numeric abbreviation for a country/region.</span></span> <span data-ttu-id="92c7c-343">Chaque langue possède un identificateur de langue unique (LANGID), une valeur de 16 bits qui se compose d’un identificateur de langue primaire et d’un identificateur de langue secondaire.</span><span class="sxs-lookup"><span data-stu-id="92c7c-343">Each language has a unique language identifier (LANGID), a 16-bit value that consists of a primary language identifier and a secondary language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-344">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="92c7c-344">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-346">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-347">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-348">Nom du fabricant du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-348">Name of the operating system manufacturer.</span></span> <span data-ttu-id="92c7c-349">Pour les systèmes Windows, cette valeur est « Microsoft Corporation ».</span><span class="sxs-lookup"><span data-stu-id="92c7c-349">For Windows-based systems, this value is "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-350">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="92c7c-350">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-351">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-353">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="92c7c-353">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-354">Nombre maximal de contextes de processus que le système d’exploitation peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="92c7c-354">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="92c7c-355">La valeur par défaut définie par le fournisseur est 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="92c7c-355">The default value set by the provider is 4294967295 (0xFFFFFFFF).</span></span> <span data-ttu-id="92c7c-356">S’il n’y a pas de valeur maximale fixe, la valeur doit être 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="92c7c-356">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="92c7c-357">Sur les systèmes qui ont un maximum fixe, cet objet peut aider à diagnostiquer les défaillances qui se produisent lorsque la valeur maximale est atteinte. si elle est inconnue, entrez 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="92c7c-357">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached—if unknown, enter 4294967295 (0xFFFFFFFF).</span></span>

<span data-ttu-id="92c7c-358">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-358">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-359">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="92c7c-359">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-360">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-361">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-362">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-362">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-363">Nombre maximal, en kilo-octets, de la mémoire qui peut être allouée à un processus.</span><span class="sxs-lookup"><span data-stu-id="92c7c-363">Maximum number, in kilobytes, of memory that can be allocated to a process.</span></span> <span data-ttu-id="92c7c-364">Pour les systèmes d’exploitation sans mémoire virtuelle, cette valeur est généralement égale à la quantité totale de mémoire physique moins la mémoire utilisée par le BIOS et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-364">For operating systems with no virtual memory, typically this value is equal to the total amount of physical memory minus the memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="92c7c-365">Pour certains systèmes d’exploitation, cette valeur peut être l’infini, auquel cas 0 (zéro) doit être entré.</span><span class="sxs-lookup"><span data-stu-id="92c7c-365">For some operating systems, this value may be infinity, in which case 0 (zero) should be entered.</span></span> <span data-ttu-id="92c7c-366">Dans d’autres cas, cette valeur peut être une constante, par exemple 2G ou 4G.</span><span class="sxs-lookup"><span data-stu-id="92c7c-366">In other cases, this value could be a constant, for example, 2G or 4G.</span></span>

<span data-ttu-id="92c7c-367">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-368">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-368">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-369">**MUILanguages**</span><span class="sxs-lookup"><span data-stu-id="92c7c-369">**MUILanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-370">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="92c7c-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-372">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-373">Langues du pack d’interface utilisateur multilingue (MUI Pack) installées sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-373">Multilingual User Interface Pack (MUI Pack ) languages installed on the computer.</span></span> <span data-ttu-id="92c7c-374">Par exemple, « en-US ».</span><span class="sxs-lookup"><span data-stu-id="92c7c-374">For example, "en-us".</span></span> <span data-ttu-id="92c7c-375">Les langues du Pack MUI sont des fichiers de ressources qui peuvent être installés sur la version anglaise du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-375">MUI Pack languages are resource files that can be installed on the English version of the operating system.</span></span> <span data-ttu-id="92c7c-376">Quand un pack MUI est installé, vous pouvez modifier la langue de l’interface utilisateur en 33 langues prises en charge.</span><span class="sxs-lookup"><span data-stu-id="92c7c-376">When an MUI Pack is installed, you can can change the user interface language to one of 33 supported languages.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-377">**Nom**</span><span class="sxs-lookup"><span data-stu-id="92c7c-377">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-378">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-378">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-379">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-380">Instance du système d’exploitation au sein d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="92c7c-380">Operating system instance within a computer system.</span></span>

<span data-ttu-id="92c7c-381">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-381">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-382">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="92c7c-382">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-383">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-385">Nombre de licences utilisateur pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-385">Number of user licenses for the operating system.</span></span> <span data-ttu-id="92c7c-386">Si la valeur est Unlimited, entrez 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="92c7c-386">If unlimited, enter 0 (zero).</span></span> <span data-ttu-id="92c7c-387">S’il est inconnu, entrez-1.</span><span class="sxs-lookup"><span data-stu-id="92c7c-387">If unknown, enter -1.</span></span>

<span data-ttu-id="92c7c-388">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-388">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-389">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="92c7c-389">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-390">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-392">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="92c7c-392">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-393">Nombre de contextes de processus actuellement chargés ou en cours d’exécution sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-393">Number of process contexts currently loaded or running on the operating system.</span></span>

<span data-ttu-id="92c7c-394">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-394">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-395">**Numdatabases**</span><span class="sxs-lookup"><span data-stu-id="92c7c-395">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-396">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-397">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-398">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Hôte IETF-ressources-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="92c7c-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-399">Nombre de sessions utilisateur pour lesquelles le système d’exploitation stocke actuellement des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="92c7c-399">Number of user sessions for which the operating system is storing state information currently.</span></span>

<span data-ttu-id="92c7c-400">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-400">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-401">**OperatingSystemSKU**</span><span class="sxs-lookup"><span data-stu-id="92c7c-401">**OperatingSystemSKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-402">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-403">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-404">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-405">Numéro SKU (Stock Keeping Unit) du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-405">Stock Keeping Unit (SKU) number for the operating system.</span></span> <span data-ttu-id="92c7c-406">Ces valeurs sont les mêmes que les constantes \**Product \_ \** _ définies dans Winnt. h, qui sont utilisées avec la fonction [_ *GetProductInfo* \*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="92c7c-406">These values are the same as the \**PRODUCT\_\** _ constants defined in WinNT.h that are used with the [_ *GetProductInfo*\*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span>

<span data-ttu-id="92c7c-407">La liste suivante répertorie les valeurs SKU possibles.</span><span class="sxs-lookup"><span data-stu-id="92c7c-407">The following list lists possible SKU values.</span></span>

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span data-ttu-id="92c7c-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Produit \_ NON défini** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT\_UNDEFINED** (0)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-409">Indéfini</span><span class="sxs-lookup"><span data-stu-id="92c7c-409">Undefined</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span data-ttu-id="92c7c-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Produit \_ ÉDITION INTÉGRALe** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT\_ULTIMATE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-411">Édition intégrale, par exemple, Windows Vista Édition intégrale.</span><span class="sxs-lookup"><span data-stu-id="92c7c-411">Ultimate Edition, e.g. Windows Vista Ultimate.</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span data-ttu-id="92c7c-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Produit \_ Édition \_ familial** (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT\_HOME\_BASIC** (2)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-413">Édition familial basique</span><span class="sxs-lookup"><span data-stu-id="92c7c-413">Home Basic Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span data-ttu-id="92c7c-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Produit \_ Édition familiale \_ Premium** (3)</span><span class="sxs-lookup"><span data-stu-id="92c7c-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT\_HOME\_PREMIUM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-415">Édition familiale Premium</span><span class="sxs-lookup"><span data-stu-id="92c7c-415">Home Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span data-ttu-id="92c7c-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Produit \_ ENTREPRISE** (4)</span><span class="sxs-lookup"><span data-stu-id="92c7c-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT\_ENTERPRISE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-417">Édition Entreprise</span><span class="sxs-lookup"><span data-stu-id="92c7c-417">Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span data-ttu-id="92c7c-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Produit \_ ENTREPRISE** (6)</span><span class="sxs-lookup"><span data-stu-id="92c7c-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT\_BUSINESS** (6)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-419">Professionnel</span><span class="sxs-lookup"><span data-stu-id="92c7c-419">Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span data-ttu-id="92c7c-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Produit \_ \_Serveur standard** (7)</span><span class="sxs-lookup"><span data-stu-id="92c7c-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT\_STANDARD\_SERVER** (7)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-421">Windows Server Standard Edition (installation de l’expérience utilisateur)</span><span class="sxs-lookup"><span data-stu-id="92c7c-421">Windows Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span data-ttu-id="92c7c-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Produit \_ \_Serveur de centre de centres** (8)</span><span class="sxs-lookup"><span data-stu-id="92c7c-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT\_DATACENTER\_SERVER** (8)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-423">Windows Server Datacenter Edition (installation de l’expérience utilisateur)</span><span class="sxs-lookup"><span data-stu-id="92c7c-423">Windows Server Datacenter Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span data-ttu-id="92c7c-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Produit \_ \_Serveur SMALLBUSINESS** (9)</span><span class="sxs-lookup"><span data-stu-id="92c7c-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT\_SMALLBUSINESS\_SERVER** (9)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-425">Édition Small Business Server</span><span class="sxs-lookup"><span data-stu-id="92c7c-425">Small Business Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span data-ttu-id="92c7c-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Produit \_ \_Serveur d’entreprise** (10)</span><span class="sxs-lookup"><span data-stu-id="92c7c-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT\_ENTERPRISE\_SERVER** (10)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-427">Édition Enterprise Server</span><span class="sxs-lookup"><span data-stu-id="92c7c-427">Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span data-ttu-id="92c7c-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Produit \_ STARTER** (11)</span><span class="sxs-lookup"><span data-stu-id="92c7c-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT\_STARTER** (11)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-429"> Starter Edition</span><span class="sxs-lookup"><span data-stu-id="92c7c-429">Starter Edition</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span data-ttu-id="92c7c-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Produit \_ DATACENTER \_ Server \_ Core** (12)</span><span class="sxs-lookup"><span data-stu-id="92c7c-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE** (12)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-431">Édition Core de Datacenter Server</span><span class="sxs-lookup"><span data-stu-id="92c7c-431">Datacenter Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span data-ttu-id="92c7c-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Produit \_ STANDARD \_ Server \_ Core** (13)</span><span class="sxs-lookup"><span data-stu-id="92c7c-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT\_STANDARD\_SERVER\_CORE** (13)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-433">Édition Standard Server Core</span><span class="sxs-lookup"><span data-stu-id="92c7c-433">Standard Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span data-ttu-id="92c7c-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Produit \_ ENTERPRISE \_ Server \_ Core** (14)</span><span class="sxs-lookup"><span data-stu-id="92c7c-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE** (14)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-435">Enterprise Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="92c7c-435">Enterprise Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span data-ttu-id="92c7c-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Produit \_ \_Serveur Web** (17)</span><span class="sxs-lookup"><span data-stu-id="92c7c-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT\_WEB\_SERVER** (17)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-437">Édition Web Server</span><span class="sxs-lookup"><span data-stu-id="92c7c-437">Web Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span data-ttu-id="92c7c-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Produit \_ \_Serveur d’hébergement** (19)</span><span class="sxs-lookup"><span data-stu-id="92c7c-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT\_HOME\_SERVER** (19)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-439">Édition de serveur principal</span><span class="sxs-lookup"><span data-stu-id="92c7c-439">Home Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span data-ttu-id="92c7c-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Produit \_ STORAGE \_ Express \_ Server** (20)</span><span class="sxs-lookup"><span data-stu-id="92c7c-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER** (20)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-441">Storage Express Server Edition</span><span class="sxs-lookup"><span data-stu-id="92c7c-441">Storage Express Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span data-ttu-id="92c7c-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Produit \_ \_ \_ Serveur de stockage standard** (21)</span><span class="sxs-lookup"><span data-stu-id="92c7c-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER** (21)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-443">Windows Storage Server Standard Edition (installation de l’expérience utilisateur)</span><span class="sxs-lookup"><span data-stu-id="92c7c-443">Windows Storage Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span data-ttu-id="92c7c-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Produit \_ STORAGE \_ Workgroup \_ Server** (22)</span><span class="sxs-lookup"><span data-stu-id="92c7c-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER** (22)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-445">Windows Storage Server Workgroup Edition (installation de l’expérience utilisateur)</span><span class="sxs-lookup"><span data-stu-id="92c7c-445">Windows Storage Server Workgroup Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span data-ttu-id="92c7c-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Produit \_ STORAGE \_ Enterprise \_ Server** (23)</span><span class="sxs-lookup"><span data-stu-id="92c7c-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER** (23)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-447">Stockage Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="92c7c-447">Storage Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span data-ttu-id="92c7c-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Produit \_ SERVEUR \_ pour \_ SMALLBUSINESS** (24)</span><span class="sxs-lookup"><span data-stu-id="92c7c-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT\_SERVER\_FOR\_SMALLBUSINESS** (24)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-449">Server pour Small Business Edition</span><span class="sxs-lookup"><span data-stu-id="92c7c-449">Server For Small Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span data-ttu-id="92c7c-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Produit \_ SMALLBUSINESS \_ Server \_ Premium** (25)</span><span class="sxs-lookup"><span data-stu-id="92c7c-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM** (25)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-451">Small Business Server Premium Edition</span><span class="sxs-lookup"><span data-stu-id="92c7c-451">Small Business Server Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span data-ttu-id="92c7c-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Produit \_ ENTREPRISE \_ N** (27)</span><span class="sxs-lookup"><span data-stu-id="92c7c-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT\_ENTERPRISE\_N** (27)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-453">Windows édition entreprise</span><span class="sxs-lookup"><span data-stu-id="92c7c-453">Windows Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span data-ttu-id="92c7c-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Produit \_ ULTIMATE \_ N** (28)</span><span class="sxs-lookup"><span data-stu-id="92c7c-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT\_ULTIMATE\_N** (28)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-455">Édition Windows édition intégrale</span><span class="sxs-lookup"><span data-stu-id="92c7c-455">Windows Ultimate Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span data-ttu-id="92c7c-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Produit \_ WEB \_ Server \_ Core** (29)</span><span class="sxs-lookup"><span data-stu-id="92c7c-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT\_WEB\_SERVER\_CORE** (29)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-457">Windows Server Web Edition (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-457">Windows Server Web Server Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span data-ttu-id="92c7c-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Produit \_ \_Serveur standard \_ V** (36)</span><span class="sxs-lookup"><span data-stu-id="92c7c-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT\_STANDARD\_SERVER\_V** (36)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-459">Windows Server Standard Edition sans Hyper-V</span><span class="sxs-lookup"><span data-stu-id="92c7c-459">Windows Server Standard Edition without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span data-ttu-id="92c7c-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Produit \_ DATACENTER \_ Server \_ V** (37)</span><span class="sxs-lookup"><span data-stu-id="92c7c-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT\_DATACENTER\_SERVER\_V** (37)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-461">Windows Server Datacenter Edition sans Hyper-V (installation complète)</span><span class="sxs-lookup"><span data-stu-id="92c7c-461">Windows Server Datacenter Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span data-ttu-id="92c7c-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Produit \_ Serveur d’entreprise \_ \_ V** (38)</span><span class="sxs-lookup"><span data-stu-id="92c7c-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_V** (38)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-463">Windows Server Enterprise Edition sans Hyper-V (installation complète)</span><span class="sxs-lookup"><span data-stu-id="92c7c-463">Windows Server Enterprise Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span data-ttu-id="92c7c-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Produit \_ DATACENTER \_ Server \_ Core \_ V** (39)</span><span class="sxs-lookup"><span data-stu-id="92c7c-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE\_V** (39)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-465">Windows Server Datacenter Edition sans Hyper-V (installation Server Core)</span><span class="sxs-lookup"><span data-stu-id="92c7c-465">Windows Server Datacenter Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span data-ttu-id="92c7c-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Produit \_ STANDARD \_ Server \_ Core \_ V** (40)</span><span class="sxs-lookup"><span data-stu-id="92c7c-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT\_STANDARD\_SERVER\_CORE\_V** (40)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-467">Windows Server Standard Edition sans Hyper-V (installation Server Core)</span><span class="sxs-lookup"><span data-stu-id="92c7c-467">Windows Server Standard Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span data-ttu-id="92c7c-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Produit \_ ENTERPRISE \_ Server \_ Core \_ V** (41)</span><span class="sxs-lookup"><span data-stu-id="92c7c-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE\_V** (41)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-469">Windows Server entreprise Edition sans Hyper-V (installation Server Core)</span><span class="sxs-lookup"><span data-stu-id="92c7c-469">Windows Server Enterprise Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span data-ttu-id="92c7c-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Produit \_ HYPERV** (42)</span><span class="sxs-lookup"><span data-stu-id="92c7c-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT\_HYPERV** (42)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-471">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="92c7c-471">Microsoft Hyper-V Server</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span data-ttu-id="92c7c-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Produit \_ STORAGE \_ Express \_ Server \_ Core** (43)</span><span class="sxs-lookup"><span data-stu-id="92c7c-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER\_CORE** (43)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-473">Storage Server Express Edition (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-473">Storage Server Express Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span data-ttu-id="92c7c-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Produit \_ \_Core Storage standard \_ Server \_ Core** (44)</span><span class="sxs-lookup"><span data-stu-id="92c7c-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER\_CORE** (44)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-475">Storage Server Standard Edition (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-475">Storage Server Standard Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span data-ttu-id="92c7c-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Produit \_ STORAGE \_ Workgroup \_ Server \_ Core** (45)</span><span class="sxs-lookup"><span data-stu-id="92c7c-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER\_CORE** (45)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-477">Storage Server Workgroup Edition (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-477">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span data-ttu-id="92c7c-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Produit \_ STOCKAGE \_ Enterprise \_ Server \_ Core** (46)</span><span class="sxs-lookup"><span data-stu-id="92c7c-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER\_CORE** (46)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-479">Storage Server Workgroup Edition (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-479">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span data-ttu-id="92c7c-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Produit \_ PROFESSIONNEL** (48)</span><span class="sxs-lookup"><span data-stu-id="92c7c-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT\_PROFESSIONAL** (48)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-481">Windows professionnel</span><span class="sxs-lookup"><span data-stu-id="92c7c-481">Windows Professional</span></span>

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span data-ttu-id="92c7c-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Produit \_ \_ \_ Serveur de solutions SB** (50)</span><span class="sxs-lookup"><span data-stu-id="92c7c-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT\_SB\_SOLUTION\_SERVER** (50)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-483">Windows Server Essentials (installation de l’expérience utilisateur)</span><span class="sxs-lookup"><span data-stu-id="92c7c-483">Windows Server Essentials (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span data-ttu-id="92c7c-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Produit \_ SMALLBUSINESS \_ Server \_ Premium \_ Core** (63)</span><span class="sxs-lookup"><span data-stu-id="92c7c-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM\_CORE** (63)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-485">Small Business Server Premium (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-485">Small Business Server Premium (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span data-ttu-id="92c7c-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Produit \_ Serveur de CLUSTER \_ \_ V** (64)</span><span class="sxs-lookup"><span data-stu-id="92c7c-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT\_CLUSTER\_SERVER\_V** (64)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-487">Windows Compute Cluster Server sans Hyper-V</span><span class="sxs-lookup"><span data-stu-id="92c7c-487">Windows Compute Cluster Server without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span data-ttu-id="92c7c-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Produit \_ \_ARM Core** (97)</span><span class="sxs-lookup"><span data-stu-id="92c7c-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT\_CORE\_ARM** (97)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-489">Windows RT</span><span class="sxs-lookup"><span data-stu-id="92c7c-489">Windows RT</span></span>

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span data-ttu-id="92c7c-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**Produit \_ CORE** (101)</span><span class="sxs-lookup"><span data-stu-id="92c7c-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT\_CORE** (101)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-491">Page d’hébergement Windows</span><span class="sxs-lookup"><span data-stu-id="92c7c-491">Windows Home</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span data-ttu-id="92c7c-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Produit \_ \_WMC professionnel** (103)</span><span class="sxs-lookup"><span data-stu-id="92c7c-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT\_PROFESSIONAL\_WMC** (103)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-493">Windows professionnel avec Media Center</span><span class="sxs-lookup"><span data-stu-id="92c7c-493">Windows Professional with Media Center</span></span>

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span data-ttu-id="92c7c-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Produit \_ MOBILE \_ Core** (104)</span><span class="sxs-lookup"><span data-stu-id="92c7c-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT\_MOBILE\_CORE** (104)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-495">Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="92c7c-495">Windows Mobile</span></span>

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span data-ttu-id="92c7c-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Produit \_ IOTUAP** (123)</span><span class="sxs-lookup"><span data-stu-id="92c7c-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT\_IOTUAP** (123)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-497">Noyau Windows IoT (Internet des objets)</span><span class="sxs-lookup"><span data-stu-id="92c7c-497">Windows IoT (Internet of Things) Core</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span data-ttu-id="92c7c-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Produit \_ Serveur de centre de \_ \_ serveurs de NANO** (143)</span><span class="sxs-lookup"><span data-stu-id="92c7c-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT\_DATACENTER\_NANO\_SERVER** (143)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-499">Windows Server Datacenter Edition (installation nano Server)</span><span class="sxs-lookup"><span data-stu-id="92c7c-499">Windows Server Datacenter Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span data-ttu-id="92c7c-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Produit \_ \_Nano \_ Server STANDARD** (144)</span><span class="sxs-lookup"><span data-stu-id="92c7c-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT\_STANDARD\_NANO\_SERVER** (144)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-501">Windows Server Standard Edition (installation nano Server)</span><span class="sxs-lookup"><span data-stu-id="92c7c-501">Windows Server Standard Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span data-ttu-id="92c7c-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Produit \_ DATACENTER \_ WS \_ Server \_ Core** (147)</span><span class="sxs-lookup"><span data-stu-id="92c7c-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT\_DATACENTER\_WS\_SERVER\_CORE** (147)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-503">Windows Server Datacenter Edition (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-503">Windows Server Datacenter Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span data-ttu-id="92c7c-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Produit \_ STANDARD \_ WS \_ Server \_ Core** (148)</span><span class="sxs-lookup"><span data-stu-id="92c7c-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT\_STANDARD\_WS\_SERVER\_CORE** (148)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-505">Windows Server Standard Edition (installation minimale)</span><span class="sxs-lookup"><span data-stu-id="92c7c-505">Windows Server Standard Edition (Server Core installation)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-506">**Organisation**</span><span class="sxs-lookup"><span data-stu-id="92c7c-506">**Organization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-507">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-508">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-508">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-509">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")</span><span class="sxs-lookup"><span data-stu-id="92c7c-509">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|RegisteredOrganization")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-510">Nom de la société pour l’utilisateur inscrit du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-510">Company name for the registered user of the operating system.</span></span>

<span data-ttu-id="92c7c-511">Exemple : « Microsoft Corporation »</span><span class="sxs-lookup"><span data-stu-id="92c7c-511">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-512">**OSArchitecture**</span><span class="sxs-lookup"><span data-stu-id="92c7c-512">**OSArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-513">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-513">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-514">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-515">Architecture du système d’exploitation, par opposition au processeur.</span><span class="sxs-lookup"><span data-stu-id="92c7c-515">Architecture of the operating system, as opposed to the processor.</span></span> <span data-ttu-id="92c7c-516">Cette propriété peut être localisée.</span><span class="sxs-lookup"><span data-stu-id="92c7c-516">This property can be localized.</span></span>

<span data-ttu-id="92c7c-517">Exemple : 32-bit</span><span class="sxs-lookup"><span data-stu-id="92c7c-517">Example: 32-bit</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-518">**OSLanguage**</span><span class="sxs-lookup"><span data-stu-id="92c7c-518">**OSLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-519">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-519">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-520">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-520">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-521">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| par défaut \\ \\ du panneau de configuration \\ \\ \| paramètres régionaux")</span><span class="sxs-lookup"><span data-stu-id="92c7c-521">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|DEFAULT\\\\Control Panel\\\\International\|Locale")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-522">Version linguistique du système d’exploitation installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-522">Language version of the operating system installed.</span></span> <span data-ttu-id="92c7c-523">La liste suivante répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="92c7c-523">The following list lists the possible values.</span></span> <span data-ttu-id="92c7c-524">Exemple : 0x0807 (allemand, Suisse).</span><span class="sxs-lookup"><span data-stu-id="92c7c-524">Example: 0x0807 (German, Switzerland).</span></span>

<dt>

<span data-ttu-id="92c7c-525">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-525">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-526">Arabe</span><span class="sxs-lookup"><span data-stu-id="92c7c-526">Arabic</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-527">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="92c7c-527">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-528">Chinois (simplifié) – Chine</span><span class="sxs-lookup"><span data-stu-id="92c7c-528">Chinese (Simplified)– China</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-529">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="92c7c-529">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-530">Anglais</span><span class="sxs-lookup"><span data-stu-id="92c7c-530">English</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-531">1025 (0x401)</span><span class="sxs-lookup"><span data-stu-id="92c7c-531">1025 (0x401)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-532">Arabe – Arabie saoudite</span><span class="sxs-lookup"><span data-stu-id="92c7c-532">Arabic – Saudi Arabia</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-533">1026 (0x402)</span><span class="sxs-lookup"><span data-stu-id="92c7c-533">1026 (0x402)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-534">Bulgare</span><span class="sxs-lookup"><span data-stu-id="92c7c-534">Bulgarian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-535">1027 (0x403)</span><span class="sxs-lookup"><span data-stu-id="92c7c-535">1027 (0x403)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-536">Catalan</span><span class="sxs-lookup"><span data-stu-id="92c7c-536">Catalan</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-537">1028 (0x404)</span><span class="sxs-lookup"><span data-stu-id="92c7c-537">1028 (0x404)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-538">Chinois (traditionnel) – Taïwan</span><span class="sxs-lookup"><span data-stu-id="92c7c-538">Chinese (Traditional) – Taiwan</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-539">1029 (0x405)</span><span class="sxs-lookup"><span data-stu-id="92c7c-539">1029 (0x405)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-540">Tchèque</span><span class="sxs-lookup"><span data-stu-id="92c7c-540">Czech</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-541">1030 (0x406)</span><span class="sxs-lookup"><span data-stu-id="92c7c-541">1030 (0x406)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-542">Danois</span><span class="sxs-lookup"><span data-stu-id="92c7c-542">Danish</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-543">1031 (0x407)</span><span class="sxs-lookup"><span data-stu-id="92c7c-543">1031 (0x407)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-544">Allemand – Allemagne</span><span class="sxs-lookup"><span data-stu-id="92c7c-544">German – Germany</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-545">1032 (0x408)</span><span class="sxs-lookup"><span data-stu-id="92c7c-545">1032 (0x408)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-546">Grec</span><span class="sxs-lookup"><span data-stu-id="92c7c-546">Greek</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-547">1033 (0x40C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-547">1033 (0x409)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-548">Anglais – États-Unis</span><span class="sxs-lookup"><span data-stu-id="92c7c-548">English – United States</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-549">1034 (0x40A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-549">1034 (0x40A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-550">Espagnol – tri traditionnel</span><span class="sxs-lookup"><span data-stu-id="92c7c-550">Spanish – Traditional Sort</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-551">1035 (0x40B)</span><span class="sxs-lookup"><span data-stu-id="92c7c-551">1035 (0x40B)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-552">Finnois</span><span class="sxs-lookup"><span data-stu-id="92c7c-552">Finnish</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-553">1036 (0x40C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-553">1036 (0x40C)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-554">Français – France</span><span class="sxs-lookup"><span data-stu-id="92c7c-554">French – France</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-555">1037 (0x40D)</span><span class="sxs-lookup"><span data-stu-id="92c7c-555">1037 (0x40D)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-556">Hébreu</span><span class="sxs-lookup"><span data-stu-id="92c7c-556">Hebrew</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-557">1038 (0x40E)</span><span class="sxs-lookup"><span data-stu-id="92c7c-557">1038 (0x40E)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-558">Hongrois</span><span class="sxs-lookup"><span data-stu-id="92c7c-558">Hungarian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-559">1039 (0x40F)</span><span class="sxs-lookup"><span data-stu-id="92c7c-559">1039 (0x40F)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-560">Islandais</span><span class="sxs-lookup"><span data-stu-id="92c7c-560">Icelandic</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-561">1040 (0x410)</span><span class="sxs-lookup"><span data-stu-id="92c7c-561">1040 (0x410)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-562">Italien – Italie</span><span class="sxs-lookup"><span data-stu-id="92c7c-562">Italian – Italy</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-563">1041 (0x411)</span><span class="sxs-lookup"><span data-stu-id="92c7c-563">1041 (0x411)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-564">Japonais</span><span class="sxs-lookup"><span data-stu-id="92c7c-564">Japanese</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-565">1042 (0x412)</span><span class="sxs-lookup"><span data-stu-id="92c7c-565">1042 (0x412)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-566">Coréen</span><span class="sxs-lookup"><span data-stu-id="92c7c-566">Korean</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-567">1043 (0x413)</span><span class="sxs-lookup"><span data-stu-id="92c7c-567">1043 (0x413)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-568">Néerlandais – Pays-Bas</span><span class="sxs-lookup"><span data-stu-id="92c7c-568">Dutch – Netherlands</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-569">1044 (0x414)</span><span class="sxs-lookup"><span data-stu-id="92c7c-569">1044 (0x414)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-570">Norvégien – bokmal</span><span class="sxs-lookup"><span data-stu-id="92c7c-570">Norwegian – Bokmal</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-571">1045 (0x415)</span><span class="sxs-lookup"><span data-stu-id="92c7c-571">1045 (0x415)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-572">Polonais</span><span class="sxs-lookup"><span data-stu-id="92c7c-572">Polish</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-573">1046 (0x416)</span><span class="sxs-lookup"><span data-stu-id="92c7c-573">1046 (0x416)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-574">Portugais – Brésil</span><span class="sxs-lookup"><span data-stu-id="92c7c-574">Portuguese – Brazil</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-575">1047 (0x417)</span><span class="sxs-lookup"><span data-stu-id="92c7c-575">1047 (0x417)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-576">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="92c7c-576">Rhaeto-Romanic</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-577">1048 (0x418)</span><span class="sxs-lookup"><span data-stu-id="92c7c-577">1048 (0x418)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-578">Roumain</span><span class="sxs-lookup"><span data-stu-id="92c7c-578">Romanian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-579">1049 (0x419)</span><span class="sxs-lookup"><span data-stu-id="92c7c-579">1049 (0x419)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-580">Russe</span><span class="sxs-lookup"><span data-stu-id="92c7c-580">Russian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-581">1050 (0x41A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-581">1050 (0x41A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-582">Croate</span><span class="sxs-lookup"><span data-stu-id="92c7c-582">Croatian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-583">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="92c7c-583">1051 (0x41B)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-584">Slovaque</span><span class="sxs-lookup"><span data-stu-id="92c7c-584">Slovak</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-585">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-585">1052 (0x41C)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-586">Albanais</span><span class="sxs-lookup"><span data-stu-id="92c7c-586">Albanian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-587">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="92c7c-587">1053 (0x41D)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-588">Suédois</span><span class="sxs-lookup"><span data-stu-id="92c7c-588">Swedish</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-589">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="92c7c-589">1054 (0x41E)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-590">Thaï</span><span class="sxs-lookup"><span data-stu-id="92c7c-590">Thai</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-591">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="92c7c-591">1055 (0x41F)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-592">Turc</span><span class="sxs-lookup"><span data-stu-id="92c7c-592">Turkish</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-593">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="92c7c-593">1056 (0x420)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-594">Ourdou</span><span class="sxs-lookup"><span data-stu-id="92c7c-594">Urdu</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-595">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="92c7c-595">1057 (0x421)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-596">Indonésien</span><span class="sxs-lookup"><span data-stu-id="92c7c-596">Indonesian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-597">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="92c7c-597">1058 (0x422)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-598">Ukrainien</span><span class="sxs-lookup"><span data-stu-id="92c7c-598">Ukrainian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-599">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="92c7c-599">1059 (0x423)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-600">Biélorusse</span><span class="sxs-lookup"><span data-stu-id="92c7c-600">Belarusian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-601">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="92c7c-601">1060 (0x424)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-602">Slovène</span><span class="sxs-lookup"><span data-stu-id="92c7c-602">Slovenian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-603">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="92c7c-603">1061 (0x425)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-604">Estonien</span><span class="sxs-lookup"><span data-stu-id="92c7c-604">Estonian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-605">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="92c7c-605">1062 (0x426)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-606">Letton</span><span class="sxs-lookup"><span data-stu-id="92c7c-606">Latvian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-607">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="92c7c-607">1063 (0x427)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-608">Lituanien</span><span class="sxs-lookup"><span data-stu-id="92c7c-608">Lithuanian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-609">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="92c7c-609">1065 (0x429)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-610">Persan</span><span class="sxs-lookup"><span data-stu-id="92c7c-610">Persian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-611">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-611">1066 (0x42A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-612">Vietnamien</span><span class="sxs-lookup"><span data-stu-id="92c7c-612">Vietnamese</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-613">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="92c7c-613">1069 (0x42D)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-614">Basque (Basque)</span><span class="sxs-lookup"><span data-stu-id="92c7c-614">Basque (Basque)</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-615">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="92c7c-615">1070 (0x42E)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-616">Serbe</span><span class="sxs-lookup"><span data-stu-id="92c7c-616">Serbian</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-617">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="92c7c-617">1071 (0x42F)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-618">Macédonien (Macédoine du Nord)</span><span class="sxs-lookup"><span data-stu-id="92c7c-618">Macedonian (North Macedonia)</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-619">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="92c7c-619">1072 (0x430)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-620">Sutu</span><span class="sxs-lookup"><span data-stu-id="92c7c-620">Sutu</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-621">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="92c7c-621">1073 (0x431)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-622">Tsonga</span><span class="sxs-lookup"><span data-stu-id="92c7c-622">Tsonga</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-623">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="92c7c-623">1074 (0x432)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-624">Tswana</span><span class="sxs-lookup"><span data-stu-id="92c7c-624">Tswana</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-625">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="92c7c-625">1076 (0x434)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-626">Xhosa</span><span class="sxs-lookup"><span data-stu-id="92c7c-626">Xhosa</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-627">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="92c7c-627">1077 (0x435)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-628">Zoulou</span><span class="sxs-lookup"><span data-stu-id="92c7c-628">Zulu</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-629">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="92c7c-629">1078 (0x436)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-630">Afrikaans</span><span class="sxs-lookup"><span data-stu-id="92c7c-630">Afrikaans</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-631">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="92c7c-631">1080 (0x438)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-632">Féroïen</span><span class="sxs-lookup"><span data-stu-id="92c7c-632">Faeroese</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-633">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="92c7c-633">1081 (0x439)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-634">Hindi</span><span class="sxs-lookup"><span data-stu-id="92c7c-634">Hindi</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-635">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-635">1082 (0x43A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-636">Maltais</span><span class="sxs-lookup"><span data-stu-id="92c7c-636">Maltese</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-637">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-637">1084 (0x43C)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-638">Gaélique écossais (Royaume-Uni)</span><span class="sxs-lookup"><span data-stu-id="92c7c-638">Scottish Gaelic (United Kingdom)</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-639">1085 (0x43D)</span><span class="sxs-lookup"><span data-stu-id="92c7c-639">1085 (0x43D)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-640">Yiddish</span><span class="sxs-lookup"><span data-stu-id="92c7c-640">Yiddish</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-641">1086 (0x43E)</span><span class="sxs-lookup"><span data-stu-id="92c7c-641">1086 (0x43E)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-642">Malais – Malaisie</span><span class="sxs-lookup"><span data-stu-id="92c7c-642">Malay – Malaysia</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-643">2049 (0x801)</span><span class="sxs-lookup"><span data-stu-id="92c7c-643">2049 (0x801)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-644">Arabe – Irak</span><span class="sxs-lookup"><span data-stu-id="92c7c-644">Arabic – Iraq</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-645">2052 (0x804)</span><span class="sxs-lookup"><span data-stu-id="92c7c-645">2052 (0x804)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-646">Chinois (simplifié) – RPC</span><span class="sxs-lookup"><span data-stu-id="92c7c-646">Chinese (Simplified) – PRC</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-647">2055 (0x807)</span><span class="sxs-lookup"><span data-stu-id="92c7c-647">2055 (0x807)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-648">Allemand – Suisse</span><span class="sxs-lookup"><span data-stu-id="92c7c-648">German – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-649">2057 (0x809)</span><span class="sxs-lookup"><span data-stu-id="92c7c-649">2057 (0x809)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-650">Anglais – Royaume-Uni</span><span class="sxs-lookup"><span data-stu-id="92c7c-650">English – United Kingdom</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-651">2058 (0x80A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-651">2058 (0x80A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-652">Espagnol – Mexique</span><span class="sxs-lookup"><span data-stu-id="92c7c-652">Spanish – Mexico</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-653">2060 (0x80C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-653">2060 (0x80C)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-654">Français – Belgique</span><span class="sxs-lookup"><span data-stu-id="92c7c-654">French – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-655">2064 (0x810)</span><span class="sxs-lookup"><span data-stu-id="92c7c-655">2064 (0x810)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-656">Italien – Suisse</span><span class="sxs-lookup"><span data-stu-id="92c7c-656">Italian – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-657">2067 (0x813)</span><span class="sxs-lookup"><span data-stu-id="92c7c-657">2067 (0x813)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-658">Néerlandais – Belgique</span><span class="sxs-lookup"><span data-stu-id="92c7c-658">Dutch – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-659">2068 (0x814)</span><span class="sxs-lookup"><span data-stu-id="92c7c-659">2068 (0x814)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-660">Norvégien – nynorsk</span><span class="sxs-lookup"><span data-stu-id="92c7c-660">Norwegian – Nynorsk</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-661">2070 (0x816)</span><span class="sxs-lookup"><span data-stu-id="92c7c-661">2070 (0x816)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-662">Portugais – Portugal</span><span class="sxs-lookup"><span data-stu-id="92c7c-662">Portuguese – Portugal</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-663">2072 (0x818)</span><span class="sxs-lookup"><span data-stu-id="92c7c-663">2072 (0x818)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-664">Roumain – Moldavie</span><span class="sxs-lookup"><span data-stu-id="92c7c-664">Romanian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-665">2073 (0x819)</span><span class="sxs-lookup"><span data-stu-id="92c7c-665">2073 (0x819)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-666">Russe – Moldavie</span><span class="sxs-lookup"><span data-stu-id="92c7c-666">Russian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-667">2074 (0x81A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-667">2074 (0x81A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-668">Serbe – latin</span><span class="sxs-lookup"><span data-stu-id="92c7c-668">Serbian – Latin</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-669">2077 (0x81D)</span><span class="sxs-lookup"><span data-stu-id="92c7c-669">2077 (0x81D)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-670">Suédois – Finlande</span><span class="sxs-lookup"><span data-stu-id="92c7c-670">Swedish – Finland</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-671">3073 (0xC01)</span><span class="sxs-lookup"><span data-stu-id="92c7c-671">3073 (0xC01)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-672">Arabe – Égypte</span><span class="sxs-lookup"><span data-stu-id="92c7c-672">Arabic – Egypt</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-673">3076 (0xC04)</span><span class="sxs-lookup"><span data-stu-id="92c7c-673">3076 (0xC04)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-674">Chinois (traditionnel) – Hong Kong (R.A.S.)</span><span class="sxs-lookup"><span data-stu-id="92c7c-674">Chinese (Traditional) – Hong Kong SAR</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-675">3079 (0xC07)</span><span class="sxs-lookup"><span data-stu-id="92c7c-675">3079 (0xC07)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-676">Allemand – Autriche</span><span class="sxs-lookup"><span data-stu-id="92c7c-676">German – Austria</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-677">3081 (0xC09)</span><span class="sxs-lookup"><span data-stu-id="92c7c-677">3081 (0xC09)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-678">Anglais – Australie</span><span class="sxs-lookup"><span data-stu-id="92c7c-678">English – Australia</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-679">3082 (0xC0A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-679">3082 (0xC0A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-680">Espagnol – international</span><span class="sxs-lookup"><span data-stu-id="92c7c-680">Spanish – International Sort</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-681">3084 (0xC0C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-681">3084 (0xC0C)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-682">Français – Canada</span><span class="sxs-lookup"><span data-stu-id="92c7c-682">French – Canada</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-683">3098 (0xC1A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-683">3098 (0xC1A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-684">Serbe – cyrillique</span><span class="sxs-lookup"><span data-stu-id="92c7c-684">Serbian – Cyrillic</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-685">4097 (0x1001)</span><span class="sxs-lookup"><span data-stu-id="92c7c-685">4097 (0x1001)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-686">Arabe – Libye</span><span class="sxs-lookup"><span data-stu-id="92c7c-686">Arabic – Libya</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-687">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="92c7c-687">4100 (0x1004)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-688">Chinois (simplifié) – Singapour</span><span class="sxs-lookup"><span data-stu-id="92c7c-688">Chinese (Simplified) – Singapore</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-689">4103 (0x1007)</span><span class="sxs-lookup"><span data-stu-id="92c7c-689">4103 (0x1007)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-690">Allemand – Luxembourg</span><span class="sxs-lookup"><span data-stu-id="92c7c-690">German – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-691">4105 (0x1009)</span><span class="sxs-lookup"><span data-stu-id="92c7c-691">4105 (0x1009)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-692">Anglais – Canada</span><span class="sxs-lookup"><span data-stu-id="92c7c-692">English – Canada</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-693">4106 (0x100A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-693">4106 (0x100A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-694">Espagnol – Guatemala</span><span class="sxs-lookup"><span data-stu-id="92c7c-694">Spanish – Guatemala</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-695">4108 (0x100C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-695">4108 (0x100C)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-696">Français-Suisse</span><span class="sxs-lookup"><span data-stu-id="92c7c-696">French – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-697">5121 (0x1401)</span><span class="sxs-lookup"><span data-stu-id="92c7c-697">5121 (0x1401)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-698">Arabe – Algérie</span><span class="sxs-lookup"><span data-stu-id="92c7c-698">Arabic – Algeria</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-699">5127 (0x1407)</span><span class="sxs-lookup"><span data-stu-id="92c7c-699">5127 (0x1407)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-700">Allemand – Liechtenstein</span><span class="sxs-lookup"><span data-stu-id="92c7c-700">German – Liechtenstein</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-701">5129 (0x1409)</span><span class="sxs-lookup"><span data-stu-id="92c7c-701">5129 (0x1409)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-702">Anglais-Nouvelle-Zélande</span><span class="sxs-lookup"><span data-stu-id="92c7c-702">English – New Zealand</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-703">5130 (0x140A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-703">5130 (0x140A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-704">Espagnol – Costa Rica</span><span class="sxs-lookup"><span data-stu-id="92c7c-704">Spanish – Costa Rica</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-705">5132 (0x140C)</span><span class="sxs-lookup"><span data-stu-id="92c7c-705">5132 (0x140C)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-706">Français – Luxembourg</span><span class="sxs-lookup"><span data-stu-id="92c7c-706">French – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-707">6145 (0x1801)</span><span class="sxs-lookup"><span data-stu-id="92c7c-707">6145 (0x1801)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-708">Arabe – Maroc</span><span class="sxs-lookup"><span data-stu-id="92c7c-708">Arabic – Morocco</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-709">6153 (0x1809)</span><span class="sxs-lookup"><span data-stu-id="92c7c-709">6153 (0x1809)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-710">Anglais – Irlande</span><span class="sxs-lookup"><span data-stu-id="92c7c-710">English – Ireland</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-711">6154 (0x180A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-711">6154 (0x180A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-712">Espagnol – Panama</span><span class="sxs-lookup"><span data-stu-id="92c7c-712">Spanish – Panama</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-713">7169 (0x1C01)</span><span class="sxs-lookup"><span data-stu-id="92c7c-713">7169 (0x1C01)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-714">Arabe – Tunisie</span><span class="sxs-lookup"><span data-stu-id="92c7c-714">Arabic – Tunisia</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-715">7177 (0x1C09)</span><span class="sxs-lookup"><span data-stu-id="92c7c-715">7177 (0x1C09)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-716">Anglais – Afrique du Sud</span><span class="sxs-lookup"><span data-stu-id="92c7c-716">English – South Africa</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-717">7178 (0x1C0A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-717">7178 (0x1C0A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-718">Espagnol – République dominicaine</span><span class="sxs-lookup"><span data-stu-id="92c7c-718">Spanish – Dominican Republic</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-719">8193 (0x2001)</span><span class="sxs-lookup"><span data-stu-id="92c7c-719">8193 (0x2001)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-720">Arabe – Oman</span><span class="sxs-lookup"><span data-stu-id="92c7c-720">Arabic – Oman</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-721">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="92c7c-721">8201 (0x2009)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-722">Anglais – Jamaïque</span><span class="sxs-lookup"><span data-stu-id="92c7c-722">English – Jamaica</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-723">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-723">8202 (0x200A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-724">Espagnol – Venezuela</span><span class="sxs-lookup"><span data-stu-id="92c7c-724">Spanish – Venezuela</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-725">9217 (0x2401)</span><span class="sxs-lookup"><span data-stu-id="92c7c-725">9217 (0x2401)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-726">Arabe – Yémen</span><span class="sxs-lookup"><span data-stu-id="92c7c-726">Arabic – Yemen</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-727">9226 (0x240A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-727">9226 (0x240A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-728">Espagnol – Colombie</span><span class="sxs-lookup"><span data-stu-id="92c7c-728">Spanish – Colombia</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-729">10241 (0x2801)</span><span class="sxs-lookup"><span data-stu-id="92c7c-729">10241 (0x2801)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-730">Arabe – Syrie</span><span class="sxs-lookup"><span data-stu-id="92c7c-730">Arabic – Syria</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-731">10249 (0x2809)</span><span class="sxs-lookup"><span data-stu-id="92c7c-731">10249 (0x2809)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-732">Anglais – Belize</span><span class="sxs-lookup"><span data-stu-id="92c7c-732">English – Belize</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-733">10250 (0x280A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-733">10250 (0x280A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-734">Espagnol – Pérou</span><span class="sxs-lookup"><span data-stu-id="92c7c-734">Spanish – Peru</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-735">11265 (0x2C01)</span><span class="sxs-lookup"><span data-stu-id="92c7c-735">11265 (0x2C01)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-736">Arabe – Jordanie</span><span class="sxs-lookup"><span data-stu-id="92c7c-736">Arabic – Jordan</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-737">11273 (0x2C09)</span><span class="sxs-lookup"><span data-stu-id="92c7c-737">11273 (0x2C09)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-738">Anglais – Trinidad</span><span class="sxs-lookup"><span data-stu-id="92c7c-738">English – Trinidad</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-739">11274 (0x2C0A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-739">11274 (0x2C0A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-740">Espagnol – Argentine</span><span class="sxs-lookup"><span data-stu-id="92c7c-740">Spanish – Argentina</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-741">12289 (0x3001)</span><span class="sxs-lookup"><span data-stu-id="92c7c-741">12289 (0x3001)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-742">Arabe – Liban</span><span class="sxs-lookup"><span data-stu-id="92c7c-742">Arabic – Lebanon</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-743">12298 (0x300A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-743">12298 (0x300A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-744">Espagnol – Équateur</span><span class="sxs-lookup"><span data-stu-id="92c7c-744">Spanish – Ecuador</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-745">13313 (0x3401)</span><span class="sxs-lookup"><span data-stu-id="92c7c-745">13313 (0x3401)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-746">Arabe – Koweït</span><span class="sxs-lookup"><span data-stu-id="92c7c-746">Arabic – Kuwait</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-747">13322 (0x340A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-747">13322 (0x340A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-748">Espagnol – Chili</span><span class="sxs-lookup"><span data-stu-id="92c7c-748">Spanish – Chile</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-749">14337 (0x3801)</span><span class="sxs-lookup"><span data-stu-id="92c7c-749">14337 (0x3801)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-750">Arabe – E.A.U.</span><span class="sxs-lookup"><span data-stu-id="92c7c-750">Arabic – U.A.E.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-751">14346 (0x380A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-751">14346 (0x380A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-752">Espagnol – Uruguay</span><span class="sxs-lookup"><span data-stu-id="92c7c-752">Spanish – Uruguay</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-753">15361 (0x3C01)</span><span class="sxs-lookup"><span data-stu-id="92c7c-753">15361 (0x3C01)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-754">Arabe – Bahreïn</span><span class="sxs-lookup"><span data-stu-id="92c7c-754">Arabic – Bahrain</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-755">15370 (0x3C0A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-755">15370 (0x3C0A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-756">Espagnol – Paraguay</span><span class="sxs-lookup"><span data-stu-id="92c7c-756">Spanish – Paraguay</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-757">16385 (0x4001)</span><span class="sxs-lookup"><span data-stu-id="92c7c-757">16385 (0x4001)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-758">Arabe – Qatar</span><span class="sxs-lookup"><span data-stu-id="92c7c-758">Arabic – Qatar</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-759">16394 (0x400A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-759">16394 (0x400A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-760">Espagnol – Bolivie</span><span class="sxs-lookup"><span data-stu-id="92c7c-760">Spanish – Bolivia</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-761">17418 (0x440A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-761">17418 (0x440A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-762">Espagnol – El Salvador</span><span class="sxs-lookup"><span data-stu-id="92c7c-762">Spanish – El Salvador</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-763">18442 (0x480A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-763">18442 (0x480A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-764">Espagnol – Honduras</span><span class="sxs-lookup"><span data-stu-id="92c7c-764">Spanish – Honduras</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-765">19466 (0x4C0A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-765">19466 (0x4C0A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-766">Espagnol – Nicaragua</span><span class="sxs-lookup"><span data-stu-id="92c7c-766">Spanish – Nicaragua</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-767">20490 (0x500A)</span><span class="sxs-lookup"><span data-stu-id="92c7c-767">20490 (0x500A)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-768">Espagnol – Porto Rico</span><span class="sxs-lookup"><span data-stu-id="92c7c-768">Spanish – Puerto Rico</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-769">**OSProductSuite**</span><span class="sxs-lookup"><span data-stu-id="92c7c-769">**OSProductSuite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-770">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-770">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-771">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-771">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-772">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ ProductOptions \| ProductSuite »), [**bitvalues**](../wmisdk/standard-qualifiers.md) (« Small Business », « Enterprise », « BackOffice », « communication Server », « Terminal Server », « Small Business (Restricted) », « Embedded NT », « Data Center »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-772">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\ProductOptions\|ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-773">Des compléments de produits système installés et sous licence au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-773">Installed and licensed system product additions to the operating system.</span></span> <span data-ttu-id="92c7c-774">Par exemple, la valeur de 146 (0x92) pour **OSProductSuite** indique Enterprise, Terminal Services et Data Center (bits 1, quatre et sept Set).</span><span class="sxs-lookup"><span data-stu-id="92c7c-774">For example, the value of 146 (0x92) for **OSProductSuite** indicates Enterprise, Terminal Services, and Data Center (bits one, four, and seven set).</span></span> <span data-ttu-id="92c7c-775">La liste suivante répertorie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="92c7c-775">The following list lists possible values.</span></span>

<dt>

<span data-ttu-id="92c7c-776">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-776">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-777">Microsoft Small Business Server a été installé, mais il a peut-être été mis à niveau vers une autre version de Windows.</span><span class="sxs-lookup"><span data-stu-id="92c7c-777">Microsoft Small Business Server was once installed, but may have been upgraded to another version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-778">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-778">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-779">Windows Server 2008 Enterprise est installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-779">Windows Server 2008 Enterprise is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-780">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="92c7c-780">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-781">Les composants Windows BackOffice sont installés.</span><span class="sxs-lookup"><span data-stu-id="92c7c-781">Windows BackOffice components are installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-782">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="92c7c-782">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-783">Communication Server est installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-783">Communication Server is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-784">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="92c7c-784">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-785">Les services Terminal Server sont installés.</span><span class="sxs-lookup"><span data-stu-id="92c7c-785">Terminal Services is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-786">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="92c7c-786">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-787">Microsoft Small Business Server est installé avec la licence client restrictive.</span><span class="sxs-lookup"><span data-stu-id="92c7c-787">Microsoft Small Business Server is installed with the restrictive client license.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-788">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="92c7c-788">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-789">Windows Embedded est installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-789">Windows Embedded is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-790">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="92c7c-790">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-791">Une édition Datacenter est installée.</span><span class="sxs-lookup"><span data-stu-id="92c7c-791">A Datacenter edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-792">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="92c7c-792">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-793">Les services Terminal Server sont installés, mais une seule session interactive est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="92c7c-793">Terminal Services is installed, but only one interactive session is supported.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-794">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="92c7c-794">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-795">Windows Édition personnelle est installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-795">Windows Home Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-796">1024 (0x400)</span><span class="sxs-lookup"><span data-stu-id="92c7c-796">1024 (0x400)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-797">L’édition Web Server est installée.</span><span class="sxs-lookup"><span data-stu-id="92c7c-797">Web Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-798">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="92c7c-798">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-799">L’édition Storage Server est installée.</span><span class="sxs-lookup"><span data-stu-id="92c7c-799">Storage Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-800">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="92c7c-800">16384 (0x4000)</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-801">Compute Cluster Edition est installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-801">Compute Cluster Edition is installed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-802">**OSType**</span><span class="sxs-lookup"><span data-stu-id="92c7c-802">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-803">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c7c-803">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-804">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-804">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-805">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="92c7c-805">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-806">Type de système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-806">Type of operating system.</span></span> <span data-ttu-id="92c7c-807">La liste suivante identifie les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="92c7c-807">The following list identifies the possible values.</span></span>

<span data-ttu-id="92c7c-808">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-808">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92c7c-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="92c7c-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="92c7c-811"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-812">MACROS</span><span class="sxs-lookup"><span data-stu-id="92c7c-812">MACROS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="92c7c-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="92c7c-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="92c7c-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="92c7c-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="92c7c-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="92c7c-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="92c7c-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX numérique** (6)</span><span class="sxs-lookup"><span data-stu-id="92c7c-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="92c7c-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="92c7c-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="92c7c-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="92c7c-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="92c7c-819"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="92c7c-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="92c7c-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="92c7c-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="92c7c-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="92c7c-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="92c7c-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span><span class="sxs-lookup"><span data-stu-id="92c7c-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="92c7c-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="92c7c-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="92c7c-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="92c7c-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="92c7c-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="92c7c-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="92c7c-826"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="92c7c-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="92c7c-827"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="92c7c-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="92c7c-828"><span id="WINNT"></span><span id="winnt"></span>**Winnt** (18)</span><span class="sxs-lookup"><span data-stu-id="92c7c-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="92c7c-829"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="92c7c-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="92c7c-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="92c7c-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="92c7c-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="92c7c-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="92c7c-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="92c7c-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="92c7c-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="92c7c-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="92c7c-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Dépendant d’UNIX** (24)</span><span class="sxs-lookup"><span data-stu-id="92c7c-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="92c7c-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="92c7c-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="92c7c-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="92c7c-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="92c7c-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="92c7c-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="92c7c-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="92c7c-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="92c7c-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="92c7c-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd>

<span data-ttu-id="92c7c-840">Solaris</span><span class="sxs-lookup"><span data-stu-id="92c7c-840">Solaris</span></span>

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="92c7c-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="92c7c-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="92c7c-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="92c7c-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="92c7c-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="92c7c-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="92c7c-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="92c7c-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="92c7c-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="92c7c-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="92c7c-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="92c7c-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="92c7c-847"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="92c7c-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="92c7c-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="92c7c-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="92c7c-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="92c7c-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="92c7c-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**Machine virtuelle/SEEE** (39)</span><span class="sxs-lookup"><span data-stu-id="92c7c-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="92c7c-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interactif** (40)</span><span class="sxs-lookup"><span data-stu-id="92c7c-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="92c7c-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="92c7c-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="92c7c-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="92c7c-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="92c7c-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="92c7c-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="92c7c-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**Hurd gnu** (44)</span><span class="sxs-lookup"><span data-stu-id="92c7c-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="92c7c-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="92c7c-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="92c7c-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Noyau Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="92c7c-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="92c7c-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="92c7c-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="92c7c-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="92c7c-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="92c7c-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="92c7c-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="92c7c-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="92c7c-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="92c7c-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="92c7c-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="92c7c-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menthe** (52)</span><span class="sxs-lookup"><span data-stu-id="92c7c-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="92c7c-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="92c7c-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="92c7c-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="92c7c-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="92c7c-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="92c7c-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="92c7c-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="92c7c-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="92c7c-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="92c7c-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="92c7c-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="92c7c-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="92c7c-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dédié** (59)</span><span class="sxs-lookup"><span data-stu-id="92c7c-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="92c7c-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span><span class="sxs-lookup"><span data-stu-id="92c7c-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="92c7c-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="92c7c-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="92c7c-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="92c7c-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-874">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="92c7c-874">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-875">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-875">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-876">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-876">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-877">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="92c7c-877">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-878">Description supplémentaire pour la version actuelle du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-878">Additional description for the current operating system version.</span></span>

<span data-ttu-id="92c7c-879">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-879">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-880">**PAEEnabled**</span><span class="sxs-lookup"><span data-stu-id="92c7c-880">**PAEEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-881">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-881">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-882">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-882">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-883">Si la **valeur est true**, les extensions d’adresse physique (PAE) sont activées par le système d’exploitation qui s’exécute sur les processeurs Intel.</span><span class="sxs-lookup"><span data-stu-id="92c7c-883">If **True**, the physical address extensions (PAE) are enabled by the operating system running on Intel processors.</span></span> <span data-ttu-id="92c7c-884">PAE permet aux applications d’adresser plus de 4 Go de mémoire physique.</span><span class="sxs-lookup"><span data-stu-id="92c7c-884">PAE allows applications to address more than 4 GB of physical memory.</span></span> <span data-ttu-id="92c7c-885">Lorsque PAE est activé, le système d’exploitation utilise la traduction d’adresses linéaires à trois niveaux plutôt que deux niveaux.</span><span class="sxs-lookup"><span data-stu-id="92c7c-885">When PAE is enabled, the operating system uses three-level linear address translation rather than two-level.</span></span> <span data-ttu-id="92c7c-886">Le fait de fournir plus de mémoire physique à une application réduit la nécessité d’échanger la mémoire dans le fichier d’échange et d’augmenter les performances.</span><span class="sxs-lookup"><span data-stu-id="92c7c-886">Providing more physical memory to an application reduces the need to swap memory to the page file and increases performance.</span></span> <span data-ttu-id="92c7c-887">Pour activer, PAE, utilisez le commutateur « /PAE » dans le fichier Boot.ini.</span><span class="sxs-lookup"><span data-stu-id="92c7c-887">To enable, PAE, use the "/PAE" switch in the Boot.ini file.</span></span> <span data-ttu-id="92c7c-888">Pour plus d’informations sur la fonctionnalité d’extension d’adresse physique, consultez <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .</span><span class="sxs-lookup"><span data-stu-id="92c7c-888">For more information about the Physical Address Extension feature, see <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912>.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-889">**PlusProductID**</span><span class="sxs-lookup"><span data-stu-id="92c7c-889">**PlusProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-890">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-890">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-891">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-891">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-892">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion plus \| !</span><span class="sxs-lookup"><span data-stu-id="92c7c-892">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="92c7c-893">ProductId»)</span><span class="sxs-lookup"><span data-stu-id="92c7c-893">ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-894">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="92c7c-894">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-895">**PlusVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="92c7c-895">**PlusVersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-896">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-896">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-897">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-897">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-898">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion plus \| !</span><span class="sxs-lookup"><span data-stu-id="92c7c-898">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="92c7c-899">VersionNumber»)</span><span class="sxs-lookup"><span data-stu-id="92c7c-899">VersionNumber")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-900">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="92c7c-900">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-901">**PortableOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="92c7c-901">**PortableOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-902">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-902">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-903">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-903">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-904">Spécifie si le système d’exploitation est démarré à partir d’un périphérique USB externe.</span><span class="sxs-lookup"><span data-stu-id="92c7c-904">Specifies whether the operating system booted from an external USB device.</span></span> <span data-ttu-id="92c7c-905">Si la valeur est true, le système d’exploitation a détecté qu’il démarre sur un dispositif de stockage connecté localement et pris en charge.</span><span class="sxs-lookup"><span data-stu-id="92c7c-905">If true, the operating system has detected it is booting on a supported locally connected storage device.</span></span>

<span data-ttu-id="92c7c-906">**Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="92c7c-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-907">**Primaire**</span><span class="sxs-lookup"><span data-stu-id="92c7c-907">**Primary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-908">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="92c7c-908">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-909">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-909">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-910">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-910">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-911">Spécifie s’il s’agit du système d’exploitation principal.</span><span class="sxs-lookup"><span data-stu-id="92c7c-911">Specifies whether this is the primary operating system.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-912">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="92c7c-912">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-913">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-913">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-914">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-914">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-915">Informations système supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="92c7c-915">Additional system information.</span></span>

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

<span data-ttu-id="92c7c-916">**Poste de travail** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-916">**Work Station** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

<span data-ttu-id="92c7c-917">**Contrôleur de domaine** (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-917">**Domain Controller** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="92c7c-918">**Serveur** (3)</span><span class="sxs-lookup"><span data-stu-id="92c7c-918">**Server** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-919">**QuantumLength**</span><span class="sxs-lookup"><span data-stu-id="92c7c-919">**QuantumLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-920">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="92c7c-920">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-921">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="92c7c-921">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-922">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="92c7c-922">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-923">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="92c7c-923">Not supported</span></span>

<span data-ttu-id="92c7c-924">\* \* Windows Server 2008 et Windows Vista : \* \*</span><span class="sxs-lookup"><span data-stu-id="92c7c-924">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="92c7c-925">La propriété **QuantumLength** définit le nombre de battements d’horloge par Quantum.</span><span class="sxs-lookup"><span data-stu-id="92c7c-925">The **QuantumLength** property defines the number of clock ticks per quantum.</span></span> <span data-ttu-id="92c7c-926">Un Quantum est une unité de durée d’exécution que le planificateur est autorisé à fournir à une application avant de basculer vers d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="92c7c-926">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to other applications.</span></span> <span data-ttu-id="92c7c-927">Lorsqu’un thread exécute un Quantum, le noyau le prépasse et le déplace à la fin d’une file d’attente pour les applications avec des priorités identiques.</span><span class="sxs-lookup"><span data-stu-id="92c7c-927">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="92c7c-928">La longueur réelle du quantum d’un thread varie selon les plateformes Windows.</span><span class="sxs-lookup"><span data-stu-id="92c7c-928">The actual length of a thread's quantum varies across different Windows platforms.</span></span> <span data-ttu-id="92c7c-929">Pour Windows NT/Windows 2000 uniquement.</span><span class="sxs-lookup"><span data-stu-id="92c7c-929">For Windows NT/Windows 2000 only.</span></span>

<span data-ttu-id="92c7c-930">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="92c7c-930">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92c7c-931">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-931">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

<span data-ttu-id="92c7c-932">**Un battement** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-932">**One tick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

<span data-ttu-id="92c7c-933">**Deux graduations** (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-933">**Two ticks** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-934">**QuantumType**</span><span class="sxs-lookup"><span data-stu-id="92c7c-934">**QuantumType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-935">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="92c7c-935">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-936">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="92c7c-936">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-937">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="92c7c-937">Not supported</span></span>

<span data-ttu-id="92c7c-938">\* \* Windows Server 2008 et Windows Vista : \* \*</span><span class="sxs-lookup"><span data-stu-id="92c7c-938">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="92c7c-939">La propriété **QuantumType** spécifie des quantums de longueur fixe ou variable.</span><span class="sxs-lookup"><span data-stu-id="92c7c-939">The **QuantumType** property specifies either fixed or variable length quantums.</span></span> <span data-ttu-id="92c7c-940">Windows utilise par défaut des quantums de longueur variable, où l’application de premier plan a un Quantum plus long que les applications en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="92c7c-940">Windows defaults to variable length quantums where the foreground application has a longer quantum than the background applications.</span></span> <span data-ttu-id="92c7c-941">Windows Server passe par défaut à des quantums de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="92c7c-941">Windows Server defaults to fixed-length quantums.</span></span> <span data-ttu-id="92c7c-942">Un Quantum est une unité de durée d’exécution que le planificateur est autorisé à fournir à une application avant de passer à une autre application.</span><span class="sxs-lookup"><span data-stu-id="92c7c-942">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to another application.</span></span> <span data-ttu-id="92c7c-943">Lorsqu’un thread exécute un Quantum, le noyau le prépasse et le déplace à la fin d’une file d’attente pour les applications avec des priorités identiques.</span><span class="sxs-lookup"><span data-stu-id="92c7c-943">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="92c7c-944">La longueur réelle du quantum d’un thread varie selon les plateformes Windows.</span><span class="sxs-lookup"><span data-stu-id="92c7c-944">The actual length of a thread's quantum varies across different Windows platforms.</span></span>

<span data-ttu-id="92c7c-945">Les valeurs possibles sont.</span><span class="sxs-lookup"><span data-stu-id="92c7c-945">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92c7c-946">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="92c7c-946">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="92c7c-947">**Fixe** (1)</span><span class="sxs-lookup"><span data-stu-id="92c7c-947">**Fixed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

<span data-ttu-id="92c7c-948">**Variable** (2)</span><span class="sxs-lookup"><span data-stu-id="92c7c-948">**Variable** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-949">**Inscrit**</span><span class="sxs-lookup"><span data-stu-id="92c7c-949">**RegisteredUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-950">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-950">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-951">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-952">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")</span><span class="sxs-lookup"><span data-stu-id="92c7c-952">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|RegisteredOwner")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-953">Nom de l’utilisateur inscrit du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-953">Name of the registered user of the operating system.</span></span>

<span data-ttu-id="92c7c-954">Exemple : « Ben Smith »</span><span class="sxs-lookup"><span data-stu-id="92c7c-954">Example: "Ben Smith"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-955">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="92c7c-955">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-956">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-956">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-957">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-958">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="92c7c-958">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-959">Numéro d’identification de série du produit de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-959">Operating system product serial identification number.</span></span>

<span data-ttu-id="92c7c-960">Exemple : « 10497-OEM-0031416-71674 »</span><span class="sxs-lookup"><span data-stu-id="92c7c-960">Example: "10497-OEM-0031416-71674"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-961">**ServicePackMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="92c7c-961">**ServicePackMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-962">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c7c-962">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-963">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-963">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-964">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")</span><span class="sxs-lookup"><span data-stu-id="92c7c-964">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMajor**")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-965">Numéro de version principale du Service Pack installé sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="92c7c-965">Major version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="92c7c-966">Si aucun Service Pack n’a été installé, la valeur est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="92c7c-966">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-967">**ServicePackMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="92c7c-967">**ServicePackMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-968">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="92c7c-968">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-969">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-969">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-970">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")</span><span class="sxs-lookup"><span data-stu-id="92c7c-970">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMinor**")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-971">Numéro de version mineure du Service Pack installé sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="92c7c-971">Minor version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="92c7c-972">Si aucun Service Pack n’a été installé, la valeur est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="92c7c-972">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-973">**SizeStoredInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="92c7c-973">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-974">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-974">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-975">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-975">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-976">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Paramètres de mémoire système DMTF \| 001,3»), [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-976">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-977">Nombre total de kilo-octets pouvant être stockés dans les fichiers de pagination du système d’exploitation : 0 (zéro) indique qu’il n’y a aucun fichier de pagination.</span><span class="sxs-lookup"><span data-stu-id="92c7c-977">Total number of kilobytes that can be stored in the operating system paging files—0 (zero) indicates that there are no paging files.</span></span> <span data-ttu-id="92c7c-978">N’oubliez pas que ce nombre ne représente pas la taille physique réelle du fichier d’échange sur le disque.</span><span class="sxs-lookup"><span data-stu-id="92c7c-978">Be aware that this number does not represent the actual physical size of the paging file on disk.</span></span>

<span data-ttu-id="92c7c-979">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-979">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-980">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-980">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-981">**État**</span><span class="sxs-lookup"><span data-stu-id="92c7c-981">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-982">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-982">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-983">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-983">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-984">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="92c7c-984">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-985">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="92c7c-985">Current status of the object.</span></span> <span data-ttu-id="92c7c-986">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="92c7c-986">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="92c7c-987">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent peut fonctionner correctement, mais prédit une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="92c7c-987">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="92c7c-988">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="92c7c-988">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="92c7c-989">L’état du service s’applique aux tâches administratives, telles que la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="92c7c-989">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="92c7c-990">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="92c7c-990">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="92c7c-991">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-991">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="92c7c-992">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-992">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="92c7c-993">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-993">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="92c7c-994">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-994">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="92c7c-995">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="92c7c-995">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="92c7c-996">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-996">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="92c7c-997">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-997">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="92c7c-998">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-998">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="92c7c-999">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-999">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="92c7c-1000">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1000">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="92c7c-1001">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1001">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="92c7c-1002">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1002">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="92c7c-1003">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1003">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-1004">**SuiteMask**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1004">**SuiteMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1005">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1005">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1006">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1006">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1007">Qualificateurs : [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), deux- [**TValue**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition», « Windows Server, BackOffice Edition », « Windows Server, Communications Edition », « Microsoft Terminal Services », « Windows Server, Small Business Edition Restricted », « Windows Embedded », « Windows Server, Datacenter Edition », « Single User », « Windows Édition personnelle », « Windows Server, Web Edition »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1007">Qualifiers: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1008">Indicateurs de bits qui identifient les suites de produits disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1008">Bit flags that identify the product suites available on the system.</span></span>

<span data-ttu-id="92c7c-1009">Par exemple, pour spécifier Personal et BackOffice, définissez **SuiteMask** sur `4 | 512` ou `516` .</span><span class="sxs-lookup"><span data-stu-id="92c7c-1009">For example, to specify both Personal and BackOffice, set **SuiteMask** to `4 | 512` or `516`.</span></span>

<dt>

<span data-ttu-id="92c7c-1010">1</span><span class="sxs-lookup"><span data-stu-id="92c7c-1010">1</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1011">Small Business</span><span class="sxs-lookup"><span data-stu-id="92c7c-1011">Small Business</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1012">2</span><span class="sxs-lookup"><span data-stu-id="92c7c-1012">2</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1013">Enterprise</span><span class="sxs-lookup"><span data-stu-id="92c7c-1013">Enterprise</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1014">4</span><span class="sxs-lookup"><span data-stu-id="92c7c-1014">4</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1015">BackOffice</span><span class="sxs-lookup"><span data-stu-id="92c7c-1015">BackOffice</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1016">8</span><span class="sxs-lookup"><span data-stu-id="92c7c-1016">8</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1017">Communications</span><span class="sxs-lookup"><span data-stu-id="92c7c-1017">Communications</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1018">16</span><span class="sxs-lookup"><span data-stu-id="92c7c-1018">16</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1019">Terminal Services</span><span class="sxs-lookup"><span data-stu-id="92c7c-1019">Terminal Services</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1020">32</span><span class="sxs-lookup"><span data-stu-id="92c7c-1020">32</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1021">Restreint aux petites entreprises</span><span class="sxs-lookup"><span data-stu-id="92c7c-1021">Small Business Restricted</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1022">64</span><span class="sxs-lookup"><span data-stu-id="92c7c-1022">64</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1023">Édition intégrée</span><span class="sxs-lookup"><span data-stu-id="92c7c-1023">Embedded Edition</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1024">128</span><span class="sxs-lookup"><span data-stu-id="92c7c-1024">128</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1025">Édition Datacenter</span><span class="sxs-lookup"><span data-stu-id="92c7c-1025">Datacenter Edition</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1026">256</span><span class="sxs-lookup"><span data-stu-id="92c7c-1026">256</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1027">Utilisateur unique</span><span class="sxs-lookup"><span data-stu-id="92c7c-1027">Single User</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1028">512</span><span class="sxs-lookup"><span data-stu-id="92c7c-1028">512</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1029">Édition personnelle</span><span class="sxs-lookup"><span data-stu-id="92c7c-1029">Home Edition</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1030">1 024</span><span class="sxs-lookup"><span data-stu-id="92c7c-1030">1024</span></span>
</dt> <dd>

<span data-ttu-id="92c7c-1031">Édition Web Server</span><span class="sxs-lookup"><span data-stu-id="92c7c-1031">Web Server Edition</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="92c7c-1032">**SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1032">**SystemDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1033">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1033">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1034">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1034">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1035">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| Registry Functions \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| paths \| appareil cible »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1035">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Registry Functions\|[**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)\|Paths\|TargetDevice")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1036">Partition de disque physique sur laquelle le système d’exploitation est installé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1036">Physical disk partition on which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1037">**SystemDirectory**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1037">**SystemDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1038">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1038">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1039">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1039">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1040">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| , fonctions d’informations système [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span><span class="sxs-lookup"><span data-stu-id="92c7c-1040">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1041">Répertoire système du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1041">System directory of the operating system.</span></span>

<span data-ttu-id="92c7c-1042">Exemple : « C : \\ Windows \\ system32 »</span><span class="sxs-lookup"><span data-stu-id="92c7c-1042">Example: "C:\\WINDOWS\\SYSTEM32"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1043">**%SystemDrive%**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1043">**SystemDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1044">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1044">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1045">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1045">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1046">Lettre du lecteur de disque sur lequel réside le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1046">Letter of the disk drive on which the operating system resides.</span></span> <span data-ttu-id="92c7c-1047">Exemple : "C :"</span><span class="sxs-lookup"><span data-stu-id="92c7c-1047">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1048">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1048">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1049">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1049">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1050">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1050">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1051">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1051">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1052">Espace d’échange total en kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1052">Total swap space in kilobytes.</span></span> <span data-ttu-id="92c7c-1053">Cette valeur peut être **null** (non spécifié) si l’espace d’échange n’est pas distingué des fichiers d’échange.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1053">This value may be **NULL** (unspecified) if the swap space is not distinguished from page files.</span></span> <span data-ttu-id="92c7c-1054">Toutefois, certains systèmes d’exploitation distinguent ces concepts.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1054">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="92c7c-1055">Par exemple, dans UNIX, les processus entiers peuvent être échangés lorsque la liste de pages libre tombe et reste sous un montant spécifié.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1055">For example, in UNIX, whole processes can be swapped out when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="92c7c-1056">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-1056">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-1057">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-1057">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1058">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1058">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1059">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1059">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1060">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1060">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1061">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1061">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1062">Nombre, en kilo-octets, de la mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1062">Number, in kilobytes, of virtual memory.</span></span> <span data-ttu-id="92c7c-1063">Par exemple, cela peut être calculé en ajoutant la quantité de mémoire RAM totale à la quantité d’espace de pagination, c’est-à-dire en ajoutant la quantité de mémoire dans ou agrégée par le système informatique à la propriété, **SizeStoredInPagingFiles**.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1063">For example, this may be calculated by adding the amount of total RAM to the amount of paging space, that is, adding the amount of memory in or aggregated by the computer system to the property, **SizeStoredInPagingFiles**.</span></span>

<span data-ttu-id="92c7c-1064">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-1064">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-1065">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-1065">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1066">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1066">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1067">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1067">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1068">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1068">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1069">Qualificateurs : [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1069">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1070">Quantité totale, en kilo-octets, de la mémoire physique disponible pour le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1070">Total amount, in kilobytes, of physical memory available to the operating system.</span></span> <span data-ttu-id="92c7c-1071">Cette valeur n’indique pas nécessairement la véritable quantité de mémoire physique, mais ce qui est signalé au système d’exploitation comme disponible.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1071">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="92c7c-1072">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="92c7c-1072">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="92c7c-1073">Cette propriété est héritée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-1073">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1074">**Version**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1074">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1075">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1075">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1076">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1076">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1077">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| System Information structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")</span><span class="sxs-lookup"><span data-stu-id="92c7c-1077">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwMajorVersion, dwMinorVersion")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1078">Numéro de version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1078">Version number of the operating system.</span></span>

<span data-ttu-id="92c7c-1079">Exemple : « 4,0 »</span><span class="sxs-lookup"><span data-stu-id="92c7c-1079">Example: "4.0"</span></span>

</dd> <dt>

<span data-ttu-id="92c7c-1080">**WindowsDirectory**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1080">**WindowsDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92c7c-1081">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1081">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1082">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="92c7c-1082">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="92c7c-1083">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| System Information Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)»)</span><span class="sxs-lookup"><span data-stu-id="92c7c-1083">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span></span>
</dt> </dl>

<span data-ttu-id="92c7c-1084">Répertoire Windows du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1084">Windows directory of the operating system.</span></span>

<span data-ttu-id="92c7c-1085">Exemple : « C : \\ Windows »</span><span class="sxs-lookup"><span data-stu-id="92c7c-1085">Example: "C:\\WINDOWS"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92c7c-1086">Notes</span><span class="sxs-lookup"><span data-stu-id="92c7c-1086">Remarks</span></span>

<span data-ttu-id="92c7c-1087">La classe **Win32 \_ OperatingSystem** est dérivée de [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="92c7c-1087">The **Win32\_OperatingSystem** class is derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<span data-ttu-id="92c7c-1088">Tout système d’exploitation qui peut être installé sur un ordinateur qui peut exécuter un système d’exploitation Windows est un descendant ou un membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1088">Any operating system that can be installed on a computer that can run a Windows-based operating system is a descendant or member of this class.</span></span> <span data-ttu-id="92c7c-1089">**Win32 \_ OperatingSystem** est une classe singleton.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1089">**Win32\_OperatingSystem** is a singleton class.</span></span> <span data-ttu-id="92c7c-1090">Pour obtenir l’instance unique, utilisez « @ » pour la clé.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1090">To get the single instance, use "@" for the key.</span></span>

<span data-ttu-id="92c7c-1091">Contrairement à la plupart des autres classes WMI générées par MgmtClassGen, la méthode **OperatingSystem. CreateInstance**() renverra un objet **OperatingSystem** vide.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1091">Unlike most of the other WMI classes generated by MgmtClassGen, the **OperatingSystem.CreateInstance**() method will return a blank **OperatingSystem** object.</span></span> <span data-ttu-id="92c7c-1092">Par conséquent, si vous utilisez C \# avec MgmtClassGen, vous pouvez utiliser le code suivant :</span><span class="sxs-lookup"><span data-stu-id="92c7c-1092">Therefore, if you are using C\# with MgmtClassGen, you can use the following code:</span></span>


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a><span data-ttu-id="92c7c-1093">Exemples</span><span class="sxs-lookup"><span data-stu-id="92c7c-1093">Examples</span></span>

<span data-ttu-id="92c7c-1094">Vous trouverez un exemple VBScript qui obtient les données du système d’exploitation et du processeur à partir de [**Win32 \_ ComputerSystem**](win32-computersystem.md), du [**\_ processeur Win32**](win32-processor.md)et de **Win32 \_ OperatingSystem** dans les exemples de sujets relatifs au [**\_ processeur Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="92c7c-1094">You can find a VBScript example that obtains operating system and processor data from [**Win32\_ComputerSystem**](win32-computersystem.md), [**Win32\_Processor**](win32-processor.md), and **Win32\_OperatingSystem** in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="92c7c-1095">L’exemple de [génération de rapports d’environnement Exchange à l’aide](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) de PowerShell PowerShell sur la Galerie TechNet utilise une classe **Win32 \_ OperatingSystem** dans le cadre d’une application plus volumineuse pour générer des rapports d’environnement Exchange.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1095">The [Generate Exchange Environment Reports using Powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell sample on TechNet Gallery uses a **Win32\_OperatingSystem** class as part of a larger application to generate exchange environment reports.</span></span>

<span data-ttu-id="92c7c-1096">L’exemple [obtenir le temps d’activité du serveur à l’aide de WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) dans la Galerie TechNet utilise la propriété **LastBootupTime** pour déterminer la durée pendant laquelle le serveur a été actif.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1096">The [Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) sample in the TechNet Gallery uses the **LastBootupTime** property to determine how long the server has been active.</span></span> <span data-ttu-id="92c7c-1097">L’exemple utilise également l’option timeout pour s’assurer que l’appel WMI ne se bloque pas.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1097">The sample also uses the timeout option to ensure that the WMI call does not hang.</span></span>

<span data-ttu-id="92c7c-1098">L’exemple de code VBScript de l' [extracteur d’informations WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) sur la Galerie TechNet utilise la classe **Win32 \_ OperatingSystem** pour récupérer des informations de système d’exploitation à partir d’un certain nombre d’ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1098">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_OperatingSystem** class to retrieve OS information from a number of remote computers.</span></span>

<span data-ttu-id="92c7c-1099">Le script suivant obtient les instances de **Win32 \_ OperatingSystem** dans l’espace de noms « root \\ cimv2 » par défaut, puis affiche des informations sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1099">The following script obtains the instances of **Win32\_OperatingSystem** in the default "Root\\CIMv2" namespace, and then displays information about the operating system.</span></span>


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="92c7c-1100">L’exemple de code PowerShell suivant affiche toutes les informations d’exploitation relatives au système d’exploitation actuel.</span><span class="sxs-lookup"><span data-stu-id="92c7c-1100">The following PowerShell code sample displays all the operating information about the current OS.</span></span>


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a><span data-ttu-id="92c7c-1101">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92c7c-1101">Requirements</span></span>



| <span data-ttu-id="92c7c-1102">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92c7c-1102">Requirement</span></span> | <span data-ttu-id="92c7c-1103">Valeur</span><span class="sxs-lookup"><span data-stu-id="92c7c-1103">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92c7c-1104">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92c7c-1104">Minimum supported client</span></span><br/> | <span data-ttu-id="92c7c-1105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92c7c-1105">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92c7c-1106">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92c7c-1106">Minimum supported server</span></span><br/> | <span data-ttu-id="92c7c-1107">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92c7c-1107">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92c7c-1108">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92c7c-1108">Namespace</span></span><br/>                | <span data-ttu-id="92c7c-1109">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="92c7c-1109">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="92c7c-1110">MOF</span><span class="sxs-lookup"><span data-stu-id="92c7c-1110">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92c7c-1111"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92c7c-1111"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="92c7c-1112">DLL</span><span class="sxs-lookup"><span data-stu-id="92c7c-1112">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92c7c-1113"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c7c-1113"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c7c-1114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92c7c-1114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c7c-1115">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="92c7c-1115">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="92c7c-1116">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="92c7c-1116">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="92c7c-1117">Tâches WMI : systèmes d’exploitation</span><span class="sxs-lookup"><span data-stu-id="92c7c-1117">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[<span data-ttu-id="92c7c-1118">Tâches WMI : matériel de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="92c7c-1118">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[<span data-ttu-id="92c7c-1119">Tâches WMI : gestion des postes de travail</span><span class="sxs-lookup"><span data-stu-id="92c7c-1119">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
