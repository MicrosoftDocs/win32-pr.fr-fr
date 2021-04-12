---
title: Classe Win32_TSClientSetting
description: Définit les paramètres de configuration pour la \_ classe de terminal Win32 associée à la stratégie de connexion.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Win32_TSClientSetting de la classe Services Bureau à distance
- Win32_TSClientSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105835"
---
# <a name="win32_tsclientsetting-class"></a><span data-ttu-id="8f2cb-105">\_Classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="8f2cb-105">Win32\_TSClientSetting class</span></span>

<span data-ttu-id="8f2cb-106">La classe WMI **Win32 \_ TSClientSetting** définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) associée à la stratégie de connexion.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-106">The **Win32\_TSClientSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

<span data-ttu-id="8f2cb-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="8f2cb-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f2cb-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a><span data-ttu-id="8f2cb-110">Membres</span><span class="sxs-lookup"><span data-stu-id="8f2cb-110">Members</span></span>

<span data-ttu-id="8f2cb-111">La classe **Win32 \_ TSClientSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8f2cb-111">The **Win32\_TSClientSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8f2cb-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f2cb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f2cb-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f2cb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f2cb-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8f2cb-114">Methods</span></span>

<span data-ttu-id="8f2cb-115">La classe **Win32 \_ TSClientSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-115">The **Win32\_TSClientSetting** class has these methods.</span></span>



