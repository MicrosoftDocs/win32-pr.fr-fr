---
description: La liste suivante répertorie les qualificateurs utilisés pour définir les classes de fournisseur d’affichage.
ms.assetid: 31a6af2d-33da-44f2-86d7-c467dd2f3e00
ms.tgt_platform: multiple
title: Qualificateurs spécifiques au fournisseur de vues
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: 76f28e4ba3433c168e1d0bf86887ee93df953444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209647"
---
# <a name="qualifiers-specific-to-the-view-provider"></a><span data-ttu-id="c9cc0-103">Qualificateurs spécifiques au fournisseur de vues</span><span class="sxs-lookup"><span data-stu-id="c9cc0-103">Qualifiers Specific to the View Provider</span></span>

<span data-ttu-id="c9cc0-104">La liste suivante répertorie les qualificateurs utilisés pour définir les classes de fournisseur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-104">The following lists the qualifiers use to define View Provider classes.</span></span>

> [!Note]  
> <span data-ttu-id="c9cc0-105">La classe de fournisseur d’affichages prend en charge uniquement les noms NetBIOS lors de l’utilisation de références distantes.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-105">The View provider class only supports NetBIOS names when using remote references.</span></span> <span data-ttu-id="c9cc0-106">Si vous utilisez une adresse IP ou un nom DNS dans une référence distante, la connexion échoue avec une erreur 0x800706BA.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-106">If you use an IP address or a DNS name in a remote reference, then the connection fails with a 0x800706ba error.</span></span>

 

<dt>

<span data-ttu-id="c9cc0-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Directe**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-107"><span id="Direct"></span><span id="direct"></span><span id="DIRECT"></span>**Direct**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-108">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-108">Data type: **boolean**</span></span>

<span data-ttu-id="c9cc0-109">Utilisé avec les propriétés d’association de vue pour empêcher le mappage des références d’association à une référence de vue.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-109">Used with view association properties to prevent association references from being mapped to a view reference.</span></span>

<span data-ttu-id="c9cc0-110">L’exemple suivant définit la propriété **GroupComponent** comme une référence d’association qui n’est pas mappée dans la référence de vue.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-110">The following example defines the property **GroupComponent** as an association reference that is not mapped in the view reference.</span></span>


```mof
[Direct, key, PropertySources
{"GroupComponent"}]
```



</dd> <dt>

<span data-ttu-id="c9cc0-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-111"><span id="HiddenDefault"></span><span id="hiddendefault"></span><span id="HIDDENDEFAULT"></span>**HiddenDefault**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-112">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-112">Data type: **boolean**</span></span>

<span data-ttu-id="c9cc0-113">Valeur par défaut pour une propriété de la classe d’affichage basée sur une propriété de classe source avec une valeur par défaut différente.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-113">Default value for a view class property based on a source class property with a different default value.</span></span> <span data-ttu-id="c9cc0-114">La classe source sous-jacente est impliquée dans la vue.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-114">The underlying source class is implied by the view.</span></span>

<span data-ttu-id="c9cc0-115">Par exemple, la classe source [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) a une [](boolean.md) propriété booléenne **RunRepeatedly** qui indique si le travail doit être effectué périodiquement ou une seule fois.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-115">For example, the source class [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) has a [boolean](boolean.md) property **RunRepeatedly** that indicates whether the job is to be carried out periodically or one time only.</span></span> <span data-ttu-id="c9cc0-116">La valeur par défaut de **RunRepeatedly** n’est pas true pour **Win32 \_ ScheduledJob**, mais est true pour la classe d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-116">The default value of **RunRepeatedly** is not True for **Win32\_ScheduledJob**, but is True for the view class.</span></span>


```mof
#pragma namespace("\\\\.\\root\\ns_view")
[Union,
ViewSources{"select * from Win32_ScheduledJob where RunRepeatedly=True"},
ViewSpaces{"\\\\.\\root\\cimv2"},
dynamic,provider("MS_VIEW_INSTANCE_PROVIDER")]
Class View_PeriodicJob
{
 [key, PropertySources{"JobId"}]
 uint32 JobId;
 [PropertySources{"Command"}]
 string Command;
 [HiddenDefault,PropertySources{"RunRepeatedly"}]
 boolean Repeat = True;
};
```



</dd> <dt>

<span data-ttu-id="c9cc0-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-117"><span id="JoinOn"></span><span id="joinon"></span><span id="JOINON"></span>**JoinOn**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-118">Data type: **string**</span></span>

<span data-ttu-id="c9cc0-119">Définit comment les instances de classe source sont jointes dans les classes de vue de jointure.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-119">Defines how source class instances are joined in join view classes.</span></span> <span data-ttu-id="c9cc0-120">L’exemple suivant montre comment utiliser le qualificateur **JoinOn** pour joindre deux classes sources.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-120">The following example shows how to use the **JoinOn** qualifier to join two source classes.</span></span>


```mof
JoinOn("Win32Perf_RawProcess.IDProcess = Win32Perf_RawThread.IDProcess")
```



</dd> <dt>

<span data-ttu-id="c9cc0-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-121"><span id="MethodSource"></span><span id="methodsource"></span><span id="METHODSOURCE"></span>**MethodSource**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-122">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-122">Data type: **string array**</span></span>

