---
description: Attribut qui est transmis dans le IMFMediaEngineNeedKeyNotify au moteur multimédia lors de la création.
ms.assetid: B9625B3C-00AC-4F46-BD76-5C77822F5829
title: Attribut MF_MEDIA_ENGINE_NEEDKEY_CALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3de502bbe1d7f83dfd8ee7478e20786244f654e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522504"
---
# <a name="mf_media_engine_needkey_callback-attribute"></a><span data-ttu-id="d8977-103">\_Attribut de \_ \_ rappel NEEDKEY du moteur multimédia MF \_</span><span class="sxs-lookup"><span data-stu-id="d8977-103">MF\_MEDIA\_ENGINE\_NEEDKEY\_CALLBACK attribute</span></span>

<span data-ttu-id="d8977-104">Attribut qui est transmis dans le [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) au moteur multimédia lors de la création.</span><span class="sxs-lookup"><span data-stu-id="d8977-104">Attribute which is passed in the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) to the media engine on creation.</span></span>

## <a name="data-type"></a><span data-ttu-id="d8977-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d8977-105">Data type</span></span>

<span data-ttu-id="d8977-106">**IMFMediaEngineNeedKeyNotify \* *_ stocké en tant que _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="d8977-106">**IMFMediaEngineNeedKeyNotify\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="d8977-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="d8977-107">Get/set</span></span>

<span data-ttu-id="d8977-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="d8977-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="d8977-109">Pour définir cet attribut, appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="d8977-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8977-110">Notes</span><span class="sxs-lookup"><span data-stu-id="d8977-110">Remarks</span></span>

<span data-ttu-id="d8977-111">La valeur de cet attribut est un pointeur vers l’interface [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) , implémentée par l’application.</span><span class="sxs-lookup"><span data-stu-id="d8977-111">The value of this attribute is a pointer to the [**IMFMediaEngineNeedKeyNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify) interface, implemented by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8977-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8977-112">Requirements</span></span>



| <span data-ttu-id="d8977-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8977-113">Requirement</span></span> | <span data-ttu-id="d8977-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8977-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8977-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8977-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d8977-116">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8977-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d8977-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8977-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d8977-118">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8977-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d8977-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="d8977-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8977-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8977-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8977-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8977-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8977-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d8977-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




