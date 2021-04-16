---
description: La \_ \_ classe système abstraite Trusted représente un tiers de confiance. Un nom ou un SID (tableau d’octets) peut être utilisé.
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: Classe __Trustee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
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
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530369"
---
# <a name="__trustee-class"></a><span data-ttu-id="13236-104">\_\_Classe fiduciaire</span><span class="sxs-lookup"><span data-stu-id="13236-104">\_\_Trustee class</span></span>

<span data-ttu-id="13236-105">La classe système abstraite [**\_ \_ Trusted**](--securitydescriptor.md) représente un [*tiers de confiance*](/windows/desktop/SecGloss/t-gly).</span><span class="sxs-lookup"><span data-stu-id="13236-105">The [**\_\_Trustee**](--securitydescriptor.md) abstract system class represents a [*trustee*](/windows/desktop/SecGloss/t-gly).</span></span> <span data-ttu-id="13236-106">Un nom ou un SID (tableau d’octets) peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="13236-106">Either a name or an SID (byte array) can be used.</span></span>

<span data-ttu-id="13236-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="13236-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="13236-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="13236-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="13236-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13236-109">Syntax</span></span>

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="13236-110">Membres</span><span class="sxs-lookup"><span data-stu-id="13236-110">Members</span></span>

<span data-ttu-id="13236-111">La classe de **\_ \_ tiers de confiance** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="13236-111">The **\_\_Trustee** class has these types of members:</span></span>

-   [<span data-ttu-id="13236-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13236-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13236-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="13236-113">Properties</span></span>

<span data-ttu-id="13236-114">La classe de **\_ \_ tiers de confiance** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="13236-114">The **\_\_Trustee** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13236-115">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="13236-115">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13236-116">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13236-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13236-117">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13236-117">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13236-118">Partie domaine du compte.</span><span class="sxs-lookup"><span data-stu-id="13236-118">Domain portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="13236-119">**Nom**</span><span class="sxs-lookup"><span data-stu-id="13236-119">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13236-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13236-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13236-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13236-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13236-122">Partie nom du compte.</span><span class="sxs-lookup"><span data-stu-id="13236-122">Name portion of the account.</span></span>

</dd> <dt>

<span data-ttu-id="13236-123">**SID**</span><span class="sxs-lookup"><span data-stu-id="13236-123">**SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13236-124">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="13236-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="13236-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13236-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13236-126">SID du tiers de confiance dans la forme de tableau d’octets binaire.</span><span class="sxs-lookup"><span data-stu-id="13236-126">The SID of the trustee in the binary byte array form.</span></span>

</dd> <dt>

<span data-ttu-id="13236-127">**SidLength**</span><span class="sxs-lookup"><span data-stu-id="13236-127">**SidLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13236-128">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13236-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13236-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13236-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13236-130">Longueur du SID en octets.</span><span class="sxs-lookup"><span data-stu-id="13236-130">The length of the SID in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="13236-131">**SidString**</span><span class="sxs-lookup"><span data-stu-id="13236-131">**SidString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13236-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="13236-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13236-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="13236-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="13236-134">SID du tiers de confiance dans le format de chaîne, par exemple, « S-1-1-0 ».</span><span class="sxs-lookup"><span data-stu-id="13236-134">The SID of the trustee in the string format, for example, "S-1-1-0".</span></span>

</dd> <dt>

<span data-ttu-id="13236-135">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="13236-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13236-136">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="13236-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="13236-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="13236-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13236-138">Heure au format [ \_ DateTime CIM](cim-datetime.md) lorsque le descripteur de sécurité a été créé.</span><span class="sxs-lookup"><span data-stu-id="13236-138">Time in the [CIM\_DATETIME](cim-datetime.md) format when the security descriptor was created.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13236-139">Notes</span><span class="sxs-lookup"><span data-stu-id="13236-139">Remarks</span></span>

<span data-ttu-id="13236-140">Cette classe fournit des propriétés qui sont héritées par la classe [**Win32 \_ Trusted**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , qui est un membre de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="13236-140">This class provides properties that are inherited by the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="13236-141">Pour plus d’informations, consultez [objets descripteur de sécurité WMI](wmi-security-descriptor-objects.md) et [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="13236-141">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="13236-142">Pour plus d’informations sur les ACE, consultez [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="13236-142">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="13236-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13236-143">Requirements</span></span>



| <span data-ttu-id="13236-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13236-144">Requirement</span></span> | <span data-ttu-id="13236-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="13236-145">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="13236-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13236-146">Minimum supported client</span></span><br/> | <span data-ttu-id="13236-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13236-147">Windows Vista</span></span><br/>       |
| <span data-ttu-id="13236-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13236-148">Minimum supported server</span></span><br/> | <span data-ttu-id="13236-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13236-149">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="13236-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13236-150">Namespace</span></span><br/>                | <span data-ttu-id="13236-151">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="13236-151">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="13236-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13236-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13236-153">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="13236-153">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="13236-154">**\_Confiance Win32**</span><span class="sxs-lookup"><span data-stu-id="13236-154">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[<span data-ttu-id="13236-155">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="13236-155">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

