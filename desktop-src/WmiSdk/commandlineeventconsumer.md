---
description: La classe CommandLineEventConsumer démarre un processus arbitraire dans le système local lorsqu’un événement lui est remis.
ms.assetid: 0dcae783-1722-45a4-b5d4-3fcf455dacf8
ms.tgt_platform: multiple
title: CommandLineEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommandLineEventConsumer
- CommandLineEventConsumer.CreatorSID
- CommandLineEventConsumer.MachineName
- CommandLineEventConsumer.MaximumQueueSize
- CommandLineEventConsumer.CommandLineTemplate
- CommandLineEventConsumer.CreateNewConsole
- CommandLineEventConsumer.CreateNewProcessGroup
- CommandLineEventConsumer.CreateSeparateWowVdm
- CommandLineEventConsumer.CreateSharedWowVdm
- CommandLineEventConsumer.DesktopName
- CommandLineEventConsumer.ExecutablePath
- CommandLineEventConsumer.FillAttributes
- CommandLineEventConsumer.ForceOffFeedback
- CommandLineEventConsumer.ForceOnFeedback
- CommandLineEventConsumer.KillTimeout
- CommandLineEventConsumer.Name
- CommandLineEventConsumer.Priority
- CommandLineEventConsumer.RunInteractively
- CommandLineEventConsumer.ShowWindowCommand
- CommandLineEventConsumer.UseDefaultErrorMode
- CommandLineEventConsumer.WindowTitle
- CommandLineEventConsumer.WorkingDirectory
- CommandLineEventConsumer.XCoordinate
- CommandLineEventConsumer.XNumCharacters
- CommandLineEventConsumer.XSize
- CommandLineEventConsumer.YCoordinate
- CommandLineEventConsumer.YNumCharacters
- CommandLineEventConsumer.YSize
- CommandLineEventConsumer.FillAttribute
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: 1784ba116417f6ed94aed2249a797cf8de4b3527
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106539267"
---
# <a name="commandlineeventconsumer-class"></a><span data-ttu-id="6a145-103">CommandLineEventConsumer, classe</span><span class="sxs-lookup"><span data-stu-id="6a145-103">CommandLineEventConsumer class</span></span>

<span data-ttu-id="6a145-104">La classe **CommandLineEventConsumer** démarre un processus arbitraire dans le système local lorsqu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="6a145-104">The **CommandLineEventConsumer** class starts an arbitrary process in the local system when an event is delivered to it.</span></span> <span data-ttu-id="6a145-105">Cette classe est l’un des consommateurs d’événements standard fournis par WMI.</span><span class="sxs-lookup"><span data-stu-id="6a145-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="6a145-106">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

> [!Note]  
> <span data-ttu-id="6a145-107">Quand vous utilisez la classe **CommandLineEventConsumer** , sécurisez l’exécutable que vous souhaitez démarrer.</span><span class="sxs-lookup"><span data-stu-id="6a145-107">When using the **CommandLineEventConsumer** class, secure the executable that you want to start.</span></span> <span data-ttu-id="6a145-108">Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou sécurisé à l’aide d’une liste de contrôle d’accès (ACL) forte, un utilisateur non autorisé peut remplacer votre exécutable par un exécutable malveillant.</span><span class="sxs-lookup"><span data-stu-id="6a145-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), an unauthorized user can replace your executable with a malicious executable.</span></span> <span data-ttu-id="6a145-109">Pour plus d’informations sur les listes de contrôle d’accès, consultez la section sécurité du kit de développement logiciel (SDK) Microsoft Windows et consultez [création d’un descripteur de sécurité pour un nouvel objet](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="6a145-109">For more information about ACLs, visit the Security section of the Microsoft Windows Software Development Kit (SDK), and see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6a145-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a145-110">Syntax</span></span>

``` syntax
[AMENDMENT]
class CommandLineEventConsumer : __EventConsumer
{
  uint8   CreatorSID[];
  string  MachineName;
  uint32  MaximumQueueSize;
  string  CommandLineTemplate;
  boolean CreateNewConsole = False;
  boolean CreateNewProcessGroup = True;
  boolean CreateSeparateWowVdm = False;
  boolean CreateSharedWowVdm = False;
  string  DesktopName;
  string  ExecutablePath;
  uint32  FillAttributes;
  boolean ForceOffFeedback = False;
  boolean ForceOnFeedback = False;
  uint32  KillTimeout = 0;
  string  Name;
  sint32  Priority = 0x20;
  boolean RunInteractively = False;
  uint32  ShowWindowCommand;
  boolean UseDefaultErrorMode = False;
  string  WindowTitle;
  string  WorkingDirectory;
  uint32  XCoordinate;
  uint32  XNumCharacters;
  uint32  XSize;
  uint32  YCoordinate;
  uint32  YNumCharacters;
  uint32  YSize;
  uint32  FillAttribute;
};
```

