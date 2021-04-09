---
title: Chaîne de liaison
description: En raison du nombre d’objets accessibles à partir d’un service d’annuaire, des collisions de noms peuvent se produire.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Chaîne de liaison ADSI
- ADsPath ADSI, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941356"
---
# <a name="binding-string"></a><span data-ttu-id="0cf69-105">Chaîne de liaison</span><span class="sxs-lookup"><span data-stu-id="0cf69-105">Binding String</span></span>

<span data-ttu-id="0cf69-106">En raison du nombre d’objets accessibles à partir d’un service d’annuaire, des collisions de noms peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="0cf69-106">Due to the number of objects accessible from a directory service, naming collisions can occur.</span></span> <span data-ttu-id="0cf69-107">La chaîne de liaison, qui est communément appelée ADsPath, vous permet de spécifier un objet particulier sans provoquer de collision de noms.</span><span class="sxs-lookup"><span data-stu-id="0cf69-107">The binding string, which is commonly referred to as the ADsPath, enables you to specify a particular object without causing a naming collision.</span></span> <span data-ttu-id="0cf69-108">Cela peut s’appliquer à un fournisseur de services d’annuaire unique ou à plusieurs fournisseurs de services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="0cf69-108">This can be applied for a single directory service provider or across multiple directory service providers.</span></span>

<span data-ttu-id="0cf69-109">Un ADsPath est une chaîne qui identifie de façon unique un objet ADSI sur un service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="0cf69-109">An ADsPath is a string that uniquely identifies an ADSI object on a directory service.</span></span> <span data-ttu-id="0cf69-110">Étant donné que les objets ADSI existent dans le contexte de l’espace de noms du service d’annuaire sous-jacent, une partie de la syntaxe d’un nom ADsPath est spécifique au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0cf69-110">Because ADSI objects exist within the context of the namespace of the underlying directory service, part of the syntax of an ADsPath name is provider-specific.</span></span>

<span data-ttu-id="0cf69-111">Le tableau suivant répertorie les fournisseurs ADSI fournis par défaut.</span><span class="sxs-lookup"><span data-stu-id="0cf69-111">The following table lists the ADSI providers provided by default.</span></span>



| <span data-ttu-id="0cf69-112">Fournisseur</span><span class="sxs-lookup"><span data-stu-id="0cf69-112">Provider</span></span>         | <span data-ttu-id="0cf69-113">Description</span><span class="sxs-lookup"><span data-stu-id="0cf69-113">Description</span></span>                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf69-114">WinNT</span><span class="sxs-lookup"><span data-stu-id="0cf69-114">WinNT</span></span><br/> | <span data-ttu-id="0cf69-115">Utilisé pour communiquer avec les contrôleurs de domaine Windows.</span><span class="sxs-lookup"><span data-stu-id="0cf69-115">Used to communicate with Windows domain controllers.</span></span> <span data-ttu-id="0cf69-116">Pour plus d’informations sur le ADsPath de WinNT, consultez [winnt ADsPath](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="0cf69-116">For more information about the WinNT ADsPath, see [WinNT ADsPath](winnt-adspath.md).</span></span><br/>           |
| <span data-ttu-id="0cf69-117">LDAP</span><span class="sxs-lookup"><span data-stu-id="0cf69-117">LDAP</span></span><br/>  | <span data-ttu-id="0cf69-118">Utilisé pour communiquer avec les serveurs LDAP, par exemple Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0cf69-118">Used to communicate with LDAP servers, such as Active Directory.</span></span> <span data-ttu-id="0cf69-119">Pour plus d’informations sur l’ADsPath LDAP, consultez [LDAP ADsPath](ldap-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="0cf69-119">For more information about the LDAP ADsPath, see [LDAP ADsPath](ldap-adspath.md).</span></span><br/>  |
| <span data-ttu-id="0cf69-120">Fenêtres</span><span class="sxs-lookup"><span data-stu-id="0cf69-120">ADs</span></span><br/>   | <span data-ttu-id="0cf69-121">Fournit une implémentation de [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) qui peut être utilisée pour énumérer tous les fournisseurs ADSI installés sur le client.</span><span class="sxs-lookup"><span data-stu-id="0cf69-121">Provides an [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) implementation that can be used to enumerate all of the ADSI providers installed on the client.</span></span><br/> |



 

