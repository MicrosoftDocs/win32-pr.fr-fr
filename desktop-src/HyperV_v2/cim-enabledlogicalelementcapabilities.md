---
description: Décrit les restrictions sur les propriétés d’un objet CIM \_ EnabledLogicalElement associé.
ms.assetid: debce40c-9a0e-43a7-88fa-9336afd52e17
title: Classe CIM_EnabledLogicalElementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElementCapabilities
- CIM_EnabledLogicalElementCapabilities.ElementNameEditSupported
- CIM_EnabledLogicalElementCapabilities.MaxElementNameLen
- CIM_EnabledLogicalElementCapabilities.RequestedStatesSupported
- CIM_EnabledLogicalElementCapabilities.ElementNameMask
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35f400643e01821667c999342603fd402a3ae419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519928"
---
# <a name="cim_enabledlogicalelementcapabilities-class"></a><span data-ttu-id="b822a-103">\_Classe CIM EnabledLogicalElementCapabilities</span><span class="sxs-lookup"><span data-stu-id="b822a-103">CIM\_EnabledLogicalElementCapabilities class</span></span>

<span data-ttu-id="b822a-104">Décrit les restrictions sur les propriétés d’un objet [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md) associé.</span><span class="sxs-lookup"><span data-stu-id="b822a-104">Describes the restrictions on the properties of an associated [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b822a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b822a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_EnabledLogicalElementCapabilities : CIM_Capabilities
{
  boolean ElementNameEditSupported;
  uint16  MaxElementNameLen;
  uint16  RequestedStatesSupported[];
  string  ElementNameMask;
};
```

## <a name="members"></a><span data-ttu-id="b822a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b822a-106">Members</span></span>

<span data-ttu-id="b822a-107">La classe **CIM \_ EnabledLogicalElementCapabilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b822a-107">The **CIM\_EnabledLogicalElementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="b822a-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b822a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b822a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b822a-109">Properties</span></span>

<span data-ttu-id="b822a-110">La classe **CIM \_ EnabledLogicalElementCapabilities** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b822a-110">The **CIM\_EnabledLogicalElementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b822a-111">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="b822a-111">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b822a-112">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b822a-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b822a-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b822a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b822a-114">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. INCITS-T11 \| swapi configuration de l' \_ unité \_ \_ Caps \_ T \| EditName "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ propriété ManagedElement**](cim-managedelement.md).**ElementName**»)</span><span class="sxs-lookup"><span data-stu-id="b822a-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|EditName"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ManagedElement**](cim-managedelement.md).**ElementName**")</span></span>
</dt> </dl>

<span data-ttu-id="b822a-115">**true** si la propriété **ElementName** de l’élément logique activé peut être modifiée ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="b822a-115">**true** if the **ElementName** property of the enabled logical element can be modified; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="b822a-116">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="b822a-116">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b822a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b822a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b822a-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b822a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b822a-119">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span><span class="sxs-lookup"><span data-stu-id="b822a-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EnabledLogicalElementCapabilities**.**MaxElementNameLen**")</span></span>
</dt> </dl>

<span data-ttu-id="b822a-120">Expression régulière qui indique les restrictions sur la propriété **ElementName** de l’élément logique Enable.</span><span class="sxs-lookup"><span data-stu-id="b822a-120">A regular expression that indicates the restrictions on the **ElementName** property of the enable logical element.</span></span> <span data-ttu-id="b822a-121">Consultez la *norme DMTF standard ABNF avec le Guide d’utilisation de la spécification de profil de gestion*, annexe C pour connaître la syntaxe autorisée.</span><span class="sxs-lookup"><span data-stu-id="b822a-121">See *DMTF standard ABNF with the Management Profile Specification Usage Guide*, appendix C for the permitted syntax.</span></span>

> [!Note]  
> <span data-ttu-id="b822a-122">Si cette propriété et la propriété **ElementNameMask** de l’élément logique Enable décrivent la longueur maximale de **ElementName**, la valeur la plus petite est utilisée.</span><span class="sxs-lookup"><span data-stu-id="b822a-122">If this property and the **ElementNameMask** property of the enable logical element describe the maximum length of **ElementName**, the smaller value is used.</span></span>

 

</dd> <dt>

<span data-ttu-id="b822a-123">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="b822a-123">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b822a-124">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b822a-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b822a-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b822a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b822a-126">Qualificateurs : [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-swapi. INCITS-T11 \| swapi \_ configuration unit \_ \_ Caps \_ T \| MaxNameChars "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ FCSwitchCapabilities. ElementNameEditSupported ","**CIM \_ EnabledLogicalElementCapabilities**.**ElementNameMask**")</span><span class="sxs-lookup"><span data-stu-id="b822a-126">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("FC-SWAPI.INCITS-T11\|SWAPI\_UNIT\_CONFIG\_CAPS\_T\|MaxNameChars"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_FCSwitchCapabilities.ElementNameEditSupported", "**CIM\_EnabledLogicalElementCapabilities**.**ElementNameMask**")</span></span>
</dt> </dl>

<span data-ttu-id="b822a-127">Longueur maximale prise en charge de la propriété **ElementName** de l’élément logique activé.</span><span class="sxs-lookup"><span data-stu-id="b822a-127">The maximum supported length of the **ElementName** property of the enabled logical element.</span></span>

</dd> <dt>

<span data-ttu-id="b822a-128">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="b822a-128">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b822a-129">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b822a-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b822a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b822a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b822a-131">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**»)</span><span class="sxs-lookup"><span data-stu-id="b822a-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).**RequestStateChange**")</span></span>
</dt> </dl>

<span data-ttu-id="b822a-132">États possibles qui peuvent être demandés sur l’élément logique activé par la méthode [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="b822a-132">The possible states that can be requested on the enabled logical element by the [**RequestStateChange**](cim-enabledlogicalelement-requeststatechange.md) method.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b822a-133">**Activé** (2)</span><span class="sxs-lookup"><span data-stu-id="b822a-133">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b822a-134">**Désactivé** (3)</span><span class="sxs-lookup"><span data-stu-id="b822a-134">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="b822a-135">**Arrêter** (4)</span><span class="sxs-lookup"><span data-stu-id="b822a-135">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="b822a-136">**Hors connexion** (6)</span><span class="sxs-lookup"><span data-stu-id="b822a-136">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="b822a-137">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="b822a-137">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="b822a-138">**Différer** (8)</span><span class="sxs-lookup"><span data-stu-id="b822a-138">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="b822a-139">**Suspension** (9)</span><span class="sxs-lookup"><span data-stu-id="b822a-139">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="b822a-140">**Redémarrer** (10)</span><span class="sxs-lookup"><span data-stu-id="b822a-140">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="b822a-141">**Réinitialiser** (11)</span><span class="sxs-lookup"><span data-stu-id="b822a-141">**Reset** (11)</span></span>


<span data-ttu-id="b822a-142"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b822a-142"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b822a-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b822a-143">Requirements</span></span>



| <span data-ttu-id="b822a-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b822a-144">Requirement</span></span> | <span data-ttu-id="b822a-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="b822a-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b822a-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b822a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b822a-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b822a-147">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b822a-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b822a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b822a-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b822a-149">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b822a-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b822a-150">Namespace</span></span><br/>                | <span data-ttu-id="b822a-151">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="b822a-151">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b822a-152">MOF</span><span class="sxs-lookup"><span data-stu-id="b822a-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b822a-153"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b822a-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b822a-154">DLL</span><span class="sxs-lookup"><span data-stu-id="b822a-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b822a-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b822a-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b822a-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b822a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b822a-157">**\_Fonctionnalités CIM**</span><span class="sxs-lookup"><span data-stu-id="b822a-157">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

