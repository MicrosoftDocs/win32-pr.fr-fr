---
description: 'Contient l’URL du fichier IFO (informations sur le DVD) spécifié par le serveur HTTP dans l’en-tête HTTP, &\# 0034 ; Pragma : ifoFileURI.dlna.org&\# 0034 ;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Attribut MF_BYTESTREAM_IFO_FILE_URI (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534161"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a><span data-ttu-id="3ecd4-103">\_Attribut d' \_ \_ URI de fichier IFO BYTESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="3ecd4-103">MF\_BYTESTREAM\_IFO\_FILE\_URI attribute</span></span>

<span data-ttu-id="3ecd4-104">Contient l’URL du fichier IFO (informations sur le DVD) spécifié par le serveur HTTP dans l’en-tête HTTP, « Pragma : ifoFileURI.dlna.org ».</span><span class="sxs-lookup"><span data-stu-id="3ecd4-104">Contains the URL of the IFO (DVD Information) file specified by the HTTP server in the HTTP header, "Pragma: ifoFileURI.dlna.org".</span></span>

## <a name="data-type"></a><span data-ttu-id="3ecd4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="3ecd4-105">Data type</span></span>

<span data-ttu-id="3ecd4-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="3ecd4-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="3ecd4-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="3ecd4-107">Get/set</span></span>

<span data-ttu-id="3ecd4-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="3ecd4-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="3ecd4-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="3ecd4-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3ecd4-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="3ecd4-110">Applies to</span></span>

[<span data-ttu-id="3ecd4-111">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="3ecd4-111">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="3ecd4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="3ecd4-112">Remarks</span></span>

<span data-ttu-id="3ecd4-113">Le flux d’octets HTTP recherche la chaîne « ifoFileURI.dlna.org » dans l’en-tête HTTP.</span><span class="sxs-lookup"><span data-stu-id="3ecd4-113">The HTTP byte stream searches the HTTP header for the "ifoFileURI.dlna.org" string.</span></span> <span data-ttu-id="3ecd4-114">Si la chaîne est trouvée, elle est copiée dans cet attribut sur le flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="3ecd4-114">If the string is found, it is copied to this attribute on the byte stream.</span></span>

<span data-ttu-id="3ecd4-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3ecd4-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecd4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ecd4-116">Requirements</span></span>



| <span data-ttu-id="3ecd4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ecd4-117">Requirement</span></span> | <span data-ttu-id="3ecd4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ecd4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecd4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ecd4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecd4-120">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3ecd4-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                                        |
| <span data-ttu-id="3ecd4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ecd4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecd4-122">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3ecd4-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="3ecd4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ecd4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ecd4-124"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ecd4-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ecd4-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ecd4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecd4-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ecd4-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ecd4-127">Attributs de flux d’octets</span><span class="sxs-lookup"><span data-stu-id="3ecd4-127">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ecd4-128">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="3ecd4-128">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