<span data-ttu-id="0cf69-122">Utilisez ces noms de fournisseurs pour accéder à l’espace de noms du fournisseur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0cf69-122">Use these provider names to access the default provider namespace.</span></span> <span data-ttu-id="0cf69-123">Par exemple, si vous établissez une liaison à LDAP, ADSI est lié à un conteneur qui contient l’objet de domaine actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="0cf69-123">For example, if you bind to LDAP, ADSI binds to a container that contains the domain object currently logged on.</span></span> <span data-ttu-id="0cf69-124">Si vous effectuez une liaison à WinNT, ADSI est lié à un conteneur qui contient des objets qui correspondent à tous les domaines du réseau.</span><span class="sxs-lookup"><span data-stu-id="0cf69-124">If you bind to WinNT, ADSI binds to a container that holds objects that correlate to all domains on the network.</span></span>

<span data-ttu-id="0cf69-125">Les éléments initiaux de la chaîne ADsPath sont l’identificateur programmatique (progID) du fournisseur ADSI, suivi de « :// », suivi de la syntaxe dictée par l’espace de noms du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0cf69-125">The initial elements of the ADsPath string are the programmatic identifier (progID) of the ADSI provider, followed by "://", followed by syntax dictated by the provider namespace.</span></span> <span data-ttu-id="0cf69-126">La chaîne progID peut ou non respecter la casse, en fonction du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0cf69-126">The progID string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="0cf69-127">Les chaînes progID pour les fournisseurs répertoriés ci-dessus respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="0cf69-127">The progID strings for the providers listed above are case-sensitive.</span></span>

<span data-ttu-id="0cf69-128">La chaîne de chemin d’accès peut ou non respecter la casse, en fonction du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0cf69-128">The path string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="0cf69-129">Les chaînes de chemin d’accès pour les fournisseurs répertoriés ci-dessus ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="0cf69-129">The path strings for the providers listed above are not case-sensitive.</span></span>

<span data-ttu-id="0cf69-130">Voici quelques exemples de ADsPaths.</span><span class="sxs-lookup"><span data-stu-id="0cf69-130">The following are examples of ADsPaths.</span></span>

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

<span data-ttu-id="0cf69-131">Pour rechercher tous les fournisseurs installés sur votre ordinateur, établissez une liaison avec le fournisseur ADs comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="0cf69-131">To find all providers installed on your computer, bind to the ADs provider as shown in the following code example.</span></span>


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



<span data-ttu-id="0cf69-132">À l’aide du fournisseur LDAP, vous pouvez spécifier l’ADsPath dans un format de nom unique X. 500 (DN), en commençant par la balise CN, ou vous pouvez spécifier son inverse hiérarchique, en commençant par la balise O.</span><span class="sxs-lookup"><span data-stu-id="0cf69-132">Using the LDAP provider, you can specify the ADsPath either in an X.500 distinguished name (DN) form, starting with the CN tag, or you can specify its hierarchical inverse, starting with the O tag.</span></span> <span data-ttu-id="0cf69-133">Le formulaire que vous utilisez dans l’ADsPath initial détermine l’ordre des balises.</span><span class="sxs-lookup"><span data-stu-id="0cf69-133">The form you use in the initial ADsPath determines the order of the tags.</span></span>

<span data-ttu-id="0cf69-134">Le tableau suivant répertorie les caractères spéciaux ADsPath.</span><span class="sxs-lookup"><span data-stu-id="0cf69-134">The following table lists ADsPath special characters.</span></span>



