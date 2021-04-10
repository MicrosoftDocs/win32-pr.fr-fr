---
description: Le qualificateur CIMType contient le texte décrivant le type d’une propriété.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Qualificateur CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115867"
---
# <a name="cimtype-qualifier"></a><span data-ttu-id="b22c6-103">Qualificateur CIMType</span><span class="sxs-lookup"><span data-stu-id="b22c6-103">CIMType Qualifier</span></span>

<span data-ttu-id="b22c6-104">Le qualificateur **CimType** contient le texte décrivant le type d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="b22c6-104">The **CIMType** qualifier contains text describing the type of a property.</span></span>

<span data-ttu-id="b22c6-105">Ce texte peut être le type MOF, par exemple « String » et « sint32 » ou le type CIM, par exemple « CIM \_ String » et « CIM \_ sint32 ».</span><span class="sxs-lookup"><span data-stu-id="b22c6-105">This text can be the MOF type such as "string" and "sint32" or the CIM type such as "CIM\_STRING" and "CIM\_SINT32".</span></span> <span data-ttu-id="b22c6-106">Il existe une correspondance un-à-un entre le qualificateur **CimType** et le type de la propriété utilisée dans le paramètre *pvtType* de la méthode [**IWbemClassObject :: obtenir**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="b22c6-106">There is a one-to-one correspondence between the **CIMType** qualifier and the type of the property used in the *pvtType* parameter of the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="b22c6-107">Les deux exceptions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b22c6-107">The two exceptions are:</span></span>

-   <span data-ttu-id="b22c6-108">[*Propriétés de référence*](gloss-r.md), qui ont le **type \_ référence CIM**, qui contient la valeur « Ref : ClassName ».</span><span class="sxs-lookup"><span data-stu-id="b22c6-108">[*Reference properties*](gloss-r.md), which have the type **CIM\_REFERENCE**, that contains the "REF:classname" value.</span></span> <span data-ttu-id="b22c6-109">La valeur ClassName décrit le type de classe de la propriété de référence.</span><span class="sxs-lookup"><span data-stu-id="b22c6-109">The classname value describes the class type of the reference property.</span></span>
-   <span data-ttu-id="b22c6-110">Propriétés de l’objet incorporé, qui ont le type d' **\_ objet CIM** .</span><span class="sxs-lookup"><span data-stu-id="b22c6-110">Embedded object properties, which have the **CIM\_OBJECT** type.</span></span>

<span data-ttu-id="b22c6-111">Notez, toutefois, que le qualificateur **CimType** peut et doit être utilisé pour taper une propriété de référence plus exactement.</span><span class="sxs-lookup"><span data-stu-id="b22c6-111">Please note, however, that the **CIMType** qualifier can and should be used to type a reference property more exactly.</span></span> <span data-ttu-id="b22c6-112">Par exemple, si la propriété fait toujours référence à des instances de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , son qualificateur **CimType** doit avoir la valeur :</span><span class="sxs-lookup"><span data-stu-id="b22c6-112">For example, if the property always refers to instances of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class, its **CIMType** qualifier should be set to:</span></span>


```mof
"ref:Win32_LogicalDisk"
```



<span data-ttu-id="b22c6-113">Par défaut, le qualificateur **CimType** d’une propriété de référence a le type **ref**.</span><span class="sxs-lookup"><span data-stu-id="b22c6-113">By default, the **CIMType** qualifier of a reference property has the type **ref**.</span></span>

<span data-ttu-id="b22c6-114">Comme avec les propriétés de référence, le qualificateur **CimType** doit être utilisé pour taper une propriété d’objet incorporée plus exactement avec la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="b22c6-114">As with reference properties, the **CIMType** qualifier should used to type an embedded object property more exactly with the following syntax:</span></span>


```mof
"object:EmbedClass"
```



<span data-ttu-id="b22c6-115">Étant donné que WMI autorise plus de types que ce qui peut être exprimé par des constantes standard avec le \_ préfixe VT, le qualificateur **CimType** peut aider à interpréter les valeurs de type.</span><span class="sxs-lookup"><span data-stu-id="b22c6-115">Because WMI allows more types than can be expressed by standard constants with the VT\_ prefix, the **CIMType** qualifier can help interpret type values.</span></span> <span data-ttu-id="b22c6-116">Le qualificateur **CimType** est ajouté automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b22c6-116">The **CIMType** qualifier is added automatically.</span></span> <span data-ttu-id="b22c6-117">Pour plus d’informations, consultez [types de données MOF](mof-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="b22c6-117">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b22c6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b22c6-118">Requirements</span></span>



| <span data-ttu-id="b22c6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b22c6-119">Requirement</span></span> | <span data-ttu-id="b22c6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b22c6-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b22c6-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b22c6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b22c6-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b22c6-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b22c6-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b22c6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b22c6-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b22c6-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b22c6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b22c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b22c6-126">**Qualificateurs WMI standard**</span><span class="sxs-lookup"><span data-stu-id="b22c6-126">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="b22c6-127">Qualificateurs WMI</span><span class="sxs-lookup"><span data-stu-id="b22c6-127">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="b22c6-128">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="b22c6-128">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