## <a name="members"></a><span data-ttu-id="6a145-111">Membres</span><span class="sxs-lookup"><span data-stu-id="6a145-111">Members</span></span>

<span data-ttu-id="6a145-112">La classe **CommandLineEventConsumer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a145-112">The **CommandLineEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="6a145-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a145-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a145-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6a145-114">Properties</span></span>

<span data-ttu-id="6a145-115">La classe **CommandLineEventConsumer** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a145-115">The **CommandLineEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a145-116">**CommandLineTemplate**</span><span class="sxs-lookup"><span data-stu-id="6a145-116">**CommandLineTemplate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a145-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-119">Modèle de chaîne standard qui spécifie le processus à démarrer.</span><span class="sxs-lookup"><span data-stu-id="6a145-119">Standard string template that specifies the process to be started.</span></span> <span data-ttu-id="6a145-120">Cette propriété peut avoir la **valeur null** et la propriété **ExecutablePath** est utilisée comme ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="6a145-120">This property can be **NULL**, and the **ExecutablePath** property is used as the command line.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-121">**CreateNewConsole**</span><span class="sxs-lookup"><span data-stu-id="6a145-121">**CreateNewConsole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-122">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6a145-124">Not used.</span></span> <span data-ttu-id="6a145-125">Si une valeur est assignée à cette propriété, un message de suivi est généré.</span><span class="sxs-lookup"><span data-stu-id="6a145-125">If a value is assigned to this property, a tracing message is generated.</span></span> <span data-ttu-id="6a145-126">Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-126">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a145-127">**CreateNewProcessGroup**</span><span class="sxs-lookup"><span data-stu-id="6a145-127">**CreateNewProcessGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-130">Si la **valeur est true**, le nouveau processus est le processus racine d’un nouveau groupe de processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-130">If **True**, the new process is the root process of a new process group.</span></span> <span data-ttu-id="6a145-131">Le groupe de processus comprend tous les processus qui sont des descendants de ce processus racine.</span><span class="sxs-lookup"><span data-stu-id="6a145-131">The process group includes all processes that are descendants of this root process.</span></span> <span data-ttu-id="6a145-132">L’identificateur de processus du nouveau groupe de processus est le même que cet identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-132">The process identifier of the new process group is the same as this process identifier.</span></span> <span data-ttu-id="6a145-133">Les groupes de processus sont utilisés par la méthode [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) pour permettre l’envoi d’un signal Ctrl + C ou CTRL + ATTN à un groupe de processus de console.</span><span class="sxs-lookup"><span data-stu-id="6a145-133">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable sending a CTRL+C or CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-134">**CreateSeparateWowVdm**</span><span class="sxs-lookup"><span data-stu-id="6a145-134">**CreateSeparateWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-135">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-137">Si la **valeur est true**, le nouveau processus s’exécute sur une machine virtuelle DOS privée (VDM).</span><span class="sxs-lookup"><span data-stu-id="6a145-137">If **True**, the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="6a145-138">Cela est valide uniquement lors du démarrage d’une application exécutée sur un système d’exploitation Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6a145-138">This is only valid when starting an application running on a 16-bit Windows operating system.</span></span> <span data-ttu-id="6a145-139">Si la valeur est **false**, toutes les applications qui s’exécutent sur un système d’exploitation Windows 16 bits s’exécutent en tant que threads dans un VDM partagé unique.</span><span class="sxs-lookup"><span data-stu-id="6a145-139">If set to **False**, all applications running on a 16-bit Windows operating system run as threads in a single, shared VDM.</span></span> <span data-ttu-id="6a145-140">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6a145-140">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-141">**CreateSharedWowVdm**</span><span class="sxs-lookup"><span data-stu-id="6a145-141">**CreateSharedWowVdm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-144">Si la **valeur est true**, la méthode [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) exécute le nouveau processus dans l’ordinateur virtuel dos (VDM) partagé.</span><span class="sxs-lookup"><span data-stu-id="6a145-144">If **True**, the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method runs the new process in the shared Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="6a145-145">Cette propriété peut remplacer le commutateur DefaultSeparateVDM dans la section Windows de Win.ini si la valeur est **true**.</span><span class="sxs-lookup"><span data-stu-id="6a145-145">This property can override the DefaultSeparateVDM switch in the Windows section of Win.ini if set to **True**.</span></span> <span data-ttu-id="6a145-146">Pour plus d’informations, consultez la section Notes de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="6a145-146">For more information, see the Remarks section of this topic.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-147">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="6a145-147">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-148">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="6a145-148">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6a145-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-150">Identificateur de sécurité (SID) qui identifie de façon unique l’utilisateur qui crée un filtre.</span><span class="sxs-lookup"><span data-stu-id="6a145-150">Security identifier (SID) that uniquely identifies the user who creates a filter.</span></span> <span data-ttu-id="6a145-151">WMI stocke le SID de l’utilisateur qui crée une instance de [**\_ \_ EventConsumer**](--eventconsumer.md) ou le SID d’administrateur, selon le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6a145-151">WMI stores the SID of the user who creates an instance of [**\_\_EventConsumer**](--eventconsumer.md) or the Administrator SID, depending on the operating system.</span></span> <span data-ttu-id="6a145-152">Pour plus d’informations, consultez [liaison d’un filtre d’événements avec un consommateur logique](binding-an-event-filter-with-a-logical-consumer.md) et [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-152">For more information, see [Binding an Event Filter with a Logical Consumer](binding-an-event-filter-with-a-logical-consumer.md) and [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="6a145-153">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-153">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a145-154">**DesktopName**</span><span class="sxs-lookup"><span data-stu-id="6a145-154">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a145-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-157">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="6a145-157">Not used.</span></span> <span data-ttu-id="6a145-158">Si une valeur est affectée à cette propriété, un message de suivi est généré.</span><span class="sxs-lookup"><span data-stu-id="6a145-158">If a value is assigned to this property a tracing message is generated.</span></span> <span data-ttu-id="6a145-159">Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-159">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a145-160">**ExecutablePath**</span><span class="sxs-lookup"><span data-stu-id="6a145-160">**ExecutablePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a145-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-163">Module à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6a145-163">Module to execute.</span></span> <span data-ttu-id="6a145-164">La chaîne peut spécifier le chemin d’accès complet et le nom de fichier du module à exécuter, ou elle peut spécifier un nom partiel.</span><span class="sxs-lookup"><span data-stu-id="6a145-164">The string can specify the full path and file name of the module to execute, or it can specify a partial name.</span></span> <span data-ttu-id="6a145-165">Si un nom partiel est spécifié, le lecteur actif et le répertoire actif sont pris en défaut.</span><span class="sxs-lookup"><span data-stu-id="6a145-165">If a partial name is specified, the current drive and current directory are assumed.</span></span>

<span data-ttu-id="6a145-166">La propriété **ExecutablePath** peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6a145-166">The **ExecutablePath** property can be **NULL**.</span></span> <span data-ttu-id="6a145-167">Dans ce cas, le nom du module doit être le premier jeton délimité par des espaces blancs dans la valeur de la propriété **CommandLineTemplate** .</span><span class="sxs-lookup"><span data-stu-id="6a145-167">In that case, the module name must be the first white space-delimited token in the **CommandLineTemplate** property value.</span></span> <span data-ttu-id="6a145-168">Si vous utilisez un nom de fichier long qui contient un espace, utilisez des chaînes entre guillemets pour indiquer l’emplacement où se termine le nom de fichier et les arguments commencent à clarifier le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="6a145-168">If using a long file name that contains a space, use quoted strings to indicate where the file name ends and the arguments begin to clarify the file name.</span></span>

> [!Note]  
> <span data-ttu-id="6a145-169">Étant donné que la propriété **CommandLineTemplate** peut être un modèle dans lequel le module à exécuter est fourni par une variable, une propriété **ExecutablePath** **null** autorise le module spécifié dans le paramètre à exécuter, puis il est hors de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="6a145-169">Because the **CommandLineTemplate** property can be a template where the module to execute is supplied by a variable, a **NULL** **ExecutablePath** property permits the module that is specified in the parameter to execute, and then it is out of your control.</span></span> <span data-ttu-id="6a145-170">Définissez toujours la propriété **ExecutablePath** dans l’inscription **CommandLineEventConsumer** pour inclure l’exécutable requis, ce qui évite le remplacement par les paramètres d’événements.</span><span class="sxs-lookup"><span data-stu-id="6a145-170">Always set the **ExecutablePath** property in the **CommandLineEventConsumer** registration to include the required executable, which avoids overwriting by events parameters.</span></span> <span data-ttu-id="6a145-171">Si vous devez utiliser un modèle et une variable pour spécifier le module à exécuter, veillez à savoir qui dispose des privilèges d’écriture complets dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6a145-171">If you must use a template and variable to specify the module to execute, be careful about who is granted full write privilege in the namespace.</span></span>

 

</dd> <dt>

<span data-ttu-id="6a145-172">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="6a145-172">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-173">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-175">Spécifie le texte et les couleurs d’arrière-plan initiaux si une nouvelle fenêtre de console est créée dans une application console</span><span class="sxs-lookup"><span data-stu-id="6a145-175">Specifies the initial text and background colors if a new console window is created in a console application</span></span>

</dd> <dt>

<span data-ttu-id="6a145-176">**FillAttributes**</span><span class="sxs-lookup"><span data-stu-id="6a145-176">**FillAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-177">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a145-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6a145-179">Texte initial et couleurs d’arrière-plan, si une nouvelle fenêtre de console est créée dans une application console.</span><span class="sxs-lookup"><span data-stu-id="6a145-179">Initial text and background colors, if a new console window is created in a console application.</span></span> <span data-ttu-id="6a145-180">Cette propriété est ignorée dans une application GUI.</span><span class="sxs-lookup"><span data-stu-id="6a145-180">This property is ignored in a GUI application.</span></span> <span data-ttu-id="6a145-181">La valeur peut être n’importe quelle combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="6a145-181">The value can be any combination of the following values.</span></span>

<dt>

<span data-ttu-id="6a145-182">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6a145-182">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-183">premier plan bleu</span><span class="sxs-lookup"><span data-stu-id="6a145-183">blue foreground</span></span>

</dd> <dt>

<span data-ttu-id="6a145-184">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="6a145-184">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-185">premier plan vert</span><span class="sxs-lookup"><span data-stu-id="6a145-185">green foreground</span></span>

</dd> <dt>

<span data-ttu-id="6a145-186">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="6a145-186">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-187">premier plan rouge</span><span class="sxs-lookup"><span data-stu-id="6a145-187">red foreground</span></span>

</dd> <dt>

<span data-ttu-id="6a145-188">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="6a145-188">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-189">intensité du premier plan</span><span class="sxs-lookup"><span data-stu-id="6a145-189">foreground intensity</span></span>

</dd> <dt>

<span data-ttu-id="6a145-190">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="6a145-190">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-191">arrière-plan bleu</span><span class="sxs-lookup"><span data-stu-id="6a145-191">blue background</span></span>

</dd> <dt>

<span data-ttu-id="6a145-192">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="6a145-192">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-193">arrière-plan vert</span><span class="sxs-lookup"><span data-stu-id="6a145-193">green background</span></span>

</dd> <dt>

<span data-ttu-id="6a145-194">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="6a145-194">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-195">arrière-plan rouge</span><span class="sxs-lookup"><span data-stu-id="6a145-195">red background</span></span>

</dd> <dt>

<span data-ttu-id="6a145-196">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="6a145-196">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-197">intensité de l’arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6a145-197">background intensity</span></span>

</dd> </dl>

<span data-ttu-id="6a145-198">Par exemple, les combinaisons suivantes produisent du texte rouge sur un arrière-plan blanc :</span><span class="sxs-lookup"><span data-stu-id="6a145-198">For example, the following combinations produce red text on a white background:</span></span>


```mof
0x4 | 0x40 | 0x20 | 0x10
```



  <span data-ttu-id="6a145-199">ou</span><span class="sxs-lookup"><span data-stu-id="6a145-199">or</span></span>  


```mof
0x74
```



</dd> <dt>

<span data-ttu-id="6a145-200">**ForceOffFeedback**</span><span class="sxs-lookup"><span data-stu-id="6a145-200">**ForceOffFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-201">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-201">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-203">Si la **valeur est true**, le curseur de commentaires est forcé pendant le démarrage du processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-203">If **True**, the feedback cursor is forced off while the process is starting.</span></span> <span data-ttu-id="6a145-204">Le curseur normal s’affiche.</span><span class="sxs-lookup"><span data-stu-id="6a145-204">The normal cursor is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-205">**ForceOnFeedback**</span><span class="sxs-lookup"><span data-stu-id="6a145-205">**ForceOnFeedback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-206">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-206">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-208">Si la **valeur est true**, le curseur est en mode commentaires pendant deux secondes après l’appel de [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="6a145-208">If **True**, the cursor is in feedback mode for two seconds after [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) is called.</span></span> <span data-ttu-id="6a145-209">Pendant ces deux secondes, si le processus effectue le premier appel d’interface utilisateur graphique, le système accorde cinq secondes supplémentaires au processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-209">During those two seconds, if the process makes the first GUI call, the system gives five more seconds to the process.</span></span> <span data-ttu-id="6a145-210">Pendant ces cinq secondes, si le processus affiche une fenêtre, le système donne une autre période de cinq secondes au processus pour terminer le dessin de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a145-210">During those five seconds, if the process shows a window, the system gives another five seconds to the process to finish drawing the window.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-211">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="6a145-211">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-212">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-214">Nombre, en secondes, pendant lequel le service WMI attend avant de tuer un processus 0 (zéro) indique qu’un processus ne doit pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="6a145-214">Number, in seconds, that the WMI service waits before killing a process 0 (zero) indicates a process is not to be killed.</span></span> <span data-ttu-id="6a145-215">Le fait de tuer un processus empêche l’exécution indéfinie d’un processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-215">Killing a process prevents a process from running indefinitely.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-216">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="6a145-216">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a145-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-219">Nom de l’ordinateur sur lequel Windows Management Instrumentation (WMI) envoie des événements.</span><span class="sxs-lookup"><span data-stu-id="6a145-219">Name of the computer to which Windows Management Instrumentation (WMI) sends events.</span></span>

<span data-ttu-id="6a145-220">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-220">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a145-221">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="6a145-221">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-222">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-224">File d’attente maximale pour un consommateur spécifique, en octets.</span><span class="sxs-lookup"><span data-stu-id="6a145-224">Maximum queue for a specific consumer, in bytes.</span></span>

<span data-ttu-id="6a145-225">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-225">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="6a145-226">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6a145-226">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a145-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a145-229">Qualificateurs : [ **clé**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="6a145-229">Qualifiers: [**key**](key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="6a145-230">Nom unique d’un consommateur.</span><span class="sxs-lookup"><span data-stu-id="6a145-230">Unique name of a consumer.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-231">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="6a145-231">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-232">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="6a145-232">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-234">Niveau de priorité de planification des threads de processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-234">Scheduling priority level of the process threads.</span></span> <span data-ttu-id="6a145-235">La liste suivante répertorie les niveaux de priorité disponibles.</span><span class="sxs-lookup"><span data-stu-id="6a145-235">The following list lists the priority levels available.</span></span>

<dt>

<span data-ttu-id="6a145-236">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="6a145-236">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-237">Indique un processus normal sans besoins de planification.</span><span class="sxs-lookup"><span data-stu-id="6a145-237">Indicates a normal process without scheduling needs.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-238">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="6a145-238">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-239">Indique un processus dont les threads s’exécutent uniquement lorsque le système est inactif et qui sont précédés par les threads de tout processus s’exécutant dans une classe de priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="6a145-239">Indicates a process whose threads run only when the system is idle, and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="6a145-240">Par exemple, un écran de veille.</span><span class="sxs-lookup"><span data-stu-id="6a145-240">An example is a screen saver.</span></span> <span data-ttu-id="6a145-241">La classe de priorité Idle est héritée par les processus enfants.</span><span class="sxs-lookup"><span data-stu-id="6a145-241">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-242">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="6a145-242">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-243">Indique un processus qui exécute des tâches critiques de haute priorité.</span><span class="sxs-lookup"><span data-stu-id="6a145-243">Indicates a process that performs high-priority, time critical tasks.</span></span> <span data-ttu-id="6a145-244">Les threads d’un processus de classe de priorité élevée précèdent les threads de processus de classe de priorité normale ou d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="6a145-244">The threads of a high-priority class process preempts the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="6a145-245">Par exemple, la Liste des tâches, qui doit répondre rapidement lorsqu’elle est appelée par l’utilisateur, quelle que soit la charge sur le système.</span><span class="sxs-lookup"><span data-stu-id="6a145-245">An example is the Task List, which must respond quickly when called by the user regardless of the load on the system.</span></span> <span data-ttu-id="6a145-246">Soyez extrêmement vigilant lorsque vous utilisez la classe de priorité élevée, car une application liée au processeur avec une classe de priorité élevée peut utiliser presque tous les cycles disponibles.</span><span class="sxs-lookup"><span data-stu-id="6a145-246">Use extreme care when using the high-priority class, because a CPU-bound application with a high-priority class can use nearly all available cycles.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-247">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="6a145-247">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="6a145-248">Indique un processus qui a la priorité la plus élevée possible.</span><span class="sxs-lookup"><span data-stu-id="6a145-248">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="6a145-249">Les threads d’un processus de classe de priorité en temps réel devancent les threads de tous les autres processus, y compris les processus du système d’exploitation qui effectuent des tâches importantes.</span><span class="sxs-lookup"><span data-stu-id="6a145-249">The threads of a real-time priority class process preempt the threads of all other processes, including operating system processes that perform important tasks.</span></span> <span data-ttu-id="6a145-250">Par exemple, un processus en temps réel qui s’exécute depuis plus d’un court intervalle peut entraîner la non-vidage du cache disque ou l’absence de réponse de la souris.</span><span class="sxs-lookup"><span data-stu-id="6a145-250">For example, a real-time process that executes for more than a brief interval can cause disk caches not to flush, or cause the mouse to be unresponsive.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6a145-251">**RunInteractively**</span><span class="sxs-lookup"><span data-stu-id="6a145-251">**RunInteractively**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-252">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-254">Si la **valeur est true**, le processus est lancé dans la fenêtre interactive.</span><span class="sxs-lookup"><span data-stu-id="6a145-254">If **True**, the process is launched in the interactive WinStation.</span></span> <span data-ttu-id="6a145-255">Si la **valeur est false**, le processus est lancé dans la station de service par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a145-255">If **False**, the process is launched in the default service WinStation.</span></span> <span data-ttu-id="6a145-256">Cette propriété remplace la propriété **DesktopName** .</span><span class="sxs-lookup"><span data-stu-id="6a145-256">This property overrides the **DesktopName** property.</span></span> <span data-ttu-id="6a145-257">Cette propriété est utilisée uniquement localement, et uniquement si l’utilisateur interactif est le même utilisateur qui a configuré le consommateur.</span><span class="sxs-lookup"><span data-stu-id="6a145-257">This property is only used locally, and only if the interactive user is the same user who set up the consumer.</span></span>

<span data-ttu-id="6a145-258">À compter de Windows Vista, le processus qui exécute l’instance **CommandLineEventConsumer** est démarré sous le compte **LocalSystem** et est dans la session 0.</span><span class="sxs-lookup"><span data-stu-id="6a145-258">Starting with Windows Vista, the process running the **CommandLineEventConsumer** instance is started under the **LocalSystem** account and is in session 0.</span></span> <span data-ttu-id="6a145-259">Les services qui s’exécutent dans la session 0 ne peuvent pas interagir avec les sessions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a145-259">Services which run in session 0 cannot interact with user sessions.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-260">**ShowWindowCommand**</span><span class="sxs-lookup"><span data-stu-id="6a145-260">**ShowWindowCommand**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-261">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-263">Affichage de l’état de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a145-263">Window show state.</span></span> <span data-ttu-id="6a145-264">Il peut s’agir de l’une des valeurs qui peuvent être spécifiées dans le paramètre *nCmdShow* pour la fonction [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="6a145-264">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-265">**UseDefaultErrorMode**</span><span class="sxs-lookup"><span data-stu-id="6a145-265">**UseDefaultErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-266">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6a145-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-268">Si la **valeur est true**, le mode d’erreur par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6a145-268">If **True**, the default error mode is used.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-269">**WindowTitle**</span><span class="sxs-lookup"><span data-stu-id="6a145-269">**WindowTitle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a145-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-271">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-272">Titre qui apparaît dans la barre de titre du processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-272">Title that appears on the title bar of the process.</span></span> <span data-ttu-id="6a145-273">Cette propriété est ignorée pour les applications GUI.</span><span class="sxs-lookup"><span data-stu-id="6a145-273">This property is ignored for GUI applications.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-274">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="6a145-274">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-275">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6a145-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-277">Répertoire de travail pour ce processus.</span><span class="sxs-lookup"><span data-stu-id="6a145-277">Working directory for this process.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-278">**XCoordinate**</span><span class="sxs-lookup"><span data-stu-id="6a145-278">**XCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-279">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-281">Décalage X, en pixels, entre le bord gauche de l’écran et le bord gauche de la fenêtre, si une nouvelle fenêtre est créée.</span><span class="sxs-lookup"><span data-stu-id="6a145-281">X-offset, in pixels, from the left edge of the screen to the left edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-282">**XNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="6a145-282">**XNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-285">Largeur de la mémoire tampon d’écran, dans les colonnes de caractères, si une nouvelle fenêtre de console est créée.</span><span class="sxs-lookup"><span data-stu-id="6a145-285">Screen buffer width, in character columns, if a new console window is created.</span></span> <span data-ttu-id="6a145-286">Cette propriété est ignorée dans un processus GUI.</span><span class="sxs-lookup"><span data-stu-id="6a145-286">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-287">**XSize**</span><span class="sxs-lookup"><span data-stu-id="6a145-287">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-288">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-289">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-290">Largeur, en pixels, d’une nouvelle fenêtre, si une nouvelle fenêtre est créée.</span><span class="sxs-lookup"><span data-stu-id="6a145-290">Width, in pixels, of a new window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-291">**YCoordinate**</span><span class="sxs-lookup"><span data-stu-id="6a145-291">**YCoordinate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-292">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-293">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-294">Décalage Y, en pixels, entre le bord supérieur de l’écran et le bord supérieur de la fenêtre, si une nouvelle fenêtre est créée.</span><span class="sxs-lookup"><span data-stu-id="6a145-294">Y-offset, in pixels, from the top edge of the screen to the top edge of the window, if a new window is created.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-295">**YNumCharacters**</span><span class="sxs-lookup"><span data-stu-id="6a145-295">**YNumCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-296">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-297">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-298">Hauteur de la mémoire tampon d’écran, en lignes de caractères, si une nouvelle fenêtre de console est créée.</span><span class="sxs-lookup"><span data-stu-id="6a145-298">Screen buffer height, in character rows, if a new console window is created.</span></span> <span data-ttu-id="6a145-299">Cette propriété est ignorée dans un processus GUI.</span><span class="sxs-lookup"><span data-stu-id="6a145-299">This property is ignored in a GUI process.</span></span>

</dd> <dt>

<span data-ttu-id="6a145-300">**YSize**</span><span class="sxs-lookup"><span data-stu-id="6a145-300">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a145-301">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6a145-301">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6a145-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6a145-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6a145-303">Hauteur, en pixels, de la nouvelle fenêtre, si une nouvelle fenêtre est créée.</span><span class="sxs-lookup"><span data-stu-id="6a145-303">Height, in pixels, of the new window, if a new window is created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a145-304">Notes</span><span class="sxs-lookup"><span data-stu-id="6a145-304">Remarks</span></span>

<span data-ttu-id="6a145-305">La classe **CommandLineEventConsumer** est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="6a145-305">The **CommandLineEventConsumer** class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span>

<span data-ttu-id="6a145-306">La propriété **CreateSeparateWowVdm** indique si le nouveau processus s’exécute sur une machine virtuelle DOS privée (VDM).</span><span class="sxs-lookup"><span data-stu-id="6a145-306">The **CreateSeparateWowVdm** property indicates whether or not the new process runs in a private Virtual DOS Machine (VDM).</span></span> <span data-ttu-id="6a145-307">L’avantage de s’exécuter séparément est qu’un incident ne met fin qu’à un seul VDM.</span><span class="sxs-lookup"><span data-stu-id="6a145-307">The advantage of running separately is that a crash only terminates the single VDM.</span></span> <span data-ttu-id="6a145-308">Les programmes qui s’exécutent dans des VDM distincts continuent de fonctionner normalement, et les applications Windows 16 bits qui s’exécutent dans des VDM distincts ont des files d’attente d’entrée distinctes.</span><span class="sxs-lookup"><span data-stu-id="6a145-308">Programs running in distinct VDMs continue to function normally, and the 16-bit Windows-based applications running in separate VDMs have separate input queues.</span></span> <span data-ttu-id="6a145-309">Cela signifie que si une application cesse de répondre momentanément, les applications dans des VDM distincts continuent de recevoir l’entrée.</span><span class="sxs-lookup"><span data-stu-id="6a145-309">This means that if one application stops responding momentarily, the applications in separate VDMs continue to receive input.</span></span> <span data-ttu-id="6a145-310">L’inconvénient de l’exécution séparée est qu’il faut beaucoup plus de mémoire pour le faire.</span><span class="sxs-lookup"><span data-stu-id="6a145-310">The disadvantage of running separately is that it takes significantly more memory to do so.</span></span> <span data-ttu-id="6a145-311">Vous devez affecter à cette propriété la **valeur true** uniquement si l’utilisateur demande que des applications Windows 16 bits s’exécutent dans leur propre VDM.</span><span class="sxs-lookup"><span data-stu-id="6a145-311">You should set this property to **True** only if the user requests that 16-bit Windows-based applications run in their own VDM.</span></span>

> [!Note]  
> <span data-ttu-id="6a145-312">**CommandLineEventConsumer** utilise la méthode [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) en interne et transmet les propriétés **ExecutablePath** et **CommandLineTemplate** en tant que paramètres *lpApplicationName* et *lpCommandLine* .</span><span class="sxs-lookup"><span data-stu-id="6a145-312">The **CommandLineEventConsumer** uses the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method internally, and passes the **ExecutablePath** and **CommandLineTemplate** properties as the *lpApplicationName* and *lpCommandLine* parameters.</span></span> <span data-ttu-id="6a145-313">L’exemple de code format MOF (MOF) suivant n’utilise pas correctement **CommandLineEventConsumer** .</span><span class="sxs-lookup"><span data-stu-id="6a145-313">The following Managed Object Format (MOF) code example does not use **CommandLineEventConsumer** correctly.</span></span>

 


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="6a145-314">La méthode [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) passe *lpCommandLine* comme `argv[0]` , `argv[1]` , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6a145-314">The [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) method passes *lpCommandLine* as `argv[0]`, `argv[1]`, and so on.</span></span> <span data-ttu-id="6a145-315">Étant donné que `argv[0]` pour les applications 16 bits utilisées pour le nom de fichier exécutable, le code MOF précédent entraîne la création du processus comme si la commande suivante soit entrée à l’invite de commandes : **c : \\ Windows \\ system32 \\cscript.exe param1 param2**.</span><span class="sxs-lookup"><span data-stu-id="6a145-315">Because `argv[0]` for 16-bit applications used to be reserved for the executable file name, the previous MOF code results in the process being created as though the following command is entered at the command prompt: **c:\\windows\\system32\\cscript.exe param1 param2**.</span></span>

<span data-ttu-id="6a145-316">La commande précédente ne fonctionne pas, car Cscript.exe n’examine pas `argv[0]` , et ne reconnaît pas qu’elle ne contient pas son propre nom, mais autre chose (« c : \\ \\ scripts \\ \\MyScript.js »).</span><span class="sxs-lookup"><span data-stu-id="6a145-316">The previous command does not succeed because Cscript.exe does not look at `argv[0]`, and so it does not recognize that it does not contain its own name, but something else ("c:\\\\scripts\\\\MyScript.js").</span></span> <span data-ttu-id="6a145-317">L’exemple suivant identifie l’utilisation recommandée de **CommandLineEventConsumer**.</span><span class="sxs-lookup"><span data-stu-id="6a145-317">The following example identifies the recommended use of **CommandLineEventConsumer**.</span></span>


```mof
instance of CommandLineEventConsumer
{
  ExecutablePath = "C:\\windows\\system32\\cscript.exe";
  CommandLineTemplate = "C:\\windows\\system32\\cscript.exe"
    "C:\\scripts\\MyScript.js param1 param2";
};
```



<span data-ttu-id="6a145-318">L’utilisation précédente de **CommandLineEventConsumer** entraîne la création du processus comme si la commande suivante avait été entrée à l’invite de commandes : **c : \\ Windows \\ system32 \\cscript.exe c : \\ scripts \\MyScript.js param1 param2**</span><span class="sxs-lookup"><span data-stu-id="6a145-318">The previous use of **CommandLineEventConsumer** results in the process created as though the following command was entered at the command prompt: **c:\\windows\\system32\\cscript.exe c:\\scripts\\MyScript.js param1 param2**</span></span>

<span data-ttu-id="6a145-319">Étant donné que « c : \\ \\ scripts \\ \\MyScript.js » est maintenant `argv[1]` , il est visible par Cscript.exe et la commande est exécutée correctement.</span><span class="sxs-lookup"><span data-stu-id="6a145-319">Because "c:\\\\scripts\\\\MyScript.js" is now `argv[1]`, it is seen by Cscript.exe and the command succeeds.</span></span>

<span data-ttu-id="6a145-320">Pour plus d’informations, consultez la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="6a145-320">For more information, see the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="6a145-321">Exemples</span><span class="sxs-lookup"><span data-stu-id="6a145-321">Examples</span></span>

<span data-ttu-id="6a145-322">Pour obtenir un exemple d’utilisation de **CommandLineEventConsumer** pour créer un consommateur, consultez [exécution d’un programme à partir de la ligne de commande en fonction d’un événement](running-a-program-from-the-command-line-based-on-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="6a145-322">For an example of using **CommandLineEventConsumer** to create a consumer, see [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a145-323">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a145-323">Requirements</span></span>



| <span data-ttu-id="6a145-324">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a145-324">Requirement</span></span> | <span data-ttu-id="6a145-325">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a145-325">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a145-326">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a145-326">Minimum supported client</span></span><br/> | <span data-ttu-id="6a145-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a145-327">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a145-328">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a145-328">Minimum supported server</span></span><br/> | <span data-ttu-id="6a145-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a145-329">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a145-330">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a145-330">Namespace</span></span><br/>                | <span data-ttu-id="6a145-331">\\Abonnement racine</span><span class="sxs-lookup"><span data-stu-id="6a145-331">Root\\subscription</span></span><br/>                                                           |
| <span data-ttu-id="6a145-332">MOF</span><span class="sxs-lookup"><span data-stu-id="6a145-332">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a145-333"><dt>Wbemcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a145-333"><dt>Wbemcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a145-334">DLL</span><span class="sxs-lookup"><span data-stu-id="6a145-334">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a145-335"><dt>Wbemcons.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a145-335"><dt>Wbemcons.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a145-336">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a145-336">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a145-337">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="6a145-337">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="6a145-338">Surveillance et réponse aux événements avec des consommateurs standard</span><span class="sxs-lookup"><span data-stu-id="6a145-338">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[<span data-ttu-id="6a145-339">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="6a145-339">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="6a145-340">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="6a145-340">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="6a145-341">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="6a145-341">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

