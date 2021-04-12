---
description: La classe singleton ScriptingStandardConsumerSetting fournit des données d’inscription communes à toutes les instances de la classe de consommateur standard ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: ScriptingStandardConsumerSetting, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202167"
---
# <a name="scriptingstandardconsumersetting-class"></a><span data-ttu-id="67da7-103">ScriptingStandardConsumerSetting, classe</span><span class="sxs-lookup"><span data-stu-id="67da7-103">ScriptingStandardConsumerSetting class</span></span>

<span data-ttu-id="67da7-104">La classe singleton **ScriptingStandardConsumerSetting** fournit des données d’inscription communes à toutes les instances de la classe de consommateur standard [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="67da7-104">The singleton **ScriptingStandardConsumerSetting** class provides registration data that is common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) standard consumer class.</span></span> <span data-ttu-id="67da7-105">Une instance **ActiveScriptEventConsumer** utilise les propriétés **MaximumScripts** et **timeout** .</span><span class="sxs-lookup"><span data-stu-id="67da7-105">An **ActiveScriptEventConsumer** instance uses the **MaximumScripts** and **Timeout** properties.</span></span> <span data-ttu-id="67da7-106">Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="67da7-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="67da7-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="67da7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="67da7-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="67da7-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="67da7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67da7-109">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a><span data-ttu-id="67da7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="67da7-110">Members</span></span>

<span data-ttu-id="67da7-111">La classe **ScriptingStandardConsumerSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="67da7-111">The **ScriptingStandardConsumerSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="67da7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67da7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67da7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67da7-113">Properties</span></span>

<span data-ttu-id="67da7-114">La classe **ScriptingStandardConsumerSetting** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="67da7-114">The **ScriptingStandardConsumerSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67da7-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="67da7-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da7-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67da7-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67da7-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67da7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67da7-118">Qualificateurs : [**MaxLen**](standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="67da7-118">Qualifiers: [**MaxLen**](standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="67da7-119">Description succincte d’un objet d’une chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="67da7-119">A short description of an object a one line string.</span></span> <span data-ttu-id="67da7-120">Contient la chaîne **ScriptingStandardConsumerSetting** , car il s’agit d’une classe singleton.</span><span class="sxs-lookup"><span data-stu-id="67da7-120">Contains the string **ScriptingStandardConsumerSetting** because this is a singleton class.</span></span>

</dd> <dt>

<span data-ttu-id="67da7-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="67da7-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da7-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67da7-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67da7-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67da7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67da7-124">Description textuelle d’un objet.</span><span class="sxs-lookup"><span data-stu-id="67da7-124">A text description of an object.</span></span>

</dd> <dt>

<span data-ttu-id="67da7-125">**MaximumScripts**</span><span class="sxs-lookup"><span data-stu-id="67da7-125">**MaximumScripts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da7-126">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67da7-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67da7-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67da7-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="67da7-128">Nombre maximal de scripts qui sont exécutés avant qu’un consommateur ne démarre une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="67da7-128">Maximum number of scripts that are run before a consumer starts a new instance.</span></span> <span data-ttu-id="67da7-129">Pour éliminer les fuites de mémoire des scripts, arrêtez le consommateur régulièrement.</span><span class="sxs-lookup"><span data-stu-id="67da7-129">To clear out memory leaks from scripts, shut down the consumer regularly.</span></span> <span data-ttu-id="67da7-130">La valeur par défaut est 300.</span><span class="sxs-lookup"><span data-stu-id="67da7-130">The default value is 300.</span></span>

</dd> <dt>

<span data-ttu-id="67da7-131">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="67da7-131">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da7-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="67da7-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67da7-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="67da7-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67da7-134">Qualificateurs : [**MaxLen**](standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="67da7-134">Qualifiers: [**MaxLen**](standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67da7-135">Identificateur de l’objet de paramètre.</span><span class="sxs-lookup"><span data-stu-id="67da7-135">Identifier for the setting object.</span></span>

</dd> <dt>

<span data-ttu-id="67da7-136">**Délai d'expiration**</span><span class="sxs-lookup"><span data-stu-id="67da7-136">**Timeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67da7-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67da7-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="67da7-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="67da7-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="67da7-139">Qualificateurs : [**unités**](standard-qualifiers.md) (« minutes »)</span><span class="sxs-lookup"><span data-stu-id="67da7-139">Qualifiers: [**units**](standard-qualifiers.md) ("Minutes")</span></span>
</dt> </dl>

<span data-ttu-id="67da7-140">Nombre maximal de minutes avant le démarrage d’une nouvelle instance par un consommateur.</span><span class="sxs-lookup"><span data-stu-id="67da7-140">Maximum number of minutes before a consumer starts a new instance.</span></span> <span data-ttu-id="67da7-141">Si la valeur est 0 (zéro), la propriété **MaximumScripts** contrôle la durée de vie du consommateur.</span><span class="sxs-lookup"><span data-stu-id="67da7-141">If 0 (zero), the **MaximumScripts** property controls the consumer lifetime.</span></span> <span data-ttu-id="67da7-142">La plage valide pour le **délai d’attente** est comprise entre 0 et 71 000 et la valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="67da7-142">The valid range for **Timeout** is 0 through 71,000 and the default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67da7-143">Notes</span><span class="sxs-lookup"><span data-stu-id="67da7-143">Remarks</span></span>

<span data-ttu-id="67da7-144">L’instance unique de la classe **ScriptingStandardConsumerSetting** réside dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="67da7-144">The single instance of the **ScriptingStandardConsumerSetting** class resides in the root\\cimv2 namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="67da7-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67da7-145">Requirements</span></span>



| <span data-ttu-id="67da7-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67da7-146">Requirement</span></span> | <span data-ttu-id="67da7-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="67da7-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67da7-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67da7-148">Minimum supported client</span></span><br/> | <span data-ttu-id="67da7-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67da7-149">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="67da7-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67da7-150">Minimum supported server</span></span><br/> | <span data-ttu-id="67da7-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67da7-151">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="67da7-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="67da7-152">Namespace</span></span><br/>                | <span data-ttu-id="67da7-153">\\Abonnement racine</span><span class="sxs-lookup"><span data-stu-id="67da7-153">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="67da7-154">MOF</span><span class="sxs-lookup"><span data-stu-id="67da7-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67da7-155"><dt>Scrcons. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67da7-155"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="67da7-156">DLL</span><span class="sxs-lookup"><span data-stu-id="67da7-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67da7-157"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67da7-157"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67da7-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67da7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67da7-159">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="67da7-159">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[<span data-ttu-id="67da7-160">Classes de consommateur standard</span><span class="sxs-lookup"><span data-stu-id="67da7-160">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="67da7-161">Exécution d’un script basé sur un événement</span><span class="sxs-lookup"><span data-stu-id="67da7-161">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="67da7-162">Création d’un consommateur logique</span><span class="sxs-lookup"><span data-stu-id="67da7-162">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="67da7-163">Réception d’événements à tout moment</span><span class="sxs-lookup"><span data-stu-id="67da7-163">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="67da7-164">**\_\_EventConsumer**</span><span class="sxs-lookup"><span data-stu-id="67da7-164">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

