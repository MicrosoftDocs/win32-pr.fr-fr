---
title: Structure WMDRM_ENCRYPT_SCATTER_BLOCK (wmdrmsdk. h)
description: La \_ \_ structure de bloc de diffusion de chiffrement WMDRM \_ contient un bloc de données à chiffrer.
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- Structure WMDRM_ENCRYPT_SCATTER_BLOCK format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8911ba1822b146de4a99ff1fe144afcfd8e212e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528394"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a><span data-ttu-id="28f10-105">\_Structure de \_ bloc de diffusion de CHIFFREment WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="28f10-105">WMDRM\_ENCRYPT\_SCATTER\_BLOCK structure</span></span>

<span data-ttu-id="28f10-106">La structure de **\_ bloc de \_ diffusion \_ de chiffrement WMDRM** contient un bloc de données à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="28f10-106">The **WMDRM\_ENCRYPT\_SCATTER\_BLOCK** structure contains a block of data to be encrypted.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f10-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28f10-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a><span data-ttu-id="28f10-108">Membres</span><span class="sxs-lookup"><span data-stu-id="28f10-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="28f10-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="28f10-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="28f10-110">Identificateur du flux auquel le bloc de données appartient.</span><span class="sxs-lookup"><span data-stu-id="28f10-110">Identifier of the stream to which the data block belongs.</span></span>

</dd> <dt>

<span data-ttu-id="28f10-111">**cbBlock**</span><span class="sxs-lookup"><span data-stu-id="28f10-111">**cbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="28f10-112">Taille du bloc en octets.</span><span class="sxs-lookup"><span data-stu-id="28f10-112">Size of block in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="28f10-113">**pbBlock**</span><span class="sxs-lookup"><span data-stu-id="28f10-113">**pbBlock**</span></span>
</dt> <dd>

<span data-ttu-id="28f10-114">Pointeur vers une mémoire tampon contenant le bloc de données.</span><span class="sxs-lookup"><span data-stu-id="28f10-114">Pointer to a buffer containing the data block.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="28f10-115">Notes</span><span class="sxs-lookup"><span data-stu-id="28f10-115">Remarks</span></span>

<span data-ttu-id="28f10-116">Cette structure est utilisée par la méthode [**IWMDRMEncryptScatter :: EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) pour identifier les blocs de données à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="28f10-116">This structure is used by the [**IWMDRMEncryptScatter::EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md) method to identify blocks of data to encrypt.</span></span>

## <a name="requirements"></a><span data-ttu-id="28f10-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28f10-117">Requirements</span></span>



| <span data-ttu-id="28f10-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28f10-118">Requirement</span></span> | <span data-ttu-id="28f10-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="28f10-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28f10-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="28f10-120">Header</span></span><br/> | <dl> <span data-ttu-id="28f10-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="28f10-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f10-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28f10-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f10-123">**Structures**</span><span class="sxs-lookup"><span data-stu-id="28f10-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





