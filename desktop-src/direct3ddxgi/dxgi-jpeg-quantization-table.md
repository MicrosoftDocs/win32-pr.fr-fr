---
description: Décrit une table de quantification JPEG.
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: Structure DXGI_JPEG_QUANTIZATION_TABLE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535805"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a><span data-ttu-id="b8263-103">\_Structure de \_ table de quantification dxgi JPEG \_</span><span class="sxs-lookup"><span data-stu-id="b8263-103">DXGI\_JPEG\_QUANTIZATION\_TABLE structure</span></span>

<span data-ttu-id="b8263-104">Décrit une table de quantification JPEG.</span><span class="sxs-lookup"><span data-stu-id="b8263-104">Describes a JPEG quantization table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8263-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8263-105">Syntax</span></span>


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a><span data-ttu-id="b8263-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b8263-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b8263-107">**Éléments**</span><span class="sxs-lookup"><span data-stu-id="b8263-107">**Elements**</span></span>
</dt> <dd>

<span data-ttu-id="b8263-108">Tableau d’octets contenant les éléments de la table de quantification.</span><span class="sxs-lookup"><span data-stu-id="b8263-108">An array of bytes containing the elements of the quantization table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8263-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8263-109">Requirements</span></span>



| <span data-ttu-id="b8263-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8263-110">Requirement</span></span> | <span data-ttu-id="b8263-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8263-111">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8263-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8263-112">Header</span></span><br/> | <dl> <span data-ttu-id="b8263-113"><dt>Dxgitype. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8263-113"><dt>Dxgitype.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8263-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8263-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8263-115">Structures DXGI</span><span class="sxs-lookup"><span data-stu-id="b8263-115">DXGI Structures</span></span>](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




