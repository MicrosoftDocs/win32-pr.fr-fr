---
title: Structure WINBIO_BIR_DATA ( \_ types WINBIO. h)
description: Spécifie la taille, en octets, et le décalage d’un bloc d’informations biométriques.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- API de Windows Biometric Framework de structure de WINBIO_BIR_DATA
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384596"
---
# <a name="winbio_bir_data-structure"></a><span data-ttu-id="b499f-104">\_Structure de \_ données WINBIO Bir</span><span class="sxs-lookup"><span data-stu-id="b499f-104">WINBIO\_BIR\_DATA structure</span></span>

<span data-ttu-id="b499f-105">La structure de **\_ \_ données WINBIO Bir** spécifie la taille, en octets, et le décalage d’un bloc d’informations biométriques.</span><span class="sxs-lookup"><span data-stu-id="b499f-105">The **WINBIO\_BIR\_DATA** structure specifies the size, in bytes, and the offset of a block of biometric information.</span></span> <span data-ttu-id="b499f-106">Cette structure est utilisée par la [**structure \_ Bir WINBIO**](winbio-bir.md) pour spécifier où se trouvent les différentes parties d’un enregistrement d’informations biométriques.</span><span class="sxs-lookup"><span data-stu-id="b499f-106">This structure is used by the [**WINBIO\_BIR**](winbio-bir.md) structure to specify where the various parts of a biometric information record are located.</span></span>

## <a name="syntax"></a><span data-ttu-id="b499f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b499f-107">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a><span data-ttu-id="b499f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b499f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b499f-109">**Taille**</span><span class="sxs-lookup"><span data-stu-id="b499f-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="b499f-110">Taille, en octets, des informations biométriques.</span><span class="sxs-lookup"><span data-stu-id="b499f-110">Size, in bytes, of the biometric information.</span></span>

</dd> <dt>

<span data-ttu-id="b499f-111">**Offset**</span><span class="sxs-lookup"><span data-stu-id="b499f-111">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="b499f-112">Décalage, en octets, entre le début de la structure [**\_ Bir WINBIO**](winbio-bir.md) et les informations biométriques.</span><span class="sxs-lookup"><span data-stu-id="b499f-112">Offset, in bytes from the beginning of the [**WINBIO\_BIR**](winbio-bir.md) structure, of the biometric information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b499f-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b499f-113">Remarks</span></span>

<span data-ttu-id="b499f-114">L’utilisation de décalages plutôt que de pointeurs permet de faciliter la sérialisation du BIR et de la traduction moins compliquée entre les environnements 32 et 64 bits ou entre l’utilisateur et le mode noyau.</span><span class="sxs-lookup"><span data-stu-id="b499f-114">The use of offsets rather than pointers allows for easy serialization of the BIR and for less complicated translation between 32 and 64-bit environments or between user and kernel mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="b499f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b499f-115">Requirements</span></span>



| <span data-ttu-id="b499f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b499f-116">Requirement</span></span> | <span data-ttu-id="b499f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b499f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b499f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b499f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b499f-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b499f-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b499f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b499f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b499f-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b499f-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b499f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b499f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b499f-123"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b499f-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b499f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b499f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b499f-125">Structures d’application cliente</span><span class="sxs-lookup"><span data-stu-id="b499f-125">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="b499f-126">**WINBIO \_ Bir**</span><span class="sxs-lookup"><span data-stu-id="b499f-126">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="b499f-127">**\_ \_ en-tête Bir WINBIO**</span><span class="sxs-lookup"><span data-stu-id="b499f-127">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





