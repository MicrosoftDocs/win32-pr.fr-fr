---
description: Les conventions textuelles SNMP sont mappées à des types définis par CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro de CONVENTION textuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524121"
---
# <a name="textual-convention-macro"></a><span data-ttu-id="44409-103">Macro de CONVENTION textuelle</span><span class="sxs-lookup"><span data-stu-id="44409-103">TEXTUAL-CONVENTION Macro</span></span>

<span data-ttu-id="44409-104">Les conventions textuelles SNMP sont mappées à des types définis par CIM.</span><span class="sxs-lookup"><span data-stu-id="44409-104">SNMP textual conventions map to CIM-defined types.</span></span>

> [!Note]  
> <span data-ttu-id="44409-105">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="44409-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="44409-106">Les règles de mappage suivantes s’appliquent aux conventions de texte SNMP :</span><span class="sxs-lookup"><span data-stu-id="44409-106">The following mapping rules apply to SNMP textual conventions:</span></span>

-   <span data-ttu-id="44409-107">La définition de type nommé dans la clause de syntaxe mappe textuellement à la **\_ syntaxe d’objet** QUALIFICATEUR de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="44409-107">The named type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax**.</span></span>
-   <span data-ttu-id="44409-108">Utilisez le tableau suivant pour mapper des conventions textuelles lorsque la clause de syntaxe fait explicitement référence à une convention textuelle d’une macro de CONVENTION textuelle SNMPv2C ou fait référence à une convention textuelle implicite.</span><span class="sxs-lookup"><span data-stu-id="44409-108">Use the following table to map textual conventions when the SYNTAX clause explicitly refers to a textual convention of a SNMPv2C TEXTUAL-CONVENTION macro, or refers to an implied textual convention.</span></span> <span data-ttu-id="44409-109">La valeur par défaut est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="44409-109">The default value is always **NULL**.</span></span>



