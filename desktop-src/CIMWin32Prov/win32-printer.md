---
description: Représente un appareil connecté à un ordinateur qui exécute sur un système d’exploitation Microsoft Windows et qui peut produire une image imprimée ou du texte sur papier ou autre support.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Win32_Printer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201000"
---
# <a name="win32_printer-class"></a><span data-ttu-id="135ac-103">\_Classe d’imprimantes Win32</span><span class="sxs-lookup"><span data-stu-id="135ac-103">Win32\_Printer class</span></span>

<span data-ttu-id="135ac-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l' **\_ imprimante Win32** représente un appareil connecté à un ordinateur fonctionnant sous un système d’exploitation Microsoft Windows qui peut produire une image imprimée ou du texte sur un papier ou un autre support.</span><span class="sxs-lookup"><span data-stu-id="135ac-104">The **Win32\_Printer** [WMI class](../wmisdk/retrieving-a-class.md) represents a device connected to a computer running on a Microsoft Windows operating system that can produce a printed image or text on paper or other medium.</span></span>

<span data-ttu-id="135ac-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="135ac-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="135ac-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="135ac-106">Syntax</span></span>

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a><span data-ttu-id="135ac-107">Membres</span><span class="sxs-lookup"><span data-stu-id="135ac-107">Members</span></span>

<span data-ttu-id="135ac-108">La classe **Win32 \_ Printer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="135ac-108">The **Win32\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="135ac-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="135ac-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="135ac-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="135ac-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="135ac-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="135ac-111">Methods</span></span>

<span data-ttu-id="135ac-112">La **classe \_ Printer Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="135ac-112">The **Win32\_Printer** class has these methods.</span></span>



