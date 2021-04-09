---
description: La classe WMIEvent est une classe de base à partir de laquelle toutes les classes d’événements WMI sont dérivées.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: WMIEvent, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035078"
---
# <a name="wmievent-class"></a><span data-ttu-id="9572d-103">WMIEvent, classe</span><span class="sxs-lookup"><span data-stu-id="9572d-103">WMIEvent class</span></span>

<span data-ttu-id="9572d-104">La classe **WmiEvent** est une classe de base à partir de laquelle toutes les classes d’événements WMI sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="9572d-104">The **WMIEvent** class is a base class from which all WMI event classes are derived.</span></span>

<span data-ttu-id="9572d-105">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="9572d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9572d-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="9572d-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9572d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9572d-107">Syntax</span></span>

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="9572d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9572d-108">Members</span></span>

<span data-ttu-id="9572d-109">La classe **WmiEvent** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9572d-109">The **WMIEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="9572d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9572d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9572d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9572d-111">Properties</span></span>

<span data-ttu-id="9572d-112">La classe **WmiEvent** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="9572d-112">The **WMIEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9572d-113">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="9572d-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9572d-114">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="9572d-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9572d-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9572d-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9572d-116">Descripteur utilisé par le fournisseur d’événements pour déterminer les utilisateurs qui peuvent recevoir l’événement.</span><span class="sxs-lookup"><span data-stu-id="9572d-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="9572d-117">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="9572d-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="9572d-118">Pour plus d’informations sur les constantes utilisées pour définir ce descripteur de sécurité, voir la rubrique sur les [constantes de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="9572d-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="9572d-119">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="9572d-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9572d-120">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9572d-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9572d-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="9572d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9572d-122">Valeur unique qui indique l’heure à laquelle l’événement a été généré.</span><span class="sxs-lookup"><span data-stu-id="9572d-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="9572d-123">Il s’agit d’une valeur 64 bits qui représente le nombre d’intervalles de 100 nanosecondes après le 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="9572d-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="9572d-124">Les informations sont au format de temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="9572d-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="9572d-125">Cette propriété est héritée de l' [**\_ \_ événement**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="9572d-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="9572d-126">Pour plus d’informations sur l’utilisation des valeurs **UInt64** dans les scripts, consultez [scripts dans WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9572d-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9572d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="9572d-127">Remarks</span></span>

<span data-ttu-id="9572d-128">La classe **WmiEvent** est dérivée de [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="9572d-128">The **WMIEvent** class is derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="9572d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9572d-129">Requirements</span></span>



| <span data-ttu-id="9572d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9572d-130">Requirement</span></span> | <span data-ttu-id="9572d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="9572d-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9572d-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9572d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9572d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9572d-133">Windows Vista</span></span><br/>                                                                                                                              |
| <span data-ttu-id="9572d-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9572d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9572d-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9572d-135">Windows Server 2003</span></span><br/>                                                                                                                        |
| <span data-ttu-id="9572d-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9572d-136">Namespace</span></span><br/>                | <span data-ttu-id="9572d-137">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="9572d-137">Root\\WMI</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="9572d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9572d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9572d-139"><dt>WMI. mof ; </dt> <dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9572d-139"><dt>Wmi.mof; </dt> <dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="9572d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9572d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9572d-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9572d-141"><dt>WmiProv.dll</dt></span></span> </dl>                                                                |



## <a name="see-also"></a><span data-ttu-id="9572d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9572d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9572d-143">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="9572d-143">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="9572d-144">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="9572d-144">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

