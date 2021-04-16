---
title: Classe Win32_TSEnvironmentSetting
description: Définit les paramètres de configuration pour la \_ classe de terminal Win32, y compris la stratégie de programme initiale.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance
- Win32_TSEnvironmentSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0689536385644ae3ef95d106e50ab198e5a57f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509266"
---
# <a name="win32_tsenvironmentsetting-class"></a><span data-ttu-id="45d91-105">\_Classe TSEnvironmentSetting Win32</span><span class="sxs-lookup"><span data-stu-id="45d91-105">Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="45d91-106">La classe WMI **Win32 \_ TSEnvironmentSetting** définit les paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , y compris la stratégie de programme initiale.</span><span class="sxs-lookup"><span data-stu-id="45d91-106">The **Win32\_TSEnvironmentSetting** WMI class defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

<span data-ttu-id="45d91-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="45d91-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="45d91-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="45d91-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="45d91-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45d91-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a><span data-ttu-id="45d91-110">Membres</span><span class="sxs-lookup"><span data-stu-id="45d91-110">Members</span></span>

<span data-ttu-id="45d91-111">La classe **Win32 \_ TSEnvironmentSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="45d91-111">The **Win32\_TSEnvironmentSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="45d91-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45d91-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="45d91-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45d91-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45d91-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="45d91-114">Methods</span></span>

<span data-ttu-id="45d91-115">La classe **Win32 \_ TSEnvironmentSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="45d91-115">The **Win32\_TSEnvironmentSetting** class has these methods.</span></span>



| <span data-ttu-id="45d91-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="45d91-116">Method</span></span>                                                                      | <span data-ttu-id="45d91-117">Description</span><span class="sxs-lookup"><span data-stu-id="45d91-117">Description</span></span>                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="45d91-118">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="45d91-118">**InitialProgram**</span></span>](win32-tsenvironmentsetting-initialprogram.md)         | <span data-ttu-id="45d91-119">Définit les propriétés du programme de démarrage incluses dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="45d91-119">Sets the startup program properties included in this class.</span></span><br/> |
| [<span data-ttu-id="45d91-120">**SetClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="45d91-120">**SetClientWallPaper**</span></span>](win32-tsenvironmentsetting-setclientwallpaper.md) | <span data-ttu-id="45d91-121">Définit la propriété **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="45d91-121">Sets the **ClientWallPaper** property.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="45d91-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="45d91-122">Properties</span></span>

<span data-ttu-id="45d91-123">La classe **Win32 \_ TSEnvironmentSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="45d91-123">The **Win32\_TSEnvironmentSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45d91-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45d91-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d91-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d91-127">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="45d91-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="45d91-128">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45d91-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="45d91-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d91-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d91-130">**ClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="45d91-130">**ClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d91-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-133">Spécifie si l’image de papier peint est affichée sur le client.</span><span class="sxs-lookup"><span data-stu-id="45d91-133">Specifies whether the wallpaper image is displayed on the client.</span></span> <span data-ttu-id="45d91-134">Si vous n’affichez pas l’image de papier peint, vous pouvez économiser des ressources système en diminuant le temps nécessaire pour redessiner l’écran.</span><span class="sxs-lookup"><span data-stu-id="45d91-134">Not displaying the wallpaper image can save system resources by decreasing the time required to repaint the screen.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="45d91-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="45d91-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="45d91-136">L’image de papier peint n’est pas affichée sur le client.</span><span class="sxs-lookup"><span data-stu-id="45d91-136">The wallpaper image is not displayed on the client.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="45d91-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="45d91-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="45d91-138">L’image de papier peint est affichée sur le client.</span><span class="sxs-lookup"><span data-stu-id="45d91-138">The wallpaper image is displayed on the client.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d91-139">**Description**</span><span class="sxs-lookup"><span data-stu-id="45d91-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d91-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-141">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-142">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45d91-142">Description of the object.</span></span>

