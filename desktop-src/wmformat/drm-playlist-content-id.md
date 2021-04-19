---
title: Structure DRM_PLAYLIST_CONTENT_ID (Drmexternals. h)
description: La structure de l’ID de contenu de la \_ sélection DRM \_ contient des \_ informations sur le contenu à copier sur CD dans le cadre d’une gravure de sélection.
ms.assetid: 124e86ac-b0d4-40b2-868b-fe2fed1898e1
keywords:
- Structure DRM_PLAYLIST_CONTENT_ID format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_PLAYLIST_CONTENT_ID
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f475a8c3620ff1af64cb70914ca1ac591aa55106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513620"
---
# <a name="drm_playlist_content_id-structure"></a><span data-ttu-id="b1ba2-105">Structure de l’ID de contenu de la \_ sélection DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1ba2-105">DRM\_PLAYLIST\_CONTENT\_ID structure</span></span>

<span data-ttu-id="b1ba2-106">La structure de l’ID de contenu de la **\_ sélection \_ \_ DRM** contient des informations sur le contenu à copier sur CD dans le cadre d’une gravure de sélection.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-106">The **DRM\_PLAYLIST\_CONTENT\_ID** structure contains information about content that is to be copied to CD as part of a playlist burn.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1ba2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1ba2-107">Syntax</span></span>


```C++
typedef struct DRM_PLAYLIST_CONTENT_ID {
  LPCWSTR lpcwszV2Header;
  LPCSTR  lpcszV1KID;
  BYTE    *pbOtherData;
  DWORD   cbOtherData;
  DWORD   dwUniqueIDForSession;
  DWORD   dwValidFields;
} ;
```



## <a name="members"></a><span data-ttu-id="b1ba2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b1ba2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1ba2-109">**lpcwszV2Header**</span><span class="sxs-lookup"><span data-stu-id="b1ba2-109">**lpcwszV2Header**</span></span>
</dt> <dd>

<span data-ttu-id="b1ba2-110">En-tête DRM.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-110">DRM header.</span></span> <span data-ttu-id="b1ba2-111">Utilisez ce membre si le contenu est protégé par Windows Media DRM version 2 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-111">Use this member if the content is protected by Windows Media DRM version 2 or later.</span></span>

</dd> <dt>

<span data-ttu-id="b1ba2-112">**lpcszV1KID**</span><span class="sxs-lookup"><span data-stu-id="b1ba2-112">**lpcszV1KID**</span></span>
</dt> <dd>

<span data-ttu-id="b1ba2-113">ID de la clé.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-113">Key ID.</span></span> <span data-ttu-id="b1ba2-114">Utilisez ce membre si le contenu est protégé par Windows Media DRM version 1.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-114">Use this member if the content is protected by Windows Media DRM version 1.</span></span>

</dd> <dt>

<span data-ttu-id="b1ba2-115">**pbOtherData**</span><span class="sxs-lookup"><span data-stu-id="b1ba2-115">**pbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="b1ba2-116">Mémoire tampon contenant des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-116">Buffer containing supplementary data.</span></span>

</dd> <dt>

<span data-ttu-id="b1ba2-117">**cbOtherData**</span><span class="sxs-lookup"><span data-stu-id="b1ba2-117">**cbOtherData**</span></span>
</dt> <dd>

<span data-ttu-id="b1ba2-118">Taille de la mémoire tampon **pbOtherData** en octets.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-118">Size of the **pbOtherData** buffer in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b1ba2-119">**dwUniqueIDForSession**</span><span class="sxs-lookup"><span data-stu-id="b1ba2-119">**dwUniqueIDForSession**</span></span>
</dt> <dd>

<span data-ttu-id="b1ba2-120">Identificateur unique du contenu à utiliser dans la session active.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-120">Unique identifier for the content to be used in the current session.</span></span>

</dd> <dt>

<span data-ttu-id="b1ba2-121">**dwValidFields**</span><span class="sxs-lookup"><span data-stu-id="b1ba2-121">**dwValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="b1ba2-122">**Valeur DWORD** indiquant les champs valides de cette structure.</span><span class="sxs-lookup"><span data-stu-id="b1ba2-122">**DWORD** indicating the valid fields of this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1ba2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1ba2-123">Requirements</span></span>



| <span data-ttu-id="b1ba2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1ba2-124">Requirement</span></span> | <span data-ttu-id="b1ba2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1ba2-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ba2-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1ba2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ba2-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1ba2-127">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1ba2-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1ba2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ba2-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1ba2-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b1ba2-130">Version</span><span class="sxs-lookup"><span data-stu-id="b1ba2-130">Version</span></span><br/>                  | <span data-ttu-id="b1ba2-131">SDK Windows Media format 11</span><span class="sxs-lookup"><span data-stu-id="b1ba2-131">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="b1ba2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1ba2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1ba2-133"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1ba2-133"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1ba2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1ba2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1ba2-135">**Structures**</span><span class="sxs-lookup"><span data-stu-id="b1ba2-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





