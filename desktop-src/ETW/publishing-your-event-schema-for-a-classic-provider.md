---
description: Les fournisseurs classiques doivent utiliser format MOF (MOF) pour publier la disposition de leurs données d’événement. Les consommateurs peuvent ensuite lire la disposition publiée à partir de WMI au moment de l’exécution et l’utiliser pour lire les données d’événement.
ms.assetid: eb3d8422-2352-47cf-9825-cba9916791a9
title: Publication de votre schéma d’événement pour un fournisseur Classic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f51cfd30d0c9d73841ca906fb81e9d544dec88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318529"
---
# <a name="publishing-your-event-schema-for-a-classic-provider"></a><span data-ttu-id="17da8-104">Publication de votre schéma d’événement pour un fournisseur Classic</span><span class="sxs-lookup"><span data-stu-id="17da8-104">Publishing Your Event Schema for a Classic Provider</span></span>

<span data-ttu-id="17da8-105">Les fournisseurs [classiques](about-event-tracing.md) doivent utiliser [format MOF](../wmisdk/managed-object-format--mof-.md) (MOF) pour publier la disposition de leurs données d’événement.</span><span class="sxs-lookup"><span data-stu-id="17da8-105">[Classic](about-event-tracing.md) providers should use [Managed Object Format](../wmisdk/managed-object-format--mof-.md) (MOF) to publish the layout of their event data.</span></span> <span data-ttu-id="17da8-106">Les consommateurs peuvent ensuite lire la disposition publiée à partir de WMI au moment de l’exécution et l’utiliser pour lire les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="17da8-106">Consumers can then read the published layout from WMI at runtime and use it to read the event data.</span></span>

<span data-ttu-id="17da8-107">Si vous utilisez MOF pour publier la disposition de vos données d’événement dans WMI, vous créez généralement les trois types de classes MOF suivants dans l' \\ espace de noms WMI racine :</span><span class="sxs-lookup"><span data-stu-id="17da8-107">If you use MOF to publish the layout of your event data in WMI, you typically create the following three types of MOF classes in the root\\wmi namespace:</span></span>

