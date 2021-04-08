---
description: Spécifie les octets qui sont chiffrés dans une surface vidéo protégée.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Structure D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111802"
---
# <a name="d3dencrypted_block_info-structure"></a><span data-ttu-id="ad21a-103">\_Structure d' \_ informations sur les blocs D3DENCRYPTED</span><span class="sxs-lookup"><span data-stu-id="ad21a-103">D3DENCRYPTED\_BLOCK\_INFO structure</span></span>

<span data-ttu-id="ad21a-104">Spécifie les octets qui sont chiffrés dans une surface vidéo protégée.</span><span class="sxs-lookup"><span data-stu-id="ad21a-104">Specifies which bytes are encrypted in a protected video surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad21a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad21a-105">Syntax</span></span>


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a><span data-ttu-id="ad21a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ad21a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad21a-107">**NumEncryptedBytesAtBeginning**</span><span class="sxs-lookup"><span data-stu-id="ad21a-107">**NumEncryptedBytesAtBeginning**</span></span>
</dt> <dd>

<span data-ttu-id="ad21a-108">Nombre d’octets chiffrés au début de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ad21a-108">The number of bytes that are encrypted at the start of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ad21a-109">**NumBytesInSkipPattern**</span><span class="sxs-lookup"><span data-stu-id="ad21a-109">**NumBytesInSkipPattern**</span></span>
</dt> <dd>

<span data-ttu-id="ad21a-110">Nombre d’octets ignorés après le premier **NumEncryptedBytesAtBeginning** octets, puis après chaque bloc de **NumBytesInEncryptPattern** octets.</span><span class="sxs-lookup"><span data-stu-id="ad21a-110">The number of bytes that are skipped after the first **NumEncryptedBytesAtBeginning** bytes, and then after each block of **NumBytesInEncryptPattern** bytes.</span></span> <span data-ttu-id="ad21a-111">Les octets ignorés ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="ad21a-111">Skipped bytes are not encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="ad21a-112">**NumBytesInEncryptPattern**</span><span class="sxs-lookup"><span data-stu-id="ad21a-112">**NumBytesInEncryptPattern**</span></span>
</dt> <dd>

<span data-ttu-id="ad21a-113">Nombre d’octets qui sont chiffrés après chaque bloc d’octets ignorés.</span><span class="sxs-lookup"><span data-stu-id="ad21a-113">The number of bytes that are encrypted after each block of skipped bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad21a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad21a-114">Requirements</span></span>



| <span data-ttu-id="ad21a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad21a-115">Requirement</span></span> | <span data-ttu-id="ad21a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad21a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad21a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad21a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ad21a-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad21a-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ad21a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad21a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ad21a-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ad21a-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ad21a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad21a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad21a-122"><dt>D3d9types. h (inclure d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad21a-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad21a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad21a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad21a-124">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="ad21a-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




