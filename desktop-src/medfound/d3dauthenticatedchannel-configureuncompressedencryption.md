---
description: Contient des données d’entrée pour la \_ commande D3DAUTHENTICATEDCONFIGURE ENCRYPTIONWHENACCESSIBLE.
ms.assetid: d2d0adff-5d4d-4af3-b6b8-b8c60a506142
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c8ea4360ff7f2bbcf2c03040671013473e9873a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527598"
---
# <a name="d3dauthenticatedchannel_configureuncompressedencryption-structure"></a><span data-ttu-id="ef8be-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION, structure</span><span class="sxs-lookup"><span data-stu-id="ef8be-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION structure</span></span>

<span data-ttu-id="ef8be-104">Contient des données d’entrée pour la commande [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .</span><span class="sxs-lookup"><span data-stu-id="ef8be-104">Contains input data for the [**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) command.</span></span>

<span data-ttu-id="ef8be-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="ef8be-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef8be-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef8be-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  GUID                                    EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREUNCOMPRESSEDENCRYPTION;
```



## <a name="members"></a><span data-ttu-id="ef8be-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ef8be-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef8be-108">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="ef8be-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="ef8be-109">Un [**D3DAUTHENTICATEDCHANNEL \_ configure une structure \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) qui contient le GUID de la commande et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="ef8be-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="ef8be-110">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="ef8be-110">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="ef8be-111">GUID qui spécifie le type de chiffrement à appliquer.</span><span class="sxs-lookup"><span data-stu-id="ef8be-111">A GUID that specifies the type of encryption to apply.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef8be-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef8be-112">Requirements</span></span>



| <span data-ttu-id="ef8be-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef8be-113">Requirement</span></span> | <span data-ttu-id="ef8be-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef8be-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8be-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef8be-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8be-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef8be-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ef8be-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef8be-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8be-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef8be-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ef8be-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef8be-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef8be-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef8be-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef8be-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef8be-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef8be-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="ef8be-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="ef8be-123">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="ef8be-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




