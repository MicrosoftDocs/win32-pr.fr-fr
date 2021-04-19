---
description: Indique une entrée MCA, corrigée de la vérification de l’ordinateur (CMC) ou erreur de plateforme corrigée (CPE). Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Classe MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cda6abba06dc4d4f3fec3a4763391eee1fa81274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534699"
---
# <a name="msmcainfo_entry-class"></a><span data-ttu-id="efbb7-104">\_Classe d’entrée MSMCAInfo</span><span class="sxs-lookup"><span data-stu-id="efbb7-104">MSMCAInfo\_Entry class</span></span>

<span data-ttu-id="efbb7-105">La classe d' **\_ entrée MSMCAInfo** indique une entrée MCA, corrigée de la vérification de l’ordinateur (CMC) ou une erreur de plateforme corrigée (CPE).</span><span class="sxs-lookup"><span data-stu-id="efbb7-105">The **MSMCAInfo\_Entry** class indicates an MCA, corrected machine check (CMC), or corrected platform error (CPE) information entry.</span></span> <span data-ttu-id="efbb7-106">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="efbb7-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="efbb7-107">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="efbb7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="efbb7-108">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="efbb7-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="efbb7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efbb7-109">Syntax</span></span>

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a><span data-ttu-id="efbb7-110">Membres</span><span class="sxs-lookup"><span data-stu-id="efbb7-110">Members</span></span>

<span data-ttu-id="efbb7-111">La classe d' **\_ entrée MSMCAInfo** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="efbb7-111">The **MSMCAInfo\_Entry** class has these types of members:</span></span>

-   [<span data-ttu-id="efbb7-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="efbb7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efbb7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="efbb7-113">Properties</span></span>

<span data-ttu-id="efbb7-114">La classe d' **\_ entrée MSMCAInfo** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="efbb7-114">The **MSMCAInfo\_Entry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efbb7-115">**Données**</span><span class="sxs-lookup"><span data-stu-id="efbb7-115">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbb7-116">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="efbb7-116">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="efbb7-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="efbb7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbb7-118">Tableau d’entiers qui contient un enregistrement d’erreur MCA complet, tel qu’il est signalé par la couche d’abstraction système (SAL).</span><span class="sxs-lookup"><span data-stu-id="efbb7-118">Integer array that contains a complete MCA error record as reported by the system abstraction layer (SAL).</span></span> <span data-ttu-id="efbb7-119">Le SAL est du code gravé dans la mémoire ROM que le système d’exploitation appelle pour effectuer des opérations dépendantes de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="efbb7-119">The SAL is code burned into ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="efbb7-120">Il est similaire au BIOS sur une plateforme x86.</span><span class="sxs-lookup"><span data-stu-id="efbb7-120">It is similar to the BIOS on an x86 platform.</span></span>

</dd> <dt>

<span data-ttu-id="efbb7-121">**Durée**</span><span class="sxs-lookup"><span data-stu-id="efbb7-121">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efbb7-122">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efbb7-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efbb7-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="efbb7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efbb7-124">Nombre d’octets dans l’enregistrement d’erreur.</span><span class="sxs-lookup"><span data-stu-id="efbb7-124">Number of bytes in the error record.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efbb7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="efbb7-125">Remarks</span></span>

<span data-ttu-id="efbb7-126">La classe d' **\_ entrée MSMCAInfo** est dérivée de [**MSMCAInfo**](msmcainfo.md).</span><span class="sxs-lookup"><span data-stu-id="efbb7-126">The **MSMCAInfo\_Entry** class is derived from [**MSMCAInfo**](msmcainfo.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efbb7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efbb7-127">Requirements</span></span>



| <span data-ttu-id="efbb7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efbb7-128">Requirement</span></span> | <span data-ttu-id="efbb7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="efbb7-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="efbb7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efbb7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="efbb7-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="efbb7-131">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="efbb7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efbb7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="efbb7-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="efbb7-133">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="efbb7-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="efbb7-134">Namespace</span></span><br/>                | <span data-ttu-id="efbb7-135">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="efbb7-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="efbb7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="efbb7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efbb7-137"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efbb7-137"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="efbb7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="efbb7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efbb7-139"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efbb7-139"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbb7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efbb7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbb7-141">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="efbb7-141">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="efbb7-142">**MSMCAInfo**</span><span class="sxs-lookup"><span data-stu-id="efbb7-142">**MSMCAInfo**</span></span>](msmcainfo.md)
</dt> </dl>

 

 




