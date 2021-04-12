---
description: Définit les codes d’erreur de clé de média pour le moteur multimédia.
ms.assetid: F6E13260-74A2-40D0-A704-4E1CDB16B8D8
title: Énumération MF_MEDIA_ENGINE_KEYERR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_KEYERR
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 22dd22a7771f5d1e9466709f0b0da9ee936ef2b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321514"
---
# <a name="mf_media_engine_keyerr-enumeration"></a><span data-ttu-id="8f310-103">\_ \_ Énumération KEYERR du moteur multimédia MF \_</span><span class="sxs-lookup"><span data-stu-id="8f310-103">MF\_MEDIA\_ENGINE\_KEYERR enumeration</span></span>

<span data-ttu-id="8f310-104">Définit les codes d’erreur de clé de média pour le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="8f310-104">Defines media key error codes for the media engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f310-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8f310-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_KEYERR { 
  MF_MEDIAENGINE_KEYERR_UNKNOWN          = 1,
  MF_MEDIAENGINE_KEYERR_CLIENT           = 2,
  MF_MEDIAENGINE_KEYERR_SERVICE          = 3,
  MF_MEDIAENGINE_KEYERR_OUTPUT           = 4,
  MF_MEDIAENGINE_KEYERR_HARDWARECHANGE   = 5,
  MF_MEDIAENGINE_KEYERR_DOMAIN           = 6
} MF_MEDIA_ENGINE_KEYERR;
```



## <a name="constants"></a><span data-ttu-id="8f310-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8f310-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8f310-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="8f310-107"><span id="MF_MEDIAENGINE_KEYERR_UNKNOWN"></span><span id="mf_mediaengine_keyerr_unknown"></span>**MF\_MEDIAENGINE\_KEYERR\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="8f310-108">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8f310-108">Unknown error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8f310-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**\_ \_ client KEYERR MEDIAENGINE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8f310-109"><span id="MF_MEDIAENGINE_KEYERR_CLIENT"></span><span id="mf_mediaengine_keyerr_client"></span>**MF\_MEDIAENGINE\_KEYERR\_CLIENT**</span></span>
</dt> <dd>

<span data-ttu-id="8f310-110">Une erreur s’est produite avec le client.</span><span class="sxs-lookup"><span data-stu-id="8f310-110">An error with the client occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8f310-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**\_ \_ service KEYERR MEDIAENGINE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8f310-111"><span id="MF_MEDIAENGINE_KEYERR_SERVICE"></span><span id="mf_mediaengine_keyerr_service"></span>**MF\_MEDIAENGINE\_KEYERR\_SERVICE**</span></span>
</dt> <dd>

<span data-ttu-id="8f310-112">Une erreur s’est produite avec le service.</span><span class="sxs-lookup"><span data-stu-id="8f310-112">An error with the service occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8f310-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**\_sortie MEDIAENGINE \_ KEYERR \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8f310-113"><span id="MF_MEDIAENGINE_KEYERR_OUTPUT"></span><span id="mf_mediaengine_keyerr_output"></span>**MF\_MEDIAENGINE\_KEYERR\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="8f310-114">Une erreur avec la sortie s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8f310-114">An error with the output occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8f310-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF \_ MEDIAENGINE \_ KEYERR \_ HARDWARECHANGE**</span><span class="sxs-lookup"><span data-stu-id="8f310-115"><span id="MF_MEDIAENGINE_KEYERR_HARDWARECHANGE_"></span><span id="mf_mediaengine_keyerr_hardwarechange_"></span>**MF\_MEDIAENGINE\_KEYERR\_HARDWARECHANGE**</span></span> 
</dt> <dd>

<span data-ttu-id="8f310-116">Une erreur s’est produite en rapport avec une modification matérielle.</span><span class="sxs-lookup"><span data-stu-id="8f310-116">An error occurred related to a hardware change.</span></span>

</dd> <dt>

<span data-ttu-id="8f310-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**\_domaine MEDIAENGINE \_ KEYERR \_ MF**</span><span class="sxs-lookup"><span data-stu-id="8f310-117"><span id="MF_MEDIAENGINE_KEYERR_DOMAIN"></span><span id="mf_mediaengine_keyerr_domain"></span>**MF\_MEDIAENGINE\_KEYERR\_DOMAIN**</span></span>
</dt> <dd>

<span data-ttu-id="8f310-118">Une erreur s’est produite avec le domaine.</span><span class="sxs-lookup"><span data-stu-id="8f310-118">An error with the domain occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f310-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8f310-119">Remarks</span></span>

<span data-ttu-id="8f310-120">**MF \_ Le \_ \_ KEYERR du moteur multimédia** est utilisé avec le paramètre de *code* de [**IMFMediaKeySessionNotify :: keyerror**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) et la valeur de *code* retournée par [**IMFMediaKeySession :: GetError**](imfmediakeysession-geterror.md).</span><span class="sxs-lookup"><span data-stu-id="8f310-120">**MF\_MEDIA\_ENGINE\_KEYERR** is used with the *code* parameter of [**IMFMediaKeySessionNotify::KeyError**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror) and the *code* value returned from [**IMFMediaKeySession::GetError**](imfmediakeysession-geterror.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f310-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f310-121">Requirements</span></span>



| <span data-ttu-id="8f310-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f310-122">Requirement</span></span> | <span data-ttu-id="8f310-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f310-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f310-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f310-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8f310-125">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f310-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8f310-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f310-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8f310-127">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f310-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8f310-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="8f310-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8f310-129"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8f310-129"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f310-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f310-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f310-131">Énumérations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8f310-131">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




