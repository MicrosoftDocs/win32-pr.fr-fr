---
title: Structure WMDRM_ENCRYPT_SCATTER_INFO (wmdrmsdk. h)
description: La structure d’informations sur le \_ nuage de points de chiffrement WMDRM \_ contient les \_ informations nécessaires à la configuration de l’interface IWMDRMEncryptScatter à utiliser.
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- Structure WMDRM_ENCRYPT_SCATTER_INFO format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 500012231f6860fd94038b240355eda9aa2aee44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540396"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a><span data-ttu-id="8199e-105">\_Structure des \_ informations de diffusion de CHIFFREment WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="8199e-105">WMDRM\_ENCRYPT\_SCATTER\_INFO structure</span></span>

<span data-ttu-id="8199e-106">La structure d’informations sur le nuage de points de **\_ chiffrement \_ \_ WMDRM** contient les informations nécessaires à la configuration de l’interface [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="8199e-106">The **WMDRM\_ENCRYPT\_SCATTER\_INFO** structure contains information needed to configure the [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="8199e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8199e-107">Syntax</span></span>


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a><span data-ttu-id="8199e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8199e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8199e-109">**dwStreamID**</span><span class="sxs-lookup"><span data-stu-id="8199e-109">**dwStreamID**</span></span>
</dt> <dd>

<span data-ttu-id="8199e-110">Identificateur du flux à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="8199e-110">Identifier of the stream to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="8199e-111">**dwSampleProtectionVersion**</span><span class="sxs-lookup"><span data-stu-id="8199e-111">**dwSampleProtectionVersion**</span></span>
</dt> <dd>

<span data-ttu-id="8199e-112">Exemple de version de protection à utiliser pour encoder les données du flux spécifié.</span><span class="sxs-lookup"><span data-stu-id="8199e-112">Sample protection version to be used to encode data from the specified stream.</span></span>

</dd> <dt>

<span data-ttu-id="8199e-113">**cbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="8199e-113">**cbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8199e-114">Taille de la mémoire tampon **pbProtectionInfo** en octets.</span><span class="sxs-lookup"><span data-stu-id="8199e-114">Size of the **pbProtectionInfo** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8199e-115">**pbProtectionInfo**</span><span class="sxs-lookup"><span data-stu-id="8199e-115">**pbProtectionInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8199e-116">Mémoire tampon contenant des informations de protection supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8199e-116">Buffer containing additional protection information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8199e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8199e-117">Remarks</span></span>

<span data-ttu-id="8199e-118">Cette structure est utilisée par la méthode [**IWMDRMEncryptScatter :: InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) .</span><span class="sxs-lookup"><span data-stu-id="8199e-118">This structure is used by the [**IWMDRMEncryptScatter::InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8199e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8199e-119">Requirements</span></span>



| <span data-ttu-id="8199e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8199e-120">Requirement</span></span> | <span data-ttu-id="8199e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8199e-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8199e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8199e-122">Header</span></span><br/> | <dl> <span data-ttu-id="8199e-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8199e-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8199e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8199e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8199e-125">**Structures**</span><span class="sxs-lookup"><span data-stu-id="8199e-125">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





