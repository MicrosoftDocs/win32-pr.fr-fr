---
description: Contrôle l’accès à distance aux versions non prises en charge de Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Classe __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523401"
---
# <a name="__ntlmuser9x-class"></a><span data-ttu-id="c4eed-103">\_\_NTLMUser9X, classe</span><span class="sxs-lookup"><span data-stu-id="c4eed-103">\_\_NTLMUser9X class</span></span>

<span data-ttu-id="c4eed-104">La classe système **\_ \_ NTLMUser9X** contrôle l’accès à distance aux versions non prises en charge de Windows.</span><span class="sxs-lookup"><span data-stu-id="c4eed-104">The **\_\_NTLMUser9X** system class controls remote access to unsupported versions of Windows.</span></span> <span data-ttu-id="c4eed-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c4eed-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c4eed-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c4eed-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4eed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4eed-107">Syntax</span></span>

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="c4eed-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c4eed-108">Members</span></span>

<span data-ttu-id="c4eed-109">La classe **\_ \_ NTLMUser9X** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4eed-109">The **\_\_NTLMUser9X** class has these types of members:</span></span>

-   [<span data-ttu-id="c4eed-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4eed-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4eed-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c4eed-111">Properties</span></span>

<span data-ttu-id="c4eed-112">La classe **\_ \_ NTLMUser9X** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c4eed-112">The **\_\_NTLMUser9X** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4eed-113">**Authority**</span><span class="sxs-lookup"><span data-stu-id="c4eed-113">**Authority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eed-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4eed-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4eed-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4eed-116">Domaine auquel s’applique un nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4eed-116">Domain to which a user name applies.</span></span>

</dd> <dt>

<span data-ttu-id="c4eed-117">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="c4eed-117">**Flags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eed-118">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c4eed-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-119">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4eed-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4eed-120">Indicateurs d’héritage.</span><span class="sxs-lookup"><span data-stu-id="c4eed-120">Inheritance flags.</span></span>

<dt>

<span data-ttu-id="c4eed-121">0</span><span class="sxs-lookup"><span data-stu-id="c4eed-121">0</span></span>
</dt> <dd>

<span data-ttu-id="c4eed-122">Aucun héritage.</span><span class="sxs-lookup"><span data-stu-id="c4eed-122">No inheritance.</span></span>

</dd> <dt>

<span data-ttu-id="c4eed-123">2</span><span class="sxs-lookup"><span data-stu-id="c4eed-123">2</span></span>
</dt> <dd>

<span data-ttu-id="c4eed-124">Appliquez aux espaces de noms enfants, en plus de l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="c4eed-124">Apply to child namespaces, in addition to the current one.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c4eed-125">**Filtrage**</span><span class="sxs-lookup"><span data-stu-id="c4eed-125">**Mask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eed-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c4eed-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4eed-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4eed-128">Masque de la valeur qui spécifie les droits d’accès à l’espace de noms dans le référentiel Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c4eed-128">Bitmask that specifies access rights to the namespace in the Windows Management Instrumentation (WMI) repository.</span></span> <span data-ttu-id="c4eed-129">Pour les valeurs de bit, consultez [**constantes de droits d’accès à l’espace de noms**](namespace-access-rights-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c4eed-129">For bit values, see [**Namespace Access Rights Constants**](namespace-access-rights-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4eed-130">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c4eed-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eed-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c4eed-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4eed-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4eed-133">Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4eed-133">User name.</span></span>

</dd> <dt>

<span data-ttu-id="c4eed-134">**Type**</span><span class="sxs-lookup"><span data-stu-id="c4eed-134">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4eed-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="c4eed-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4eed-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c4eed-136">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4eed-137">Accès autorisé.</span><span class="sxs-lookup"><span data-stu-id="c4eed-137">Access allowed.</span></span>

<dt>

<span data-ttu-id="c4eed-138">0</span><span class="sxs-lookup"><span data-stu-id="c4eed-138">0</span></span>
</dt> <dd>

<span data-ttu-id="c4eed-139">Accès autorisé.</span><span class="sxs-lookup"><span data-stu-id="c4eed-139">Access allowed.</span></span>

</dd> <dt>

<span data-ttu-id="c4eed-140">2</span><span class="sxs-lookup"><span data-stu-id="c4eed-140">2</span></span>
</dt> <dd>

<span data-ttu-id="c4eed-141">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="c4eed-141">Access denied.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4eed-142">Notes</span><span class="sxs-lookup"><span data-stu-id="c4eed-142">Remarks</span></span>

<span data-ttu-id="c4eed-143">La classe **\_ \_ NTLMUser9X** est utilisée comme paramètre d’entrée pour les méthodes [**\_ \_ SystemSecurity :: Get9XUserList**](--systemsecurity-get9xuserlist.md) et [**\_ \_ SystemSecurity :: Set9XUserList**](--systemsecurity-set9xuserlist.md) .</span><span class="sxs-lookup"><span data-stu-id="c4eed-143">The **\_\_NTLMUser9X** class is used as an input parameter for the [**\_\_SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) and [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4eed-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4eed-144">Requirements</span></span>



| <span data-ttu-id="c4eed-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4eed-145">Requirement</span></span> | <span data-ttu-id="c4eed-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4eed-146">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c4eed-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4eed-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c4eed-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4eed-148">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c4eed-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4eed-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c4eed-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4eed-150">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c4eed-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c4eed-151">Namespace</span></span><br/>                | <span data-ttu-id="c4eed-152">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="c4eed-152">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c4eed-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4eed-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4eed-154">**\_\_SecurityRelatedClass**</span><span class="sxs-lookup"><span data-stu-id="c4eed-154">**\_\_SecurityRelatedClass**</span></span>](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[<span data-ttu-id="c4eed-155">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="c4eed-155">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c4eed-156">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="c4eed-156">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

