---
title: WMDRMCryptoData, structure (wmdrmsdk. h)
description: La structure WMDRMCryptoData contient des informations sur l’algorithme de chiffrement utilisé pour chiffrer et déchiffrer le contenu.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Structure WMDRMCryptoData format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529937"
---
# <a name="wmdrmcryptodata-structure"></a><span data-ttu-id="3d2ee-105">WMDRMCryptoData, structure</span><span class="sxs-lookup"><span data-stu-id="3d2ee-105">WMDRMCryptoData structure</span></span>

<span data-ttu-id="3d2ee-106">La structure **WMDRMCryptoData** contient des informations sur l’algorithme de chiffrement utilisé pour chiffrer et déchiffrer le contenu.</span><span class="sxs-lookup"><span data-stu-id="3d2ee-106">The **WMDRMCryptoData** structure contains information about the cryptographic algorithm used to encrypt and decrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2ee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d2ee-107">Syntax</span></span>


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a><span data-ttu-id="3d2ee-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3d2ee-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3d2ee-109">**cryptoType**</span><span class="sxs-lookup"><span data-stu-id="3d2ee-109">**cryptoType**</span></span>
</dt> <dd>

<span data-ttu-id="3d2ee-110">Membre de l’énumération de [**\_ \_ type de chiffrement DRM**](drm-crypto-type.md) spécifiant le type d’algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="3d2ee-110">Member of the [**DRM\_CRYPTO\_TYPE**](drm-crypto-type.md) enumeration specifying the type of cryptographic algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="3d2ee-111">**qwCounterID**</span><span class="sxs-lookup"><span data-stu-id="3d2ee-111">**qwCounterID**</span></span>
</dt> <dd>

<span data-ttu-id="3d2ee-112">64 bits de poids fort du mode de compteur AES 128 bits.</span><span class="sxs-lookup"><span data-stu-id="3d2ee-112">The high 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="3d2ee-113">Ce membre est utilisé uniquement si le membre **cryptoType** est défini sur le **type de chiffrement \_ \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="3d2ee-113">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> <dt>

<span data-ttu-id="3d2ee-114">**qwOffset**</span><span class="sxs-lookup"><span data-stu-id="3d2ee-114">**qwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="3d2ee-115">64 bits de poids faible du mode de compteur AES 128 bits.</span><span class="sxs-lookup"><span data-stu-id="3d2ee-115">The low 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="3d2ee-116">Ce membre est utilisé uniquement si le membre **cryptoType** est défini sur le **type de chiffrement \_ \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="3d2ee-116">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d2ee-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d2ee-117">Requirements</span></span>



| <span data-ttu-id="3d2ee-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d2ee-118">Requirement</span></span> | <span data-ttu-id="3d2ee-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d2ee-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2ee-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d2ee-120">Header</span></span><br/> | <dl> <span data-ttu-id="3d2ee-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d2ee-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d2ee-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d2ee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2ee-123">**Structures**</span><span class="sxs-lookup"><span data-stu-id="3d2ee-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





