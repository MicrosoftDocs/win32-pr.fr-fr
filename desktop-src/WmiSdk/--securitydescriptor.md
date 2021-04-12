---
description: Représente un descripteur de sécurité.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: Classe __SecurityDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203160"
---
# <a name="__securitydescriptor-class"></a><span data-ttu-id="1cdf3-103">\_\_SecurityDescriptor (classe)</span><span class="sxs-lookup"><span data-stu-id="1cdf3-103">\_\_SecurityDescriptor class</span></span>

<span data-ttu-id="1cdf3-104">La **\_ \_ classe de système** abstrait abstrait représente un [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="1cdf3-104">The **\_\_SecurityDescriptor** abstract system class represents a [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

<span data-ttu-id="1cdf3-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1cdf3-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cdf3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1cdf3-107">Syntax</span></span>

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="1cdf3-108">Membres</span><span class="sxs-lookup"><span data-stu-id="1cdf3-108">Members</span></span>

<span data-ttu-id="1cdf3-109">La classe **\_ \_ SecurityDescriptor** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1cdf3-109">The **\_\_SecurityDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="1cdf3-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cdf3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1cdf3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1cdf3-111">Properties</span></span>

<span data-ttu-id="1cdf3-112">La classe **\_ \_ SecurityDescriptor** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-112">The **\_\_SecurityDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1cdf3-113">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-113">**ControlFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cdf3-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1cdf3-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cdf3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cdf3-116">Indicateurs binaires qui fournissent des informations sur le contenu et le format du descripteur.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-116">Bit flags that provide information about the descriptor's contents and format.</span></span> <span data-ttu-id="1cdf3-117">Pour obtenir une description des indicateurs, consultez la propriété **ControlFlags** dans la classe [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="1cdf3-117">See the **ControlFlags** property in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class for a description of the flags.</span></span>

</dd> <dt>

<span data-ttu-id="1cdf3-118">**DACL**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-118">**DACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cdf3-119">Type de données : tableau **[**\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-119">Data type: **[**\_\_ACE**](--ace.md)** array</span></span>
</dt> <dt>

<span data-ttu-id="1cdf3-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1cdf3-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1cdf3-121">Tableau d’entrées [**\_ \_ ACE**](--ace.md) qui spécifient l’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-121">An array of [**\_\_ACE**](--ace.md) entries that specify access to the object.</span></span>

</dd> <dt>

<span data-ttu-id="1cdf3-122">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-122">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cdf3-123">Type de données : **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-123">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1cdf3-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cdf3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cdf3-125">ACE qui identifie le tiers de confiance représentant le groupe de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-125">ACE that identifies the trustee representing the group of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1cdf3-126">**Propriétaire**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-126">**Owner**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cdf3-127">Type de données : **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-127">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1cdf3-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cdf3-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cdf3-129">ACE qui identifie le tiers de confiance représentant le propriétaire de l’objet.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-129">ACE that identifies the trustee representing the owner of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1cdf3-130">**SACL**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-130">**SACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cdf3-131">Type de données : **[ **\_ \_ ACE**](--ace.md)**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-131">Data type: **[**\_\_ACE**](--ace.md)**</span></span>
</dt> <dt>

<span data-ttu-id="1cdf3-132">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cdf3-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cdf3-133">Tableau d’entrées [**\_ \_ ACE**](--ace.md) qui identifie les utilisateurs et les groupes pour lesquels des informations d’audit sont collectées.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-133">An array of [**\_\_ACE**](--ace.md) entries that identifies users and groups for which auditing information is gathered.</span></span>

</dd> <dt>

<span data-ttu-id="1cdf3-134">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1cdf3-135">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1cdf3-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1cdf3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1cdf3-137">Heure au format [ \_ DateTime CIM](cim-datetime.md) lorsque le descripteur de sécurité a été créé.</span><span class="sxs-lookup"><span data-stu-id="1cdf3-137">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1cdf3-138">Notes</span><span class="sxs-lookup"><span data-stu-id="1cdf3-138">Remarks</span></span>

<span data-ttu-id="1cdf3-139">Cette classe fournit les propriétés héritées par le [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="1cdf3-139">This class provides properties inherited by [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="1cdf3-140">Pour plus d’informations, consultez [objets descripteur de sécurité WMI](wmi-security-descriptor-objects.md) et [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1cdf3-140">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="1cdf3-141">Pour plus d’informations sur les ACE, consultez [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="1cdf3-141">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cdf3-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cdf3-142">Requirements</span></span>



| <span data-ttu-id="1cdf3-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cdf3-143">Requirement</span></span> | <span data-ttu-id="1cdf3-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cdf3-144">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1cdf3-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cdf3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1cdf3-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1cdf3-146">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1cdf3-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cdf3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1cdf3-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cdf3-148">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1cdf3-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1cdf3-149">Namespace</span></span><br/>                | <span data-ttu-id="1cdf3-150">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="1cdf3-150">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1cdf3-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1cdf3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cdf3-152">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="1cdf3-152">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="1cdf3-153">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="1cdf3-153">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="1cdf3-154">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="1cdf3-154">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

