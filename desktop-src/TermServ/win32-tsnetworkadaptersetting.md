---
title: Classe Win32_TSNetworkAdapterSetting
description: Définit différents paramètres de configuration pour la \_ classe de terminal Win32, y compris les propriétés associées à la carte réseau et le nombre maximal de connexions autorisées.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f2f2f1ac7d6bf4b1fd3fb5f5a92fc4fd5260a92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465963"
---
# <a name="win32_tsnetworkadaptersetting-class"></a><span data-ttu-id="08741-105">\_Classe TSNetworkAdapterSetting Win32</span><span class="sxs-lookup"><span data-stu-id="08741-105">Win32\_TSNetworkAdapterSetting class</span></span>

<span data-ttu-id="08741-106">La classe WMI **Win32 \_ TSNetworkAdapterSetting** définit différents paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , y compris les propriétés associées à la carte réseau et le nombre maximal de connexions autorisées.</span><span class="sxs-lookup"><span data-stu-id="08741-106">The **Win32\_TSNetworkAdapterSetting** WMI class defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

<span data-ttu-id="08741-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="08741-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="08741-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="08741-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="08741-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08741-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a><span data-ttu-id="08741-110">Membres</span><span class="sxs-lookup"><span data-stu-id="08741-110">Members</span></span>

<span data-ttu-id="08741-111">La classe **Win32 \_ TSNetworkAdapterSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="08741-111">The **Win32\_TSNetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="08741-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="08741-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="08741-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08741-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08741-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="08741-114">Methods</span></span>

<span data-ttu-id="08741-115">La classe **Win32 \_ TSNetworkAdapterSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="08741-115">The **Win32\_TSNetworkAdapterSetting** class has these methods.</span></span>