<span data-ttu-id="45d91-143">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d91-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d91-144">**InitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="45d91-144">**InitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d91-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-147">Le nom et le chemin d’accès du programme que l’utilisateur exécutera immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="45d91-147">The name and the path of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="45d91-148">**InitialProgramPolicy**</span><span class="sxs-lookup"><span data-stu-id="45d91-148">**InitialProgramPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d91-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="45d91-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45d91-151">La stratégie utilisée par le serveur pour déterminer le chemin d’accès et le nom de fichier du programme de démarrage, ainsi que le nom du dossier dans lequel il se trouve.</span><span class="sxs-lookup"><span data-stu-id="45d91-151">The policy the server uses to determine the startup program path and file name, and the name of the folder it is located in.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="45d91-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)</span><span class="sxs-lookup"><span data-stu-id="45d91-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="45d91-153">Les paramètres du programme de démarrage de l’utilisateur sont activés.</span><span class="sxs-lookup"><span data-stu-id="45d91-153">The user's startup program settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="45d91-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)</span><span class="sxs-lookup"><span data-stu-id="45d91-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="45d91-155">Les paramètres du programme de démarrage de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="45d91-155">The user's startup program settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span data-ttu-id="45d91-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Mode mono-application** (2)</span><span class="sxs-lookup"><span data-stu-id="45d91-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Single-App Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="45d91-157">Une seule application est exécutée dans cette session.</span><span class="sxs-lookup"><span data-stu-id="45d91-157">Only a single application will be run in this session.</span></span> <span data-ttu-id="45d91-158">Les informations du programme de démarrage sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="45d91-158">The startup program information is ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d91-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45d91-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-160">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45d91-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-161">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d91-162">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="45d91-162">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="45d91-163">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="45d91-163">The date the object was installed.</span></span> <span data-ttu-id="45d91-164">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="45d91-164">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="45d91-165">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d91-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d91-166">**Nom**</span><span class="sxs-lookup"><span data-stu-id="45d91-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-167">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d91-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-169">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="45d91-169">The name of the object.</span></span>

<span data-ttu-id="45d91-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d91-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="45d91-171">**PolicySourceClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="45d91-171">**PolicySourceClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d91-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-174">Indique si la propriété **ClientWallPaper** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="45d91-174">Indicates whether the **ClientWallPaper** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="45d91-175">0</span><span class="sxs-lookup"><span data-stu-id="45d91-175">0</span></span>
</dt> <dd>

<span data-ttu-id="45d91-176">Serveur</span><span class="sxs-lookup"><span data-stu-id="45d91-176">Server</span></span>

</dd> <dt>

<span data-ttu-id="45d91-177">1</span><span class="sxs-lookup"><span data-stu-id="45d91-177">1</span></span>
</dt> <dd>

<span data-ttu-id="45d91-178">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="45d91-178">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="45d91-179">2</span><span class="sxs-lookup"><span data-stu-id="45d91-179">2</span></span>
</dt> <dd>

<span data-ttu-id="45d91-180">Default</span><span class="sxs-lookup"><span data-stu-id="45d91-180">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d91-181">**PolicySourceInitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="45d91-181">**PolicySourceInitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-182">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d91-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-184">Indique si la propriété **InitialProgramPath** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="45d91-184">Indicates whether the **InitialProgramPath** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="45d91-185">0</span><span class="sxs-lookup"><span data-stu-id="45d91-185">0</span></span>
</dt> <dd>

<span data-ttu-id="45d91-186">Serveur</span><span class="sxs-lookup"><span data-stu-id="45d91-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="45d91-187">1</span><span class="sxs-lookup"><span data-stu-id="45d91-187">1</span></span>
</dt> <dd>

<span data-ttu-id="45d91-188">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="45d91-188">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="45d91-189">2</span><span class="sxs-lookup"><span data-stu-id="45d91-189">2</span></span>
</dt> <dd>

