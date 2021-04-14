---
title: DRM_LASignaturePrivKey
description: La \_ propriété DRM LASignaturePrivKey contient la clé privée utilisée pour chiffrer l’en-tête DRM.
ms.assetid: b7083237-da11-4f31-a143-c0278a54b5a6
keywords:
- Format Windows Media DRM_LASignaturePrivKey
topic_type:
- apiref
api_name:
- DRM_LASignaturePrivKey
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdb22f3abc57fc2331ff87bd05bc05d580d607c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381551"
---
# <a name="drm_lasignatureprivkey"></a><span data-ttu-id="1a0c5-104">\_LASIGNATUREPRIVKEY DRM</span><span class="sxs-lookup"><span data-stu-id="1a0c5-104">DRM\_LASignaturePrivKey</span></span>

<span data-ttu-id="1a0c5-105">La propriété **DRM \_ LASignaturePrivKey** contient la clé privée utilisée pour chiffrer l’en-tête DRM.</span><span class="sxs-lookup"><span data-stu-id="1a0c5-105">The **DRM\_LASignaturePrivKey** property contains the private key that is used to encrypt the DRM header.</span></span>

## <a name="global-constant"></a><span data-ttu-id="1a0c5-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="1a0c5-106">Global Constant</span></span>

<span data-ttu-id="1a0c5-107">g \_ wszWMDRM \_ LASignaturePrivKey</span><span class="sxs-lookup"><span data-stu-id="1a0c5-107">g\_wszWMDRM\_LASignaturePrivKey</span></span>

## <a name="data-type"></a><span data-ttu-id="1a0c5-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="1a0c5-108">Data Type</span></span>

<span data-ttu-id="1a0c5-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="1a0c5-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="1a0c5-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1a0c5-110">Remarks</span></span>

<span data-ttu-id="1a0c5-111">Cette propriété peut être générée à l’aide de la méthode [**IWMDRMWriter :: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) .</span><span class="sxs-lookup"><span data-stu-id="1a0c5-111">This property can be generated using the [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair) method.</span></span> <span data-ttu-id="1a0c5-112">Cette propriété doit rester un secret connu uniquement par le créateur du contenu.</span><span class="sxs-lookup"><span data-stu-id="1a0c5-112">This property should remain a secret known only by the content creator.</span></span> <span data-ttu-id="1a0c5-113">Cette propriété peut être définie à l’aide de la méthode [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) .</span><span class="sxs-lookup"><span data-stu-id="1a0c5-113">This property can be set with the [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method.</span></span> <span data-ttu-id="1a0c5-114">Elle n’est pas accessible à l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="1a0c5-114">It is not accessible to the reader object.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a0c5-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a0c5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a0c5-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="1a0c5-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




