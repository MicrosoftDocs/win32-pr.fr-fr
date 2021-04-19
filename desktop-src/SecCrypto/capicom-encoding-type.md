---
description: Indique le type d’encodage utilisé.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Énumération CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531090"
---
# <a name="capicom_encoding_type-enumeration"></a><span data-ttu-id="4f21c-103">\_Énumération de type d’encodage CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="4f21c-103">CAPICOM\_ENCODING\_TYPE enumeration</span></span>

<span data-ttu-id="4f21c-104">Le type d’énumération de **\_ \_ type d’encodage CAPICOM** indique le type d’encodage utilisé.</span><span class="sxs-lookup"><span data-stu-id="4f21c-104">The **CAPICOM\_ENCODING\_TYPE** enumeration type indicates the encoding type used.</span></span>

## <a name="members"></a><span data-ttu-id="4f21c-105">Membres</span><span class="sxs-lookup"><span data-stu-id="4f21c-105">Members</span></span>



| <span data-ttu-id="4f21c-106">Membre</span><span class="sxs-lookup"><span data-stu-id="4f21c-106">Member</span></span>                      | <span data-ttu-id="4f21c-107">Description</span><span class="sxs-lookup"><span data-stu-id="4f21c-107">Description</span></span>                                                                                                                                                                                 | <span data-ttu-id="4f21c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f21c-108">Value</span></span>      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="4f21c-109">**\_coder \_ tout**</span><span class="sxs-lookup"><span data-stu-id="4f21c-109">**CAPICOM\_ENCODE\_ANY**</span></span>    | <span data-ttu-id="4f21c-110">Les données sont enregistrées sous la forme d’une chaîne codée en base64 ou d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="4f21c-110">Data is saved as a base64-encoded string or a pure binary sequence.</span></span> <span data-ttu-id="4f21c-111">Ce type d’encodage est utilisé uniquement pour les données d’entrée dont le type d’encodage est inconnu.</span><span class="sxs-lookup"><span data-stu-id="4f21c-111">This encoding type is used only for input data that has an unknown encoding type.</span></span> <span data-ttu-id="4f21c-112">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="4f21c-112">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="4f21c-113">égale</span><span class="sxs-lookup"><span data-stu-id="4f21c-113">0xffffffff</span></span> |
| <span data-ttu-id="4f21c-114">**\_Encode \_ Base64**</span><span class="sxs-lookup"><span data-stu-id="4f21c-114">**CAPICOM\_ENCODE\_BASE64**</span></span> | <span data-ttu-id="4f21c-115">Les données sont enregistrées sous la forme d’une chaîne encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="4f21c-115">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                        | <span data-ttu-id="4f21c-116">0</span><span class="sxs-lookup"><span data-stu-id="4f21c-116">0</span></span>          |
| <span data-ttu-id="4f21c-117">**codage d’un \_ \_ fichier binaire CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="4f21c-117">**CAPICOM\_ENCODE\_BINARY**</span></span> | <span data-ttu-id="4f21c-118">Les données sont enregistrées sous la forme d’une séquence binaire pure.</span><span class="sxs-lookup"><span data-stu-id="4f21c-118">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                         | <span data-ttu-id="4f21c-119">1</span><span class="sxs-lookup"><span data-stu-id="4f21c-119">1</span></span>          |



## <a name="remarks"></a><span data-ttu-id="4f21c-120">Notes</span><span class="sxs-lookup"><span data-stu-id="4f21c-120">Remarks</span></span>

<span data-ttu-id="4f21c-121">Ce type d’énumération est utilisé par les méthodes et propriétés CAPICOM suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f21c-121">This enumeration type is used by the following CAPICOM methods and properties:</span></span>

-   <span data-ttu-id="4f21c-122">[**Certificate. Export,**](certificate-export.md) méthode</span><span class="sxs-lookup"><span data-stu-id="4f21c-122">[**Certificate.Export**](certificate-export.md) method</span></span>
-   <span data-ttu-id="4f21c-123">[**EncodedData. Value**](encodeddata-value.md) (propriété)</span><span class="sxs-lookup"><span data-stu-id="4f21c-123">[**EncodedData.Value**](encodeddata-value.md) property</span></span>
-   <span data-ttu-id="4f21c-124">[**EncryptedData. Encrypt,**](encrypteddata-encrypt.md) méthode</span><span class="sxs-lookup"><span data-stu-id="4f21c-124">[**EncryptedData.Encrypt**](encrypteddata-encrypt.md) method</span></span>
-   <span data-ttu-id="4f21c-125">[**EnvelopedData. Encrypt,**](envelopeddata-encrypt.md) méthode</span><span class="sxs-lookup"><span data-stu-id="4f21c-125">[**EnvelopedData.Encrypt**](envelopeddata-encrypt.md) method</span></span>
-   <span data-ttu-id="4f21c-126">[**ExtendedProperty. Value**](extendedproperty-value.md) (propriété)</span><span class="sxs-lookup"><span data-stu-id="4f21c-126">[**ExtendedProperty.Value**](extendedproperty-value.md) property</span></span>
-   <span data-ttu-id="4f21c-127">[**SignedData. Sign,**](signeddata-sign.md) méthode</span><span class="sxs-lookup"><span data-stu-id="4f21c-127">[**SignedData.Sign**](signeddata-sign.md) method</span></span>
-   <span data-ttu-id="4f21c-128">[**SignedData. cosign,**](signeddata-cosign.md) méthode</span><span class="sxs-lookup"><span data-stu-id="4f21c-128">[**SignedData.CoSign**](signeddata-cosign.md) method</span></span>
-   <span data-ttu-id="4f21c-129">[**Store. Export,**](store-export.md) méthode</span><span class="sxs-lookup"><span data-stu-id="4f21c-129">[**Store.Export**](store-export.md) method</span></span>
-   <span data-ttu-id="4f21c-130">Méthode [**Utilities. GetRandom**](utilities-getrandom.md)</span><span class="sxs-lookup"><span data-stu-id="4f21c-130">[**Utilities.GetRandom**](utilities-getrandom.md) method</span></span>

## <a name="requirements"></a><span data-ttu-id="4f21c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f21c-131">Requirements</span></span>



| <span data-ttu-id="4f21c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f21c-132">Requirement</span></span> | <span data-ttu-id="4f21c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f21c-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4f21c-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4f21c-134">Redistributable</span></span><br/> | <span data-ttu-id="4f21c-135">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="4f21c-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="4f21c-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f21c-136">Header</span></span><br/>          | <dl> <span data-ttu-id="4f21c-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f21c-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 