<span data-ttu-id="45d91-190">Default</span><span class="sxs-lookup"><span data-stu-id="45d91-190">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d91-191">**PolicySourceStartIn**</span><span class="sxs-lookup"><span data-stu-id="45d91-191">**PolicySourceStartIn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-192">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45d91-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-194">Indique si la propriété **Started** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="45d91-194">Indicates whether the **StartIn** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="45d91-195">0</span><span class="sxs-lookup"><span data-stu-id="45d91-195">0</span></span>
</dt> <dd>

<span data-ttu-id="45d91-196">Serveur</span><span class="sxs-lookup"><span data-stu-id="45d91-196">Server</span></span>

</dd> <dt>

<span data-ttu-id="45d91-197">1</span><span class="sxs-lookup"><span data-stu-id="45d91-197">1</span></span>
</dt> <dd>

<span data-ttu-id="45d91-198">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="45d91-198">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="45d91-199">2</span><span class="sxs-lookup"><span data-stu-id="45d91-199">2</span></span>
</dt> <dd>

<span data-ttu-id="45d91-200">Default</span><span class="sxs-lookup"><span data-stu-id="45d91-200">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="45d91-201">**Startin**</span><span class="sxs-lookup"><span data-stu-id="45d91-201">**Startin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d91-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-204">Chemin d’accès du répertoire de travail du programme que l’utilisateur exécutera immédiatement après l’ouverture de session sur le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="45d91-204">The path of the working directory of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="45d91-205">**État**</span><span class="sxs-lookup"><span data-stu-id="45d91-205">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d91-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45d91-208">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="45d91-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="45d91-209">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="45d91-209">Current status of the object.</span></span> <span data-ttu-id="45d91-210">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="45d91-210">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="45d91-211">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="45d91-211">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="45d91-212">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="45d91-212">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="45d91-213">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="45d91-213">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="45d91-214">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="45d91-214">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="45d91-215">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="45d91-215">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="45d91-216">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="45d91-216">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45d91-217">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="45d91-217">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45d91-218">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="45d91-218">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45d91-219">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="45d91-219">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45d91-220">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="45d91-220">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45d91-221">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="45d91-221">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45d91-222">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="45d91-222">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="45d91-223">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="45d91-223">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="45d91-224">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="45d91-224">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45d91-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="45d91-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45d91-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="45d91-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45d91-227">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="45d91-227">The name of the terminal.</span></span>

<span data-ttu-id="45d91-228">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="45d91-228">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="45d91-229">Notes</span><span class="sxs-lookup"><span data-stu-id="45d91-229">Remarks</span></span>

<span data-ttu-id="45d91-230">Sachez que les winstations qui sont associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="45d91-230">Be aware that Winstations that are associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="45d91-231">Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété **TerminalName** , les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="45d91-231">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="45d91-232">Ce code d’erreur est également retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="45d91-232">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="45d91-233">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="45d91-233">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="45d91-234">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="45d91-234">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="45d91-235">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="45d91-235">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="45d91-236">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="45d91-236">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="45d91-237">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="45d91-237">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="45d91-238">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="45d91-238">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="45d91-239">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="45d91-239">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="45d91-240">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="45d91-240">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="45d91-241">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45d91-241">Requirements</span></span>



| <span data-ttu-id="45d91-242">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45d91-242">Requirement</span></span> | <span data-ttu-id="45d91-243">Valeur</span><span class="sxs-lookup"><span data-stu-id="45d91-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45d91-244">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45d91-244">Minimum supported client</span></span><br/> | <span data-ttu-id="45d91-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45d91-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="45d91-246">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45d91-246">Minimum supported server</span></span><br/> | <span data-ttu-id="45d91-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45d91-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="45d91-248">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="45d91-248">Namespace</span></span><br/>                | <span data-ttu-id="45d91-249">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="45d91-249">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="45d91-250">MOF</span><span class="sxs-lookup"><span data-stu-id="45d91-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45d91-251"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45d91-251"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="45d91-252">DLL</span><span class="sxs-lookup"><span data-stu-id="45d91-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45d91-253"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45d91-253"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d91-254">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45d91-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d91-255">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="45d91-255">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

