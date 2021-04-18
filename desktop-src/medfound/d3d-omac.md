---
description: Contient un code d’authentification de message (MAC).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: Structure D3D_OMAC (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515952"
---
# <a name="d3d_omac-structure"></a><span data-ttu-id="c8527-103">D3D \_ OMAC, structure</span><span class="sxs-lookup"><span data-stu-id="c8527-103">D3D\_OMAC structure</span></span>

<span data-ttu-id="c8527-104">Contient un code d’authentification de message (MAC).</span><span class="sxs-lookup"><span data-stu-id="c8527-104">Contains a Message Authentication Code (MAC).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8527-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8527-105">Syntax</span></span>


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a><span data-ttu-id="c8527-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c8527-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8527-107">**Omac**</span><span class="sxs-lookup"><span data-stu-id="c8527-107">**Omac**</span></span>
</dt> <dd>

<span data-ttu-id="c8527-108">Tableau d’octets qui contient la valeur MAC de chiffrement du message.</span><span class="sxs-lookup"><span data-stu-id="c8527-108">A byte array that contains the cryptographic MAC value of the message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8527-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8527-109">Requirements</span></span>



| <span data-ttu-id="c8527-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8527-110">Requirement</span></span> | <span data-ttu-id="c8527-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8527-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8527-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8527-112">Minimum supported client</span></span><br/> | <span data-ttu-id="c8527-113">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8527-113">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c8527-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8527-114">Minimum supported server</span></span><br/> | <span data-ttu-id="c8527-115">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8527-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c8527-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8527-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8527-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8527-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8527-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8527-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8527-119">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="c8527-119">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