| <span data-ttu-id="8f2cb-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="8f2cb-116">Method</span></span>                                                                   | <span data-ttu-id="8f2cb-117">Description</span><span class="sxs-lookup"><span data-stu-id="8f2cb-117">Description</span></span>                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f2cb-118">**ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-118">**ConnectionSettings**</span></span>](win32-tsclientsetting-connectionsettings.md)   | <span data-ttu-id="8f2cb-119">Définit les propriétés **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** et **DefaultToClientPrinter** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-119">Sets the **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon**, and **DefaultToClientPrinter** properties of this class.</span></span><br/>                      |
| [<span data-ttu-id="8f2cb-120">**SetAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-120">**SetAllowDwm**</span></span>](setallowdwm-win32-tsclientsetting.md)                 | <span data-ttu-id="8f2cb-121">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-121">Not supported.</span></span><br/> <span data-ttu-id="8f2cb-122">**Windows 7 et Windows Server 2008 R2 :** Définit la propriété **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-122">**Windows 7 and Windows Server 2008 R2:** Sets the **AllowDwm** property.</span></span><br/>                                               |
| [<span data-ttu-id="8f2cb-123">**SetClientProperty**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-123">**SetClientProperty**</span></span>](win32-tsclientsetting-setclientproperty.md)     | <span data-ttu-id="8f2cb-124">Définit la propriété **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** ou **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-124">Sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property.</span></span><br/> |
| [<span data-ttu-id="8f2cb-125">**SetColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-125">**SetColorDepth**</span></span>](win32-tsclientsetting-setcolordepth.md)             | <span data-ttu-id="8f2cb-126">Définit la propriété **ColorDepth** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-126">Sets the **ColorDepth** property.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="8f2cb-127">**SetColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-127">**SetColorDepthPolicy**</span></span>](win32-tsclientsetting-setcolordepthpolicy.md) | <span data-ttu-id="8f2cb-128">Définit la propriété **ColorDepthPolicy** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-128">Sets the **ColorDepthPolicy** property.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="8f2cb-129">**SetMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-129">**SetMaxMonitors**</span></span>](setmaxmonitors-win32-tsclientsetting.md)           | <span data-ttu-id="8f2cb-130">Définit la propriété **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-130">Sets the **MaxMonitors** property.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="8f2cb-131">**SetMaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-131">**SetMaxXResolution**</span></span>](setmaxxresolution-win32-tsclientsetting.md)     | <span data-ttu-id="8f2cb-132">Définit la propriété **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-132">Sets the **MaxXResolution** property.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="8f2cb-133">**SetMaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-133">**SetMaxYResolution**</span></span>](setmaxyresolution-win32-tsclientsetting.md)     | <span data-ttu-id="8f2cb-134">Définit la propriété **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-134">Sets the **MaxYResolution** property.</span></span><br/>                                                                                                             |



 

### <a name="properties"></a><span data-ttu-id="8f2cb-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8f2cb-135">Properties</span></span>

<span data-ttu-id="8f2cb-136">La classe **Win32 \_ TSClientSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-136">The **Win32\_TSClientSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f2cb-137">**AdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-137">**AdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-140">Spécifie s’il faut activer les graphiques RemoteFX avancés pour RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-140">Specifies whether to enable advanced RemoteFX graphics for RemoteApp.</span></span>

<span data-ttu-id="8f2cb-141">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2012 R2 et Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-142"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-143">Les graphiques avancés sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-143">Advanced graphics are disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-144"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-145">Les graphiques avancés sont activés.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-145">Advanced graphics are enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-146">**AllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-146">**AllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-147">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-149">Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-149">This property is not available.</span></span>

<span data-ttu-id="8f2cb-150">\* \* Windows 7 et Windows Server 2008 R2 : \* \*</span><span class="sxs-lookup"><span data-stu-id="8f2cb-150">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="8f2cb-151">Spécifie s’il faut activer ou désactiver la composition du Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-151">Specifies whether to enable or disable remote desktop composition.</span></span> <span data-ttu-id="8f2cb-152">Zéro désactive la composition du Bureau à distance et une valeur différente de zéro le permet.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-152">Zero will disable remote desktop composition and a nonzero value will enable it.</span></span>

<span data-ttu-id="8f2cb-153">Utilisez la méthode [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) pour modifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-153">Use the [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) method to modify this property.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-154">**AudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-154">**AudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-155">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-157">Spécifie s’il faut autoriser la redirection de capture audio.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-157">Specifies whether to allow audio capture redirection.</span></span>

<span data-ttu-id="8f2cb-158">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-158">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-159">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-159">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-160">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-160">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-161">**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-161">**AudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-164">Spécifie si le mappage audio est désactivé ou activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-164">Specifies whether audio mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-165"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-166">Le mappage audio est activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-166">Audio mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-167"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-168">Le mappage audio est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-168">Audio mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-169">**AVC444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-169">**AVC444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-171">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-172">Spécifie si le mode AVC444 est préféré.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-172">Specifies whether AVC444 mode is preferred.</span></span>

<span data-ttu-id="8f2cb-173">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows Server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 10 ou Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-174">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-174">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-175">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-175">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-176">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-179">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-180">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-180">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8f2cb-181">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-182">**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-182">**ClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-183">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-185">Spécifie si le mappage du presse-papiers est désactivé ou activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-185">Specifies whether clipboard mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-186"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-187">Le mappage du presse-papiers est activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-187">Clipboard mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-188"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-189">Le mappage du presse-papiers est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-189">Clipboard mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-190">**La**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-190">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-191">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-193">Spécifie la profondeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-193">Specifies the color depth.</span></span> <span data-ttu-id="8f2cb-194">Pour connaître les valeurs possibles, consultez la méthode [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-194">For possible values, see the [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) method.</span></span>

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span data-ttu-id="8f2cb-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bits** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span data-ttu-id="8f2cb-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bits** (2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span data-ttu-id="8f2cb-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bits** (3)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span data-ttu-id="8f2cb-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bits** (4)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span data-ttu-id="8f2cb-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bits** (5)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bit** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-200">**ColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-200">**ColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-203">Spécifie s’il faut remplacer le paramètre de couleur maximal de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-203">Specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-204"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-205">Ne remplacez pas la stratégie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-205">Do not override the user's policy.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-206"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-207">Remplacez la stratégie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-207">Override the user's policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-208">**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-208">**COMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-209">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-211">Spécifie si le mappage de port COM est désactivé ou activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-211">Specifies whether COM port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-212"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-213">Le mappage de port COM est activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-213">COM port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-214"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-215">Le mappage de port COM est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-215">COM port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-216">**ConnectClientDrivesAtLogon**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-216">**ConnectClientDrivesAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-217">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-219">Spécifie si les lecteurs du client sont connectés automatiquement au cours du processus d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-219">Specifies whether the client's drives will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-220"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-221">Les lecteurs ne sont pas automatiquement connectés.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-221">Drives will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-222"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-223">Les lecteurs seront automatiquement connectés.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-223">Drives will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-224">**ConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-224">**ConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-225">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-227">La stratégie utilisée par le serveur pour récupérer les paramètres de connexion utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-227">The policy the server uses to retrieve the user connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="8f2cb-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-229">Les paramètres de connexion de l’utilisateur sont activés.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-229">The user's connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="8f2cb-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-231">Les paramètres de connexion de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-231">The user's connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-232">**ConnectPrinterAtLogon**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-232">**ConnectPrinterAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-233">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-234">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-235">Spécifie si toutes les imprimantes locales mappées du client seront connectées automatiquement au cours du processus d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-235">Specifies whether all mapped local printers of the client will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-236"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-237">Les imprimantes locales ne seront pas connectées automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-237">Local printers will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-238"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-239">Les imprimantes locales seront automatiquement connectées.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-239">Local printers will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-240">**DefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-240">**DefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-241">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-242">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-243">Spécifie si les travaux d’impression sont envoyés automatiquement à l’imprimante locale du client.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-243">Specifies whether print jobs will be automatically sent to the client's local printer.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-244"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-245">Les travaux d’impression ne sont pas envoyés automatiquement à l’imprimante locale du client.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-245">Print jobs are not to be automatically sent to the client's local printer.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-246"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-247">Les travaux d’impression doivent être envoyés automatiquement à l’imprimante locale du client.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-247">Print jobs are to be automatically sent to the client's local printer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-248">**Description**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-248">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-250">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-251">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-251">Description of the object.</span></span>

<span data-ttu-id="8f2cb-252">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-252">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-253">**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-253">**DriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-254">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-256">Spécifie si le mappage de lecteur est désactivé ou activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-256">Specifies whether drive mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-257"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-258">Le mappage de lecteur est activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-258">Drive mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-259"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-260">Le mappage de lecteur est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-260">Drive mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-261">**EncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-261">**EncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-262">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-263">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-264">Spécifie la qualité de l’image pour l’expérience RDP.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-264">Specifies the image quality for RDP experience.</span></span>

<span data-ttu-id="8f2cb-265">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-265">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

<span data-ttu-id="8f2cb-266">**sans perte** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-266">**lossless** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="8f2cb-267">**élevé** (2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-267">**high** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="8f2cb-268">**moyenne** (3)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-268">**medium** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-269">**HardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-269">**HardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-270">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-271">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-271">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-272">Spécifie si le serveur hôte de session Bureau à distance utilise le convertisseur graphique matériel comme adaptateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-272">Specifies whether the RD Session Host server uses the hardware graphics renderer as the default adapter.</span></span>

<span data-ttu-id="8f2cb-273">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-273">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-274">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-274">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-275">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-275">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-277">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-278">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-279">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8f2cb-279">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-280">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-280">The date the object was installed.</span></span> <span data-ttu-id="8f2cb-281">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-281">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8f2cb-282">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-283">**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-283">**LPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-284">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-285">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-286">Spécifie si le mappage de port LPT est désactivé ou activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-286">Specifies whether LPT port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-287"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-288">Le mappage de port LPT est activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-288">LPT port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-289"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-290">Le mappage de port LPT est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-290">LPT port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-291">**MaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-291">**MaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-292">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-294">Nombre maximal de moniteurs pris en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-294">The maximum number of monitors supported by the server.</span></span> <span data-ttu-id="8f2cb-295">Utilisez la méthode [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) pour modifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-295">Use the [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8f2cb-296">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-296">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-297">**MaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-297">**MaxXResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-298">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-300">Résolution maximale X prise en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-300">The maximum X resolution supported by the server.</span></span> <span data-ttu-id="8f2cb-301">Utilisez la méthode [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) pour modifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-301">Use the [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8f2cb-302">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-302">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-303">**MaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-303">**MaxYResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-304">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-304">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-306">Résolution Y maximale prise en charge par le serveur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-306">The maximum Y resolution supported by the server.</span></span> <span data-ttu-id="8f2cb-307">Utilisez la méthode [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) pour modifier cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-307">Use the [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="8f2cb-308">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-308">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-309">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-309">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-311">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-312">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-312">The name of the object.</span></span>

<span data-ttu-id="8f2cb-313">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-314">**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-314">**PNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-315">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-316">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-317">Spécifie s’il faut autoriser Plug-and-Play redirection.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-317">Specifies whether to allow Plug and Play redirection.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-318"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-319">Autorisez la redirection de Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-319">Allow Plug and Play redirection.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-320"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-321">N’autorisez pas la redirection de Plug-and-Play.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-321">Do not allow Plug and Play redirection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-322">**PolicyAdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-322">**PolicyAdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-323">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-325">Indique si la propriété **AdvancedRemoteAppGraphics** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-325">Indicates whether the **AdvancedRemoteAppGraphics** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8f2cb-326">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2012 R2 et Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span data-ttu-id="8f2cb-327">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-327">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-328">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-328">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-329">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-329">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-330">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-330">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-331">**PolicySourceAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-331">**PolicySourceAllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-332">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-333">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-334">Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-334">This property is not available.</span></span>

<span data-ttu-id="8f2cb-335">\* \* Windows 7 et Windows Server 2008 R2 : \* \*</span><span class="sxs-lookup"><span data-stu-id="8f2cb-335">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="8f2cb-336">Indique si la propriété **AllowDwm** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-336">Indicates whether the **AllowDwm** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="8f2cb-337">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-337">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-338">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-338">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-339">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-339">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-340">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-340">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-341">**PolicySourceAudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-341">**PolicySourceAudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-342">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-343">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-344">Indique si la propriété **AudioCaptureRedir** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-344">Indicates whether the **AudioCaptureRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8f2cb-345">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-345">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8f2cb-346">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-346">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-347">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-347">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-348">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-348">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-349">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-349">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-350">**PolicySourceAudioMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-350">**PolicySourceAudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-351">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-353">Indique si la propriété **AudioMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-353">Indicates whether the **AudioMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-354">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-354">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-355">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-355">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-356">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-356">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-357">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-357">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-358">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-358">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-359">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-359">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-360">**PolicySourceAvc444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-360">**PolicySourceAvc444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-361">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-362">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-363">Indique comment la propriété **AVC444ModePreferredis** est configurée.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-363">Indicates how the **AVC444ModePreferredis** property is configured.</span></span>

<span data-ttu-id="8f2cb-364">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows Server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 10 ou Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span data-ttu-id="8f2cb-365">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-365">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-366">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-366">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-367">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-367">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-368">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-368">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-369">**PolicySourceClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-369">**PolicySourceClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-370">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-371">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-372">Indique si la propriété **ClipboardMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-372">Indicates whether the **ClipboardMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-373">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-373">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-374">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-374">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-375">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-375">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-376">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-376">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-377">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-377">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-378">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-378">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-379">**PolicySourceColorDepth**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-379">**PolicySourceColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-380">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-381">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-382">Indique si la propriété **ColorDepth** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-382">Indicates whether the **ColorDepth** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-383">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-383">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-384">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-384">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-385">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-385">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-386">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-386">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-387">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-387">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-388">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-388">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-389">**PolicySourceColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-389">**PolicySourceColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-390">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-391">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-392">Indique si la propriété **ColorDepthPolicy** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-392">Indicates whether the **ColorDepthPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-393">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-393">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-394">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-394">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-395">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-395">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-396">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-396">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-397">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-397">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-398">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-398">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-399">**PolicySourceCOMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-399">**PolicySourceCOMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-400">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-400">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-401">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-402">Indique si la propriété **COMPortMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-402">Indicates whether the **COMPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-403">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-403">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-404">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-404">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-405">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-405">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-406">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-406">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-407">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-407">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-408">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-408">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-409">**PolicySourceDefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-409">**PolicySourceDefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-410">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-411">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-412">Indique si la propriété **DefaultToClientPrinter** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-412">Indicates whether the **DefaultToClientPrinter** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-413">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-413">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-414">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-414">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-415">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-415">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-416">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-416">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-417">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-417">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-418">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-418">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-419">**PolicySourceDriveMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-419">**PolicySourceDriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-420">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-421">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-422">Indique si la propriété **DriveMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-422">Indicates whether the **DriveMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-424">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-426">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-426">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-427">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-427">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-428">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-428">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-429">**PolicySourceEncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-429">**PolicySourceEncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-430">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-431">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-432">Indique la configuration de **EncodeImageQualityi** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-432">Indicates how the **EncodeImageQualityi** is configured.</span></span>

<span data-ttu-id="8f2cb-433">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-433">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f2cb-434">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-434">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-435">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-435">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-436">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-436">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-437">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-437">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-438">**PolicySourceHardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-438">**PolicySourceHardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-439">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-440">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-441">Indique la configuration de **HardwareGraphicsAdapter** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-441">Indicates how the **HardwareGraphicsAdapter** is configured.</span></span>

<span data-ttu-id="8f2cb-442">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-442">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f2cb-443">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-443">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-444">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-444">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-445">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-445">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-446">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-446">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-447">**PolicySourceLPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-447">**PolicySourceLPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-448">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-448">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-449">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-450">Indique si la propriété **LPTPortMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-450">Indicates whether the **LPTPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-451">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-451">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-452">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-452">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-453">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-453">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-454">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-454">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-455">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-455">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-456">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-456">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-457">**PolicySourceMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-457">**PolicySourceMaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-458">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-458">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-459">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-460">Indique si la propriété **MaxMonitors** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-460">Indicates whether the **MaxMonitors** property is configured by the server, group policy, or default.</span></span>

<dt>

<span data-ttu-id="8f2cb-461">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-461">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-462">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-462">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-463">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-463">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-464">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-464">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-465">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-465">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-466">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-466">Default</span></span>

</dd> </dl>

<span data-ttu-id="8f2cb-467">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-467">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-468">**PolicySourceMaxResolution**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-468">**PolicySourceMaxResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-469">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-469">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-470">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-471">Indique si les propriétés **MaxXResolution** et **MaxYResolution** sont configurées par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-471">Indicates whether the **MaxXResolution** and **MaxYResolution** properties are configured by the server, group policy, or default.</span></span>

<span data-ttu-id="8f2cb-472">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-472">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8f2cb-473">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-473">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-474">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-474">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-475">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-475">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-476">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-476">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-477">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-477">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-478">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-478">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-479">**PolicySourcePNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-479">**PolicySourcePNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-480">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-481">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-482">Indique si la propriété **PNPRedirection** est configurée par le serveur ou par la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-482">Indicates whether the **PNPRedirection** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="8f2cb-483">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-483">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-484">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-484">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-485">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-485">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-486">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-486">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-487">**PolicySourceRemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-487">**PolicySourceRemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-488">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-489">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-490">Indique la configuration de **RemoteSessionProfile** .</span><span class="sxs-lookup"><span data-stu-id="8f2cb-490">Indicates how the **RemoteSessionProfile** is configured.</span></span>

<span data-ttu-id="8f2cb-491">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-491">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is unavailable prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f2cb-492">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-492">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-493">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-493">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-494">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-494">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-495">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-495">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-496">**PolicySourceSelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-496">**PolicySourceSelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-497">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-497">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-498">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-499">Indique comment la propriété **SelectNetworkDetect** est configurée.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-499">Indicates how the property **SelectNetworkDetect** is configured.</span></span>

<span data-ttu-id="8f2cb-500">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-500">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f2cb-501">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-501">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-502">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-502">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-503">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-503">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-504">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-504">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-505">**PolicySourceSelectTransport**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-505">**PolicySourceSelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-506">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-507">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-508">Indique comment la propriété **SelectTransport** est configurée.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-508">Indicates how the property **SelectTransport** is configured.</span></span>

<span data-ttu-id="8f2cb-509">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-509">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f2cb-510">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-510">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-511">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-511">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-512">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-512">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-513">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-513">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-514">**PolicySourceVideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-514">**PolicySourceVideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-515">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-515">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-516">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-517">Indique si la propriété **VideoPlaybackRedir** est configurée par le serveur ou la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-517">Indicates whether the **VideoPlaybackRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="8f2cb-518">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-518">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="8f2cb-519">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-519">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-520">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-520">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-521">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-521">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-522">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-522">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-523">**PolicySourceWindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-523">**PolicySourceWindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-524">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-525">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-526">Indique si la propriété **WindowsPrinterMapping** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-526">Indicates whether the **WindowsPrinterMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="8f2cb-527">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-527">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-528">Serveur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-528">Server</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-529">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-529">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-530">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="8f2cb-530">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-531">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-531">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-532">Default</span><span class="sxs-lookup"><span data-stu-id="8f2cb-532">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-533">**RemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-533">**RemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-534">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-534">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-535">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-535">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-536">Spécifie le profil pour l’expérience RDP.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-536">Specifies the profile for the RDP experience.</span></span>

<span data-ttu-id="8f2cb-537">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-537">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="scale"></span><span id="SCALE"></span>

<span data-ttu-id="8f2cb-538">**échelle** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-538">**scale** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

<span data-ttu-id="8f2cb-539">**expérience** (2)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-539">**experience** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

<span data-ttu-id="8f2cb-540">**bande passante** (3)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-540">**bandwidth** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-541">**SelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-541">**SelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-542">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-543">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-543">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-544">Spécifie si la détection réseau est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-544">Specifies whether network detection is used.</span></span>

<span data-ttu-id="8f2cb-545">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-545">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f2cb-546">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-546">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-547">utilisé au moment de la connexion et dans un état stable.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-547">used at connect time and in steady state.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-548">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-548">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-549">désactivé au moment de la connexion</span><span class="sxs-lookup"><span data-stu-id="8f2cb-549">disabled at connect time</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-550">2</span><span class="sxs-lookup"><span data-stu-id="8f2cb-550">2</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-551">désactivé dans un état stable</span><span class="sxs-lookup"><span data-stu-id="8f2cb-551">disabled in steady state</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-552">3</span><span class="sxs-lookup"><span data-stu-id="8f2cb-552">3</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-553">désactivé au moment de la connexion et dans un état stable.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-553">disabled at connect time and in steady state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-554">**SelectTransport**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-554">**SelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-555">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-555">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-556">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8f2cb-556">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-557">Spécifie les protocoles de transport qui peuvent être utilisés pour l’accès RDP au serveur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-557">Specifies which transport protocols can be used for RDP access to server.</span></span>

<span data-ttu-id="8f2cb-558">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows 8 ou Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-558">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="8f2cb-559">0</span><span class="sxs-lookup"><span data-stu-id="8f2cb-559">0</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-560">Utilisez à la fois UDP et TCP.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-560">Use both UDP and TCP.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-561">1</span><span class="sxs-lookup"><span data-stu-id="8f2cb-561">1</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-562">Utilisez uniquement TCP.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-562">Use only TCP.</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-563">2</span><span class="sxs-lookup"><span data-stu-id="8f2cb-563">2</span></span>
</dt> <dd>

<span data-ttu-id="8f2cb-564">Utilisez le protocole UDP ou TCP.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-564">Use either UDP or TCP.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-565">**État**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-565">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-566">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-567">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-568">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-568">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-569">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-569">Current status of the object.</span></span> <span data-ttu-id="8f2cb-570">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-570">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8f2cb-571">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-571">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8f2cb-572">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="8f2cb-572">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8f2cb-573">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-573">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8f2cb-574">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-574">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8f2cb-575">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-575">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8f2cb-576">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-576">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f2cb-577">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-577">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f2cb-578">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-578">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f2cb-579">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="8f2cb-579">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f2cb-580">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-580">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f2cb-581">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-581">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f2cb-582">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-582">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8f2cb-583">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-583">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-584">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-584">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-585">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-586">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-587">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-587">The name of the terminal.</span></span>

<span data-ttu-id="8f2cb-588">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-588">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f2cb-589">**VideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-589">**VideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-590">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-591">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-592">Spécifie s’il faut autoriser la redirection de lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-592">Specifies whether to allow video playback redirection.</span></span>

<span data-ttu-id="8f2cb-593">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible avant Windows Server 2008 R2 et Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-593">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-594">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-594">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-595">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-595">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8f2cb-596">**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-596">**WindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f2cb-597">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-597">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f2cb-598">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8f2cb-598">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f2cb-599">Spécifie si le mappage de l’imprimante est désactivé ou activé pour la fenêtre du client.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-599">Specifies whether printer mapping is disabled or enabled for the client's window.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="8f2cb-600"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-601">Le mappage d’imprimante est activé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-601">Printer mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="8f2cb-602"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="8f2cb-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8f2cb-603">Le mappage d’imprimante est désactivé.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-603">Printer mapping is disabled.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f2cb-604">Notes</span><span class="sxs-lookup"><span data-stu-id="8f2cb-604">Remarks</span></span>

<span data-ttu-id="8f2cb-605">Sachez qu’une station de fenêtre associée à la session de console ne peut pas accéder aux méthodes et aux propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-605">Be aware that a window station associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="8f2cb-606">Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété **TerminalName** , les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-606">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="8f2cb-607">Ce code d’erreur est également retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-607">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="8f2cb-608">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-608">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="8f2cb-609">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-609">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="8f2cb-610">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de six.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-610">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="8f2cb-611">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-611">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="8f2cb-612">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-612">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8f2cb-613">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-613">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8f2cb-614">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="8f2cb-614">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8f2cb-615">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8f2cb-615">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f2cb-616">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f2cb-616">Requirements</span></span>



| <span data-ttu-id="8f2cb-617">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f2cb-617">Requirement</span></span> | <span data-ttu-id="8f2cb-618">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f2cb-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2cb-619">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f2cb-619">Minimum supported client</span></span><br/> | <span data-ttu-id="8f2cb-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f2cb-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f2cb-621">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f2cb-621">Minimum supported server</span></span><br/> | <span data-ttu-id="8f2cb-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f2cb-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f2cb-623">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8f2cb-623">Namespace</span></span><br/>                | <span data-ttu-id="8f2cb-624">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8f2cb-624">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8f2cb-625">MOF</span><span class="sxs-lookup"><span data-stu-id="8f2cb-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f2cb-626"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f2cb-626"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f2cb-627">DLL</span><span class="sxs-lookup"><span data-stu-id="8f2cb-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f2cb-628"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f2cb-628"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f2cb-629">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f2cb-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2cb-630">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-630">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="8f2cb-631">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-631">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="8f2cb-632">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="8f2cb-632">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