<span data-ttu-id="c9cc0-123">Méthode source à exécuter pour la méthode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-123">Source method to execute for the view method.</span></span> <span data-ttu-id="c9cc0-124">Pour obtenir une syntaxe similaire, consultez [qualificateur PropertySources](propertysources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="c9cc0-124">For similar syntax, see [PropertySources Qualifier](propertysources-qualifier.md).</span></span> <span data-ttu-id="c9cc0-125">La signature de la méthode doit correspondre exactement à la signature de la classe source.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-125">The signature of the method must match the signature of the source class exactly.</span></span> <span data-ttu-id="c9cc0-126">Copiez la signature de la méthode à partir du fichier MOF qui définit la classe source.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-126">Copy the method signature from the MOF file that defines the source class.</span></span> <span data-ttu-id="c9cc0-127">L’exemple ci-dessous définit une méthode à partir de la méthode [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="c9cc0-127">The example below defines a method from the [**ClearEventLog**](/previous-versions/windows/desktop/eventlogprov/cleareventlog-method-in-class-win32-nteventlogfile) method of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)):</span></span>


```mof
[implemented, MethodSource
{"ClearEventlog"}]
  uint32   VClearEventlog([in] string ArchiveFileName);
```



<span data-ttu-id="c9cc0-128">Ce qualificateur est valide uniquement lorsqu’il est utilisé avec les vues Union.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-128">This qualifier is only valid when it is used with union views.</span></span>

</dd> <dt>

<span data-ttu-id="c9cc0-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="c9cc0-129"><span id="PostJoinFilter"></span><span id="postjoinfilter"></span><span id="POSTJOINFILTER"></span>[**PostJoinFilter**](postjoinfilter-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-130">Data type: **string**</span></span>

<span data-ttu-id="c9cc0-131">Requête WQL pour filtrer les instances une fois qu’elles ont été jointes dans une classe join.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-131">WQL query to filter instances after they have been joined in a join class.</span></span>

</dd> <dt>

<span data-ttu-id="c9cc0-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="c9cc0-132"><span id="PropertySources"></span><span id="propertysources"></span><span id="PROPERTYSOURCES"></span>[**PropertySources**](propertysources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-133">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-133">Data type: **string array**</span></span>

<span data-ttu-id="c9cc0-134">Propriétés sources à partir desquelles une propriété de la classe d’affichage obtient des données.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-134">Source properties from which a view class property gets data.</span></span>

</dd> <dt>

<span data-ttu-id="c9cc0-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**UE**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-135"><span id="Union"></span><span id="union"></span><span id="UNION"></span>**Union**</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-136">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-136">Data type: **boolean**</span></span>

<span data-ttu-id="c9cc0-137">Indique si vous définissez une classe Union.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-137">Indicates whether you are defining a union class.</span></span> <span data-ttu-id="c9cc0-138">Les vues Union contiennent des instances basées sur l’Union des instances source.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-138">Union views contain instances based on the union of source instances.</span></span> <span data-ttu-id="c9cc0-139">Par exemple, vous pouvez déclarer ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c9cc0-139">For example, you might declare the following:</span></span>


```mof
Union, ViewSources{"SELECT Handle, Name, CreationDate FROM Win32_Process", 
                   "SELECT Caption, Name, ProcessHandle FROM Win32_Thread"}.
```



</dd> <dt>

<span data-ttu-id="c9cc0-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="c9cc0-140"><span id="ViewSources"></span><span id="viewsources"></span><span id="VIEWSOURCES"></span>[**ViewSources**](viewsources-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-141">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-141">Data type: **string array**</span></span>

<span data-ttu-id="c9cc0-142">Ensemble de requêtes de Langage de requêtes WMI (WQL) (WQL) qui définissent les instances source et les propriétés utilisées dans une classe d’affichage spécifique.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-142">Set of WMI Query Language (WQL) queries that define the source instances and properties used in a specific view class.</span></span> <span data-ttu-id="c9cc0-143">La correspondance de position de tous les qualificateurs de tableau est importante.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-143">Positional correspondence of all the array qualifiers is important.</span></span>

</dd> <dt>

<span data-ttu-id="c9cc0-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="c9cc0-144"><span id="ViewSpaces"></span><span id="viewspaces"></span><span id="VIEWSPACES"></span>[**ViewSpaces**](viewspaces-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="c9cc0-145">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="c9cc0-145">Data type: **string array**</span></span>

<span data-ttu-id="c9cc0-146">Espaces de noms où se trouvent les instances source.</span><span class="sxs-lookup"><span data-stu-id="c9cc0-146">Namespaces where the source instances are located.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9cc0-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9cc0-147">Requirements</span></span>



| <span data-ttu-id="c9cc0-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9cc0-148">Requirement</span></span> | <span data-ttu-id="c9cc0-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9cc0-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c9cc0-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9cc0-150">Minimum supported client</span></span><br/> | <span data-ttu-id="c9cc0-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9cc0-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c9cc0-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9cc0-152">Minimum supported server</span></span><br/> | <span data-ttu-id="c9cc0-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9cc0-153">Windows Server 2008</span></span><br/> |



 

