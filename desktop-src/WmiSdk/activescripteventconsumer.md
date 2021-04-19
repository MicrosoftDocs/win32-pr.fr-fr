---
description: Exécute un script prédéfini dans un langage de script arbitraire lorsqu’un événement lui est remis.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: ActiveScriptEventConsumer, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545038"
---
# <a name="activescripteventconsumer-class"></a><span data-ttu-id="d3e24-103">ActiveScriptEventConsumer, classe</span><span class="sxs-lookup"><span data-stu-id="d3e24-103">ActiveScriptEventConsumer class</span></span>

<span data-ttu-id="d3e24-104">La classe **ActiveScriptEventConsumer** exécute un script prédéfini dans un langage de script arbitraire lorsqu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="d3e24-104">The **ActiveScriptEventConsumer** class runs a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span> <span data-ttu-id="d3e24-105">Cette classe est l’un des consommateurs d’événements standard fournis par WMI.</span><span class="sxs-lookup"><span data-stu-id="d3e24-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="d3e24-106">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="d3e24-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



<span data-ttu-id="d3e24-107">Vous pouvez configurer les performances de toutes les instances de **ActiveScriptEventConsumer** sur un système en définissant les valeurs de la propriété [**timeout**](scriptingstandardconsumersetting.md) ou **MaximumScripts** dans l’instance unique de **ScriptingStandardConsumerSetting**.</span><span class="sxs-lookup"><span data-stu-id="d3e24-107">You can configure the performance of all instances of **ActiveScriptEventConsumer** on a system by setting the values of either the [**Timeout**](scriptingstandardconsumersetting.md) or **MaximumScripts** property in the single instance of **ScriptingStandardConsumerSetting**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e24-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3e24-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a><span data-ttu-id="d3e24-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d3e24-109">Members</span></span>

<span data-ttu-id="d3e24-110">La classe **ActiveScriptEventConsumer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d3e24-110">The **ActiveScriptEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="d3e24-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3e24-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d3e24-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d3e24-112">Properties</span></span>

<span data-ttu-id="d3e24-113">La classe **ActiveScriptEventConsumer** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d3e24-113">The **ActiveScriptEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d3e24-114">**CreatorSID**</span><span class="sxs-lookup"><span data-stu-id="d3e24-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-115">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="d3e24-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e24-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-117">Tableau qui représente l’identificateur de sécurité (SID), qui identifie de façon unique le créateur du consommateur d’événements active script.</span><span class="sxs-lookup"><span data-stu-id="d3e24-117">Array that represents the security identifier (SID), which uniquely identifies the creator of the Active Script Event consumer.</span></span> <span data-ttu-id="d3e24-118">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="d3e24-118">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3e24-119">**KillTimeout**</span><span class="sxs-lookup"><span data-stu-id="d3e24-119">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-120">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3e24-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e24-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-122">Nombre, en secondes, pendant lequel le script est autorisé à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="d3e24-122">Number, in seconds, that the script is allowed to run.</span></span> <span data-ttu-id="d3e24-123">Si 0 (zéro), qui est la valeur par défaut, le script n’est pas arrêté.</span><span class="sxs-lookup"><span data-stu-id="d3e24-123">If 0 (zero), which is the default, the script is not terminated.</span></span>

</dd> <dt>

<span data-ttu-id="d3e24-124">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="d3e24-124">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d3e24-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e24-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-127">Nom de l’ordinateur auquel WMI envoie des événements.</span><span class="sxs-lookup"><span data-stu-id="d3e24-127">Name of the computer to which WMI sends events.</span></span> <span data-ttu-id="d3e24-128">Par Convention des consommateurs Microsoft standard, le consommateur de script ne peut pas être exécuté à distance.</span><span class="sxs-lookup"><span data-stu-id="d3e24-128">By convention of Microsoft standard consumers, the script consumer cannot be run remotely.</span></span> <span data-ttu-id="d3e24-129">Les consommateurs tiers peuvent également utiliser cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d3e24-129">Third-party consumers can also use this property.</span></span> <span data-ttu-id="d3e24-130">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="d3e24-130">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3e24-131">**MaximumQueueSize**</span><span class="sxs-lookup"><span data-stu-id="d3e24-131">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-132">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3e24-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e24-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-134">File d’attente maximale, en octets, pour le consommateur d’événements active script.</span><span class="sxs-lookup"><span data-stu-id="d3e24-134">Maximum queue, in bytes, for the Active Script Event consumer.</span></span> <span data-ttu-id="d3e24-135">Cette propriété est héritée de [**\_ \_ EventConsumer**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="d3e24-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3e24-136">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d3e24-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d3e24-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d3e24-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-139">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d3e24-139">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-140">Identificateur unique pour le consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="d3e24-140">Unique identifier for the event consumer.</span></span> <span data-ttu-id="d3e24-141">Si vous renommez le consommateur, le résultat est égal à deux consommateurs qui ont des noms différents.</span><span class="sxs-lookup"><span data-stu-id="d3e24-141">If you rename the consumer, the result is two equal consumers that have different names.</span></span>

