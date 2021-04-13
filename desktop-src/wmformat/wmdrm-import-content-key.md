---
title: Structure WMDRM_IMPORT_CONTENT_KEY (Drmexternals. h)
description: La \_ \_ \_ structure de clé de contenu d’importation WMDRM stocke la clé de contenu utilisée pour l’importation de contenu protégé.
ms.assetid: 29a0f98d-96a3-46b2-a67c-dbb23449e927
keywords:
- Structure WMDRM_IMPORT_CONTENT_KEY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_CONTENT_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d616cfe856a19f4f8ffa5254254d3946b1544dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383991"
---
# <a name="wmdrm_import_content_key-structure"></a><span data-ttu-id="d38cd-105">\_Structure de \_ clé du contenu d’importation WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="d38cd-105">WMDRM\_IMPORT\_CONTENT\_KEY structure</span></span>

<span data-ttu-id="d38cd-106">La structure de **\_ clé de \_ contenu \_ d’importation WMDRM** stocke la clé de contenu utilisée pour l’importation de contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="d38cd-106">The **WMDRM\_IMPORT\_CONTENT\_KEY** structure stores the content key used in importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38cd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d38cd-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_CONTENT_KEY {
  DWORD dwVersion;
  DWORD cbStructSize;
  DWORD dwIVKeyType;
  DWORD cbIVKey;
  DWORD dwContentKeyType;
  DWORD cbContentKey;
  BYTE  rgbKeyData[1];
} ;
```



## <a name="members"></a><span data-ttu-id="d38cd-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d38cd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d38cd-109">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="d38cd-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d38cd-110">Version.</span><span class="sxs-lookup"><span data-stu-id="d38cd-110">Version.</span></span>

</dd> <dt>

<span data-ttu-id="d38cd-111">**cbStructSize**</span><span class="sxs-lookup"><span data-stu-id="d38cd-111">**cbStructSize**</span></span>
</dt> <dd>

<span data-ttu-id="d38cd-112">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="d38cd-112">Size of structure in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d38cd-113">**dwIVKeyType**</span><span class="sxs-lookup"><span data-stu-id="d38cd-113">**dwIVKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="d38cd-114">Type de clé du vecteur d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="d38cd-114">Initialization vector key type.</span></span> <span data-ttu-id="d38cd-115">Définissez sur le \_ type de frappe WMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="d38cd-115">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="d38cd-116">**cbIVKey**</span><span class="sxs-lookup"><span data-stu-id="d38cd-116">**cbIVKey**</span></span>
</dt> <dd>

<span data-ttu-id="d38cd-117">Taille de la clé du vecteur d’initialisation, en octets.</span><span class="sxs-lookup"><span data-stu-id="d38cd-117">Size of the initialization vector key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d38cd-118">**dwContentKeyType**</span><span class="sxs-lookup"><span data-stu-id="d38cd-118">**dwContentKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="d38cd-119">Type de clé de contenu.</span><span class="sxs-lookup"><span data-stu-id="d38cd-119">Content key type.</span></span> <span data-ttu-id="d38cd-120">Définissez sur le \_ type de cocktail de type de l’entrée WMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="d38cd-120">Set to WMDRM\_KEYTYPE\_COCKTAIL.</span></span>

</dd> <dt>

<span data-ttu-id="d38cd-121">**cbContentKey**</span><span class="sxs-lookup"><span data-stu-id="d38cd-121">**cbContentKey**</span></span>
</dt> <dd>

<span data-ttu-id="d38cd-122">Taille de la clé de contenu en octets.</span><span class="sxs-lookup"><span data-stu-id="d38cd-122">Size of the content key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d38cd-123">**rgbKeyData**</span><span class="sxs-lookup"><span data-stu-id="d38cd-123">**rgbKeyData**</span></span>
</dt> <dd>

<span data-ttu-id="d38cd-124">Adresse d’une mémoire tampon contenant la clé de contenu.</span><span class="sxs-lookup"><span data-stu-id="d38cd-124">Address of a buffer containing the content key.</span></span> <span data-ttu-id="d38cd-125">La taille de la mémoire tampon doit correspondre à la valeur de **cbContentKey**.</span><span class="sxs-lookup"><span data-stu-id="d38cd-125">The buffer size must match the value of **cbContentKey**.</span></span> <span data-ttu-id="d38cd-126">Cette clé doit correspondre à la clé importée à partir du message de licence XMR.</span><span class="sxs-lookup"><span data-stu-id="d38cd-126">This key should match the key imported from the XMR license message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d38cd-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d38cd-127">Remarks</span></span>

<span data-ttu-id="d38cd-128">Cette structure, y compris la mémoire tampon qui contient la clé de session, doit être chiffrée à l’aide de la clé de session et incluse dans le membre **pbEncryptedKeyMessage** de la structure d' [**importation/ \_ exportation \_ \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="d38cd-128">This structure, including the buffer containing the session key, must be encrypted with the session key and included in the **pbEncryptedKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="d38cd-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d38cd-129">Requirements</span></span>



| <span data-ttu-id="d38cd-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d38cd-130">Requirement</span></span> | <span data-ttu-id="d38cd-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38cd-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38cd-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d38cd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d38cd-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d38cd-133">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d38cd-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d38cd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d38cd-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d38cd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d38cd-136">Version</span><span class="sxs-lookup"><span data-stu-id="d38cd-136">Version</span></span><br/>                  | <span data-ttu-id="d38cd-137">SDK Windows Media format 11</span><span class="sxs-lookup"><span data-stu-id="d38cd-137">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="d38cd-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="d38cd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d38cd-139"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="d38cd-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d38cd-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d38cd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38cd-141">**Structures**</span><span class="sxs-lookup"><span data-stu-id="d38cd-141">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