| <span data-ttu-id="08741-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="08741-116">Method</span></span>                                                                                     | <span data-ttu-id="08741-117">Description</span><span class="sxs-lookup"><span data-stu-id="08741-117">Description</span></span>                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08741-118">**SelectAllNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="08741-118">**SelectAllNetworkAdapters**</span></span>](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | <span data-ttu-id="08741-119">Sélectionne toutes les cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="08741-119">Selects all network adapters.</span></span><br/>                                                                 |
| [<span data-ttu-id="08741-120">**SelectNetworkAdapterIP**</span><span class="sxs-lookup"><span data-stu-id="08741-120">**SelectNetworkAdapterIP**</span></span>](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | <span data-ttu-id="08741-121">Sélectionne une carte réseau en fonction de l’adresse IP de la carte.</span><span class="sxs-lookup"><span data-stu-id="08741-121">Selects a network adapter based on the adapter's IP address.</span></span><br/>                                  |
| [<span data-ttu-id="08741-122">**SetNetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="08741-122">**SetNetworkAdapterLanaID**</span></span>](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | <span data-ttu-id="08741-123">Spécifie le numéro de carte réseau locale NetBIOS (LANA) de la carte réseau à définir.</span><span class="sxs-lookup"><span data-stu-id="08741-123">Specifies the NetBIOS Local Area Network Adapter (LANA) number of the network adapter to set.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08741-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08741-124">Properties</span></span>

<span data-ttu-id="08741-125">La classe **Win32 \_ TSNetworkAdapterSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="08741-125">The **Win32\_TSNetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08741-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="08741-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08741-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08741-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08741-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="08741-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="08741-130">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08741-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="08741-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08741-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08741-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="08741-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08741-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08741-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-135">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08741-135">Description of the object.</span></span>

<span data-ttu-id="08741-136">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08741-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08741-137">**DeviceIDList**</span><span class="sxs-lookup"><span data-stu-id="08741-137">**DeviceIDList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-138">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="08741-138">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08741-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-140">Tableau de chaînes des ID d’appareil disponibles retournés dans l’ordre des cartes réseau physiques retournées dans le tableau de propriétés **NetworkAdapterList** .</span><span class="sxs-lookup"><span data-stu-id="08741-140">String array of available device IDs returned in the order of physical network adapters returned in the **NetworkAdapterList** property array.</span></span> <span data-ttu-id="08741-141">La valeur de l’ID d’appareil est la propriété **DeviceID** dans [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span><span class="sxs-lookup"><span data-stu-id="08741-141">The device ID value is the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)</span></span>

</dd> <dt>

<span data-ttu-id="08741-142">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="08741-142">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-143">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08741-143">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08741-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08741-145">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="08741-145">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="08741-146">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="08741-146">The date the object was installed.</span></span> <span data-ttu-id="08741-147">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="08741-147">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="08741-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08741-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08741-149">**MaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="08741-149">**MaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-150">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08741-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08741-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="08741-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08741-152">Nombre maximal de connexions autorisées.</span><span class="sxs-lookup"><span data-stu-id="08741-152">The maximum number of connections allowed.</span></span> <span data-ttu-id="08741-153">La valeur **maxint** désigne un nombre illimité de connexions.</span><span class="sxs-lookup"><span data-stu-id="08741-153">The value **MAXINT** denotes an unlimited number of connections.</span></span>

</dd> <dt>

<span data-ttu-id="08741-154">**Nom**</span><span class="sxs-lookup"><span data-stu-id="08741-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08741-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08741-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-157">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="08741-157">The name of the object.</span></span>

<span data-ttu-id="08741-158">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08741-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08741-159">**NetworkAdapterID**</span><span class="sxs-lookup"><span data-stu-id="08741-159">**NetworkAdapterID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-160">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08741-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08741-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-162">GUID qui représente l’ID de la carte réseau à définir.</span><span class="sxs-lookup"><span data-stu-id="08741-162">The GUID that represents the ID of the network adapter to set.</span></span> <span data-ttu-id="08741-163">Un **GUID** constitué de zéros désigne toutes les cartes réseau.</span><span class="sxs-lookup"><span data-stu-id="08741-163">A **GUID** that consists of all zeros denotes all network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="08741-164">**NetworkAdapterLanaID**</span><span class="sxs-lookup"><span data-stu-id="08741-164">**NetworkAdapterLanaID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08741-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08741-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-167">Numéro de carte réseau locale NetBIOS (LANA) de la carte réseau utilisée pour identifier la carte réseau attribuée au terminal.</span><span class="sxs-lookup"><span data-stu-id="08741-167">NetBIOS Local Area Network Adapter (LANA) number of the network adapter that is used to identify the network adapter assigned to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="08741-168">**NetworkAdapterList**</span><span class="sxs-lookup"><span data-stu-id="08741-168">**NetworkAdapterList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-169">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="08741-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="08741-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-171">Tableau de chaînes des cartes réseau physiques disponibles et des ID d’appareil correspondants.</span><span class="sxs-lookup"><span data-stu-id="08741-171">String array of available physical network adapters and the corresponding device IDs.</span></span> <span data-ttu-id="08741-172">Les ID d’appareil sont la propriété **DeviceID** dans [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span><span class="sxs-lookup"><span data-stu-id="08741-172">The device IDs are the **DeviceID** property in [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).</span></span>

</dd> <dt>

<span data-ttu-id="08741-173">**NetworkAdapterName**</span><span class="sxs-lookup"><span data-stu-id="08741-173">**NetworkAdapterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08741-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08741-175">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-176">Description de la carte réseau à définir.</span><span class="sxs-lookup"><span data-stu-id="08741-176">Description of the network adapter to set.</span></span> <span data-ttu-id="08741-177">Cette valeur est dans [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span><span class="sxs-lookup"><span data-stu-id="08741-177">This value is in [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).</span></span>

</dd> <dt>

<span data-ttu-id="08741-178">**PolicySourceMaximumConnections**</span><span class="sxs-lookup"><span data-stu-id="08741-178">**PolicySourceMaximumConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-179">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08741-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08741-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-181">Indique si la propriété **MaximumConnections** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="08741-181">Indicates whether the **MaximumConnections** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="08741-182">0</span><span class="sxs-lookup"><span data-stu-id="08741-182">0</span></span>
</dt> <dd>

<span data-ttu-id="08741-183">Serveur</span><span class="sxs-lookup"><span data-stu-id="08741-183">Server</span></span>

</dd> <dt>

<span data-ttu-id="08741-184">1</span><span class="sxs-lookup"><span data-stu-id="08741-184">1</span></span>
</dt> <dd>

<span data-ttu-id="08741-185">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="08741-185">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="08741-186">2</span><span class="sxs-lookup"><span data-stu-id="08741-186">2</span></span>
</dt> <dd>

<span data-ttu-id="08741-187">Default</span><span class="sxs-lookup"><span data-stu-id="08741-187">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08741-188">**État**</span><span class="sxs-lookup"><span data-stu-id="08741-188">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08741-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08741-190">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08741-191">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="08741-191">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="08741-192">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08741-192">Current status of the object.</span></span> <span data-ttu-id="08741-193">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="08741-193">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="08741-194">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="08741-194">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="08741-195">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="08741-195">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="08741-196">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="08741-196">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="08741-197">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="08741-197">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="08741-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08741-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="08741-199">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="08741-199">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08741-200">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="08741-200">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08741-201">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="08741-201">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08741-202">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="08741-202">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08741-203">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="08741-203">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08741-204">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="08741-204">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08741-205">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="08741-205">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="08741-206">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="08741-206">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08741-207">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="08741-207">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08741-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08741-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08741-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08741-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08741-210">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="08741-210">The name of the terminal.</span></span>

<span data-ttu-id="08741-211">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="08741-211">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08741-212">Notes</span><span class="sxs-lookup"><span data-stu-id="08741-212">Remarks</span></span>

<span data-ttu-id="08741-213">Sachez que les winstations associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="08741-213">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="08741-214">Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété TerminalName, les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="08741-214">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="08741-215">Ce code d’erreur est également retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="08741-215">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="08741-216">Pour se connecter à l’espace de noms « root \\ cimv2 \\ licences TS », le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="08741-216">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="08741-217">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="08741-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="08741-218">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="08741-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="08741-219">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="08741-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="08741-220">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="08741-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="08741-221">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="08741-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="08741-222">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="08741-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="08741-223">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="08741-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="08741-224">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08741-224">Requirements</span></span>



| <span data-ttu-id="08741-225">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08741-225">Requirement</span></span> | <span data-ttu-id="08741-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="08741-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08741-227">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08741-227">Minimum supported client</span></span><br/> | <span data-ttu-id="08741-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08741-228">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08741-229">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08741-229">Minimum supported server</span></span><br/> | <span data-ttu-id="08741-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08741-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08741-231">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="08741-231">Namespace</span></span><br/>                | <span data-ttu-id="08741-232">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="08741-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="08741-233">MOF</span><span class="sxs-lookup"><span data-stu-id="08741-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08741-234"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08741-234"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="08741-235">DLL</span><span class="sxs-lookup"><span data-stu-id="08741-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08741-236"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08741-236"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08741-237">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08741-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08741-238">**\_NetworkAdapter Win32**</span><span class="sxs-lookup"><span data-stu-id="08741-238">**Win32\_NetworkAdapter**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[<span data-ttu-id="08741-239">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="08741-239">**Win32\_NetworkAdapterConfiguration**</span></span>](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[<span data-ttu-id="08741-240">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="08741-240">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="08741-241">**\_TSNetworkAdapterListSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="08741-241">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