| <span data-ttu-id="44409-110">Convention textuelle</span><span class="sxs-lookup"><span data-stu-id="44409-110">Textual convention</span></span> | <span data-ttu-id="44409-111">Type de variante CIM</span><span class="sxs-lookup"><span data-stu-id="44409-111">CIM variant type</span></span> | <span data-ttu-id="44409-112">Qualificateur CIM</span><span class="sxs-lookup"><span data-stu-id="44409-112">CIM qualifier</span></span>                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44409-113">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="44409-113">DateAndTime</span></span>        | <span data-ttu-id="44409-114">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44409-114">**VT\_BSTR**</span></span>     | <span data-ttu-id="44409-115">**\_ Convention textuelle**: DateAndTime</span><span class="sxs-lookup"><span data-stu-id="44409-115">**textual\_convention**: DateAndTime</span></span><br/> <span data-ttu-id="44409-116">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="44409-116">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="44409-117">**\_ syntaxe** de l’objet : DateAndTime</span><span class="sxs-lookup"><span data-stu-id="44409-117">**object\_syntax**: DateAndTime</span></span><br/> <span data-ttu-id="44409-118">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="44409-118">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="44409-119">DisplayString</span><span class="sxs-lookup"><span data-stu-id="44409-119">Displaystring</span></span>      | <span data-ttu-id="44409-120">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44409-120">**VT\_BSTR**</span></span>     | <span data-ttu-id="44409-121">**\_ Convention textuelle**: DisplayString</span><span class="sxs-lookup"><span data-stu-id="44409-121">**textual\_convention**: Displaystring</span></span><br/> <span data-ttu-id="44409-122">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="44409-122">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="44409-123">**\_ syntaxe** de l’objet : DisplayString</span><span class="sxs-lookup"><span data-stu-id="44409-123">**object\_syntax**: Displaystring</span></span><br/> <span data-ttu-id="44409-124">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="44409-124">**cimtype**: string</span></span><br/>   |
| <span data-ttu-id="44409-125">MacAddress</span><span class="sxs-lookup"><span data-stu-id="44409-125">MacAddress</span></span>         | <span data-ttu-id="44409-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44409-126">**VT\_BSTR**</span></span>     | <span data-ttu-id="44409-127">**\_ Convention textuelle**: MacAddress</span><span class="sxs-lookup"><span data-stu-id="44409-127">**textual\_convention**: MacAddress</span></span><br/> <span data-ttu-id="44409-128">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="44409-128">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="44409-129">**\_ syntaxe** de l’objet : MacAddress</span><span class="sxs-lookup"><span data-stu-id="44409-129">**object\_syntax**: MacAddress</span></span><br/> <span data-ttu-id="44409-130">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="44409-130">**cimtype**: string</span></span><br/>         |
| <span data-ttu-id="44409-131">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="44409-131">PhysAddress</span></span>        | <span data-ttu-id="44409-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44409-132">**VT\_BSTR**</span></span>     | <span data-ttu-id="44409-133">**\_ Convention textuelle**: PhysAddress</span><span class="sxs-lookup"><span data-stu-id="44409-133">**textual\_convention**: PhysAddress</span></span><br/> <span data-ttu-id="44409-134">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="44409-134">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="44409-135">**\_ syntaxe** de l’objet : PhysAddress</span><span class="sxs-lookup"><span data-stu-id="44409-135">**object\_syntax**: PhysAddress</span></span><br/> <span data-ttu-id="44409-136">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="44409-136">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="44409-137">SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="44409-137">SnmpUDPAddress</span></span>     | <span data-ttu-id="44409-138">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44409-138">**VT\_BSTR**</span></span>     | <span data-ttu-id="44409-139">**\_ Convention textuelle**: SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="44409-139">**textual\_convention**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="44409-140">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="44409-140">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="44409-141">**\_ syntaxe** de l’objet : SnmpUDPAddress</span><span class="sxs-lookup"><span data-stu-id="44409-141">**object\_syntax**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="44409-142">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="44409-142">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="44409-143">SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="44409-143">SnmpOSIAddress</span></span>     | <span data-ttu-id="44409-144">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44409-144">**VT\_BSTR**</span></span>     | <span data-ttu-id="44409-145">**\_ Convention textuelle**: SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="44409-145">**textual\_convention**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="44409-146">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="44409-146">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="44409-147">**\_ syntaxe** de l’objet : SnmpOSIAddress</span><span class="sxs-lookup"><span data-stu-id="44409-147">**object\_syntax**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="44409-148">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="44409-148">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="44409-149">SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="44409-149">SnmpIPXAddress</span></span>     | <span data-ttu-id="44409-150">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="44409-150">**VT\_BSTR**</span></span>     | <span data-ttu-id="44409-151">**\_ Convention textuelle**: SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="44409-151">**textual\_convention**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="44409-152">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="44409-152">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="44409-153">**\_ syntaxe** de l’objet : SnmpIPXAddress</span><span class="sxs-lookup"><span data-stu-id="44409-153">**object\_syntax**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="44409-154">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="44409-154">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="44409-155">Le type Variant défini par CIM et la **\_ Convention textuelle** de QUALIFICATEUR de propriété CIM, l' **encodage**, la **\_ syntaxe d’objet** et la carte **CimType** à l’aide du type primitif sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="44409-155">The CIM-defined variant type and the CIM property qualifiers **textual\_convention**, **encoding**, **object\_syntax**, and **cimtype** map using the underlying primitive type.</span></span>
-   <span data-ttu-id="44409-156">La clause d’indicateur d’affichage de la macro de CONVENTION textuelle SNMPv2C mappe textuellement à l’indicateur d' **affichage \_** du QUALIFICATEUR de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="44409-156">The DISPLAY-HINT clause of the SNMPv2C TEXTUAL-CONVENTION macro maps verbatim to the CIM property qualifier **display\_hint**.</span></span> <span data-ttu-id="44409-157">Ce qualificateur n’est pas généré s’il n’y a aucune macro de CONVENTION textuelle, ou la macro ne contient pas de clause d’indication d’affichage.</span><span class="sxs-lookup"><span data-stu-id="44409-157">This qualifier is not generated if there is no TEXTUAL-CONVENTION macro, or the macro does not contain a DISPLAY-HINT clause.</span></span>

## <a name="example-code"></a><span data-ttu-id="44409-158">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="44409-158">Example Code</span></span>

<span data-ttu-id="44409-159">L’exemple suivant décrit une convention textuelle SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="44409-159">The following example describes an SNMPv1 textual convention.</span></span>

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

<span data-ttu-id="44409-160">Cet exemple génère les qualificateurs CIM suivants.</span><span class="sxs-lookup"><span data-stu-id="44409-160">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

<span data-ttu-id="44409-161">L’exemple suivant décrit une convention textuelle SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="44409-161">The following example describes an SNMPv2 textual convention.</span></span>

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

<span data-ttu-id="44409-162">Cet exemple génère les qualificateurs CIM suivants.</span><span class="sxs-lookup"><span data-stu-id="44409-162">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




