---
description: Représente un espace de noms WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: Classe __Namespace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868137"
---
# <a name="__namespace-class"></a><span data-ttu-id="0e6d1-103">\_\_Classe d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e6d1-103">\_\_Namespace class</span></span>

<span data-ttu-id="0e6d1-104">La classe de système d' **\_ \_ espace de noms** représente un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-104">The **\_\_Namespace** system class represents a WMI namespace.</span></span>

<span data-ttu-id="0e6d1-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0e6d1-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e6d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e6d1-107">Syntax</span></span>

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="0e6d1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0e6d1-108">Members</span></span>

<span data-ttu-id="0e6d1-109">La classe d' **\_ \_ espace de noms** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0e6d1-109">The **\_\_Namespace** class has these types of members:</span></span>

-   [<span data-ttu-id="0e6d1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e6d1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e6d1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0e6d1-111">Properties</span></span>

<span data-ttu-id="0e6d1-112">La classe d' **\_ \_ espace de noms** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-112">The **\_\_Namespace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e6d1-113">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0e6d1-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e6d1-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e6d1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e6d1-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0e6d1-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0e6d1-116">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="0e6d1-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="0e6d1-117">Nom de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-117">Namespace name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0e6d1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0e6d1-118">Remarks</span></span>

<span data-ttu-id="0e6d1-119">La classe d' **\_ \_ espace de noms** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-119">The **\_\_Namespace** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="0e6d1-120">Vous pouvez utiliser l' **\_ \_ espace de noms** pour identifier, créer et supprimer des espaces de noms enfants dans l’espace de noms de travail actuel pour lequel vous avez un objet [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="0e6d1-120">You can use **\_\_Namespace** to identify, create, and delete child namespaces within the current working namespace for which you have an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) object.</span></span> <span data-ttu-id="0e6d1-121">La création d’une nouvelle instance d' **\_ \_ espace de noms** dans un espace de noms de travail crée un espace de noms enfant dans l’espace de noms de travail.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-121">Creating a new instance of **\_\_Namespace** within any working namespace creates a child namespace within the working namespace.</span></span> <span data-ttu-id="0e6d1-122">À l’inverse, la suppression d’une instance d' **\_ \_ espace de noms** supprime l’espace de noms enfant de l’espace de noms de travail.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-122">Conversely, deleting an instance of **\_\_Namespace** removes the child namespace from the working namespace.</span></span> <span data-ttu-id="0e6d1-123">Notez que la suppression d’un espace de noms enfant supprime également toutes ses classes et instances.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-123">Note that deleting a child namespace also deletes all of its classes and instances.</span></span>

<span data-ttu-id="0e6d1-124">L’énumération des instances de cette classe dans n’importe quel espace de noms de travail donne les espaces de noms enfants disponibles.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-124">Enumerating instances of this class within any working namespace gives the available child namespaces.</span></span>

<span data-ttu-id="0e6d1-125">Par exemple, dans l' \\ espace de noms racine se trouvent deux instances d' **\_ \_ espace de noms**.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-125">For example, within the \\root namespace are two instances of **\_\_Namespace**.</span></span> <span data-ttu-id="0e6d1-126">La propriété **Name** est définie sur « Default », l' **autre est définie** sur « Cimv2 ».</span><span class="sxs-lookup"><span data-stu-id="0e6d1-126">One has its **Name** property set to "Default," the other has **Name** set to "Cimv2."</span></span> <span data-ttu-id="0e6d1-127">Ces instances représentent \\ \\ , respectivement, les espaces de noms root par défaut et \\ root \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-127">These instances represent the \\root\\default, and \\root\\cimv2 namespaces, respectively.</span></span>

## <a name="examples"></a><span data-ttu-id="0e6d1-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="0e6d1-128">Examples</span></span>

<span data-ttu-id="0e6d1-129">L’exemple VBScript [répertorier tous les espaces de noms WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) dans la Galerie TechNet utilise un appel récursif pour répertorier toutes les instances de la \_ \_ classe d’espace de noms sur un système.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-129">The [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript example on the TechNet Gallery uses a recursive call to list all instances of the \_\_Namespace class on a system.</span></span>

<span data-ttu-id="0e6d1-130">L’exemple de code suivant récupère tous les espaces de noms dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-130">The following code sample retrieves all namespaces in PowerShell.</span></span>


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



<span data-ttu-id="0e6d1-131">L’exemple de code suivant améliore l’exemple précédent et ajoute des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="0e6d1-131">The following code sample improves on the previous sample, and adds in additional information.</span></span>


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a><span data-ttu-id="0e6d1-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e6d1-132">Requirements</span></span>



| <span data-ttu-id="0e6d1-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e6d1-133">Requirement</span></span> | <span data-ttu-id="0e6d1-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e6d1-134">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0e6d1-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e6d1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="0e6d1-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e6d1-136">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0e6d1-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e6d1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="0e6d1-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e6d1-138">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="0e6d1-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e6d1-139">Namespace</span></span><br/>                | <span data-ttu-id="0e6d1-140">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="0e6d1-140">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="0e6d1-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e6d1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e6d1-142">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="0e6d1-142">**\_\_SystemClass**</span></span>](--systemclass.md)
</dt> <dt>

[<span data-ttu-id="0e6d1-143">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="0e6d1-143">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