</dd> <dt>

<span data-ttu-id="d3e24-142">**ScriptFileName**</span><span class="sxs-lookup"><span data-stu-id="d3e24-142">**ScriptFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d3e24-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e24-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-145">Nom du fichier à partir duquel le texte du script est lu, ce qui constitue une alternative à la spécification du texte du script dans la propriété **ScriptText** .</span><span class="sxs-lookup"><span data-stu-id="d3e24-145">Name of the file from which the script text is read, intended as an alternative to specifying the text of the script in the **ScriptText** property.</span></span> <span data-ttu-id="d3e24-146">Cette propriété doit avoir la **valeur null** si la propriété **ScriptText** n’a pas la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d3e24-146">This property must be **NULL** if the **ScriptText** property is not **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="d3e24-147">Lorsque vous spécifiez le **ScriptFileName**, il est important de sécuriser l’exécutable que vous lancez.</span><span class="sxs-lookup"><span data-stu-id="d3e24-147">When you specify the **ScriptFileName**, it is important to secure the executable that you are launching.</span></span> <span data-ttu-id="d3e24-148">Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou sécurisé à l’aide d’une liste de contrôle d’accès (ACL) forte, n’importe qui peut remplacer l’exécutable par un autre.</span><span class="sxs-lookup"><span data-stu-id="d3e24-148">If the executable is not in a secure location or secured with a strong access control list (ACL), anyone can replace the executable with a different one.</span></span> <span data-ttu-id="d3e24-149">Pour plus d’informations sur les listes de contrôle d’accès, consultez [création d’un descripteur de sécurité (SD) pour un nouvel objet en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="d3e24-149">For more information about ACLs, see [Creating a Security Descriptor (SD) for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="d3e24-150">**ScriptingEngine**</span><span class="sxs-lookup"><span data-stu-id="d3e24-150">**ScriptingEngine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d3e24-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e24-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-153">Nom du moteur de script à utiliser, par exemple, « VBScript ».</span><span class="sxs-lookup"><span data-stu-id="d3e24-153">Name of the scripting engine to use, for example, "VBScript".</span></span> <span data-ttu-id="d3e24-154">Cette propriété ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="d3e24-154">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d3e24-155">**ScriptText**</span><span class="sxs-lookup"><span data-stu-id="d3e24-155">**ScriptText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d3e24-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d3e24-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d3e24-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d3e24-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d3e24-158">Texte du script exprimé dans un langage connu du moteur de script.</span><span class="sxs-lookup"><span data-stu-id="d3e24-158">Text of the script that is expressed in a language known to the scripting engine.</span></span> <span data-ttu-id="d3e24-159">Cette propriété doit avoir la **valeur null** si la propriété **ScriptFileName** n’a pas la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d3e24-159">This property must be **NULL** if the **ScriptFileName** property is not **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3e24-160">Notes</span><span class="sxs-lookup"><span data-stu-id="d3e24-160">Remarks</span></span>

<span data-ttu-id="d3e24-161">Cette classe est dérivée de la classe abstraite [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="d3e24-161">This class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span> <span data-ttu-id="d3e24-162">Il se trouve dans l’espace de noms de l' \\ abonnement racine.</span><span class="sxs-lookup"><span data-stu-id="d3e24-162">It is located in the root\\subscription namespace.</span></span>

<span data-ttu-id="d3e24-163">Lorsque le texte d’un script est spécifié dans l’instance de consommateur d’événements, le script a accès à l’instance d’événement dans la variable d’environnement de script **TargetEvent**.</span><span class="sxs-lookup"><span data-stu-id="d3e24-163">When the text of a script is specified in the event consumer instance, the script has access to the event instance in the script environment variable **TargetEvent**.</span></span>

<span data-ttu-id="d3e24-164">Les scripts s’exécutent dans le contexte de sécurité LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="d3e24-164">The scripts run in the LocalSystem security context.</span></span> <span data-ttu-id="d3e24-165">Par mesure de sécurité, seul un administrateur système local ou un administrateur de domaine peut configurer le consommateur de script.</span><span class="sxs-lookup"><span data-stu-id="d3e24-165">As a security measure, only a local system administrator or a domain administrator can configure the scripting consumer.</span></span> <span data-ttu-id="d3e24-166">Les droits d’accès ne sont pas vérifiés jusqu’au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d3e24-166">Access rights are not checked until run time.</span></span> <span data-ttu-id="d3e24-167">Une fois le consommateur configuré, n’importe quel utilisateur peut déclencher l’événement qui provoque l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="d3e24-167">After the consumer is configured, any user can trigger the event that causes the script to .</span></span>

<span data-ttu-id="d3e24-168">L’échec du chargement du moteur de script ou de l’analyse et de la validation du script est considéré comme un échec.</span><span class="sxs-lookup"><span data-stu-id="d3e24-168">Failure to load the scripting engine or parse and validate the script is considered a failure.</span></span> <span data-ttu-id="d3e24-169">Les codes de retour d’erreur du script et l’arrêt du script à l’aide d’un délai d’attente sont également considérés comme des échecs.</span><span class="sxs-lookup"><span data-stu-id="d3e24-169">Error return codes from the script and terminating the script by using a time-out are also considered failures.</span></span>

<span data-ttu-id="d3e24-170">**ScriptText** ou **ScriptFileName** ne doit pas avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d3e24-170">Either **ScriptText** or **ScriptFileName** must be not **NULL**.</span></span> <span data-ttu-id="d3e24-171">Si les deux propriétés ont la **valeur null** ou not **null**, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="d3e24-171">If both properties are **NULL** or not **NULL**, an error is generated.</span></span>

<span data-ttu-id="d3e24-172">Lorsque WMI est exécuté en tant que service, les scripts exécutés par **ActiveScriptEventConsumer** ne génèrent pas de sortie écran.</span><span class="sxs-lookup"><span data-stu-id="d3e24-172">When WMI is run as a service, scripts run by **ActiveScriptEventConsumer** do not generate screen output.</span></span> <span data-ttu-id="d3e24-173">Les scripts qui utilisent **MsgBox** s’exécutent, mais ils n’affichent pas d’informations à l’écran.</span><span class="sxs-lookup"><span data-stu-id="d3e24-173">Scripts that use **MsgBox** do run, but they do not display information on the screen.</span></span> <span data-ttu-id="d3e24-174">L’exécution du service WMI en tant que fichier exécutable n’est pas prise en charge, mais WMI autorise les scripts qui utilisent la fonction **MsgBox** à afficher la sortie ou à accepter les entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d3e24-174">Running the WMI service as an executable file is not supported, but WMI allows scripts that use the **MsgBox** function to display output or accept user input.</span></span> <span data-ttu-id="d3e24-175">Aucune des méthodes fournies par l’objet [wscript](/previous-versions//at5ydy31(v=vs.85)) ne peut être utilisée, car **ActiveScriptEventConsumer** n’utilise pas Windows Script Host (WSH).</span><span class="sxs-lookup"><span data-stu-id="d3e24-175">None of the methods provided by the [WScript](/previous-versions//at5ydy31(v=vs.85)) object can be used because **ActiveScriptEventConsumer** does not use Windows Script Host (WSH).</span></span>

## <a name="examples"></a><span data-ttu-id="d3e24-176">Exemples</span><span class="sxs-lookup"><span data-stu-id="d3e24-176">Examples</span></span>

<span data-ttu-id="d3e24-177">L’exemple de création d’un [événement WMI permanent pour surveiller les fichiers](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell sur la Galerie TechNet utilise **ActiveScriptEventConsumer** dans le cadre d’un script complexe pour configurer une inscription d’événement WMI permanente.</span><span class="sxs-lookup"><span data-stu-id="d3e24-177">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **ActiveScriptEventConsumer** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3e24-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3e24-178">Requirements</span></span>



| <span data-ttu-id="d3e24-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3e24-179">Requirement</span></span> | <span data-ttu-id="d3e24-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3e24-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e24-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3e24-181">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e24-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d3e24-182">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d3e24-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3e24-183">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e24-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d3e24-184">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d3e24-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3e24-185">Namespace</span></span><br/>                | <span data-ttu-id="d3e24-186">\\Abonnement racine</span><span class="sxs-lookup"><span data-stu-id="d3e24-186">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="d3e24-187">MOF</span><span class="sxs-lookup"><span data-stu-id="d3e24-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3e24-188"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3e24-188"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3e24-189">DLL</span><span class="sxs-lookup"><span data-stu-id="d3e24-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3e24-190"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3e24-190"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3e24-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3e24-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3e24-192">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="d3e24-192">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="d3e24-193">Exécution d’un script basé sur un événement</span><span class="sxs-lookup"><span data-stu-id="d3e24-193">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="d3e24-194">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="d3e24-194">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="d3e24-195">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="d3e24-195">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="d3e24-196">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="d3e24-196">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="d3e24-197">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="d3e24-197">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md)
</dt> </dl>

 