-   [<span data-ttu-id="17da8-108">Classe de fournisseur MOF</span><span class="sxs-lookup"><span data-stu-id="17da8-108">A provider MOF class</span></span>](#provider-mof-classes)
-   [<span data-ttu-id="17da8-109">Une ou plusieurs classes MOF d’événements</span><span class="sxs-lookup"><span data-stu-id="17da8-109">One or more event MOF classes</span></span>](#event-mof-classes)
-   [<span data-ttu-id="17da8-110">Une ou plusieurs classes MOF de type d’événement</span><span class="sxs-lookup"><span data-stu-id="17da8-110">One or more event type MOF classes</span></span>](#event-type-mof-classes)

## <a name="provider-mof-classes"></a><span data-ttu-id="17da8-111">Classes MOF du fournisseur</span><span class="sxs-lookup"><span data-stu-id="17da8-111">Provider MOF classes</span></span>

<span data-ttu-id="17da8-112">Si vous publiez la disposition de vos données d’événement, vous devez créer une classe MOF qui identifie votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="17da8-112">If you publish the layout of your event data, you must create a MOF class that identifies your provider.</span></span> <span data-ttu-id="17da8-113">Cette classe doit dériver de la classe MOF **EventTrace** et doit être vide (aucune propriété ou méthode).</span><span class="sxs-lookup"><span data-stu-id="17da8-113">This class must derive from the **EventTrace** MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="17da8-114">La classe doit également inclure le qualificateur **GUID** qui identifie le fournisseur de manière unique.</span><span class="sxs-lookup"><span data-stu-id="17da8-114">The class must also include the **Guid** qualifier which uniquely identifies the provider.</span></span> <span data-ttu-id="17da8-115">Il s’agit du même GUID que celui utilisé lors de l’appel de la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) pour inscrire votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="17da8-115">This is the same GUID you use when you calling the [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) function to register your provider.</span></span>

## <a name="event-mof-classes"></a><span data-ttu-id="17da8-116">Classes MOF d’événements</span><span class="sxs-lookup"><span data-stu-id="17da8-116">Event MOF classes</span></span>

<span data-ttu-id="17da8-117">Une classe d’événement MOF définit une classe d’événements fournie par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="17da8-117">An event MOF class defines a class of events that the provider provides.</span></span> <span data-ttu-id="17da8-118">Cette classe dérive de la classe Provider MOF et doit être vide (aucune propriété ou méthode).</span><span class="sxs-lookup"><span data-stu-id="17da8-118">This class derives from the provider MOF class and must be empty (no properties or methods).</span></span> <span data-ttu-id="17da8-119">La classe doit également inclure le qualificateur **GUID** qui identifie de façon unique la classe des événements définis par ses classes enfants.</span><span class="sxs-lookup"><span data-stu-id="17da8-119">The class must also include the **Guid** qualifier which uniquely identifies the class of events that its child classes define.</span></span> <span data-ttu-id="17da8-120">Le fournisseur utilise ce même GUID lors de la définition du membre **GUID** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="17da8-120">The provider uses this same GUID when setting the **Guid** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="event-type-mof-classes"></a><span data-ttu-id="17da8-121">Classes MOF de type d’événement</span><span class="sxs-lookup"><span data-stu-id="17da8-121">Event type MOF classes</span></span>

<span data-ttu-id="17da8-122">Une classe MOF de type d’événement définit les données d’événement réelles.</span><span class="sxs-lookup"><span data-stu-id="17da8-122">An event type MOF class defines the actual event data.</span></span> <span data-ttu-id="17da8-123">Cette classe dérive de sa classe MOF d’événements parent.</span><span class="sxs-lookup"><span data-stu-id="17da8-123">This class derives from its parent event MOF class.</span></span> <span data-ttu-id="17da8-124">Lorsque vous nommez la classe MOF du type d’événement, la Convention consiste à utiliser le nom de classe de l’événement MOF au début du type d’événement nom de classe MOF.</span><span class="sxs-lookup"><span data-stu-id="17da8-124">When naming the event type MOF class, the convention is to use the event MOF class name at the beginning of the event type MOF class name.</span></span> <span data-ttu-id="17da8-125">Par exemple, si le nom de classe de l’événement MOF est HWConfig et que la classe de type d’événement MOF représente les informations de l’UC, vous devez nommer le type d’événement classe MOF, HWConfig \_ CPU.</span><span class="sxs-lookup"><span data-stu-id="17da8-125">For example, if the event MOF class name is HWConfig and the event type MOF class represents CPU information, you should name the event type MOF class, HWConfig\_CPU.</span></span>

<span data-ttu-id="17da8-126">Utilisez le qualificateur **eventType** sur la classe du type d’événement MOF pour identifier le type d’événement.</span><span class="sxs-lookup"><span data-stu-id="17da8-126">Use the **EventType** qualifier on the event type MOF class to identify the event type.</span></span> <span data-ttu-id="17da8-127">Si plusieurs types d’événements utilisent les mêmes données d’événement, ils peuvent utiliser la même classe MOF.</span><span class="sxs-lookup"><span data-stu-id="17da8-127">If multiple event types use the same event data, they can use the same MOF class.</span></span> <span data-ttu-id="17da8-128">Le fournisseur utilise la même valeur de type d’événement pour identifier l’événement lors de la définition du membre de **classe. type** de la structure d' [**\_ \_ en-tête de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="17da8-128">The provider uses the same event type value to identify the event when setting the **Class.Type** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

<span data-ttu-id="17da8-129">La classe MOF du type d’événement contient des propriétés.</span><span class="sxs-lookup"><span data-stu-id="17da8-129">The event type MOF class contains properties.</span></span> <span data-ttu-id="17da8-130">L’ordre de ces propriétés définit la disposition des données d’événement.</span><span class="sxs-lookup"><span data-stu-id="17da8-130">The order of these properties define the layout of the event data.</span></span> <span data-ttu-id="17da8-131">Le tableau suivant identifie les types de données et les qualificateurs que vous pouvez utiliser pour définir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="17da8-131">The following table identifies the data types and qualifiers you can use to define the properties.</span></span> <span data-ttu-id="17da8-132">Pour plus d’informations sur les qualificateurs de la propriété et de la classe que vous pouvez utiliser, consultez [qualificateurs MOF du suivi d’événements](event-tracing-mof-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="17da8-132">For more information on the property and class qualifiers that you can use, see [Event Tracing MOF Qualifiers](event-tracing-mof-qualifiers.md).</span></span>



| <span data-ttu-id="17da8-133">Type de données</span><span class="sxs-lookup"><span data-stu-id="17da8-133">Data type</span></span>              | <span data-ttu-id="17da8-134">Qualificateurs</span><span class="sxs-lookup"><span data-stu-id="17da8-134">Qualifiers</span></span>                        | <span data-ttu-id="17da8-135">Description</span><span class="sxs-lookup"><span data-stu-id="17da8-135">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17da8-136">**sint8**, **UInt8**</span><span class="sxs-lookup"><span data-stu-id="17da8-136">**sint8**, **uint8**</span></span>   | <span data-ttu-id="17da8-137">**Format**</span><span class="sxs-lookup"><span data-stu-id="17da8-137">**Format**</span></span>                        | <span data-ttu-id="17da8-138">Déclare un entier décimal sur 1 octet.</span><span class="sxs-lookup"><span data-stu-id="17da8-138">Declares a 1-byte decimal integer.</span></span> <span data-ttu-id="17da8-139">Pour déclarer un caractère ANSI, utilisez le qualificateur **format** et définissez sa valeur sur « c ».</span><span class="sxs-lookup"><span data-stu-id="17da8-139">To declare an ANSI character, use the **Format** qualifier and set its value to "c".</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="17da8-140">**sint16**, **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17da8-140">**sint16**, **uint16**</span></span> | <span data-ttu-id="17da8-141">**Format**</span><span class="sxs-lookup"><span data-stu-id="17da8-141">**Format**</span></span>                        | <span data-ttu-id="17da8-142">Déclare un entier décimal sur 2 octets.</span><span class="sxs-lookup"><span data-stu-id="17da8-142">Declares a 2-byte decimal integer.</span></span> <span data-ttu-id="17da8-143">Pour indiquer que le nombre est un nombre hexadécimal, utilisez le qualificateur de **format** .</span><span class="sxs-lookup"><span data-stu-id="17da8-143">To indicate the number is a hexadecimal number, use the **Format** qualifier.</span></span> <span data-ttu-id="17da8-144">Par exemple, format ("x").</span><span class="sxs-lookup"><span data-stu-id="17da8-144">For example, format("x").</span></span>                                                                                                                                                                               |
| <span data-ttu-id="17da8-145">**sint32**, **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17da8-145">**sint32**, **uint32**</span></span> | <span data-ttu-id="17da8-146">**Format**</span><span class="sxs-lookup"><span data-stu-id="17da8-146">**Format**</span></span>                        | <span data-ttu-id="17da8-147">Déclare un entier décimal sur 4 octets.</span><span class="sxs-lookup"><span data-stu-id="17da8-147">Declares a 4-byte decimal integer.</span></span> <span data-ttu-id="17da8-148">Pour indiquer que le nombre est un nombre hexadécimal, utilisez le qualificateur de **format** et définissez sa valeur sur « x ».</span><span class="sxs-lookup"><span data-stu-id="17da8-148">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="17da8-149">**sint64**, **UInt64**</span><span class="sxs-lookup"><span data-stu-id="17da8-149">**sint64**, **uint64**</span></span> | <span data-ttu-id="17da8-150">**Format**</span><span class="sxs-lookup"><span data-stu-id="17da8-150">**Format**</span></span>                        | <span data-ttu-id="17da8-151">Déclare un entier décimal sur 8 octets.</span><span class="sxs-lookup"><span data-stu-id="17da8-151">Declares a 8-byte decimal integer.</span></span> <span data-ttu-id="17da8-152">Pour indiquer que le nombre est un nombre hexadécimal, utilisez le qualificateur de **format** et définissez sa valeur sur « x ».</span><span class="sxs-lookup"><span data-stu-id="17da8-152">To indicate the number is a hexadecimal number, use the **Format** qualifier and set its value to "x".</span></span>                                                                                                                                                                                |
| <span data-ttu-id="17da8-153">**boolean**</span><span class="sxs-lookup"><span data-stu-id="17da8-153">**boolean**</span></span>            |                                   | <span data-ttu-id="17da8-154">Déclare une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="17da8-154">Declares a Boolean value.</span></span> <span data-ttu-id="17da8-155">Le consommateur d’événements doit interpréter la valeur comme BOOL (entier sur 4 octets).</span><span class="sxs-lookup"><span data-stu-id="17da8-155">The event consumer should interpret the value as BOOL (4-byte integer).</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="17da8-156">**char16**</span><span class="sxs-lookup"><span data-stu-id="17da8-156">**char16**</span></span>             |                                   | <span data-ttu-id="17da8-157">Déclare un caractère élargi.</span><span class="sxs-lookup"><span data-stu-id="17da8-157">Declares a wide character.</span></span> <span data-ttu-id="17da8-158">Le consommateur d’événements doit interpréter les tableaux char16 dans les événements de noyau comme des chaînes de caractères larges.</span><span class="sxs-lookup"><span data-stu-id="17da8-158">The event consumer should interpret char16 arrays in kernel events as wide character strings.</span></span> <span data-ttu-id="17da8-159">(Utilisez la taille du tableau pour copier la chaîne.</span><span class="sxs-lookup"><span data-stu-id="17da8-159">(Use the array size to copy the string.</span></span> <span data-ttu-id="17da8-160">Certaines chaînes peuvent contenir des caractères NULL de début.)</span><span class="sxs-lookup"><span data-stu-id="17da8-160">Some strings may contain leading NULL characters.)</span></span>                                                                                                      |
| <span data-ttu-id="17da8-161">**object**</span><span class="sxs-lookup"><span data-stu-id="17da8-161">**object**</span></span>             | <span data-ttu-id="17da8-162">**Extension**</span><span class="sxs-lookup"><span data-stu-id="17da8-162">**Extension**</span></span>                     | <span data-ttu-id="17da8-163">Déclare un objet blob binaire.</span><span class="sxs-lookup"><span data-stu-id="17da8-163">Declares a binary blob.</span></span> <span data-ttu-id="17da8-164">Le qualificateur d' **extension** indique le type de données dans l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="17da8-164">The **Extension** qualifier indicates the type of data in the blob.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="17da8-165">**string**</span><span class="sxs-lookup"><span data-stu-id="17da8-165">**string**</span></span>             | <span data-ttu-id="17da8-166">**Format**, **StringTermination**</span><span class="sxs-lookup"><span data-stu-id="17da8-166">**Format**, **StringTermination**</span></span> | <span data-ttu-id="17da8-167">Déclare une valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="17da8-167">Declares a string value.</span></span> <span data-ttu-id="17da8-168">Pour indiquer que la chaîne est une chaîne de caractères larges, utilisez le qualificateur de **format** et définissez sa valeur sur « w ».</span><span class="sxs-lookup"><span data-stu-id="17da8-168">To indicate the string is a wide-character string use the **Format** qualifier and set its value to "w".</span></span> <span data-ttu-id="17da8-169">La chaîne est considérée comme une chaîne ANSI si vous ne spécifiez pas le qualificateur de **format** .</span><span class="sxs-lookup"><span data-stu-id="17da8-169">The string is considered an ANSI string if you do not specify the **Format** qualifier.</span></span> <span data-ttu-id="17da8-170">Pour indiquer comment la chaîne est terminée, utilisez le qualificateur **StringTermination** .</span><span class="sxs-lookup"><span data-stu-id="17da8-170">To indicate how the string is terminated, use the **StringTermination** qualifier.</span></span> <br/> |



 

<span data-ttu-id="17da8-171">Pour spécifier un tableau, vous pouvez utiliser des crochets, \[ \] .</span><span class="sxs-lookup"><span data-stu-id="17da8-171">To specify an array, you can use square brackets, \[\].</span></span> <span data-ttu-id="17da8-172">Les crochets peuvent inclure la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="17da8-172">The square brackets can include the size of the array.</span></span> <span data-ttu-id="17da8-173">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="17da8-173">For example:</span></span>

`[WmiDataId(1), read] uint8 MyGuid[16];`

<span data-ttu-id="17da8-174">Vous pouvez également utiliser le qualificateur **Max** pour spécifier la taille d’un tableau.</span><span class="sxs-lookup"><span data-stu-id="17da8-174">You can also use the **Max** qualifier to specify the size of an array.</span></span> <span data-ttu-id="17da8-175">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="17da8-175">For example:</span></span>

`[WmiDataId(1), Max(16), read] uint8 MyGuid[];`

<span data-ttu-id="17da8-176">Si vous incluez la taille du tableau entre crochets, le compilateur MOF génère le qualificateur Max pour vous.</span><span class="sxs-lookup"><span data-stu-id="17da8-176">If you include the size of the array in the square brackets, the MOF compiler generates the Max qualifier for you.</span></span>

<span data-ttu-id="17da8-177">Il est important d’utiliser le qualificateur **Description** pour chaque propriété.</span><span class="sxs-lookup"><span data-stu-id="17da8-177">It is important that you use the **Description** qualifier for each property.</span></span> <span data-ttu-id="17da8-178">La description doit contenir un nom complet que le consommateur peut utiliser lors de l’affichage des valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="17da8-178">The description should contain a display name that the consumer can use when displaying the property values.</span></span>

<span data-ttu-id="17da8-179">L’exemple suivant montre le contenu d’un fichier MOF qui décrit un fournisseur, un événement et une classe MOF de type événement.</span><span class="sxs-lookup"><span data-stu-id="17da8-179">The following example shows the contents of a MOF file that describes a provider, event, and event type MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}")]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Class identifier"): Amended, read, Extension("Guid")] object ID;
};
```

<span data-ttu-id="17da8-180">Notez que les noms de classe de fournisseur, d’événement et de type d’événement MOF doivent être uniques dans l’ensemble de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="17da8-180">Note that the provider, event, and event type MOF class names must be unique within the entire namespace.</span></span> <span data-ttu-id="17da8-181">Pour éviter les conflits de noms, vous devez utiliser un nom unique et descriptif pour tous les noms de classe.</span><span class="sxs-lookup"><span data-stu-id="17da8-181">To avoid naming conflicts, you should use unique and descriptive name for all class names.</span></span> <span data-ttu-id="17da8-182">Les propriétés de classe doivent également être descriptives et uniques au sein de sa hiérarchie de classes : une classe enfant qui contient le même nom de propriété qu’une classe parente remplace la propriété de la classe parente.</span><span class="sxs-lookup"><span data-stu-id="17da8-182">Class properties should also be descriptive and unique within its class hierarchy—a child class that contains the same property name as a parent class overwrites the property of the parent class.</span></span>

<span data-ttu-id="17da8-183">Après avoir défini vos classes MOF, utilisez le compilateur MOF pour générer votre schéma d’événement et l’ajouter au référentiel CIM.</span><span class="sxs-lookup"><span data-stu-id="17da8-183">After defining your MOF classes, use the MOF compiler to generate your event schema and add it to the CIM repository.</span></span> <span data-ttu-id="17da8-184">Les consommateurs peuvent alors lire le schéma à partir du référentiel et lire par programmation les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="17da8-184">Consumers can then read the schema from the repository and programmatically read the event data.</span></span> <span data-ttu-id="17da8-185">Pour obtenir une description complète de la syntaxe MOF et l’utilisation du compilateur MOF (Mofcomp.exe) pour ajouter vos classes MOF au référentiel CIM, consultez [format MOF](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="17da8-185">For a complete description of the MOF syntax and using the MOF compiler (Mofcomp.exe) to add your MOF classes to the CIM repository, see [Managed Object Format](../wmisdk/managed-object-format--mof-.md).</span></span> <span data-ttu-id="17da8-186">Pour plus d’informations sur l’utilisation de Wbemtest.exe pour accéder au référentiel CIM, consultez [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span><span class="sxs-lookup"><span data-stu-id="17da8-186">For information on using Wbemtest.exe to access the CIM repository, see [Windows Management Instrumentation](../wmisdk/wmi-start-page.md) (WMI).</span></span>

## <a name="versioning-mof-class"></a><span data-ttu-id="17da8-187">Classe MOF de contrôle de version</span><span class="sxs-lookup"><span data-stu-id="17da8-187">Versioning MOF class</span></span>

<span data-ttu-id="17da8-188">Si vous ajoutez ou modifiez une classe MOF d’un type d’événement, la Convention consiste à effectuer la version de la classe MOF d’événements et de ses classes MOF d’événements enfants.</span><span class="sxs-lookup"><span data-stu-id="17da8-188">If you add or change an event type MOF class, the convention is to version both the event MOF class and its child event type MOF classes.</span></span> <span data-ttu-id="17da8-189">Pour la version de la classe MOF d’événements en cours, ajoutez \_ VN au nom de la classe, où n est un nombre incrémentiel commençant à 0.</span><span class="sxs-lookup"><span data-stu-id="17da8-189">To version the current event MOF class, append \_Vn to the class name, where n is an incremental number starting at 0.</span></span> <span data-ttu-id="17da8-190">S’il s’agit de la première révision de la classe, ajoutez \_ v0 au nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="17da8-190">If this is the first revision to the class, append \_V0 to the class name.</span></span> <span data-ttu-id="17da8-191">Vous devez également ajouter le qualificateur **EventVersion** à la classe.</span><span class="sxs-lookup"><span data-stu-id="17da8-191">You must also add the **EventVersion** qualifier to the class.</span></span> <span data-ttu-id="17da8-192">Utilisez le même numéro de version que celui utilisé dans le nom de la classe pour la valeur du qualificateur **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="17da8-192">Use the same version number you used in the class name for the value of the **EventVersion** qualifier.</span></span>

<span data-ttu-id="17da8-193">La nouvelle version de la classe MOF d’événements doit utiliser le même nom et le même qualificateur **GUID** que la classe d’origine.</span><span class="sxs-lookup"><span data-stu-id="17da8-193">The new version of the event MOF class must use the same name and **Guid** qualifier as the original class.</span></span> <span data-ttu-id="17da8-194">La nouvelle classe peut éventuellement ajouter le qualificateur **EventVersion** .</span><span class="sxs-lookup"><span data-stu-id="17da8-194">The new class may optionally add the **EventVersion** qualifier.</span></span> <span data-ttu-id="17da8-195">La classe MOF d’événements qui ne contient pas le qualificateur **EventVersion** est considérée comme la version la plus récente, ou si toutes les versions de la classe contiennent un qualificateur **EventVersion** , la classe avec le numéro de version le plus élevé est considérée comme la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="17da8-195">The event MOF class that does not contain the **EventVersion** qualifier is considered the latest version, or if all the versions of the class contain an **EventVersion** qualifier, then the class with the highest version number is considered the latest version.</span></span> <span data-ttu-id="17da8-196">Le fournisseur utilise le membre **Class. version** de la structure d' [**\_ \_ en-tête de suivi d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) pour identifier la version de l’événement inclus dans la trace.</span><span class="sxs-lookup"><span data-stu-id="17da8-196">The provider uses the **Class.Version** member of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to identify the version of the event included in the trace.</span></span>

<span data-ttu-id="17da8-197">L’exemple suivant montre comment effectuer la version d’une classe d’événements MOF.</span><span class="sxs-lookup"><span data-stu-id="17da8-197">The following example shows how to version an event MOF class.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\wmi")
#pragma classflags("forceupdate")

[dynamic: ToInstance, Description("Defines my event provider"),
 Guid("{7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}")]
class MyProvider : EventTrace
{
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."),
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(1)]
class MyCategory : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1),
 EventName("MyEvent")]
class MyCategory_MyEvent : MyCategory
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
    [WmiDataId(6), Description("Buffer Size"): Amended, read] uint32 Size;
};

[dynamic: ToInstance, Description("Defines a category of events that my provider logs."): Amended,
 Guid("{B49D5931-AD85-4070-B1B1-3F81F1532875}"),
 EventVersion(0)]
class MyCategory_V0 : MyProvider
{
};

[dynamic: ToInstance, Description("Defines an event within the category of events that my provider logs."): Amended,
 EventType(1)]
class MyCategory_V0_MyEvent : MyCategory_V0
{
    [WmiDataId(1), Description("Cost factor"): Amended, read] sint32 Cost;
    [WmiDataId(2), Description("Index values"): Amended, read] uint32 Indices[3];
    [WmiDataId(3), Description("Signature"): Amended, read, StringTermination("NullTerminated"), Format("w")] string Signature;
    [WmiDataId(4), Description("Is complete copy"): Amended, read] boolean IsComplete;
    [WmiDataId(5), Description("Identifier"): Amended, read, Extension("Guid")] object ID;
};
```

 

 
