---
description: Représente une entrée du contrôle d'accès.
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: Classe __ACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485753"
---
# <a name="__ace-class"></a><span data-ttu-id="3571d-103">\_\_Classe ACE</span><span class="sxs-lookup"><span data-stu-id="3571d-103">\_\_ACE class</span></span>

<span data-ttu-id="3571d-104">La classe système abstraite **\_ \_ ACE** représente une entrée de contrôle d’accès ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span><span class="sxs-lookup"><span data-stu-id="3571d-104">The **\_\_ACE** abstract system class represents an access control entry ([*ACE*](/windows/desktop/SecGloss/a-gly)).</span></span>

<span data-ttu-id="3571d-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3571d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3571d-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="3571d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3571d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3571d-107">Syntax</span></span>

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a><span data-ttu-id="3571d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3571d-108">Members</span></span>

<span data-ttu-id="3571d-109">La classe **\_ \_ ACE** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3571d-109">The **\_\_ACE** class has these types of members:</span></span>

-   [<span data-ttu-id="3571d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3571d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3571d-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3571d-111">Properties</span></span>

<span data-ttu-id="3571d-112">La classe **\_ \_ ACE** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3571d-112">The **\_\_ACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3571d-113">**AccessMask**</span><span class="sxs-lookup"><span data-stu-id="3571d-113">**AccessMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3571d-114">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3571d-114">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="3571d-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3571d-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3571d-116">Indicateurs de bits représentant les droits accordés ou refusés au tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="3571d-116">Bit flags representing rights that are granted or denied to the trustee.</span></span> <span data-ttu-id="3571d-117">Pour plus d’informations et pour obtenir une description des indicateurs, consultez propriété **AccessMask** dans la classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="3571d-117">For more information and a description of the flags, see **AccessMask** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="3571d-118">**AceFlags**</span><span class="sxs-lookup"><span data-stu-id="3571d-118">**AceFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3571d-119">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3571d-119">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="3571d-120">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3571d-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3571d-121">Indicateurs binaires spécifiant l’héritage de l’entrée du contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="3571d-121">Bit flags specifying the inheritance of the ACE.</span></span> <span data-ttu-id="3571d-122">Pour plus d’informations et pour obtenir une description des indicateurs, consultez la propriété **AceFlags** dans la classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="3571d-122">For more information and a description of the flags, see **AceFlags** property in the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class.</span></span>

</dd> <dt>

<span data-ttu-id="3571d-123">**AceType**</span><span class="sxs-lookup"><span data-stu-id="3571d-123">**AceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3571d-124">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3571d-124">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="3571d-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3571d-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3571d-126">Type d’entrée d’entrée du contrôle d’accès que cette instance représente.</span><span class="sxs-lookup"><span data-stu-id="3571d-126">The type of ACE entry that this instance represents.</span></span>

</dd> <dt>

<span data-ttu-id="3571d-127">**GuidInheritedObjectType**</span><span class="sxs-lookup"><span data-stu-id="3571d-127">**GuidInheritedObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3571d-128">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3571d-128">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="3571d-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3571d-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3571d-130">GUID du parent de l’objet auquel s’appliquent les droits d’accès de la propriété **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="3571d-130">The GUID of the parent of the object to which the access rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="3571d-131">**GuidObjectType**</span><span class="sxs-lookup"><span data-stu-id="3571d-131">**GuidObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3571d-132">Type de données :</span><span class="sxs-lookup"><span data-stu-id="3571d-132">Data type:</span></span> 
</dt> <dt>

<span data-ttu-id="3571d-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3571d-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3571d-134">GUID qui indique le type d’objet auquel s’appliquent les droits de la propriété **AccessMask** .</span><span class="sxs-lookup"><span data-stu-id="3571d-134">The GUID that indicates the type of object to which the rights in the **AccessMask** property apply.</span></span>

</dd> <dt>

<span data-ttu-id="3571d-135">**HEURE de \_ création**</span><span class="sxs-lookup"><span data-stu-id="3571d-135">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3571d-136">Type de données : **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3571d-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3571d-137">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3571d-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3571d-138">Heure, au format [ \_ DateTime CIM](cim-datetime.md) , de la création du descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3571d-138">The time, in the [CIM\_DATETIME](cim-datetime.md) format, when the security descriptor was created.</span></span>

</dd> <dt>

<span data-ttu-id="3571d-139">**Tiers**</span><span class="sxs-lookup"><span data-stu-id="3571d-139">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3571d-140">Type de données : **[ **\_ \_ tiers de confiance**](--trustee.md)**</span><span class="sxs-lookup"><span data-stu-id="3571d-140">Data type: **[**\_\_Trustee**](--trustee.md)**</span></span>
</dt> <dt>

<span data-ttu-id="3571d-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3571d-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3571d-142">Le tiers de confiance de l’entrée ACE représentée par cette instance de la classe **\_ \_ ACE** .</span><span class="sxs-lookup"><span data-stu-id="3571d-142">The trustee of the ACE entry represented by this instance of the **\_\_ACE** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3571d-143">Notes</span><span class="sxs-lookup"><span data-stu-id="3571d-143">Remarks</span></span>

<span data-ttu-id="3571d-144">Cette classe fournit les propriétés héritées par la classe [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , qui est un membre de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="3571d-144">This class provides the properties that are inherited by the [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) class, which is a member of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="3571d-145">Pour plus d’informations, consultez [objets descripteur de sécurité WMI](wmi-security-descriptor-objects.md) et [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3571d-145">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span> <span data-ttu-id="3571d-146">Pour plus d’informations sur les ACE, consultez [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span><span class="sxs-lookup"><span data-stu-id="3571d-146">For more information about ACEs, see [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).</span></span>

## <a name="requirements"></a><span data-ttu-id="3571d-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3571d-147">Requirements</span></span>



| <span data-ttu-id="3571d-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3571d-148">Requirement</span></span> | <span data-ttu-id="3571d-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="3571d-149">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3571d-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3571d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="3571d-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3571d-151">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3571d-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3571d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="3571d-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3571d-153">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3571d-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3571d-154">Namespace</span></span><br/>                | <span data-ttu-id="3571d-155">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="3571d-155">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3571d-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3571d-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3571d-157">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="3571d-157">**\_\_SecurityRelatedClass**</span></span>](--securityrelatedclass.md)
</dt> <dt>

[<span data-ttu-id="3571d-158">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="3571d-158">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="3571d-159">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="3571d-159">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="3571d-160">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="3571d-160">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

