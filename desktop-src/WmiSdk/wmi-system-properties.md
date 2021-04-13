---
description: Windows Management Instrumentation (WMI) définit un ensemble de propriétés système associées à toutes les classes et instances de classes.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Propriétés du système WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202279"
---
# <a name="wmi-system-properties"></a><span data-ttu-id="36b54-103">Propriétés du système WMI</span><span class="sxs-lookup"><span data-stu-id="36b54-103">WMI System Properties</span></span>

<span data-ttu-id="36b54-104">Windows Management Instrumentation (WMI) définit un ensemble de propriétés système associées à toutes les classes et instances de classes.</span><span class="sxs-lookup"><span data-stu-id="36b54-104">Windows Management Instrumentation (WMI) defines a set of system properties that are associated with all classes and instances of classes.</span></span> <span data-ttu-id="36b54-105">Comme avec les classes système, les noms de propriétés système commencent par un trait de soulignement double, en les distinguant des propriétés créées par des applications ou des fournisseurs qui ne doivent pas commencer par un trait de soulignement simple ou double.</span><span class="sxs-lookup"><span data-stu-id="36b54-105">As with system classes, system property names begin with a double underscore, distinguishing them from properties created by applications or providers that must not start with a single or double underscore.</span></span> <span data-ttu-id="36b54-106">Une autre façon d’identifier une propriété système consiste à utiliser la méthode [**IWbemClassObject :: obtenir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="36b54-106">Another way to identify a system property is to use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="36b54-107">Les propriétés système sont disponibles à tout moment, mais les valeurs peuvent être **null**.</span><span class="sxs-lookup"><span data-stu-id="36b54-107">System properties are available at any time, but values might be **NULL**.</span></span> <span data-ttu-id="36b54-108">**Null** indique qu’une propriété ne s’applique pas à un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="36b54-108">**NULL** indicates a property does not apply to a specific object.</span></span> <span data-ttu-id="36b54-109">Toutefois, les propriétés système peuvent ne pas être disponibles tout le temps pour toutes les classes ou instances.</span><span class="sxs-lookup"><span data-stu-id="36b54-109">However, system properties might not be available all the time for all classes or instances.</span></span>

## <a name="system-properties"></a><span data-ttu-id="36b54-110">Propriétés système</span><span class="sxs-lookup"><span data-stu-id="36b54-110">System Properties</span></span>

<span data-ttu-id="36b54-111">La liste suivante décrit les propriétés système WMI.</span><span class="sxs-lookup"><span data-stu-id="36b54-111">The following list describes the WMI system properties.</span></span> <span data-ttu-id="36b54-112">Les exemples donnés sont tirés des propriétés système de la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , qui est décrite en bas de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="36b54-112">The examples given are taken from the system properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which is described at the bottom of this topic.</span></span>

<dl> <dt>

<span data-ttu-id="36b54-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Type**</span><span class="sxs-lookup"><span data-stu-id="36b54-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Class**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-114">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-114">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="36b54-115">Type d’accès : lecture seule pour les instances ; lecture/écriture pour les classes</span><span class="sxs-lookup"><span data-stu-id="36b54-115">Access type: Read-only for instances; read/write for classes</span></span>

<span data-ttu-id="36b54-116">Nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="36b54-116">The name of the class.</span></span>

<span data-ttu-id="36b54-117">Exemple : Win32 \_ OptionalFeature</span><span class="sxs-lookup"><span data-stu-id="36b54-117">Example: Win32\_OptionalFeature</span></span>

</dd> <dt>

<span data-ttu-id="36b54-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Dérivation**</span><span class="sxs-lookup"><span data-stu-id="36b54-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivation**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-119">Type de données : tableau de **\_ chaînes CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-119">Data type: **CIM\_STRING** array</span></span>

<span data-ttu-id="36b54-120">Type d’accès : lecture seule pour les instances et les classes</span><span class="sxs-lookup"><span data-stu-id="36b54-120">Access type: Read-only for both instances and classes</span></span>

<span data-ttu-id="36b54-121">Hiérarchie de classes de l’instance ou de la classe actuelle.</span><span class="sxs-lookup"><span data-stu-id="36b54-121">Class hierarchy of the current class or instance.</span></span> <span data-ttu-id="36b54-122">Le premier élément est la classe parent immédiate, le suivant est son parent, et ainsi de suite ; le dernier élément est la classe de base.</span><span class="sxs-lookup"><span data-stu-id="36b54-122">The first element is the immediate parent class, the next is its parent, and so on; the last element is the base class.</span></span>

<span data-ttu-id="36b54-123">Exemple : {CIM \_ LogicalElement, CIM CIM \_ }</span><span class="sxs-lookup"><span data-stu-id="36b54-123">Example: {CIM\_LogicalElement, CIM\_ManagedSystemElement}</span></span>

</dd> <dt>

<span data-ttu-id="36b54-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span><span class="sxs-lookup"><span data-stu-id="36b54-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-125">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-125">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="36b54-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-126">Access type: Read-only</span></span>

<span data-ttu-id="36b54-127">Nom de la classe de niveau supérieur à partir de laquelle la classe ou l’instance est dérivée.</span><span class="sxs-lookup"><span data-stu-id="36b54-127">Name of the top-level class from which the class or instance is derived.</span></span> <span data-ttu-id="36b54-128">Quand cette classe ou instance est la classe de niveau supérieur, les valeurs de **\_ \_ Dynasty** et de **\_ \_ Class** sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="36b54-128">When this class or instance is the top-level class, the values of **\_\_Dynasty** and **\_\_Class** are the same.</span></span>

<span data-ttu-id="36b54-129">Exemple : \_ MANAGEDSYSTEMELEMENT CIM</span><span class="sxs-lookup"><span data-stu-id="36b54-129">Example: CIM\_ManagedSystemElement</span></span>

</dd> <dt>

<span data-ttu-id="36b54-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genres**</span><span class="sxs-lookup"><span data-stu-id="36b54-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-131">Type de données : **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="36b54-131">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="36b54-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-132">Access type: Read-only</span></span>

<span data-ttu-id="36b54-133">Valeur utilisée pour faire la distinction entre les classes et les instances.</span><span class="sxs-lookup"><span data-stu-id="36b54-133">Value that is used to distinguish between classes and instances.</span></span> <span data-ttu-id="36b54-134">Cette valeur est **la \_ \_ classe de genre WBEM** (1) pour les classes, et l' **\_ \_ instance de genre WBEM** (2) pour les instances et les événements.</span><span class="sxs-lookup"><span data-stu-id="36b54-134">This value is **WBEM\_GENUS\_CLASS** (1) for classes, and **WBEM\_GENUS\_INSTANCE** (2) for instances and events.</span></span>

<span data-ttu-id="36b54-135">Exemple : 2</span><span class="sxs-lookup"><span data-stu-id="36b54-135">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="36b54-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Joint**](--namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36b54-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="36b54-137">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-137">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="36b54-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-138">Access type: Read-only</span></span>

<span data-ttu-id="36b54-139">Nom de l' [*espace de noms*](gloss-n.md) de la classe ou de l’instance.</span><span class="sxs-lookup"><span data-stu-id="36b54-139">Name of the [*namespace*](gloss-n.md) of the class or instance.</span></span>

<span data-ttu-id="36b54-140">Exemple : root \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="36b54-140">Example: root\\cimv2</span></span>

</dd> <dt>

<span data-ttu-id="36b54-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_D**</span><span class="sxs-lookup"><span data-stu-id="36b54-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Path**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-142">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-142">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="36b54-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-143">Access type: Read-only</span></span>

<span data-ttu-id="36b54-144">Chemin d’accès complet à la classe ou à l’instance, y compris le serveur et l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="36b54-144">Full path to the class or instance—including server and namespace.</span></span>

<span data-ttu-id="36b54-145">Exemple : \\ \\ monserveur \\ root \\ cimv2 : Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="36b54-145">Example: \\\\MyServer\\root\\cimv2:Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="36b54-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Nombre de propriétés \_**</span><span class="sxs-lookup"><span data-stu-id="36b54-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Property\_Count**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-147">Type de données : **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="36b54-147">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="36b54-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-148">Access type: Read-only</span></span>

<span data-ttu-id="36b54-149">Nombre de propriétés qui ne sont pas du système définies pour la classe ou l’instance.</span><span class="sxs-lookup"><span data-stu-id="36b54-149">Number of nonsystem properties defined for the class or instance.</span></span>

<span data-ttu-id="36b54-150">Exemple : 6</span><span class="sxs-lookup"><span data-stu-id="36b54-150">Example: 6</span></span>

</dd> <dt>

<span data-ttu-id="36b54-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Constitue**</span><span class="sxs-lookup"><span data-stu-id="36b54-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-152">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-152">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="36b54-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-153">Access type: Read-only</span></span>

<span data-ttu-id="36b54-154">Chemin d’accès relatif à la classe ou à l’instance.</span><span class="sxs-lookup"><span data-stu-id="36b54-154">Relative path to the class or instance.</span></span>

<span data-ttu-id="36b54-155">Exemple : Win32 \_ OptionalFeature. Name = "TelnetClient"</span><span class="sxs-lookup"><span data-stu-id="36b54-155">Example: Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="36b54-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Serveurs**</span><span class="sxs-lookup"><span data-stu-id="36b54-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-157">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-157">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="36b54-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-158">Access type: Read-only</span></span>

<span data-ttu-id="36b54-159">Nom du serveur qui fournit la classe ou l’instance.</span><span class="sxs-lookup"><span data-stu-id="36b54-159">Name of the server supplying the class or instance.</span></span>

<span data-ttu-id="36b54-160">Exemple : MyServer</span><span class="sxs-lookup"><span data-stu-id="36b54-160">Example: MyServer</span></span>

</dd> <dt>

<span data-ttu-id="36b54-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclasse**</span><span class="sxs-lookup"><span data-stu-id="36b54-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclass**</span></span>
</dt> <dd>

<span data-ttu-id="36b54-162">Type de données **: \_ chaîne CIM**</span><span class="sxs-lookup"><span data-stu-id="36b54-162">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="36b54-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="36b54-163">Access type: Read-only</span></span>

<span data-ttu-id="36b54-164">Nom de la classe parent immédiate de la classe ou de l’instance.</span><span class="sxs-lookup"><span data-stu-id="36b54-164">Name of the immediate parent class of the class or instance.</span></span>

<span data-ttu-id="36b54-165">Exemple : CIM \_ LogicalElement</span><span class="sxs-lookup"><span data-stu-id="36b54-165">Example: CIM\_LogicalElement</span></span>

</dd> </dl>

<span data-ttu-id="36b54-166">Le code PowerShell suivant récupère les propriétés de la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , qui comprend les propriétés système.</span><span class="sxs-lookup"><span data-stu-id="36b54-166">The following PowerShell code retrieves the properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which includes the system properties.</span></span>


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



<span data-ttu-id="36b54-167">L’exemple de code précédent retourne ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="36b54-167">The previous code sample returns the following:</span></span>


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
