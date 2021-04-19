---
description: Définit l’ID de clé de l’exemple.
ms.assetid: 75339350-05AA-486E-9C28-11070C0DA61D
title: Attribut MFSampleExtension_Content_KeyID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40d698dbb2d64e9744027b3cd8a3bb2dceec226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524585"
---
# <a name="mfsampleextension_content_keyid-attribute"></a><span data-ttu-id="44d2b-103">\_ \_ Attribut KeyId content MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="44d2b-103">MFSampleExtension\_Content\_KeyID attribute</span></span>

<span data-ttu-id="44d2b-104">Définit l’ID de clé de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="44d2b-104">Sets the Key ID for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="44d2b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="44d2b-105">Data type</span></span>

<span data-ttu-id="44d2b-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="44d2b-106">**GUID**</span></span>

## <a name="examples"></a><span data-ttu-id="44d2b-107">Exemples</span><span class="sxs-lookup"><span data-stu-id="44d2b-107">Examples</span></span>

<span data-ttu-id="44d2b-108">L’exemple suivant montre comment définir l’ID de clé de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="44d2b-108">The following example shows how to set the Key ID for the sample.</span></span>


```C++
// m_spSample is a IMFSample
// guidKID is a GUID

m_spSample->SetGUID( MFSampleExtension_Content_KeyID, guidKID );
```



## <a name="requirements"></a><span data-ttu-id="44d2b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44d2b-109">Requirements</span></span>



| <span data-ttu-id="44d2b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44d2b-110">Requirement</span></span> | <span data-ttu-id="44d2b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="44d2b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44d2b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44d2b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="44d2b-113">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44d2b-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="44d2b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44d2b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="44d2b-115">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="44d2b-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="44d2b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="44d2b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="44d2b-117"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44d2b-117"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d2b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44d2b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44d2b-119">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44d2b-119">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44d2b-120">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="44d2b-120">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="44d2b-121">MFSampleExtension de \_ chiffrement \_ SubSampleMappingSplit</span><span class="sxs-lookup"><span data-stu-id="44d2b-121">MFSampleExtension\_Encryption\_SubSampleMappingSplit</span></span>](mfsampleextension-encryption-subsamplemappingsplit.md)
</dt> </dl>

 

 