| <span data-ttu-id="135ac-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="135ac-113">Method</span></span>                                                                               | <span data-ttu-id="135ac-114">Description</span><span class="sxs-lookup"><span data-stu-id="135ac-114">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="135ac-115">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="135ac-115">**AddPrinterConnection**</span></span>](addprinterconnection-method-in-class-win32-printer.md)   | <span data-ttu-id="135ac-116">Ajoute une connexion à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-116">Adds a connection to the printer.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="135ac-117">**CancelAllJobs**</span><span class="sxs-lookup"><span data-stu-id="135ac-117">**CancelAllJobs**</span></span>](cancelalljobs-method-in-class-win32-printer.md)                 | <span data-ttu-id="135ac-118">Annule tous les travaux.</span><span class="sxs-lookup"><span data-stu-id="135ac-118">Cancels all jobs.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="135ac-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="135ac-119">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="135ac-120">Retourne le descripteur de sécurité qui contrôle l’accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-120">Returns the security descriptor that controls access to the printer.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="135ac-121">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="135ac-121">**Pause**</span></span>](pause-method-in-class-win32-printer.md)                                 | <span data-ttu-id="135ac-122">Pause la file d'attente à l'impression.</span><span class="sxs-lookup"><span data-stu-id="135ac-122">Pauses the print queue.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="135ac-123">**PrintTestPage**</span><span class="sxs-lookup"><span data-stu-id="135ac-123">**PrintTestPage**</span></span>](printtestpage-method-in-class-win32-printer.md)                 | <span data-ttu-id="135ac-124">Imprime une page de test.</span><span class="sxs-lookup"><span data-stu-id="135ac-124">Prints a test page.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="135ac-125">**RenamePrinter**</span><span class="sxs-lookup"><span data-stu-id="135ac-125">**RenamePrinter**</span></span>](renameprinter-method-in-class-win32-printer.md)                 | <span data-ttu-id="135ac-126">Renomme une imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-126">Renames a printer.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="135ac-127">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="135ac-127">**Reset**</span></span>                                                                            | <span data-ttu-id="135ac-128">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="135ac-128">Not implemented.</span></span> <span data-ttu-id="135ac-129">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**Reset**](reset-method-in-class-cim-controller.md) dans l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-129">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/>                 |
| [<span data-ttu-id="135ac-130">**Sort**</span><span class="sxs-lookup"><span data-stu-id="135ac-130">**Resume**</span></span>](resume-method-in-class-win32-printer.md)                               | <span data-ttu-id="135ac-131">Reprend la file d’attente à l’impression en pause.</span><span class="sxs-lookup"><span data-stu-id="135ac-131">Resumes paused print queue.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="135ac-132">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="135ac-132">**SetDefaultPrinter**</span></span>](setdefaultprinter-method-in-class-win32-printer.md)         | <span data-ttu-id="135ac-133">Définit l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="135ac-133">Sets the default printer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="135ac-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="135ac-134">**SetPowerState**</span></span>                                                                    | <span data-ttu-id="135ac-135">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="135ac-135">Not implemented.</span></span> <span data-ttu-id="135ac-136">Pour plus d’informations sur l’implémentation de cette méthode, consultez la méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) dans l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-136">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/> |
| [<span data-ttu-id="135ac-137">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="135ac-137">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="135ac-138">Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-138">Writes an updated version of the security descriptor that controls access to the printer.</span></span><br/>                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="135ac-139">Propriétés</span><span class="sxs-lookup"><span data-stu-id="135ac-139">Properties</span></span>

<span data-ttu-id="135ac-140">La classe **Win32 \_ Printer** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="135ac-140">The **Win32\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="135ac-141">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="135ac-141">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-144">Bitmap d’attributs pour un périphérique d’impression Windows.</span><span class="sxs-lookup"><span data-stu-id="135ac-144">Bitmap of attributes for a Windows-based printing device.</span></span>

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span data-ttu-id="135ac-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Imprimante \_ ATTRIBUT \_ mis en file d’attente** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="135ac-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**PRINTER\_ATTRIBUTE\_QUEUED** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-146">Mis en file d'attente.</span><span class="sxs-lookup"><span data-stu-id="135ac-146">Queued</span></span>

<span data-ttu-id="135ac-147">Les travaux d’impression sont mis en mémoire tampon et mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="135ac-147">Print jobs are buffered and queued.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span data-ttu-id="135ac-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Imprimante \_ ATTRIBUT \_ direct** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="135ac-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER\_ATTRIBUTE\_DIRECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-149">Direct</span><span class="sxs-lookup"><span data-stu-id="135ac-149">Direct</span></span>

<span data-ttu-id="135ac-150">Document à envoyer directement à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-150">Document to be sent directly to the printer.</span></span> <span data-ttu-id="135ac-151">Cette valeur est utilisée si les travaux d’impression ne sont pas mis en file d’attente correctement.</span><span class="sxs-lookup"><span data-stu-id="135ac-151">This value is used if print jobs are not queued correctly.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span data-ttu-id="135ac-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Imprimante \_ ATTRIBUT \_ par défaut** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="135ac-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER\_ATTRIBUTE\_DEFAULT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-153">Default</span><span class="sxs-lookup"><span data-stu-id="135ac-153">Default</span></span>

<span data-ttu-id="135ac-154">Imprimante par défaut sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="135ac-154">Default printer on a computer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span data-ttu-id="135ac-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Imprimante \_ ATTRIBUT \_ Shared** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="135ac-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER\_ATTRIBUTE\_SHARED** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-156">Partagé</span><span class="sxs-lookup"><span data-stu-id="135ac-156">Shared</span></span>

<span data-ttu-id="135ac-157">Disponible en tant que ressource réseau partagée.</span><span class="sxs-lookup"><span data-stu-id="135ac-157">Available as a shared network resource.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span data-ttu-id="135ac-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Imprimante \_ \_Réseau d’attributs** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="135ac-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER\_ATTRIBUTE\_NETWORK** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-159">Réseau</span><span class="sxs-lookup"><span data-stu-id="135ac-159">Network</span></span>

<span data-ttu-id="135ac-160">Attaché à un réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-160">Attached to a network.</span></span> <span data-ttu-id="135ac-161">Si les bits réseau et locaux sont tous deux définis, cela indique une imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-161">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span data-ttu-id="135ac-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Imprimante \_ ATTRIBUT \_ masqué** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="135ac-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**PRINTER\_ATTRIBUTE\_HIDDEN** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-163">Hidden</span><span class="sxs-lookup"><span data-stu-id="135ac-163">Hidden</span></span>

<span data-ttu-id="135ac-164">Masqué pour certains utilisateurs sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-164">Hidden from some users on the network.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span data-ttu-id="135ac-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Imprimante \_ ATTRIBUT \_ local** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="135ac-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER\_ATTRIBUTE\_LOCAL** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-166">Local</span><span class="sxs-lookup"><span data-stu-id="135ac-166">Local</span></span>

<span data-ttu-id="135ac-167">Connecté directement à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="135ac-167">Directly connected to a computer.</span></span> <span data-ttu-id="135ac-168">Si les bits réseau et locaux sont tous deux définis, cela indique une imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-168">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span data-ttu-id="135ac-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Imprimante \_ ATTRIBUT \_ ENABLEDEVQ** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="135ac-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER\_ATTRIBUTE\_ENABLEDEVQ** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-170">EnableDevQ</span><span class="sxs-lookup"><span data-stu-id="135ac-170">EnableDevQ</span></span>

<span data-ttu-id="135ac-171">Activez la file d’attente sur l’imprimante si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="135ac-171">Enable the queue on the printer if available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span data-ttu-id="135ac-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Imprimante \_ ATTRIBUT \_ KEEPPRINTEDJOBS** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="135ac-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-173">KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="135ac-173">KeepPrintedJobs</span></span>

<span data-ttu-id="135ac-174">Le spouleur ne doit pas supprimer les documents une fois qu’ils sont imprimés.</span><span class="sxs-lookup"><span data-stu-id="135ac-174">Spooler should not delete documents after they are printed.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span data-ttu-id="135ac-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Imprimante \_ L’attribut se \_ \_ termine en \_ premier** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="135ac-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-176">DoCompleteFirst</span><span class="sxs-lookup"><span data-stu-id="135ac-176">DoCompleteFirst</span></span>

<span data-ttu-id="135ac-177">Démarrer en premier les travaux qui se sont terminés.</span><span class="sxs-lookup"><span data-stu-id="135ac-177">Start jobs that are finished spooling first.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span data-ttu-id="135ac-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Imprimante \_ Travail d’attribut \_ \_ hors connexion** (1024 (0x400))</span><span class="sxs-lookup"><span data-stu-id="135ac-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER\_ATTRIBUTE\_WORK\_OFFLINE** (1024 (0x400))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-179">WorkOffline</span><span class="sxs-lookup"><span data-stu-id="135ac-179">WorkOffline</span></span>

<span data-ttu-id="135ac-180">Met en file d’attente les travaux d’impression quand une imprimante n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="135ac-180">Queue print jobs when a printer is not available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span data-ttu-id="135ac-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Imprimante \_ ATTRIBUT \_ Enable \_ BIDI** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="135ac-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER\_ATTRIBUTE\_ENABLE\_BIDI** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-182">EnableBIDI</span><span class="sxs-lookup"><span data-stu-id="135ac-182">EnableBIDI</span></span>

<span data-ttu-id="135ac-183">Activez l’impression bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="135ac-183">Enable bidirectional printing.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span data-ttu-id="135ac-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Imprimante \_ ATTRIBUT \_ brut \_ uniquement** (4096 (0x1000))</span><span class="sxs-lookup"><span data-stu-id="135ac-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER\_ATTRIBUTE\_RAW\_ONLY** (4096 (0x1000))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-185">Autorisez uniquement les travaux de type de données bruts à être mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="135ac-185">Allow only raw data type jobs to be spooled.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span data-ttu-id="135ac-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Imprimante \_ ATTRIBUT \_ publié** (8192 (0x2000))</span><span class="sxs-lookup"><span data-stu-id="135ac-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER\_ATTRIBUTE\_PUBLISHED** (8192 (0x2000))</span></span>


</dt> <dd>

<span data-ttu-id="135ac-187">Publié</span><span class="sxs-lookup"><span data-stu-id="135ac-187">Published</span></span>

<span data-ttu-id="135ac-188">Publié dans le service d’annuaire réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-188">Published in the network directory service.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-189">**Disponibilité**</span><span class="sxs-lookup"><span data-stu-id="135ac-189">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-190">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-192">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,5 "," MIB. \|Hôte IETF-ressources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="135ac-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-193">Disponibilité et état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-193">Availability and status of the device.</span></span>

<span data-ttu-id="135ac-194">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="135ac-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**En cours d’exécution/pleine puissance** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-198">En cours d’exécution ou pleine puissance</span><span class="sxs-lookup"><span data-stu-id="135ac-198">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="135ac-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avertissement** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="135ac-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Dans le test** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="135ac-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="135ac-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Mise hors tension** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="135ac-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Hors ligne** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="135ac-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Hors** service (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="135ac-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Détérioré** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="135ac-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installé** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="135ac-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erreur d’installation** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="135ac-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Économie **d’énergie-inconnu** (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-209">L’appareil est connu pour être en mode d’économie d’énergie, mais son état exact est inconnu.</span><span class="sxs-lookup"><span data-stu-id="135ac-209">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="135ac-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Économie **d’énergie-mode faible puissance** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-211">L’appareil est dans un état d’économie d’énergie, mais fonctionne toujours et peut présenter des performances dégradées.</span><span class="sxs-lookup"><span data-stu-id="135ac-211">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="135ac-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Économie **d’énergie-veille** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-213">L’appareil ne fonctionne pas, mais peut être mis à la pleine puissance rapidement.</span><span class="sxs-lookup"><span data-stu-id="135ac-213">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="135ac-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Cycle d’alimentation** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="135ac-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Économie **d’énergie-Avertissement** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-216">L’appareil est dans un état d’avertissement, bien qu’il soit également en mode d’économie d’énergie.</span><span class="sxs-lookup"><span data-stu-id="135ac-216">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="135ac-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **Pause** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-218">L’appareil est suspendu.</span><span class="sxs-lookup"><span data-stu-id="135ac-218">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="135ac-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non prêt** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-220">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="135ac-220">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="135ac-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configuré** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-222">L’appareil n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="135ac-222">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="135ac-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Suspendu** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-224">L’appareil est calme.</span><span class="sxs-lookup"><span data-stu-id="135ac-224">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-225">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="135ac-225">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-226">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-226">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-228">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="135ac-228">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-229">Tableau de toutes les feuilles de travail disponibles sur une imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-229">Array of all the job sheets available on a printer.</span></span> <span data-ttu-id="135ac-230">Peut également être utilisé pour décrire la bannière qu’une imprimante peut fournir au début de chaque travail, ou d’autres options spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="135ac-230">Can also be used to describe the banner that a printer might provide at the beginning of each job, or other user-specified options.</span></span>

<span data-ttu-id="135ac-231">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-231">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-232">**AveragePagesPerMinute**</span><span class="sxs-lookup"><span data-stu-id="135ac-232">**AveragePagesPerMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-233">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-235">Vitesse d’impression, en nombre moyen de pages par minute, qu’une imprimante peut produire en sortie.</span><span class="sxs-lookup"><span data-stu-id="135ac-235">Printing rate, in average number of pages per minute, that a printer can produce output.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-236">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="135ac-236">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-237">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-237">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-239">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). CapabilityDescriptions "," CIM \_ PrintJob. finition "," CIM \_ printservice. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="135ac-239">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-240">Tableau de fonctionnalités d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-240">Array of printer capabilities.</span></span>

<span data-ttu-id="135ac-241">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-241">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="135ac-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="135ac-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="135ac-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="135ac-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="135ac-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="135ac-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="135ac-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="135ac-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="135ac-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="135ac-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="135ac-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="135ac-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-255">One-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-255">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="135ac-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-257">Bord long Two-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-257">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="135ac-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-259">Bord Two-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-259">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="135ac-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="135ac-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="135ac-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="135ac-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="135ac-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="135ac-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="135ac-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-267">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="135ac-267">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-268">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-270">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="135ac-270">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-271">Tableau de chaînes de forme libre qui fournissent des explications détaillées sur les fonctionnalités de l’imprimante indiquées dans le tableau des **fonctionnalités** .</span><span class="sxs-lookup"><span data-stu-id="135ac-271">Array of free-form strings that provide detailed explanations for the printer features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="135ac-272">Chaque entrée de ce tableau est liée à une entrée du tableau de **fonctionnalités** qui se trouve dans le même index.</span><span class="sxs-lookup"><span data-stu-id="135ac-272">Each entry of this array is related to an entry in the **Capabilities** array that is located in the same index.</span></span>

<span data-ttu-id="135ac-273">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-273">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-274">**Caption**</span><span class="sxs-lookup"><span data-stu-id="135ac-274">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-275">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-277">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="135ac-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-278">Description succincte d’un objet : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="135ac-278">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="135ac-279">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-279">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-280">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="135ac-280">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-281">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-281">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-282">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-283">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="135ac-283">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-284">Tableau des jeux de caractères disponibles pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="135ac-284">Array of available character sets for output.</span></span> <span data-ttu-id="135ac-285">Les chaînes fournies dans cette propriété doivent être conformes à la sémantique et à la syntaxe spécifiées par la section 4.1.2 ("charset Parameters") dans la norme RFC 2046 (MIME part 2) et contenues dans le Registre du jeu de caractères IANA.</span><span class="sxs-lookup"><span data-stu-id="135ac-285">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="135ac-286">Exemples : « UTF-8 », « US-ASCII » et « ISO-8859-1 ».</span><span class="sxs-lookup"><span data-stu-id="135ac-286">Examples include, "UTF-8", "us-ASCII", and "iso-8859-1".</span></span>

<span data-ttu-id="135ac-287">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-287">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-288">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="135ac-288">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-290">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-291">Commentaire pour une file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="135ac-291">Comment for a print queue.</span></span>

<span data-ttu-id="135ac-292">Exemple : imprimante couleur</span><span class="sxs-lookup"><span data-stu-id="135ac-292">Example: Color printer</span></span>

</dd> <dt>

<span data-ttu-id="135ac-293">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="135ac-293">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-294">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-295">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-296">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="135ac-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-297">Code d’erreur Configuration Manager Win32.</span><span class="sxs-lookup"><span data-stu-id="135ac-297">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="135ac-298">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="135ac-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Ce périphérique fonctionne correctement.**</span><span class="sxs-lookup"><span data-stu-id="135ac-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="135ac-300"> (0)</span><span class="sxs-lookup"><span data-stu-id="135ac-300">(0)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-301">L’appareil fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="135ac-301">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="135ac-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Ce périphérique n’est pas configuré correctement.**</span><span class="sxs-lookup"><span data-stu-id="135ac-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="135ac-303">(1)</span><span class="sxs-lookup"><span data-stu-id="135ac-303">(1)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-304">L’appareil n’est pas configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="135ac-304">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="135ac-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows ne peut pas charger le pilote de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="135ac-306">(2)</span><span class="sxs-lookup"><span data-stu-id="135ac-306">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="135ac-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Le pilote de cet appareil est peut-être endommagé ou votre système ne dispose peut-être pas de suffisamment de mémoire ou d’autres ressources.**</span><span class="sxs-lookup"><span data-stu-id="135ac-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="135ac-308">(3)</span><span class="sxs-lookup"><span data-stu-id="135ac-308">(3)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-309">Le pilote de cet appareil est peut-être endommagé ou la mémoire ou d’autres ressources du système sont peut-être insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="135ac-309">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="135ac-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Cet appareil ne fonctionne pas correctement. L’un de ses pilotes ou votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="135ac-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="135ac-311">(4)</span><span class="sxs-lookup"><span data-stu-id="135ac-311">(4)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-312">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="135ac-312">Device is not working properly.</span></span> <span data-ttu-id="135ac-313">L’un de ses pilotes ou le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="135ac-313">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="135ac-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Le pilote de cet appareil a besoin d’une ressource que Windows ne peut pas gérer.**</span><span class="sxs-lookup"><span data-stu-id="135ac-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="135ac-315">(5)</span><span class="sxs-lookup"><span data-stu-id="135ac-315">(5)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-316">Le pilote de l’appareil requiert une ressource que Windows ne peut pas gérer.</span><span class="sxs-lookup"><span data-stu-id="135ac-316">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="135ac-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuration de démarrage de cet appareil est en conflit avec d’autres appareils.**</span><span class="sxs-lookup"><span data-stu-id="135ac-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="135ac-318"> (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-318">(6)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-319">La configuration de démarrage de l’appareil est en conflit avec d’autres appareils.</span><span class="sxs-lookup"><span data-stu-id="135ac-319">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="135ac-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossible de filtrer.**</span><span class="sxs-lookup"><span data-stu-id="135ac-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="135ac-321">(7)</span><span class="sxs-lookup"><span data-stu-id="135ac-321">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="135ac-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Le chargeur de pilote de l’appareil est manquant.**</span><span class="sxs-lookup"><span data-stu-id="135ac-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="135ac-323">(8)</span><span class="sxs-lookup"><span data-stu-id="135ac-323">(8)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-324">Le chargeur de pilote de l’appareil est manquant.</span><span class="sxs-lookup"><span data-stu-id="135ac-324">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="135ac-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Ce périphérique ne fonctionne pas correctement, car le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="135ac-326">(9)</span><span class="sxs-lookup"><span data-stu-id="135ac-326">(9)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-327">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="135ac-327">Device is not working properly.</span></span> <span data-ttu-id="135ac-328">Le microprogramme de contrôle ne signale pas correctement les ressources pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-328">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="135ac-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossible de démarrer cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="135ac-330">(10)</span><span class="sxs-lookup"><span data-stu-id="135ac-330">(10)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-331">Impossible de démarrer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-331">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="135ac-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Échec de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="135ac-333">(11)</span><span class="sxs-lookup"><span data-stu-id="135ac-333">(11)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-334">Échec de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-334">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="135ac-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Ce périphérique ne peut pas trouver suffisamment de ressources disponibles.**</span><span class="sxs-lookup"><span data-stu-id="135ac-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="135ac-336">douze</span><span class="sxs-lookup"><span data-stu-id="135ac-336">(12)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-337">L’appareil ne peut pas trouver suffisamment de ressources libres à utiliser.</span><span class="sxs-lookup"><span data-stu-id="135ac-337">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="135ac-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows ne peut pas vérifier les ressources de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="135ac-339">(13)</span><span class="sxs-lookup"><span data-stu-id="135ac-339">(13)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-340">Windows ne peut pas vérifier les ressources de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-340">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="135ac-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Ce périphérique ne peut pas fonctionner correctement tant que vous n’avez pas redémarré votre ordinateur.**</span><span class="sxs-lookup"><span data-stu-id="135ac-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="135ac-342">(14)</span><span class="sxs-lookup"><span data-stu-id="135ac-342">(14)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-343">L’appareil ne peut pas fonctionner correctement tant que l’ordinateur n’a pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="135ac-343">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="135ac-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Cet appareil ne fonctionne pas correctement en raison d’un problème de réénumération.**</span><span class="sxs-lookup"><span data-stu-id="135ac-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="135ac-345">(15)</span><span class="sxs-lookup"><span data-stu-id="135ac-345">(15)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-346">L’appareil ne fonctionne pas correctement en raison d’un éventuel problème de réénumération.</span><span class="sxs-lookup"><span data-stu-id="135ac-346">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="135ac-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows ne peut pas identifier toutes les ressources utilisées par cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="135ac-348">(16)</span><span class="sxs-lookup"><span data-stu-id="135ac-348">(16)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-349">Windows ne peut pas identifier toutes les ressources utilisées par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-349">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="135ac-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Ce périphérique demande un type de ressource inconnu.**</span><span class="sxs-lookup"><span data-stu-id="135ac-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="135ac-351">(17)</span><span class="sxs-lookup"><span data-stu-id="135ac-351">(17)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-352">L’appareil demande un type de ressource inconnu.</span><span class="sxs-lookup"><span data-stu-id="135ac-352">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="135ac-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Réinstallez les pilotes pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="135ac-354">(18)</span><span class="sxs-lookup"><span data-stu-id="135ac-354">(18)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-355">Les pilotes de périphérique doivent être réinstallés.</span><span class="sxs-lookup"><span data-stu-id="135ac-355">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="135ac-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Échec lors de l’utilisation du chargeur VxD.**</span><span class="sxs-lookup"><span data-stu-id="135ac-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="135ac-357">(19)</span><span class="sxs-lookup"><span data-stu-id="135ac-357">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="135ac-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Votre registre est peut-être endommagé.**</span><span class="sxs-lookup"><span data-stu-id="135ac-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="135ac-359">(20)</span><span class="sxs-lookup"><span data-stu-id="135ac-359">(20)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-360">Le Registre est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="135ac-360">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="135ac-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel. Windows supprime cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="135ac-362">(21)</span><span class="sxs-lookup"><span data-stu-id="135ac-362">(21)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-363">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="135ac-363">System failure.</span></span> <span data-ttu-id="135ac-364">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="135ac-364">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="135ac-365">Windows supprime l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-365">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="135ac-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Cet appareil est désactivé.**</span><span class="sxs-lookup"><span data-stu-id="135ac-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="135ac-367">(22)</span><span class="sxs-lookup"><span data-stu-id="135ac-367">(22)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-368">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="135ac-368">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="135ac-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Défaillance du système : essayez de modifier le pilote de cet appareil. Si cela ne fonctionne pas, consultez la documentation de votre matériel.**</span><span class="sxs-lookup"><span data-stu-id="135ac-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="135ac-370">(23)</span><span class="sxs-lookup"><span data-stu-id="135ac-370">(23)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-371">Défaillance du système.</span><span class="sxs-lookup"><span data-stu-id="135ac-371">System failure.</span></span> <span data-ttu-id="135ac-372">Si la modification du pilote de périphérique n’est pas efficace, consultez la documentation du matériel.</span><span class="sxs-lookup"><span data-stu-id="135ac-372">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="135ac-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Ce périphérique n’est pas présent, ne fonctionne pas correctement ou tous ses pilotes ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="135ac-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="135ac-374">(24)</span><span class="sxs-lookup"><span data-stu-id="135ac-374">(24)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-375">L’appareil n’est pas présent, ne fonctionne pas correctement ou n’a pas tous ses pilotes installés.</span><span class="sxs-lookup"><span data-stu-id="135ac-375">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="135ac-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="135ac-377">(25)</span><span class="sxs-lookup"><span data-stu-id="135ac-377">(25)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-378">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-378">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="135ac-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows est toujours en cours de configuration de cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="135ac-380">(26)</span><span class="sxs-lookup"><span data-stu-id="135ac-380">(26)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-381">Windows est toujours en cours de configuration de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="135ac-381">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="135ac-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Cet appareil n’a pas de configuration de journal valide.**</span><span class="sxs-lookup"><span data-stu-id="135ac-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="135ac-383">(27)</span><span class="sxs-lookup"><span data-stu-id="135ac-383">(27)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-384">L’appareil n’a pas de configuration de journal valide.</span><span class="sxs-lookup"><span data-stu-id="135ac-384">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="135ac-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Les pilotes de cet appareil ne sont pas installés.**</span><span class="sxs-lookup"><span data-stu-id="135ac-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="135ac-386">(28)</span><span class="sxs-lookup"><span data-stu-id="135ac-386">(28)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-387">Les pilotes de périphérique ne sont pas installés.</span><span class="sxs-lookup"><span data-stu-id="135ac-387">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="135ac-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Ce périphérique est désactivé, car le microprogramme de l’appareil ne lui a pas donné les ressources requises.**</span><span class="sxs-lookup"><span data-stu-id="135ac-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="135ac-389">(29)</span><span class="sxs-lookup"><span data-stu-id="135ac-389">(29)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-390">L’appareil est désactivé.</span><span class="sxs-lookup"><span data-stu-id="135ac-390">Device is disabled.</span></span> <span data-ttu-id="135ac-391">Le microprogramme de l’appareil n’a pas fourni les ressources requises.</span><span class="sxs-lookup"><span data-stu-id="135ac-391">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="135ac-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Cet appareil utilise une ressource de demande d’interruption (IRQ) qu’un autre appareil utilise.**</span><span class="sxs-lookup"><span data-stu-id="135ac-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="135ac-393">(30)</span><span class="sxs-lookup"><span data-stu-id="135ac-393">(30)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-394">L’appareil utilise une ressource IRQ qu’un autre appareil utilise.</span><span class="sxs-lookup"><span data-stu-id="135ac-394">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="135ac-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Ce périphérique ne fonctionne pas correctement, car Windows ne peut pas charger les pilotes requis pour cet appareil.**</span><span class="sxs-lookup"><span data-stu-id="135ac-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="135ac-396">31</span><span class="sxs-lookup"><span data-stu-id="135ac-396">(31)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-397">L’appareil ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="135ac-397">Device is not working properly.</span></span> <span data-ttu-id="135ac-398">Windows ne peut pas charger les pilotes de périphérique requis.</span><span class="sxs-lookup"><span data-stu-id="135ac-398">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-399">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="135ac-399">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-400">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-401">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-402">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="135ac-402">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-403">Si la **valeur est true**, l’appareil utilise une configuration définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="135ac-403">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="135ac-404">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-405">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="135ac-405">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-407">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-408">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="135ac-408">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="135ac-409">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée pour créer une instance.</span><span class="sxs-lookup"><span data-stu-id="135ac-409">Name of the first concrete class to appear in the inheritance chain used to create an instance.</span></span> <span data-ttu-id="135ac-410">Lorsqu’elle est utilisée avec d’autres propriétés de clé de la classe, la propriété autorise l’identification de toutes les instances de cette classe et de ses sous-classes de manière unique.</span><span class="sxs-lookup"><span data-stu-id="135ac-410">When used with other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="135ac-411">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-412">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="135ac-412">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-413">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-413">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-414">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-415">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="135ac-415">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-416">Tableau de fonctionnalités d’imprimante actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="135ac-416">Array of printer capabilities that are being used currently.</span></span> <span data-ttu-id="135ac-417">Une entrée de cette propriété doit également être listée dans le tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="135ac-417">An entry in this property must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="135ac-418">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-418">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="135ac-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="135ac-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="135ac-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="135ac-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="135ac-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="135ac-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="135ac-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="135ac-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="135ac-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="135ac-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="135ac-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="135ac-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-432">One-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-432">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="135ac-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-434">Bord long Two-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-434">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="135ac-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-436">Bord Two-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-436">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="135ac-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="135ac-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="135ac-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="135ac-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="135ac-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="135ac-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="135ac-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-444">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="135ac-444">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-446">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-447">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="135ac-447">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-448">Jeu de caractères actuellement utilisé pour la sortie.</span><span class="sxs-lookup"><span data-stu-id="135ac-448">The character set currently used for output.</span></span> <span data-ttu-id="135ac-449">Les chaînes fournies dans cette propriété doivent être conformes à la sémantique et à la syntaxe spécifiées par la section 4.1.2 ("charset Parameters") dans la norme RFC 2046 (MIME part 2) et contenues dans le Registre du jeu de caractères IANA.</span><span class="sxs-lookup"><span data-stu-id="135ac-449">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="135ac-450">Exemples : « UTF-8 », « US-ASCII » et ISO-8859-1.</span><span class="sxs-lookup"><span data-stu-id="135ac-450">Examples include "utf-8", "us-ASCII", and iso-8859-1.</span></span>

<span data-ttu-id="135ac-451">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-451">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-452">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="135ac-452">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-453">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-454">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-455">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). LanguagesSupported ","**\_ imprimante CIM**.**CurrentMimeType**")</span><span class="sxs-lookup"><span data-stu-id="135ac-455">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**CurrentMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-456">Langue de l’imprimante actuellement utilisée.</span><span class="sxs-lookup"><span data-stu-id="135ac-456">Printer language currently used.</span></span> <span data-ttu-id="135ac-457">La langue utilisée doit être indiquée dans la propriété **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="135ac-457">The language used must be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="135ac-458">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-458">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="135ac-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="135ac-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="135ac-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="135ac-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="135ac-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="135ac-466"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="135ac-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="135ac-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="135ac-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="135ac-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="135ac-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpression** (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="135ac-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="135ac-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Données de ligne** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-474">LineData</span><span class="sxs-lookup"><span data-stu-id="135ac-474">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="135ac-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-476">DODCA</span><span class="sxs-lookup"><span data-stu-id="135ac-476">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="135ac-477"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="135ac-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="135ac-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="135ac-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="135ac-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="135ac-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="135ac-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="135ac-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="135ac-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="135ac-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="135ac-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="135ac-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="135ac-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="135ac-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="135ac-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="135ac-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="135ac-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="135ac-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="135ac-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="135ac-489"><span id="CPAP"></span><span id="cpap"></span>**Pression positive** (29)</span><span class="sxs-lookup"><span data-stu-id="135ac-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="135ac-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="135ac-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="135ac-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texte simple** (31)</span><span class="sxs-lookup"><span data-stu-id="135ac-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-492">SimpleText</span><span class="sxs-lookup"><span data-stu-id="135ac-492">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="135ac-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="135ac-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="135ac-494"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="135ac-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="135ac-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressionne** (34)</span><span class="sxs-lookup"><span data-stu-id="135ac-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="135ac-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="135ac-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="135ac-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="135ac-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="135ac-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="135ac-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="135ac-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique** (38)</span><span class="sxs-lookup"><span data-stu-id="135ac-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="135ac-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span><span class="sxs-lookup"><span data-stu-id="135ac-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="135ac-501"><span id="LIPS"></span><span id="lips"></span>**Lèvres** (40)</span><span class="sxs-lookup"><span data-stu-id="135ac-501"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="135ac-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="135ac-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="135ac-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span><span class="sxs-lookup"><span data-stu-id="135ac-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="135ac-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Majuscules** (43)</span><span class="sxs-lookup"><span data-stu-id="135ac-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="135ac-505"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="135ac-505"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="135ac-506"><span id="LCDS"></span><span id="lcds"></span>**Écrans plats** (45)</span><span class="sxs-lookup"><span data-stu-id="135ac-506"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="135ac-507"><span id="XES"></span><span id="xes"></span>**X** (46)</span><span class="sxs-lookup"><span data-stu-id="135ac-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="135ac-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="135ac-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="135ac-509">48</span><span class="sxs-lookup"><span data-stu-id="135ac-509">48</span></span>
</dt> <dd>

<span data-ttu-id="135ac-510">XPS</span><span class="sxs-lookup"><span data-stu-id="135ac-510">XPS</span></span>

</dd> <dt>

<span data-ttu-id="135ac-511">49</span><span class="sxs-lookup"><span data-stu-id="135ac-511">49</span></span>
</dt> <dd>

<span data-ttu-id="135ac-512">HPGL2</span><span class="sxs-lookup"><span data-stu-id="135ac-512">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="135ac-513">50</span><span class="sxs-lookup"><span data-stu-id="135ac-513">50</span></span>
</dt> <dd>

<span data-ttu-id="135ac-514">PCLXL</span><span class="sxs-lookup"><span data-stu-id="135ac-514">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-515">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="135ac-515">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-516">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-517">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-518">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="135ac-518">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-519">Type MIME actuellement utilisé si **currentLanguage** est un type MIME (valeur = 47).</span><span class="sxs-lookup"><span data-stu-id="135ac-519">MIME type currently being used if the **CurrentLanguage** is a MIME type (value = 47).</span></span>

<span data-ttu-id="135ac-520">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-520">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-521">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="135ac-521">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-522">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-523">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-524">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="135ac-524">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-525">Langue actuellement utilisée par l’imprimante pour la gestion.</span><span class="sxs-lookup"><span data-stu-id="135ac-525">Language that the printer is using for management currently.</span></span> <span data-ttu-id="135ac-526">La langue répertoriée ici doit également être répertoriée dans la propriété **NaturalLanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="135ac-526">The language listed here must also be listed in the **NaturalLanguagesSupported** property.</span></span>

<span data-ttu-id="135ac-527">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-527">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-528">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="135ac-528">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-529">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-530">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-531">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="135ac-531">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-532">Type de papier utilisé par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-532">Type of paper the printer is using.</span></span> <span data-ttu-id="135ac-533">Doit être exprimée sous la forme spécifiée par l’application d’impression de documents ISO/IEC 10175 (DPA), qui est résumée dans l’annexe C de la RFC 1759 (MIB de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="135ac-533">Must be expressed in the form specified by the ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

<span data-ttu-id="135ac-534">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-534">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-535">**Par défaut**</span><span class="sxs-lookup"><span data-stu-id="135ac-535">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-536">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-536">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-537">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-538">Si la **valeur est true**, l’imprimante est l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="135ac-538">If **TRUE**, the printer is the default printer.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-539">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="135ac-539">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-540">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-540">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-541">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-542">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**Capacités**»)</span><span class="sxs-lookup"><span data-stu-id="135ac-542">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-543">Tableau des fonctionnalités d’imprimante utilisées par défaut.</span><span class="sxs-lookup"><span data-stu-id="135ac-543">Array of the printer capabilities used by default.</span></span> <span data-ttu-id="135ac-544">Chaque entrée du tableau **DefaultCapabilities** doit également être listée dans le tableau **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="135ac-544">Each entry in the **DefaultCapabilities** array must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="135ac-545">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-545">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="135ac-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="135ac-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impression des couleurs** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="135ac-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impression recto-verso** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="135ac-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="135ac-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Classement** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="135ac-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Agrafage** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="135ac-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impression** de la transparence (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="135ac-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Poinçon** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="135ac-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Couverture** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="135ac-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Liaison** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="135ac-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impression en noir et blanc** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="135ac-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un côté** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-559">One-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-559">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="135ac-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bord long** recto-verso (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-561">Bord long Two-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-561">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="135ac-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bord à deux côtés** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-563">Bord Two-Sided</span><span class="sxs-lookup"><span data-stu-id="135ac-563">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="135ac-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="135ac-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paysage** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="135ac-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Portrait inversé** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="135ac-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paysage inversé** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="135ac-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualité élevée** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="135ac-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualité normale** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="135ac-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualité faible** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-571">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="135ac-571">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-572">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-572">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-573">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-574">Nombre de copies produites pour un travail, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="135ac-574">Number of copies produced for one job—unless otherwise specified.</span></span>

<span data-ttu-id="135ac-575">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-575">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-576">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="135ac-576">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-577">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-577">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-578">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-579">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). LanguagesSupported ","**\_ imprimante CIM**.**DefaultMimeType**")</span><span class="sxs-lookup"><span data-stu-id="135ac-579">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**DefaultMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-580">Langue de l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="135ac-580">Default printer language.</span></span> <span data-ttu-id="135ac-581">La langue répertoriée ici doit également être répertoriée dans la propriété **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="135ac-581">The language listed here must also be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="135ac-582">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-582">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="135ac-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="135ac-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="135ac-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="135ac-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="135ac-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="135ac-590"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="135ac-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="135ac-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="135ac-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="135ac-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="135ac-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpression** (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="135ac-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="135ac-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Données de ligne** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-598">LineData</span><span class="sxs-lookup"><span data-stu-id="135ac-598">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="135ac-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-600">DODCA</span><span class="sxs-lookup"><span data-stu-id="135ac-600">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="135ac-601"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="135ac-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="135ac-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="135ac-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="135ac-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="135ac-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="135ac-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="135ac-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="135ac-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="135ac-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="135ac-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="135ac-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="135ac-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="135ac-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="135ac-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="135ac-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="135ac-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="135ac-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="135ac-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="135ac-613"><span id="CPAP"></span><span id="cpap"></span>**Pression positive** (29)</span><span class="sxs-lookup"><span data-stu-id="135ac-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="135ac-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="135ac-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="135ac-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texte simple** (31)</span><span class="sxs-lookup"><span data-stu-id="135ac-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-616">SimpleText</span><span class="sxs-lookup"><span data-stu-id="135ac-616">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="135ac-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="135ac-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="135ac-618"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="135ac-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="135ac-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressionne** (34)</span><span class="sxs-lookup"><span data-stu-id="135ac-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="135ac-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="135ac-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="135ac-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="135ac-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="135ac-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="135ac-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="135ac-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique** (38)</span><span class="sxs-lookup"><span data-stu-id="135ac-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="135ac-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span><span class="sxs-lookup"><span data-stu-id="135ac-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="135ac-625"><span id="LIPS"></span><span id="lips"></span>**Lèvres** (40)</span><span class="sxs-lookup"><span data-stu-id="135ac-625"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="135ac-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="135ac-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="135ac-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span><span class="sxs-lookup"><span data-stu-id="135ac-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="135ac-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Majuscules** (43)</span><span class="sxs-lookup"><span data-stu-id="135ac-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="135ac-629"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="135ac-629"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="135ac-630"><span id="LCDS"></span><span id="lcds"></span>**Écrans plats** (45)</span><span class="sxs-lookup"><span data-stu-id="135ac-630"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="135ac-631"><span id="XES"></span><span id="xes"></span>**X** (46)</span><span class="sxs-lookup"><span data-stu-id="135ac-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="135ac-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="135ac-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="135ac-633">48</span><span class="sxs-lookup"><span data-stu-id="135ac-633">48</span></span>
</dt> <dd>

<span data-ttu-id="135ac-634">XPS</span><span class="sxs-lookup"><span data-stu-id="135ac-634">XPS</span></span>

</dd> <dt>

<span data-ttu-id="135ac-635">49</span><span class="sxs-lookup"><span data-stu-id="135ac-635">49</span></span>
</dt> <dd>

<span data-ttu-id="135ac-636">HPGL2</span><span class="sxs-lookup"><span data-stu-id="135ac-636">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="135ac-637">50</span><span class="sxs-lookup"><span data-stu-id="135ac-637">50</span></span>
</dt> <dd>

<span data-ttu-id="135ac-638">PCLXL</span><span class="sxs-lookup"><span data-stu-id="135ac-638">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-639">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="135ac-639">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-640">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-641">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-642">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="135ac-642">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-643">Type MIME en cours d’utilisation, si la valeur **DefaultLanguage** est un type MIME (valeur = 47).</span><span class="sxs-lookup"><span data-stu-id="135ac-643">MIME type currently being used, if the **DefaultLanguage** value is a MIME type (value = 47).</span></span>

<span data-ttu-id="135ac-644">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-644">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-645">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="135ac-645">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-646">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-646">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-647">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-648">Nombre de pages de flux d’impression rendues par l’imprimante sur une feuille de support, sauf si une tâche le spécifie autrement.</span><span class="sxs-lookup"><span data-stu-id="135ac-648">Number of print-stream pages that the printer renders on one media sheet—unless a job specifies otherwise.</span></span>

<span data-ttu-id="135ac-649">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-649">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-650">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="135ac-650">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-651">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-652">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-653">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="135ac-653">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-654">Type de papier utilisé par l’imprimante, à moins qu’un travail d’impression spécifie un type de papier différent.</span><span class="sxs-lookup"><span data-stu-id="135ac-654">Paper type that the printer uses—unless a print job specifies a different paper type.</span></span> <span data-ttu-id="135ac-655">La chaîne doit être exprimée sous la forme spécifiée par l’application d’impression de documents ISO/IEC 1017 (DPA), qui est résumée dans l’annexe C de la [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (MIB de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="135ac-655">The string must be expressed in the form specified by ISO/IEC 1017 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span>

<span data-ttu-id="135ac-656">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-656">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-657">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="135ac-657">**DefaultPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-658">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-658">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-659">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-659">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-660">Valeur de priorité par défaut assignée à chaque travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="135ac-660">Default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-661">**Description**</span><span class="sxs-lookup"><span data-stu-id="135ac-661">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-662">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-663">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-664">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="135ac-664">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-665">Description d’un objet.</span><span class="sxs-lookup"><span data-stu-id="135ac-665">Description of an object.</span></span>

<span data-ttu-id="135ac-666">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-666">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-667">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="135ac-667">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-668">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-668">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-669">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-669">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-670">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB. \|Imprimante IETF-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="135ac-670">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-671">Informations sur l’erreur de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-671">Printer error information.</span></span>

<span data-ttu-id="135ac-672">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-672">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-673">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="135ac-673">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-674">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-674">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="135ac-675">**Aucune erreur** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-675">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="135ac-676">**Papier faible** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-676">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="135ac-677">**Aucun papier** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-677">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="135ac-678">**Toner faible** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-678">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="135ac-679">**Aucun toner** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-679">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="135ac-680">**Porte ouverte** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-680">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="135ac-681">**Coincé** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-681">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="135ac-682">**Hors connexion** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-682">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="135ac-683">**Service demandé** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-683">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="135ac-684">**Bac de sortie complet** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-684">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-685">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="135ac-685">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-686">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-687">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-688">Qualificateurs : [ **\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="135ac-688">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="135ac-689">Identificateur unique de l’imprimante sur un système.</span><span class="sxs-lookup"><span data-stu-id="135ac-689">Unique identifier of the printer on a system.</span></span>

<span data-ttu-id="135ac-690">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-690">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-691">**Direct**</span><span class="sxs-lookup"><span data-stu-id="135ac-691">**Direct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-692">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-692">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-693">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-693">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-694">Si la **valeur est true**, le travail d’impression est envoyé directement à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-694">If **TRUE**, the print job is sent directly to the printer.</span></span> <span data-ttu-id="135ac-695">Si la **valeur est false**, le travail d’impression est mis en attente.</span><span class="sxs-lookup"><span data-stu-id="135ac-695">If **FALSE**, the print job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-696">**DoCompleteFirst**</span><span class="sxs-lookup"><span data-stu-id="135ac-696">**DoCompleteFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-697">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-697">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-698">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-698">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-699">Si la **valeur est true**, l’imprimante démarre les travaux qui sont terminés.</span><span class="sxs-lookup"><span data-stu-id="135ac-699">If **TRUE**, the printer starts jobs that are finished spooling.</span></span> <span data-ttu-id="135ac-700">Si la **valeur est false**, l’imprimante démarre les travaux dans l’ordre dans lequel les travaux sont reçus.</span><span class="sxs-lookup"><span data-stu-id="135ac-700">If **FALSE**, the printer starts jobs in the order that the jobs are received.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-701">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="135ac-701">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-702">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-702">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-703">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-703">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-704">Nom du pilote d’imprimante Windows.</span><span class="sxs-lookup"><span data-stu-id="135ac-704">Name of the Windows printer driver.</span></span>

<span data-ttu-id="135ac-705">Exemple : pilote de télécopie Windows</span><span class="sxs-lookup"><span data-stu-id="135ac-705">Example: Windows Fax Driver</span></span>

</dd> <dt>

<span data-ttu-id="135ac-706">**EnableBIDI**</span><span class="sxs-lookup"><span data-stu-id="135ac-706">**EnableBIDI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-707">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-707">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-708">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-708">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-709">Si la **valeur est true**, l’imprimante peut imprimer de manière bidirectionnelle.</span><span class="sxs-lookup"><span data-stu-id="135ac-709">If **TRUE**, the printer can print bidirectionally.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-710">**EnableDevQueryPrint**</span><span class="sxs-lookup"><span data-stu-id="135ac-710">**EnableDevQueryPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-711">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-711">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-712">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-712">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-713">Si la **valeur est true**, l’imprimante conserve les documents dans la file d’attente lorsque les configurations du document et de l’imprimante ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="135ac-713">If **TRUE**, the printer holds documents in the queue when document and printer setups do not match.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-714">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="135ac-714">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-715">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-715">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-716">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-716">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-717">Si la **valeur est true**, l’erreur signalée dans **LastErrorCode** a été effacée.</span><span class="sxs-lookup"><span data-stu-id="135ac-717">If **TRUE**, the error reported in **LastErrorCode** has been cleared.</span></span>

<span data-ttu-id="135ac-718">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-718">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-719">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="135ac-719">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-720">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-720">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-721">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-721">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-722">Informations sur l’erreur enregistrée dans **LastErrorCode**, et informations sur les actions correctives qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="135ac-722">Information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="135ac-723">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-723">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-724">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="135ac-724">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-725">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-725">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-726">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-726">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="135ac-727">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md).**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="135ac-727">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-728">Tableau d’informations supplémentaires pour l’état d’erreur actuel indiqué dans **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="135ac-728">Array of supplemental information for the current error state indicated in **DetectedErrorState**.</span></span>

<span data-ttu-id="135ac-729">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-729">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-730">**ExtendedDetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="135ac-730">**ExtendedDetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-731">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-731">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-732">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-732">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-733">Signale des informations d’erreur standard.</span><span class="sxs-lookup"><span data-stu-id="135ac-733">Reports standard error information.</span></span> <span data-ttu-id="135ac-734">Des informations supplémentaires doivent être enregistrées dans **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="135ac-734">Additional information should be recorded in **DetectedErrorState**.</span></span>

<span data-ttu-id="135ac-735">Les valeurs sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="135ac-735">Values are:</span></span>

<dt>

<span data-ttu-id="135ac-736">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="135ac-736">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-737">Unknown</span><span class="sxs-lookup"><span data-stu-id="135ac-737">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="135ac-738">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="135ac-738">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-739">Autres</span><span class="sxs-lookup"><span data-stu-id="135ac-739">Other</span></span>

</dd> <dt>

<span data-ttu-id="135ac-740">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="135ac-740">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-741">Aucune erreur</span><span class="sxs-lookup"><span data-stu-id="135ac-741">No Error</span></span>

</dd> <dt>

<span data-ttu-id="135ac-742">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="135ac-742">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-743">Niveau de papier faible</span><span class="sxs-lookup"><span data-stu-id="135ac-743">Low Paper</span></span>

</dd> <dt>

<span data-ttu-id="135ac-744">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="135ac-744">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-745">Plus de papier</span><span class="sxs-lookup"><span data-stu-id="135ac-745">No Paper</span></span>

</dd> <dt>

<span data-ttu-id="135ac-746">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="135ac-746">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-747">Niveau de toner faible</span><span class="sxs-lookup"><span data-stu-id="135ac-747">Low Toner</span></span>

</dd> <dt>

<span data-ttu-id="135ac-748">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="135ac-748">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-749">Il n'y a plus d'encre</span><span class="sxs-lookup"><span data-stu-id="135ac-749">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="135ac-750">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="135ac-750">7 (0x7)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-751">Capot ouvert</span><span class="sxs-lookup"><span data-stu-id="135ac-751">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="135ac-752">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="135ac-752">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-753">Bourrage papier</span><span class="sxs-lookup"><span data-stu-id="135ac-753">Jammed</span></span>

</dd> <dt>

<span data-ttu-id="135ac-754">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="135ac-754">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-755">Entretien nécessaire</span><span class="sxs-lookup"><span data-stu-id="135ac-755">Service Requested</span></span>

</dd> <dt>

<span data-ttu-id="135ac-756">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="135ac-756">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-757">Bac de réception plein</span><span class="sxs-lookup"><span data-stu-id="135ac-757">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="135ac-758">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="135ac-758">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-759">Problème de papier</span><span class="sxs-lookup"><span data-stu-id="135ac-759">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="135ac-760">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="135ac-760">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-761">Impossible d’imprimer la page</span><span class="sxs-lookup"><span data-stu-id="135ac-761">Cannot Print Page</span></span>

</dd> <dt>

<span data-ttu-id="135ac-762">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="135ac-762">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-763">Intervention de l’utilisateur requise</span><span class="sxs-lookup"><span data-stu-id="135ac-763">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="135ac-764">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="135ac-764">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-765">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="135ac-765">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="135ac-766">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="135ac-766">15 (0xF)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-767">Serveur inconnu</span><span class="sxs-lookup"><span data-stu-id="135ac-767">Server Unknown</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-768">**ExtendedPrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="135ac-768">**ExtendedPrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-769">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-769">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-770">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-770">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-771">Informations d’État pour une imprimante qui diffèrent de celles spécifiées dans la propriété **Availability** .</span><span class="sxs-lookup"><span data-stu-id="135ac-771">Status information for a printer that is different from information specified in the **Availability** property.</span></span>

<dt>

<span data-ttu-id="135ac-772">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="135ac-772">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-773">Autres</span><span class="sxs-lookup"><span data-stu-id="135ac-773">Other</span></span>

</dd> <dt>

<span data-ttu-id="135ac-774">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="135ac-774">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-775">Unknown</span><span class="sxs-lookup"><span data-stu-id="135ac-775">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="135ac-776">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="135ac-776">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-777">Idle</span><span class="sxs-lookup"><span data-stu-id="135ac-777">Idle</span></span>

</dd> <dt>

<span data-ttu-id="135ac-778">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="135ac-778">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-779">Impression</span><span class="sxs-lookup"><span data-stu-id="135ac-779">Printing</span></span>

</dd> <dt>

<span data-ttu-id="135ac-780">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="135ac-780">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-781">Préchauffage</span><span class="sxs-lookup"><span data-stu-id="135ac-781">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="135ac-782">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="135ac-782">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-783">Impression arrêtée</span><span class="sxs-lookup"><span data-stu-id="135ac-783">Stopped Printing</span></span>

</dd> <dt>

<span data-ttu-id="135ac-784">7</span><span class="sxs-lookup"><span data-stu-id="135ac-784">7</span></span>
</dt> <dd>

<span data-ttu-id="135ac-785">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="135ac-785">Offline</span></span>

</dd> <dt>

<span data-ttu-id="135ac-786">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="135ac-786">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-787">Suspendu</span><span class="sxs-lookup"><span data-stu-id="135ac-787">Paused</span></span>

</dd> <dt>

<span data-ttu-id="135ac-788">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="135ac-788">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-789">Error</span><span class="sxs-lookup"><span data-stu-id="135ac-789">Error</span></span>

</dd> <dt>

<span data-ttu-id="135ac-790">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="135ac-790">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-791">Busy</span><span class="sxs-lookup"><span data-stu-id="135ac-791">Busy</span></span>

</dd> <dt>

<span data-ttu-id="135ac-792">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="135ac-792">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-793">Non disponible</span><span class="sxs-lookup"><span data-stu-id="135ac-793">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="135ac-794">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="135ac-794">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-795">En attente</span><span class="sxs-lookup"><span data-stu-id="135ac-795">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="135ac-796">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="135ac-796">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-797">Traitement en cours</span><span class="sxs-lookup"><span data-stu-id="135ac-797">Processing</span></span>

</dd> <dt>

<span data-ttu-id="135ac-798">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="135ac-798">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-799">Initialisation</span><span class="sxs-lookup"><span data-stu-id="135ac-799">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="135ac-800">15</span><span class="sxs-lookup"><span data-stu-id="135ac-800">15</span></span>
</dt> <dd>

<span data-ttu-id="135ac-801">Économie d’énergie</span><span class="sxs-lookup"><span data-stu-id="135ac-801">Power Save</span></span>

</dd> <dt>

<span data-ttu-id="135ac-802">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="135ac-802">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-803">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="135ac-803">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="135ac-804">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="135ac-804">17 (0x11)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-805">E/s actives</span><span class="sxs-lookup"><span data-stu-id="135ac-805">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="135ac-806">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="135ac-806">18 (0x12)</span></span>
</dt> <dd>

<span data-ttu-id="135ac-807">Alimentation manuelle</span><span class="sxs-lookup"><span data-stu-id="135ac-807">Manual Feed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-808">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="135ac-808">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-809">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-809">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-810">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-810">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-811">Si la **valeur est true**, l’imprimante est masquée pour les utilisateurs du réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-811">If **TRUE**, the printer is hidden from network users.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-812">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="135ac-812">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-813">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-813">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-814">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-814">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-815">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unités**](../wmisdk/standard-qualifiers.md) ("pixels par pouce")</span><span class="sxs-lookup"><span data-stu-id="135ac-815">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-816">Résolution horizontale de l’imprimante (en pixels par pouce).</span><span class="sxs-lookup"><span data-stu-id="135ac-816">Horizontal resolution of the printer—in pixels per inch.</span></span>

<span data-ttu-id="135ac-817">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-817">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-818">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="135ac-818">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-819">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="135ac-819">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-820">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-820">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-821">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="135ac-821">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-822">Date et heure d’installation d’un objet.</span><span class="sxs-lookup"><span data-stu-id="135ac-822">Date and time an object was installed.</span></span> <span data-ttu-id="135ac-823">L’objet peut être installé sans qu’une valeur ne soit écrite dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="135ac-823">The object may be installed without a value being written to this property.</span></span> <span data-ttu-id="135ac-824">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-824">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-825">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="135ac-825">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-826">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-826">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-827">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-827">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-828">Qualificateurs : **compteur**</span><span class="sxs-lookup"><span data-stu-id="135ac-828">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="135ac-829">Nombre de travaux d’impression depuis la dernière réinitialisation de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-829">Number of print jobs since the printer was last reset.</span></span>

<span data-ttu-id="135ac-830">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-830">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-831">**KeepPrintedJobs**</span><span class="sxs-lookup"><span data-stu-id="135ac-831">**KeepPrintedJobs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-832">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-832">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-833">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-833">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-834">Si la **valeur est true**, le spouleur d’impression ne supprime pas les travaux terminés.</span><span class="sxs-lookup"><span data-stu-id="135ac-834">If **TRUE**, the print spooler does not delete the completed jobs.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-835">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="135ac-835">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-836">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-836">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-837">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-837">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-838">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ printservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="135ac-838">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-839">Tableau des langues d’impression prises en charge en mode natif.</span><span class="sxs-lookup"><span data-stu-id="135ac-839">Array of the print languages natively supported.</span></span>

<span data-ttu-id="135ac-840">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-840">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="135ac-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="135ac-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="135ac-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="135ac-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="135ac-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="135ac-848"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="135ac-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="135ac-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="135ac-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="135ac-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="135ac-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpression** (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="135ac-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="135ac-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Données de ligne** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-856">LineData</span><span class="sxs-lookup"><span data-stu-id="135ac-856">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="135ac-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-858">DODCA</span><span class="sxs-lookup"><span data-stu-id="135ac-858">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="135ac-859"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="135ac-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="135ac-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="135ac-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="135ac-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="135ac-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="135ac-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="135ac-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="135ac-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="135ac-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="135ac-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="135ac-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="135ac-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="135ac-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="135ac-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="135ac-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="135ac-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="135ac-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="135ac-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="135ac-871"><span id="CPAP"></span><span id="cpap"></span>**Pression positive** (29)</span><span class="sxs-lookup"><span data-stu-id="135ac-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="135ac-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="135ac-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="135ac-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texte simple** (31)</span><span class="sxs-lookup"><span data-stu-id="135ac-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-874">SimpleText</span><span class="sxs-lookup"><span data-stu-id="135ac-874">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="135ac-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="135ac-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="135ac-876"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="135ac-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="135ac-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressionne** (34)</span><span class="sxs-lookup"><span data-stu-id="135ac-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="135ac-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="135ac-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="135ac-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="135ac-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="135ac-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="135ac-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="135ac-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique** (38)</span><span class="sxs-lookup"><span data-stu-id="135ac-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="135ac-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span><span class="sxs-lookup"><span data-stu-id="135ac-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="135ac-883"><span id="LIPS"></span><span id="lips"></span>**Lèvres** (40)</span><span class="sxs-lookup"><span data-stu-id="135ac-883"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="135ac-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="135ac-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="135ac-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span><span class="sxs-lookup"><span data-stu-id="135ac-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="135ac-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Majuscules** (43)</span><span class="sxs-lookup"><span data-stu-id="135ac-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="135ac-887"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="135ac-887"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="135ac-888"><span id="LCDS"></span><span id="lcds"></span>**Écrans plats** (45)</span><span class="sxs-lookup"><span data-stu-id="135ac-888"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="135ac-889"><span id="XES"></span><span id="xes"></span>**X** (46)</span><span class="sxs-lookup"><span data-stu-id="135ac-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="135ac-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="135ac-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="135ac-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="135ac-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="135ac-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="135ac-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="135ac-893"><span id="PCLXL"></span><span id="pclxl"></span>**Pclxl** (50)</span><span class="sxs-lookup"><span data-stu-id="135ac-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-894">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="135ac-894">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-895">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-895">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-896">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-896">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-897">Dernier code d’erreur signalé par l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="135ac-897">Last error code that the logical device reports.</span></span>

<span data-ttu-id="135ac-898">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-898">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-899">**Local**</span><span class="sxs-lookup"><span data-stu-id="135ac-899">**Local**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-900">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-900">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-901">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-901">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-902">Si la **valeur est true**, l’imprimante n’est pas attachée à un réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-902">If **TRUE**, the printer is not attached to a network.</span></span> <span data-ttu-id="135ac-903">Si les propriétés **local** et **réseau** ont toutes les deux la valeur **true**, l’imprimante est une imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-903">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-904">**Lieu**</span><span class="sxs-lookup"><span data-stu-id="135ac-904">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-905">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-905">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-906">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-906">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-907">Emplacement physique de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-907">Physical location of the printer.</span></span>

<span data-ttu-id="135ac-908">Exemple : Bldg.</span><span class="sxs-lookup"><span data-stu-id="135ac-908">Example: Bldg.</span></span> <span data-ttu-id="135ac-909">38, salle 1164</span><span class="sxs-lookup"><span data-stu-id="135ac-909">38, Room 1164</span></span>

</dd> <dt>

<span data-ttu-id="135ac-910">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="135ac-910">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-911">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-911">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-912">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-913">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="135ac-913">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-914">Marquage de la technologie utilisée par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-914">Marking technology the printer uses.</span></span>

<span data-ttu-id="135ac-915">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-915">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-916">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-916">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-917">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-917">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="135ac-918">**LED électrophotographique** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-918">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="135ac-919">**Laser électrophotographique** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-919">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="135ac-920">**Électrophotographique autre** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-920">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="135ac-921">**Impact sur le déplacement de la matrice point-tête 9** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-921">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="135ac-922">**Impact sur le déplacement de la matrice point-tête 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-922">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="135ac-923">**Impact-déplacement de la matrice des points en-tête** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-923">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="135ac-924">**Impact du déplacement de la tête en forme complète** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-924">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="135ac-925">**Bande d’impact** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-925">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="135ac-926">**Impact sur Other** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-926">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="135ac-927">**Jet d’encre aqueux** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-927">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="135ac-928">**Jet d’encre solide** (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-928">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="135ac-929">**Autre encre** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-929">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="135ac-930">**Stylet** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-930">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="135ac-931">**Transfert thermique** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-931">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="135ac-932">**Sensibilité thermique** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-932">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="135ac-933">**Diffusion thermique** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-933">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="135ac-934">**Autre température** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-934">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="135ac-935">**Electroerosion** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-935">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="135ac-936">**Électrostatique** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-936">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="135ac-937">**Microfiche photographique** (22)</span><span class="sxs-lookup"><span data-stu-id="135ac-937">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="135ac-938">**Photocomposeuse photo** (23)</span><span class="sxs-lookup"><span data-stu-id="135ac-938">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="135ac-939">**Photographie autre** (24)</span><span class="sxs-lookup"><span data-stu-id="135ac-939">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="135ac-940">**Déposition d’ions** (25)</span><span class="sxs-lookup"><span data-stu-id="135ac-940">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="135ac-941">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="135ac-941">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="135ac-942">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="135ac-942">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-943">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="135ac-943">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-944">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-944">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-945">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-945">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-946">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. copies")</span><span class="sxs-lookup"><span data-stu-id="135ac-946">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-947">Nombre maximal de copies que l’imprimante peut produire pour un seul travail.</span><span class="sxs-lookup"><span data-stu-id="135ac-947">Maximum number of copies the printer can produce for one job.</span></span>

<span data-ttu-id="135ac-948">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-948">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-949">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="135ac-949">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-950">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-950">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-951">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-952">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="135ac-952">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-953">Nombre maximal de pages de flux d’impression que l’imprimante peut afficher sur une feuille de support, par exemple un papier.</span><span class="sxs-lookup"><span data-stu-id="135ac-953">Maximum number of print-stream pages the printer can render on one media sheet, such as paper.</span></span>

<span data-ttu-id="135ac-954">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-954">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-955">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="135ac-955">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-956">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-956">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-957">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-958">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (« CIM \_ PrintJob. Jobs »), [**unités**](../wmisdk/standard-qualifiers.md) (« kilo-octets »)</span><span class="sxs-lookup"><span data-stu-id="135ac-958">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-959">Plus grande tâche en tant que flux d’octets, en kilo-octets, que l’imprimante peut accepter.</span><span class="sxs-lookup"><span data-stu-id="135ac-959">Largest job as a byte stream, in kilobytes, that the printer can accept.</span></span> <span data-ttu-id="135ac-960">La valeur 0 (zéro) indique qu’aucune limite n’est définie.</span><span class="sxs-lookup"><span data-stu-id="135ac-960">A value of 0 (zero) indicates that no limit is set.</span></span>

<span data-ttu-id="135ac-961">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-961">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-962">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="135ac-962">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-963">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-963">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-964">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-964">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-965">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ imprimante CIM**](cim-printer.md). LanguagesSupported "," CIM \_ PrintJob. mimeTypes "," CIM \_ printservice. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="135ac-965">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-966">Tableau d’explications détaillées sur les types MIME que l’imprimante prend en charge.</span><span class="sxs-lookup"><span data-stu-id="135ac-966">Array of detailed MIME-type explanations that the printer supports.</span></span> <span data-ttu-id="135ac-967">Si des données sont fournies, la valeur 47 (« MIME ») doit être incluse dans la propriété **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="135ac-967">If data is provided, then the value 47 ("MIME") must be included in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="135ac-968">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-968">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-969">**Nom**</span><span class="sxs-lookup"><span data-stu-id="135ac-969">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-970">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-970">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-971">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-971">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-972">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="135ac-972">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-973">Nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-973">Name of the printer.</span></span>

<span data-ttu-id="135ac-974">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-974">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-975">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="135ac-975">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-976">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-976">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-977">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-977">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-978">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="135ac-978">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-979">Tableau de langues prises en charge pour les chaînes utilisées par l’imprimante pour la sortie des informations de gestion.</span><span class="sxs-lookup"><span data-stu-id="135ac-979">Array of languages supported for strings that the printer uses for output of management information.</span></span> <span data-ttu-id="135ac-980">Doit être conforme à la [norme RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span><span class="sxs-lookup"><span data-stu-id="135ac-980">Must conform to [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span></span> <span data-ttu-id="135ac-981">Par exemple, « fr » est utilisé pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="135ac-981">For example, "en" is used for English.</span></span>

<span data-ttu-id="135ac-982">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-982">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-983">**Réseau**</span><span class="sxs-lookup"><span data-stu-id="135ac-983">**Network**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-984">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-984">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-985">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-985">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-986">Si la **valeur est true**, l’imprimante est une imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-986">If **TRUE**, the printer is a network printer.</span></span> <span data-ttu-id="135ac-987">Si les propriétés **local** et **réseau** ont toutes les deux la valeur **true**, l’imprimante est une imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-987">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-988">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="135ac-988">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-989">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-989">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-990">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-990">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-991">Tableau des types de papier pris en charge par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-991">Array of the paper types that the printer supports.</span></span>

<span data-ttu-id="135ac-992">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-992">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="135ac-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="135ac-995"><span id="A"></span><span id="a"></span>**A** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-995"><span id="A"></span><span id="a"></span>**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="135ac-996"><span id="B"></span><span id="b"></span>**B** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-996"><span id="B"></span><span id="b"></span>**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="135ac-997"><span id="C"></span><span id="c"></span>**C** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-997"><span id="C"></span><span id="c"></span>**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="135ac-998"><span id="D"></span><span id="d"></span>**D** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-998"><span id="D"></span><span id="d"></span>**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="135ac-999"><span id="E"></span><span id="e"></span>**E** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-999"><span id="E"></span><span id="e"></span>**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="135ac-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Lettre** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="135ac-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Légal** (8)</span><span class="sxs-lookup"><span data-stu-id="135ac-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="135ac-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-Envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="135ac-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="135ac-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-Envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="135ac-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="135ac-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-Number-10-enveloppe** (11)</span><span class="sxs-lookup"><span data-stu-id="135ac-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="135ac-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Na-7x9-Envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="135ac-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="135ac-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Na-9x11-Envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="135ac-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="135ac-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-Envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="135ac-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="135ac-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-Number-9-enveloppe** (15)</span><span class="sxs-lookup"><span data-stu-id="135ac-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="135ac-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-Envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="135ac-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="135ac-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-Envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="135ac-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="135ac-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="135ac-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="135ac-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="135ac-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="135ac-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="135ac-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="135ac-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="135ac-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="135ac-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="135ac-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="135ac-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="135ac-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="135ac-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="135ac-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="135ac-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="135ac-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="135ac-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="135ac-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="135ac-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="135ac-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="135ac-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="135ac-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="135ac-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="135ac-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="135ac-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="135ac-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="135ac-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="135ac-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="135ac-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="135ac-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="135ac-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="135ac-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="135ac-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="135ac-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="135ac-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="135ac-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="135ac-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="135ac-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="135ac-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="135ac-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="135ac-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="135ac-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="135ac-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="135ac-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="135ac-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="135ac-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="135ac-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="135ac-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1035">C2</span><span class="sxs-lookup"><span data-stu-id="135ac-1035">C2</span></span>

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="135ac-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="135ac-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1037">C3</span><span class="sxs-lookup"><span data-stu-id="135ac-1037">C3</span></span>

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="135ac-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="135ac-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1039">C4</span><span class="sxs-lookup"><span data-stu-id="135ac-1039">C4</span></span>

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="135ac-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="135ac-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1041">C5</span><span class="sxs-lookup"><span data-stu-id="135ac-1041">C5</span></span>

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="135ac-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="135ac-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1043">C6</span><span class="sxs-lookup"><span data-stu-id="135ac-1043">C6</span></span>

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="135ac-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="135ac-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1045">C7</span><span class="sxs-lookup"><span data-stu-id="135ac-1045">C7</span></span>

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="135ac-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Désignée ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="135ac-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-Designated** (47)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1047">C8</span><span class="sxs-lookup"><span data-stu-id="135ac-1047">C8</span></span>

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="135ac-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="135ac-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1049">ISO-Designated</span><span class="sxs-lookup"><span data-stu-id="135ac-1049">ISO-Designated</span></span>

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="135ac-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="135ac-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1051">JIS B0</span><span class="sxs-lookup"><span data-stu-id="135ac-1051">JIS B0</span></span>

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="135ac-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="135ac-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1053">JIS B1</span><span class="sxs-lookup"><span data-stu-id="135ac-1053">JIS B1</span></span>

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="135ac-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="135ac-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1055">JIS B2</span><span class="sxs-lookup"><span data-stu-id="135ac-1055">JIS B2</span></span>

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="135ac-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="135ac-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1057">JIS B3</span><span class="sxs-lookup"><span data-stu-id="135ac-1057">JIS B3</span></span>

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="135ac-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="135ac-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1059">JIS B4</span><span class="sxs-lookup"><span data-stu-id="135ac-1059">JIS B4</span></span>

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="135ac-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="135ac-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1061">JIS B5</span><span class="sxs-lookup"><span data-stu-id="135ac-1061">JIS B5</span></span>

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="135ac-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="135ac-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1063">JIS B6</span><span class="sxs-lookup"><span data-stu-id="135ac-1063">JIS B6</span></span>

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="135ac-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="135ac-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1065">JIS B7</span><span class="sxs-lookup"><span data-stu-id="135ac-1065">JIS B7</span></span>

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="135ac-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="135ac-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1067">JIS B8</span><span class="sxs-lookup"><span data-stu-id="135ac-1067">JIS B8</span></span>

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="135ac-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="135ac-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1069">JIS B9</span><span class="sxs-lookup"><span data-stu-id="135ac-1069">JIS B9</span></span>

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="135ac-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Lettre na** (59)</span><span class="sxs-lookup"><span data-stu-id="135ac-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1071">JIS B10</span><span class="sxs-lookup"><span data-stu-id="135ac-1071">JIS B10</span></span>

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="135ac-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-Legal** (60)</span><span class="sxs-lookup"><span data-stu-id="135ac-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="135ac-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-enveloppe** (61)</span><span class="sxs-lookup"><span data-stu-id="135ac-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="135ac-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-enveloppe** (62)</span><span class="sxs-lookup"><span data-stu-id="135ac-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="135ac-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-enveloppe** (63)</span><span class="sxs-lookup"><span data-stu-id="135ac-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="135ac-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-enveloppe** (64)</span><span class="sxs-lookup"><span data-stu-id="135ac-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="135ac-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-enveloppe** (65)</span><span class="sxs-lookup"><span data-stu-id="135ac-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="135ac-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-enveloppe** (66)</span><span class="sxs-lookup"><span data-stu-id="135ac-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="135ac-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Enveloppe indiquée-long** (67)</span><span class="sxs-lookup"><span data-stu-id="135ac-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="135ac-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-enveloppe** (68)</span><span class="sxs-lookup"><span data-stu-id="135ac-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="135ac-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span><span class="sxs-lookup"><span data-stu-id="135ac-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="135ac-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span><span class="sxs-lookup"><span data-stu-id="135ac-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="135ac-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Facture** (71)</span><span class="sxs-lookup"><span data-stu-id="135ac-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="135ac-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Grand livre** (72)</span><span class="sxs-lookup"><span data-stu-id="135ac-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="135ac-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Papier Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="135ac-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-1086">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="135ac-1086">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1087">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-1087">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1088">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1088">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1089">Qualificateurs : [**arrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ printservice. PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="135ac-1089">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1090">Tableau de types de papier actuellement disponibles sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1090">Array of paper types that are currently available on the printer.</span></span> <span data-ttu-id="135ac-1091">Chaque chaîne doit être exprimée dans le format spécifié par l’application d’impression des documents ISO/IEC 10175 (DPA), qui est résumée dans l’annexe C de la [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (MIB de l’imprimante).</span><span class="sxs-lookup"><span data-stu-id="135ac-1091">Each string must be expressed in the format specified by ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span> <span data-ttu-id="135ac-1092">Toute taille de papier identifiée dans cette propriété doit également apparaître dans la propriété **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="135ac-1092">Any paper size identified in this property must also appear in the **PaperSizesSupported** property.</span></span>

<span data-ttu-id="135ac-1093">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1093">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<span data-ttu-id="135ac-1094">Exemple : ISO-A4-couleur</span><span class="sxs-lookup"><span data-stu-id="135ac-1094">Example: iso-a4-colored</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1095">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="135ac-1095">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1096">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1096">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1097">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1097">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1098">Paramètres facultatifs du processeur d’impression.</span><span class="sxs-lookup"><span data-stu-id="135ac-1098">Optional parameters for the print processor.</span></span>

<span data-ttu-id="135ac-1099">Exemple : « copies = 2 »</span><span class="sxs-lookup"><span data-stu-id="135ac-1099">Example: "Copies=2"</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1100">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="135ac-1100">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1101">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1101">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1102">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1102">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1103">Qualificateurs : [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="135ac-1103">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1104">Identificateur d’appareil Windows Plug-and-Play de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="135ac-1104">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="135ac-1105">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1105">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="135ac-1106">Exemple : \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="135ac-1106">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1107">**PortName**</span><span class="sxs-lookup"><span data-stu-id="135ac-1107">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1108">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1108">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1109">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1109">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1110">Port utilisé pour transmettre des données à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1110">Port that is used to transmit data to a printer.</span></span> <span data-ttu-id="135ac-1111">Si une imprimante est connectée à plusieurs ports, les noms de chaque port sont séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="135ac-1111">If a printer is connected to more than one port, the names of each port are separated by commas.</span></span>

<span data-ttu-id="135ac-1112">Exemple : LPT1 :, LPT2 :, LPT3 :</span><span class="sxs-lookup"><span data-stu-id="135ac-1112">Example: LPT1:, LPT2:, LPT3:</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1113">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="135ac-1113">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1114">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-1114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1116">Tableau des fonctionnalités d’alimentation spécifiques d’un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="135ac-1116">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="135ac-1117">Cette propriété est héritée de **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="135ac-1117">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="135ac-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="135ac-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="135ac-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="135ac-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1122">Les fonctionnalités de gestion de l’alimentation sont actuellement activées, mais le jeu de fonctionnalités exact est inconnu ou les informations ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="135ac-1122">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="135ac-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modes d’économie d’énergie entrés automatiquement** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1124">L’appareil peut modifier son état d’alimentation en fonction de l’utilisation ou d’autres critères.</span><span class="sxs-lookup"><span data-stu-id="135ac-1124">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="135ac-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**État d’alimentation définissable** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1126">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="135ac-1126">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="135ac-1127">Cette méthode se trouve sur la classe parente du **\_ LogicalDevice CIM** et peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="135ac-1127">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="135ac-1128">Pour plus d’informations, consultez [conception de Classes format MOF (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1128">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="135ac-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Cycle d’alimentation pris en charge** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1130">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation).</span><span class="sxs-lookup"><span data-stu-id="135ac-1130">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="135ac-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Mise sous tension minutée prise en charge** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1132">Power-On chronométré pris en charge</span><span class="sxs-lookup"><span data-stu-id="135ac-1132">Timed Power-On Supported</span></span>

<span data-ttu-id="135ac-1133">La méthode [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) peut être appelée avec le paramètre *PowerState* défini à 5 (cycle d’alimentation) et l' *heure* définie sur une date et une heure spécifiques, ou un intervalle, pour la mise sous tension.</span><span class="sxs-lookup"><span data-stu-id="135ac-1133">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-1134">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="135ac-1134">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-1135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1137">Si la **valeur est true**, la puissance de l’appareil peut être gérée, ce qui signifie qu’il peut être mis en mode de suspension.</span><span class="sxs-lookup"><span data-stu-id="135ac-1137">If **TRUE**, the power of the device can be managed, which means that it can be put into suspend mode.</span></span> <span data-ttu-id="135ac-1138">La propriété n’indique pas que les fonctionnalités de gestion de l’alimentation sont activées, mais uniquement que l’appareil logique est capable de gérer l’alimentation.</span><span class="sxs-lookup"><span data-stu-id="135ac-1138">The property does not indicate that power management features are enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="135ac-1139">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1140">**PrinterPaperNames**</span><span class="sxs-lookup"><span data-stu-id="135ac-1140">**PrinterPaperNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1141">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="135ac-1141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1143">Tableau de formats de papier pris en charge par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1143">Array of paper sizes supported by the printer.</span></span> <span data-ttu-id="135ac-1144">Les noms spécifiés par l’imprimante sont utilisés pour représenter les formats de papier pris en charge.</span><span class="sxs-lookup"><span data-stu-id="135ac-1144">The printer-specified names are used to represent supported paper sizes.</span></span>

<span data-ttu-id="135ac-1145">Exemple : B5 (JIS)</span><span class="sxs-lookup"><span data-stu-id="135ac-1145">Example: B5 (JIS)</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1146">**PrinterState**</span><span class="sxs-lookup"><span data-stu-id="135ac-1146">**PrinterState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-1147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1149">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="135ac-1149">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1150">L’un des États possibles associés à cette imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1150">One of the possible states relating to this printer.</span></span> <span data-ttu-id="135ac-1151">Cette propriété est obsolète.</span><span class="sxs-lookup"><span data-stu-id="135ac-1151">This property is obsolete.</span></span> <span data-ttu-id="135ac-1152">À la place de cette propriété, utilisez **PrinterStatus**.</span><span class="sxs-lookup"><span data-stu-id="135ac-1152">In place of this property, use **PrinterStatus**.</span></span>

<dt>

<span data-ttu-id="135ac-1153">0</span><span class="sxs-lookup"><span data-stu-id="135ac-1153">0</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1154">Inactif-pour plus d’informations, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="135ac-1154">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1155">1</span><span class="sxs-lookup"><span data-stu-id="135ac-1155">1</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1156">Suspendu</span><span class="sxs-lookup"><span data-stu-id="135ac-1156">Paused</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1157">2</span><span class="sxs-lookup"><span data-stu-id="135ac-1157">2</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1158">Error</span><span class="sxs-lookup"><span data-stu-id="135ac-1158">Error</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1159">3</span><span class="sxs-lookup"><span data-stu-id="135ac-1159">3</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1160">Suppression en attente</span><span class="sxs-lookup"><span data-stu-id="135ac-1160">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1161">4</span><span class="sxs-lookup"><span data-stu-id="135ac-1161">4</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1162">Bourrage papier</span><span class="sxs-lookup"><span data-stu-id="135ac-1162">Paper Jam</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1163">5</span><span class="sxs-lookup"><span data-stu-id="135ac-1163">5</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1164">Papier sortant</span><span class="sxs-lookup"><span data-stu-id="135ac-1164">Paper Out</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1165">6</span><span class="sxs-lookup"><span data-stu-id="135ac-1165">6</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1166">Alimentation manuelle</span><span class="sxs-lookup"><span data-stu-id="135ac-1166">Manual Feed</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1167">7</span><span class="sxs-lookup"><span data-stu-id="135ac-1167">7</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1168">Problème de papier</span><span class="sxs-lookup"><span data-stu-id="135ac-1168">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1169">8</span><span class="sxs-lookup"><span data-stu-id="135ac-1169">8</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1170">Hors connexion</span><span class="sxs-lookup"><span data-stu-id="135ac-1170">Offline</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1171">9</span><span class="sxs-lookup"><span data-stu-id="135ac-1171">9</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1172">E/s actives</span><span class="sxs-lookup"><span data-stu-id="135ac-1172">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1173">10</span><span class="sxs-lookup"><span data-stu-id="135ac-1173">10</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1174">Busy</span><span class="sxs-lookup"><span data-stu-id="135ac-1174">Busy</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1175">11</span><span class="sxs-lookup"><span data-stu-id="135ac-1175">11</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1176">Impression</span><span class="sxs-lookup"><span data-stu-id="135ac-1176">Printing</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1177">12</span><span class="sxs-lookup"><span data-stu-id="135ac-1177">12</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1178">Bac de réception plein</span><span class="sxs-lookup"><span data-stu-id="135ac-1178">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1179">13</span><span class="sxs-lookup"><span data-stu-id="135ac-1179">13</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1180">Non disponible</span><span class="sxs-lookup"><span data-stu-id="135ac-1180">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1181">14</span><span class="sxs-lookup"><span data-stu-id="135ac-1181">14</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1182">En attente</span><span class="sxs-lookup"><span data-stu-id="135ac-1182">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1183">15</span><span class="sxs-lookup"><span data-stu-id="135ac-1183">15</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1184">Traitement en cours</span><span class="sxs-lookup"><span data-stu-id="135ac-1184">Processing</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1185">16</span><span class="sxs-lookup"><span data-stu-id="135ac-1185">16</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1186">Initialisation</span><span class="sxs-lookup"><span data-stu-id="135ac-1186">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1187">17</span><span class="sxs-lookup"><span data-stu-id="135ac-1187">17</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1188">Préchauffage</span><span class="sxs-lookup"><span data-stu-id="135ac-1188">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1189">18</span><span class="sxs-lookup"><span data-stu-id="135ac-1189">18</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1190">Toner faible</span><span class="sxs-lookup"><span data-stu-id="135ac-1190">Toner Low</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1191">19</span><span class="sxs-lookup"><span data-stu-id="135ac-1191">19</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1192">Il n'y a plus d'encre</span><span class="sxs-lookup"><span data-stu-id="135ac-1192">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1193">20</span><span class="sxs-lookup"><span data-stu-id="135ac-1193">20</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1194">Page chargeur</span><span class="sxs-lookup"><span data-stu-id="135ac-1194">Page Punt</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1195">21</span><span class="sxs-lookup"><span data-stu-id="135ac-1195">21</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1196">Intervention de l’utilisateur requise</span><span class="sxs-lookup"><span data-stu-id="135ac-1196">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1197">22</span><span class="sxs-lookup"><span data-stu-id="135ac-1197">22</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1198">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="135ac-1198">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1199">23</span><span class="sxs-lookup"><span data-stu-id="135ac-1199">23</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1200">Capot ouvert</span><span class="sxs-lookup"><span data-stu-id="135ac-1200">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1201">24</span><span class="sxs-lookup"><span data-stu-id="135ac-1201">24</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1202">Serveur \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="135ac-1202">Server\_Unknown</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1203">25</span><span class="sxs-lookup"><span data-stu-id="135ac-1203">25</span></span>
</dt> <dd>

<span data-ttu-id="135ac-1204">Économie d’énergie</span><span class="sxs-lookup"><span data-stu-id="135ac-1204">Power Save</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-1205">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="135ac-1205">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1206">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-1206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1208">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Imprimante IETF-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="135ac-1208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1209">Informations d’État pour une imprimante qui diffèrent de celles spécifiées dans la propriété de **disponibilité** de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="135ac-1209">Status information for a printer that is different from information specified in the logical device **Availability** property.</span></span>

<span data-ttu-id="135ac-1210">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1210">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="135ac-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactif** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (3)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1214">Inactif-pour plus d’informations, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="135ac-1214">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="135ac-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Impression** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="135ac-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Préchauffage** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Warmup** (5)</span></span>


</dt> <dd>

<span data-ttu-id="135ac-1217">Préchauffage</span><span class="sxs-lookup"><span data-stu-id="135ac-1217">Warming Up</span></span>

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="135ac-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Impression arrêtée** (6)</span><span class="sxs-lookup"><span data-stu-id="135ac-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="135ac-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Hors connexion** (7)</span><span class="sxs-lookup"><span data-stu-id="135ac-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-1220">**PrintJobDataType**</span><span class="sxs-lookup"><span data-stu-id="135ac-1220">**PrintJobDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1221">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1222">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1223">Type de données d’un travail d’impression en attente du périphérique d’impression Windows.</span><span class="sxs-lookup"><span data-stu-id="135ac-1223">Data type of a print job waiting for the Windows-based printing device.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1224">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="135ac-1224">**PrintProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1227">Nom du spouleur d’impression qui gère les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="135ac-1227">Name of the print spooler that handles print jobs.</span></span>

<span data-ttu-id="135ac-1228">Exemple : SPOOLSS.DLL</span><span class="sxs-lookup"><span data-stu-id="135ac-1228">Example: SPOOLSS.DLL</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1229">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="135ac-1229">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1230">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-1230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1231">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1232">Priorité de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1232">Priority of the printer.</span></span> <span data-ttu-id="135ac-1233">Les travaux sur une imprimante de priorité supérieure sont planifiés en premier.</span><span class="sxs-lookup"><span data-stu-id="135ac-1233">Jobs on a higher priority printer are scheduled first.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1234">**Publié**</span><span class="sxs-lookup"><span data-stu-id="135ac-1234">**Published**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1235">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-1235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1236">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1237">Si la **valeur est true**, l’imprimante est publiée dans le service d’annuaire réseau.</span><span class="sxs-lookup"><span data-stu-id="135ac-1237">If **TRUE**, the printer is published in the network directory service.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1238">**Mis en file d'attente.**</span><span class="sxs-lookup"><span data-stu-id="135ac-1238">**Queued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1239">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-1239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1240">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1241">Si la **valeur est true**, l’imprimante met en mémoire tampon et met en file d’attente les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="135ac-1241">If **TRUE**, the printer buffers and queues print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1242">**RawOnly**</span><span class="sxs-lookup"><span data-stu-id="135ac-1242">**RawOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1243">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-1243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1245">Si la **valeur est true**, l’imprimante accepte uniquement les données brutes à mettre en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="135ac-1245">If **TRUE**, the printer accepts only raw data to be spooled.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1246">**SeparatorFile**</span><span class="sxs-lookup"><span data-stu-id="135ac-1246">**SeparatorFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1248">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1249">Nom du fichier utilisé pour créer une page de séparation.</span><span class="sxs-lookup"><span data-stu-id="135ac-1249">Name of the file used to create a separator page.</span></span> <span data-ttu-id="135ac-1250">Cette page est utilisée pour séparer les travaux d’impression envoyés à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1250">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1251">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="135ac-1251">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1254">Nom du serveur qui contrôle l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1254">Name of the server that controls the printer.</span></span> <span data-ttu-id="135ac-1255">Si cette chaîne est **null**, l’imprimante est contrôlée localement.</span><span class="sxs-lookup"><span data-stu-id="135ac-1255">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1256">**Partagé**</span><span class="sxs-lookup"><span data-stu-id="135ac-1256">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1257">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-1257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1258">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1258">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1259">Si la **valeur est true**, l’imprimante est disponible en tant que ressource réseau partagée.</span><span class="sxs-lookup"><span data-stu-id="135ac-1259">If **TRUE**, the printer is available as a shared network resource.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1260">**ShareName**</span><span class="sxs-lookup"><span data-stu-id="135ac-1260">**ShareName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1263">Nom de partage du périphérique d’impression Windows.</span><span class="sxs-lookup"><span data-stu-id="135ac-1263">Share name of the Windows-based printing device.</span></span>

<span data-ttu-id="135ac-1264">Exemple : « \\ \\ PRINTSERVER1 \\ .</span><span class="sxs-lookup"><span data-stu-id="135ac-1264">Example: "\\\\PRINTSERVER1\\PRINTER2"</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1265">**SpoolEnabled**</span><span class="sxs-lookup"><span data-stu-id="135ac-1265">**SpoolEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1266">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-1266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1268">Qualificateurs : [ **déconseillé**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="135ac-1268">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1269">Cette propriété est obsolète. n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="135ac-1269">This property is obsolete; do not use.</span></span> <span data-ttu-id="135ac-1270">Si la **valeur est true**, la mise en file d’attente est activée pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1270">If **TRUE**, spooling is enabled for printer.</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1271">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="135ac-1271">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1272">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="135ac-1272">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1273">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1273">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1274">Date et heure auxquelles une imprimante peut commencer à imprimer un travail : si l’imprimante est limitée à une impression à des moments spécifiques.</span><span class="sxs-lookup"><span data-stu-id="135ac-1274">Date and time that a printer can start to print a job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="135ac-1275">Cette valeur est exprimée sous la forme du temps écoulé depuis 12:00 AM GMT (heure de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="135ac-1275">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1276">**État**</span><span class="sxs-lookup"><span data-stu-id="135ac-1276">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1277">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1279">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="135ac-1279">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1280">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="135ac-1280">Current status of the object.</span></span> <span data-ttu-id="135ac-1281">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="135ac-1281">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="135ac-1282">Les États opérationnels sont les suivants : **OK**, **détérioré** et **prédit échec** (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="135ac-1282">Operational statuses include: **OK**, **Degraded**, and **Pred Fail** (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="135ac-1283">Les États qui ne sont pas opérationnels sont les suivants : **erreur**, **démarrage**, **arrêt** et **service**.</span><span class="sxs-lookup"><span data-stu-id="135ac-1283">Nonoperational statuses include: **Error**, **Starting**, **Stopping**, and **Service**.</span></span> <span data-ttu-id="135ac-1284">Cette dernière, **service**, peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="135ac-1284">The latter, **Service**, could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="135ac-1285">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni **OK** ni dans l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="135ac-1285">Not all such work is online, yet the managed element is neither **OK** nor in one of the other states.</span></span>

<span data-ttu-id="135ac-1286">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1286">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="135ac-1287">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="135ac-1287">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="135ac-1288">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1288">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="135ac-1289">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1289">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="135ac-1290">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1290">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-1291">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="135ac-1291">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="135ac-1292">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1292">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="135ac-1293">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1293">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="135ac-1294">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1294">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="135ac-1295">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1295">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="135ac-1296">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1296">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="135ac-1297">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1297">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="135ac-1298">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1298">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="135ac-1299">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="135ac-1299">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-1300">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="135ac-1300">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1301">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="135ac-1301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1303">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|État opérationnel DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="135ac-1303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1304">État de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="135ac-1304">State of the logical device.</span></span> <span data-ttu-id="135ac-1305">Si cette propriété ne s’applique pas à l’unité logique, la valeur 5 (**non applicable**) doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="135ac-1305">If this property does not apply to the logical device, the value 5 (**Not Applicable**) should be used.</span></span>

<span data-ttu-id="135ac-1306">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="135ac-1307">**Autre** (1)</span><span class="sxs-lookup"><span data-stu-id="135ac-1307">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="135ac-1308">**Inconnu** (2)</span><span class="sxs-lookup"><span data-stu-id="135ac-1308">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="135ac-1309">**Activé** (3)</span><span class="sxs-lookup"><span data-stu-id="135ac-1309">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="135ac-1310">**Désactivé** (4)</span><span class="sxs-lookup"><span data-stu-id="135ac-1310">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="135ac-1311">**Non applicable** (5)</span><span class="sxs-lookup"><span data-stu-id="135ac-1311">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="135ac-1312">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="135ac-1312">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1314">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1315">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="135ac-1315">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1316">Valeur de la propriété **CreationClassName** de l’ordinateur d’étendue.</span><span class="sxs-lookup"><span data-stu-id="135ac-1316">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="135ac-1317">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1318">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="135ac-1318">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="135ac-1319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1320">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1321">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="135ac-1321">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1322">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="135ac-1322">Name of the scoping system.</span></span>

<span data-ttu-id="135ac-1323">Cette propriété est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1324">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="135ac-1324">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1325">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="135ac-1325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1327">Date et heure de la dernière réinitialisation de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1327">Date and time the printer was last reset.</span></span>

<span data-ttu-id="135ac-1328">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1328">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1329">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="135ac-1329">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1330">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="135ac-1330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1331">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1331">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1332">Date et heure auxquelles une imprimante peut imprimer la dernière tâche : si l’imprimante est limitée à une impression à des moments spécifiques.</span><span class="sxs-lookup"><span data-stu-id="135ac-1332">Date and time that a printer can print the last job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="135ac-1333">Cette valeur est exprimée sous la forme du temps écoulé depuis 12:00 AM GMT (heure de Greenwich).</span><span class="sxs-lookup"><span data-stu-id="135ac-1333">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1334">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="135ac-1334">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1335">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="135ac-1335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1336">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="135ac-1336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1337">Qualificateurs : [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unités**](../wmisdk/standard-qualifiers.md) ("pixels par pouce")</span><span class="sxs-lookup"><span data-stu-id="135ac-1337">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1338">Résolution verticale, en pixels par pouce, de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="135ac-1338">Vertical resolution, in pixels-per-inch, of the printer.</span></span>

<span data-ttu-id="135ac-1339">Cette propriété est héritée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1339">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="135ac-1340">**WorkOffline**</span><span class="sxs-lookup"><span data-stu-id="135ac-1340">**WorkOffline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="135ac-1341">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="135ac-1341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="135ac-1342">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="135ac-1342">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="135ac-1343">Si la **valeur est true**, vous pouvez faire une mise en file d’attente des travaux d’impression sur l’ordinateur lorsque l’imprimante est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="135ac-1343">If **TRUE**, you can queue print jobs on the computer when the printer is offline.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="135ac-1344">Notes</span><span class="sxs-lookup"><span data-stu-id="135ac-1344">Remarks</span></span>

<span data-ttu-id="135ac-1345">La classe **Win32 \_ Printer** est dérivée de l' [**\_ imprimante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1345">The **Win32\_Printer** class is derived from [**CIM\_Printer**](cim-printer.md).</span></span> <span data-ttu-id="135ac-1346">Avant d’appeler [**SWbemObject. \_ put**](../wmisdk/swbemobject-put-.md) ou [**IWbemServices ::P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) pour une instance d' **\_ imprimante Win32** , le privilège **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** pour Visual Basic et LoadDriver pour les monikers de script) doit être activé.</span><span class="sxs-lookup"><span data-stu-id="135ac-1346">Before calling [**SWbemObject.Put\_**](../wmisdk/swbemobject-put-.md) or [**IWbemServices::PutInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) for a **Win32\_Printer** instance, the **SeLoadDriverPrivilege** privilege (**wbemPrivilegeLoadDriver** for Visual Basic and LoadDriver for scripting monikers) must be enabled.</span></span> <span data-ttu-id="135ac-1347">Pour plus d’informations, consultez [**constantes de privilège**](../wmisdk/privilege-constants.md) et [exécution d’opérations privilégiées](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="135ac-1347">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span> <span data-ttu-id="135ac-1348">L’exemple de code VBScript suivant montre comment activer le privilège **SetLoadDriverPrivilege** dans le script.</span><span class="sxs-lookup"><span data-stu-id="135ac-1348">The following VBScript code example shows how to enable the **SetLoadDriverPrivilege** privilege in script.</span></span>

<span data-ttu-id="135ac-1349">Pour travailler avec des clusters d’imprimantes MSCS, utilisez l’assembly prnadmin.dll ou l’espace de noms [System. printing](/dotnet/api/system.printing) .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="135ac-1349">For working with MSCS Printer clusters, use the prnadmin.dll assembly, or else the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



<span data-ttu-id="135ac-1350">Windows utilise les informations d’identification de l’utilisateur qui exécute le script pour déterminer les imprimantes disponibles.</span><span class="sxs-lookup"><span data-stu-id="135ac-1350">Windows uses the credentials of the user running the script to determine what the available printers are.</span></span> <span data-ttu-id="135ac-1351">Par conséquent, si vous exécutez un script à distance, vous ne pourrez peut-être accéder qu’aux imprimantes disponibles pour votre compte d’utilisateur sur ce système distant.</span><span class="sxs-lookup"><span data-stu-id="135ac-1351">Therefore, if you are running a script remotely, you may only be able to access any printer that is available to your user account on that remote system.</span></span>

<span data-ttu-id="135ac-1352">Vous ne pouvez pas utiliser la classe d' **\_ imprimante Win32** pour les imprimantes sur un cluster d’impression MSCS.</span><span class="sxs-lookup"><span data-stu-id="135ac-1352">You cannot use the **Win32\_Printer** class for printers on an MSCS print cluster.</span></span> <span data-ttu-id="135ac-1353">Au lieu de cela, vous devrez peut-être utiliser l’outil PrinterAdmin (PrnAdmin.dll) ou l’espace de noms [System. printing](/dotnet/api/system.printing) .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="135ac-1353">Instead, you may need to use either the PrinterAdmin tool (PrnAdmin.dll) or the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="135ac-1354">Si vous récupérez **PrinterStatus** = 3 ou **PrinterState** = 0, il se peut que le pilote d’imprimante n’alimente pas correctement les informations dans WMI.</span><span class="sxs-lookup"><span data-stu-id="135ac-1354">If you are retrieving **PrinterStatus** = 3 or **PrinterState** = 0, the printer driver may not be feeding accurate information into WMI.</span></span> <span data-ttu-id="135ac-1355">WMI récupère les informations de l’imprimante à partir du processus de spoolsv.exe.</span><span class="sxs-lookup"><span data-stu-id="135ac-1355">WMI retrieves the printer information from the spoolsv.exe process.</span></span> <span data-ttu-id="135ac-1356">Il est possible que le pilote d’imprimante ne signale pas son état au spouleur.</span><span class="sxs-lookup"><span data-stu-id="135ac-1356">It is possible the printer driver does not report its status to the spooler.</span></span> <span data-ttu-id="135ac-1357">Dans ce cas, **l' \_ imprimante Win32** signale l’imprimante comme étant **inactive**.</span><span class="sxs-lookup"><span data-stu-id="135ac-1357">In this case, **Win32\_Printer** reports the printer as **Idle**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="135ac-1358">Exemples</span><span class="sxs-lookup"><span data-stu-id="135ac-1358">Examples</span></span>

<span data-ttu-id="135ac-1359">L’exemple [PS créer un dessin de configuration d’ordinateur à l’aide de Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sur la Galerie TechNet utilise l' **\_ imprimante Win32** pour interagir avec le modèle Visio Automation afin de créer un dessin Visio.</span><span class="sxs-lookup"><span data-stu-id="135ac-1359">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_Printer** to interact with Visio automation model to create a Visio drawing.</span></span>

<span data-ttu-id="135ac-1360">Le [script PowerShell Remote PC info](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) utilise un certain nombre de classes, y compris **Win32 \_ Printer**, pour récupérer des informations sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="135ac-1360">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) uses a number of classes, including **Win32\_Printer**, to retrieve information about a remote computer.</span></span>

<span data-ttu-id="135ac-1361">L’exemple de code PowerShell suivant montre comment déterminer l’imprimante par défaut de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="135ac-1361">The following PowerShell code sample shows how to determine the default printer of the local computer.</span></span>


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



<span data-ttu-id="135ac-1362">L’exemple de code VBScript suivant décrit comment récupérer des statistiques d’imprimante à partir des instances d’une **\_ imprimante Win32**.</span><span class="sxs-lookup"><span data-stu-id="135ac-1362">The following VBScript code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



<span data-ttu-id="135ac-1363">L’exemple de code perl suivant décrit comment récupérer des statistiques d’imprimante à partir des instances d’une **\_ imprimante Win32**.</span><span class="sxs-lookup"><span data-stu-id="135ac-1363">The following Perl code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="135ac-1364">L’exemple de code VBScript suivant montre comment obtenir le nom de l’imprimante par défaut d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="135ac-1364">The following VBScript code example shows how to obtain the name of the default printer for a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="135ac-1365">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="135ac-1365">Requirements</span></span>



| <span data-ttu-id="135ac-1366">Condition requise</span><span class="sxs-lookup"><span data-stu-id="135ac-1366">Requirement</span></span> | <span data-ttu-id="135ac-1367">Valeur</span><span class="sxs-lookup"><span data-stu-id="135ac-1367">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="135ac-1368">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="135ac-1368">Minimum supported client</span></span><br/> | <span data-ttu-id="135ac-1369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="135ac-1369">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="135ac-1370">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="135ac-1370">Minimum supported server</span></span><br/> | <span data-ttu-id="135ac-1371">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="135ac-1371">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="135ac-1372">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="135ac-1372">Namespace</span></span><br/>                | <span data-ttu-id="135ac-1373">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="135ac-1373">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="135ac-1374">MOF</span><span class="sxs-lookup"><span data-stu-id="135ac-1374">MOF</span></span><br/>                      | <dl> <span data-ttu-id="135ac-1375"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="135ac-1375"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="135ac-1376">DLL</span><span class="sxs-lookup"><span data-stu-id="135ac-1376">DLL</span></span><br/>                      | <dl> <span data-ttu-id="135ac-1377"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="135ac-1377"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="135ac-1378">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="135ac-1378">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135ac-1379">**\_Imprimante CIM**</span><span class="sxs-lookup"><span data-stu-id="135ac-1379">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dt>

[<span data-ttu-id="135ac-1380">Classes matérielles du système informatique</span><span class="sxs-lookup"><span data-stu-id="135ac-1380">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="135ac-1381">Tâches WMI : imprimantes et impression</span><span class="sxs-lookup"><span data-stu-id="135ac-1381">WMI Tasks: Printers and Printing</span></span>](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