| <span data-ttu-id="0cf69-135">Nom</span><span class="sxs-lookup"><span data-stu-id="0cf69-135">Name</span></span>                      | <span data-ttu-id="0cf69-136">Caractère</span><span class="sxs-lookup"><span data-stu-id="0cf69-136">Character</span></span>           | <span data-ttu-id="0cf69-137">Description</span><span class="sxs-lookup"><span data-stu-id="0cf69-137">Description</span></span>                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf69-138">Guillemet double</span><span class="sxs-lookup"><span data-stu-id="0cf69-138">Double quote</span></span><br/>   | <span data-ttu-id="0cf69-139">"</span><span class="sxs-lookup"><span data-stu-id="0cf69-139">"</span></span><br/>        | <span data-ttu-id="0cf69-140">Utilisé pour citer une partie quelconque de l’ADsPath qui peut contenir un caractère spécial afin que la chaîne soit interprétée littéralement.</span><span class="sxs-lookup"><span data-stu-id="0cf69-140">Used to quote any part of the ADsPath that may contain a special character so that the string is interpreted literally.</span></span> <span data-ttu-id="0cf69-141">Par exemple, « CN = nom/préfixe ».</span><span class="sxs-lookup"><span data-stu-id="0cf69-141">For example, "CN=Name/Prefix".</span></span><br/>                                     |
| <span data-ttu-id="0cf69-142">Barre oblique inverse</span><span class="sxs-lookup"><span data-stu-id="0cf69-142">Backslash</span></span><br/>      | \\<br/>       | <span data-ttu-id="0cf69-143">Utilisé pour précéder les caractères spéciaux pour indiquer qu’ils doivent être utilisés en tant que littéraux.</span><span class="sxs-lookup"><span data-stu-id="0cf69-143">Used to precede special characters to signify they should be used as literals.</span></span> <span data-ttu-id="0cf69-144">Pour plus d’informations et pour obtenir la liste des caractères spéciaux, consultez [noms uniques](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="0cf69-144">For more information and a list of special characters, see [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span><br/> |
| <span data-ttu-id="0cf69-145">Barr</span><span class="sxs-lookup"><span data-stu-id="0cf69-145">Slash</span></span><br/>          | /<br/>        | <span data-ttu-id="0cf69-146">Séparateur de composants.</span><span class="sxs-lookup"><span data-stu-id="0cf69-146">Component separator.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="0cf69-147">Crochets pointus</span><span class="sxs-lookup"><span data-stu-id="0cf69-147">Angle brackets</span></span><br/> | <><br/> | <span data-ttu-id="0cf69-148">Délimiter une ADsPath dans une autre convention d’affectation de noms.</span><span class="sxs-lookup"><span data-stu-id="0cf69-148">Delimit an ADsPath within another naming convention.</span></span><br/>                                                                                                                                       |



 

<span data-ttu-id="0cf69-149">Pour délimiter une ADsPath dans une spécification de recherche ou dans le cadre d’une URL, utilisez le Chevron gauche et le Chevron droit (< >).</span><span class="sxs-lookup"><span data-stu-id="0cf69-149">To delimit an ADsPath in a search specification or as part of a URL, use the left and right angle bracket (< >).</span></span> <span data-ttu-id="0cf69-150">Par exemple, « &lt; winnt://MyDomain/UserAccount &gt; ».</span><span class="sxs-lookup"><span data-stu-id="0cf69-150">For example, "&lt;WinNT://MyDomain/UserAccount&gt;".</span></span>

<span data-ttu-id="0cf69-151">Certains fournisseurs ADSI peuvent avoir ajouté des restrictions de syntaxe en raison des exigences de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0cf69-151">Some ADSI providers may have added syntax restrictions due to namespace requirements.</span></span>

## <a name="active-directory-binding-options"></a><span data-ttu-id="0cf69-152">Options de liaison Active Directory</span><span class="sxs-lookup"><span data-stu-id="0cf69-152">Active Directory Binding Options</span></span>

<span data-ttu-id="0cf69-153">Active Directory permet de lier un objet à l’aide de plusieurs autres types de chaînes de liaison, par exemple un identificateur global unique (GUID) COM ou un identificateur de sécurité (SID).</span><span class="sxs-lookup"><span data-stu-id="0cf69-153">Active Directory provides the ability to bind to an object using several other types of binding strings, such as a COM globally unique identifier (GUID) or a security identifier (SID).</span></span> <span data-ttu-id="0cf69-154">Pour plus d’informations, consultez [liaison à Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="0cf69-154">For more information, see [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span></span>

 

