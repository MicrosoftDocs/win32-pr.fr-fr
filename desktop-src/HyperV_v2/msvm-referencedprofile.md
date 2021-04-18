---
description: Décrit un profil qui est référencé par un autre profil enregistré.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Classe Msvm_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519927"
---
# <a name="msvm_referencedprofile-class"></a><span data-ttu-id="3661e-103">MSVM \_ ReferencedProfile, classe</span><span class="sxs-lookup"><span data-stu-id="3661e-103">Msvm\_ReferencedProfile class</span></span>

<span data-ttu-id="3661e-104">Décrit un profil qui est référencé par un autre profil enregistré.</span><span class="sxs-lookup"><span data-stu-id="3661e-104">Describes a profile that is referenced by another registered profile.</span></span>

<span data-ttu-id="3661e-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3661e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3661e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3661e-106">Syntax</span></span>

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3661e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3661e-107">Members</span></span>

<span data-ttu-id="3661e-108">La classe **MSVM \_ ReferencedProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3661e-108">The **Msvm\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="3661e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3661e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3661e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3661e-110">Properties</span></span>

<span data-ttu-id="3661e-111">La classe **MSVM \_ ReferencedProfile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3661e-111">The **Msvm\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3661e-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="3661e-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3661e-113">Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3661e-113">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="3661e-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3661e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3661e-115">Profil inscrit qui est référencé par le profil **dépendant** .</span><span class="sxs-lookup"><span data-stu-id="3661e-115">The registered profile that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="3661e-116">**Charge**</span><span class="sxs-lookup"><span data-stu-id="3661e-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3661e-117">Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="3661e-117">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="3661e-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3661e-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3661e-119">Profil inscrit qui référence d’autres profils.</span><span class="sxs-lookup"><span data-stu-id="3661e-119">A registered profile that references other profiles.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3661e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3661e-120">Requirements</span></span>



| <span data-ttu-id="3661e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3661e-121">Requirement</span></span> | <span data-ttu-id="3661e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3661e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3661e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3661e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3661e-124">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3661e-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3661e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3661e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3661e-126">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3661e-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3661e-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3661e-127">Namespace</span></span><br/>                | <span data-ttu-id="3661e-128">\\Interop racine</span><span class="sxs-lookup"><span data-stu-id="3661e-128">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="3661e-129">MOF</span><span class="sxs-lookup"><span data-stu-id="3661e-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3661e-130"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3661e-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3661e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3661e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3661e-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3661e-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

