---
title: Structure WINBIO_VERSION ( \_ types WINBIO. h)
description: Contient le numéro de version du logiciel d’un composant du fournisseur de services biométriques.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- API de Windows Biometric Framework de structure de WINBIO_VERSION
- API du pointeur de structure PWINBIO_VERSION Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466914"
---
# <a name="winbio_version-structure"></a><span data-ttu-id="9178a-105">Structure de la version de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="9178a-105">WINBIO\_VERSION structure</span></span>

<span data-ttu-id="9178a-106">La structure de **\_ version WINBIO** contient le numéro de version du logiciel d’un composant du fournisseur de services biométriques.</span><span class="sxs-lookup"><span data-stu-id="9178a-106">The **WINBIO\_VERSION** structure contains the software version number of a biometric service provider component.</span></span>

## <a name="syntax"></a><span data-ttu-id="9178a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9178a-107">Syntax</span></span>


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a><span data-ttu-id="9178a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="9178a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9178a-109">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="9178a-109">**MajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9178a-110">**Valeur DWORD** qui contient le numéro de version principale.</span><span class="sxs-lookup"><span data-stu-id="9178a-110">A **DWORD** that contains the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="9178a-111">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="9178a-111">**MinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9178a-112">**Valeur DWORD** qui contient le numéro de version mineure.</span><span class="sxs-lookup"><span data-stu-id="9178a-112">A **DWORD** that contains the minor version number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9178a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9178a-113">Requirements</span></span>



| <span data-ttu-id="9178a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9178a-114">Requirement</span></span> | <span data-ttu-id="9178a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9178a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9178a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9178a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9178a-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9178a-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="9178a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9178a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9178a-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9178a-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9178a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9178a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9178a-121"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9178a-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9178a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9178a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9178a-123">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="9178a-123">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="9178a-124">**\_schéma BSP \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="9178a-124">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)
</dt> <dt>

[<span data-ttu-id="9178a-125">**\_schéma d’unité WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="9178a-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





