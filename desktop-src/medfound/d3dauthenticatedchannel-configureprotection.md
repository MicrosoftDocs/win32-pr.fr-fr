---
description: Contient des données d’entrée pour une \_ commande de protection D3DAUTHENTICATEDCONFIGURE.
ms.assetid: 44f37e78-7218-42be-a07a-5ab911f2ba21
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b3fc1daee7bfd9320539a03974ab431c4ba588d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861809"
---
# <a name="d3dauthenticatedchannel_configureprotection-structure"></a><span data-ttu-id="af802-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION, structure</span><span class="sxs-lookup"><span data-stu-id="af802-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREPROTECTION structure</span></span>

<span data-ttu-id="af802-104">Contient des données d’entrée pour une commande de [**\_ protection D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="af802-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_PROTECTION**](d3dauthenticatedconfigure-protection.md) command.</span></span>

<span data-ttu-id="af802-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="af802-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="af802-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af802-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT  Parameters;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS Protections;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREPROTECTION;
```



## <a name="members"></a><span data-ttu-id="af802-107">Membres</span><span class="sxs-lookup"><span data-stu-id="af802-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="af802-108">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="af802-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="af802-109">Un [**D3DAUTHENTICATEDCHANNEL \_ configure une structure \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) qui contient le GUID de la commande et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="af802-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="af802-110">**Protections**</span><span class="sxs-lookup"><span data-stu-id="af802-110">**Protections**</span></span>
</dt> <dd>

<span data-ttu-id="af802-111">Structure [**d' \_ \_ indicateurs de protection D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) qui spécifie le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="af802-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af802-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af802-112">Requirements</span></span>



| <span data-ttu-id="af802-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af802-113">Requirement</span></span> | <span data-ttu-id="af802-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="af802-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af802-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af802-115">Minimum supported client</span></span><br/> | <span data-ttu-id="af802-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af802-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af802-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af802-117">Minimum supported server</span></span><br/> | <span data-ttu-id="af802-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af802-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="af802-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="af802-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="af802-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="af802-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af802-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af802-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af802-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="af802-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="af802-123">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="af802-123">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




