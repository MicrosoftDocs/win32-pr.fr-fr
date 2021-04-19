---
description: Représente une entrée de contrôle d’accès (ACE) qui détermine l’accès à la session interactive d’un ordinateur virtuel.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Classe Msvm_InteractiveSessionACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515883"
---
# <a name="msvm_interactivesessionace-class"></a><span data-ttu-id="08a6d-103">MSVM \_ InteractiveSessionACE, classe</span><span class="sxs-lookup"><span data-stu-id="08a6d-103">Msvm\_InteractiveSessionACE class</span></span>

<span data-ttu-id="08a6d-104">Représente une *entrée de contrôle d’accès* (ACE) qui détermine l’accès à la session interactive d’un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="08a6d-104">Represents an *access control entry* (ACE) that determines access to the interactive session of a virtual machine.</span></span>

<span data-ttu-id="08a6d-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="08a6d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a6d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08a6d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a><span data-ttu-id="08a6d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="08a6d-107">Members</span></span>

<span data-ttu-id="08a6d-108">La classe **MSVM \_ InteractiveSessionACE** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="08a6d-108">The **Msvm\_InteractiveSessionACE** class has these types of members:</span></span>

-   [<span data-ttu-id="08a6d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08a6d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08a6d-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08a6d-110">Properties</span></span>

<span data-ttu-id="08a6d-111">La classe **MSVM \_ InteractiveSessionACE** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="08a6d-111">The **Msvm\_InteractiveSessionACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08a6d-112">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="08a6d-112">**AccessType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08a6d-113">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08a6d-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08a6d-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08a6d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08a6d-115">Indique si l’entrée du contrôle d’accès accorde ou refuse l’accès au tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="08a6d-115">Indicates whether the ACE grants or denies access to the trustee.</span></span>

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

<span data-ttu-id="08a6d-116">**Accès autorisé** (0)</span><span class="sxs-lookup"><span data-stu-id="08a6d-116">**Access Allowed** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

<span data-ttu-id="08a6d-117">**Accès refusé** (1)</span><span class="sxs-lookup"><span data-stu-id="08a6d-117">**Access Denied** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08a6d-118">**Tiers**</span><span class="sxs-lookup"><span data-stu-id="08a6d-118">**Trustee**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08a6d-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="08a6d-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08a6d-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="08a6d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08a6d-121">Identifie le principal de sécurité auquel l’entrée de contrôle d’accès accorde ou refuse l’accès.</span><span class="sxs-lookup"><span data-stu-id="08a6d-121">Identifies the security principal that the ACE grants or denies access to.</span></span> <span data-ttu-id="08a6d-122">Les formats valides pour cette propriété sont le format de nom d’utilisateur compatible avec SAM Windows et le format de chaîne SID Windows.</span><span class="sxs-lookup"><span data-stu-id="08a6d-122">Valid formats for this property include the Windows SAM-compatible user name format and the Windows SID string format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08a6d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08a6d-123">Requirements</span></span>



| <span data-ttu-id="08a6d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08a6d-124">Requirement</span></span> | <span data-ttu-id="08a6d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="08a6d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a6d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a6d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="08a6d-127">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a6d-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="08a6d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a6d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="08a6d-129">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a6d-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="08a6d-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="08a6d-130">Namespace</span></span><br/>                | <span data-ttu-id="08a6d-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="08a6d-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="08a6d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="08a6d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08a6d-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08a6d-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08a6d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="08a6d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a6d-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08a6d-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08a6d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08a6d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a6d-137">**GetInteractiveSessionACL**</span><span class="sxs-lookup"><span data-stu-id="08a6d-137">**GetInteractiveSessionACL**</span></span>](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




