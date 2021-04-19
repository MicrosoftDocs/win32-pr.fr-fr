---
description: Spécifie si le IMFTransform souhaite recevoir des notifications d’achèvement MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533624"
---
# <a name="mft_policy_set_aware-attribute"></a><span data-ttu-id="de942-103">Attribut de reconnaissance de l' \_ ensemble de stratégies MFT \_ \_</span><span class="sxs-lookup"><span data-stu-id="de942-103">MFT\_POLICY\_SET\_AWARE attribute</span></span>

<span data-ttu-id="de942-104">Si la valeur est différente de zéro, indique que le **IMFTransform** souhaite recevoir des notifications d’achèvement [MEPolicySet](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="de942-104">If non-zero, indicates that the **IMFTransform** wants to receive [MEPolicySet](./mepolicyset.md) completion notifications.</span></span>

## <a name="data-type"></a><span data-ttu-id="de942-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="de942-105">Data type</span></span>

<span data-ttu-id="de942-106">**UInt32** (traité comme **bool**)</span><span class="sxs-lookup"><span data-stu-id="de942-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="getset"></a><span data-ttu-id="de942-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="de942-107">Get/set</span></span>

<span data-ttu-id="de942-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="de942-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="de942-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="de942-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="de942-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="de942-110">Applies to</span></span>

[<span data-ttu-id="de942-111">**IMFInputTrustAuthority**</span><span class="sxs-lookup"><span data-stu-id="de942-111">**IMFInputTrustAuthority**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a><span data-ttu-id="de942-112">Notes</span><span class="sxs-lookup"><span data-stu-id="de942-112">Remarks</span></span>

<span data-ttu-id="de942-113">Cet attribute peut être utilisé par un Decrypter **IMFInputTrustAuthority** .</span><span class="sxs-lookup"><span data-stu-id="de942-113">This attributet can be used by an **IMFInputTrustAuthority** decrypter.</span></span> <span data-ttu-id="de942-114">Une implémentation d’un module de déchiffrement de contenu (CDM) peut inclure une implémentation de **IMFInputTrustAuthority**.</span><span class="sxs-lookup"><span data-stu-id="de942-114">An implementation of a Content Decryption Module (CDM) may include an implementation of **IMFInputTrustAuthority**.</span></span> <span data-ttu-id="de942-115">L’objet **IMFInputTrustAuthority** est accessible via [IMFContentDecryptionModule :: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span><span class="sxs-lookup"><span data-stu-id="de942-115">The **IMFInputTrustAuthority** object is accessed through [IMFContentDecryptionModule::CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).</span></span>


<span data-ttu-id="de942-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="de942-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="de942-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de942-117">Requirements</span></span>



| <span data-ttu-id="de942-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de942-118">Requirement</span></span> | <span data-ttu-id="de942-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="de942-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de942-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de942-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de942-121">Mise à jour 2020 de Windows 10 avril</span><span class="sxs-lookup"><span data-stu-id="de942-121">Windows 10 April 2020 Update</span></span>   <br/>                                        |
| <span data-ttu-id="de942-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="de942-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de942-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="de942-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de942-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de942-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de942-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de942-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[<span data-ttu-id="de942-126">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="de942-126">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
