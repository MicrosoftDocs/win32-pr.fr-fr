---
title: Structure WMDRM_IMPORT_SESSION_KEY (Drmexternals. h)
description: La \_ \_ \_ structure de la clé de session d’importation WMDRM contient la clé de session pour l’importation de contenu protégé.
ms.assetid: 2dd1e8ec-a25f-4ced-8f1b-286534c66ebf
keywords:
- Structure WMDRM_IMPORT_SESSION_KEY format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- WMDRM_IMPORT_SESSION_KEY
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93295e73e4e3e5e13b438f8b62e0ab6bfff43ee7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105304"
---
# <a name="wmdrm_import_session_key-structure"></a><span data-ttu-id="8fd54-105">Structure de la clé de session d' \_ importation WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="8fd54-105">WMDRM\_IMPORT\_SESSION\_KEY structure</span></span>

<span data-ttu-id="8fd54-106">La structure de la **\_ clé de \_ session \_ d’importation WMDRM** contient la clé de session pour l’importation de contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="8fd54-106">The **WMDRM\_IMPORT\_SESSION\_KEY** structure holds the session key for importing protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd54-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fd54-107">Syntax</span></span>


```C++
typedef struct WMDRM_IMPORT_SESSION_KEY {
  DWORD dwKeyType;
  DWORD cbKey;
  BYTE  rgbKey[1];
} ;
```



## <a name="members"></a><span data-ttu-id="8fd54-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8fd54-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8fd54-109">**dwKeyType**</span><span class="sxs-lookup"><span data-stu-id="8fd54-109">**dwKeyType**</span></span>
</dt> <dd>

<span data-ttu-id="8fd54-110">Type de clé de session.</span><span class="sxs-lookup"><span data-stu-id="8fd54-110">Session key type.</span></span> <span data-ttu-id="8fd54-111">Définissez sur le \_ type de frappe WMDRM \_ .</span><span class="sxs-lookup"><span data-stu-id="8fd54-111">Set to WMDRM\_KEYTYPE\_RC4.</span></span>

</dd> <dt>

<span data-ttu-id="8fd54-112">**cbKey**</span><span class="sxs-lookup"><span data-stu-id="8fd54-112">**cbKey**</span></span>
</dt> <dd>

<span data-ttu-id="8fd54-113">Taille de la clé de session, en octets.</span><span class="sxs-lookup"><span data-stu-id="8fd54-113">Size of the session key, in bytes.</span></span> <span data-ttu-id="8fd54-114">Cette valeur peut être aussi importante que nécessaire, étant donné les limites d’une seule opération OAEP RSA sur l’ensemble du message (cette structure plus la clé de session).</span><span class="sxs-lookup"><span data-stu-id="8fd54-114">This value can be as large as you need, given the limits of a single RSA OAEP operation over the entire message (this structure plus the session key).</span></span>

</dd> <dt>

<span data-ttu-id="8fd54-115">**rgbKey**</span><span class="sxs-lookup"><span data-stu-id="8fd54-115">**rgbKey**</span></span>
</dt> <dd>

<span data-ttu-id="8fd54-116">Adresse d’une mémoire tampon contenant la clé de session.</span><span class="sxs-lookup"><span data-stu-id="8fd54-116">Address of a buffer containing the session key.</span></span> <span data-ttu-id="8fd54-117">La taille de la mémoire tampon doit correspondre à la valeur de **cbKey**.</span><span class="sxs-lookup"><span data-stu-id="8fd54-117">The buffer size must match the value of **cbKey**.</span></span> <span data-ttu-id="8fd54-118">Les données de la mémoire tampon sont une valeur de clé générée de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="8fd54-118">The data in the buffer is a randomly generated key value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fd54-119">Notes</span><span class="sxs-lookup"><span data-stu-id="8fd54-119">Remarks</span></span>

<span data-ttu-id="8fd54-120">Cette structure, y compris la mémoire tampon contenant la clé de session, doit être chiffrée à l’aide de la clé publique de l’ordinateur Windows Media DRM et incluse dans le membre **pbEncryptedSessionKeyMessage** de la structure d' [**importation/ \_ exportation \_ \_ WMDRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) .</span><span class="sxs-lookup"><span data-stu-id="8fd54-120">This structure, including the buffer containing the session key, must be encrypted with the Windows Media DRM machine public key and included in the **pbEncryptedSessionKeyMessage** member of the [**WMDRM\_IMPORT\_INIT\_STRUCT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fd54-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fd54-121">Requirements</span></span>



| <span data-ttu-id="8fd54-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fd54-122">Requirement</span></span> | <span data-ttu-id="8fd54-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fd54-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd54-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fd54-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd54-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fd54-125">Windows XP \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8fd54-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fd54-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd54-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fd54-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8fd54-128">Version</span><span class="sxs-lookup"><span data-stu-id="8fd54-128">Version</span></span><br/>                  | <span data-ttu-id="8fd54-129">SDK Windows Media format 11</span><span class="sxs-lookup"><span data-stu-id="8fd54-129">Windows Media Format 11 SDK</span></span><br/>                                                    |
| <span data-ttu-id="8fd54-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fd54-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fd54-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fd54-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fd54-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fd54-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd54-133">**Structures**</span><span class="sxs-lookup"><span data-stu-id="8fd54-133">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





