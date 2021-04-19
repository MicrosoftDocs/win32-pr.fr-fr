---
description: Contient des données d’entrée pour une \_ commande D3DAUTHENTICATEDCONFIGURE CRYPTOSESSION.
ms.assetid: eed5591d-20b0-495c-8c05-b9cb3b91deab
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2b1cca13bcd37e488cd0ed455098afa62492579f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515390"
---
# <a name="d3dauthenticatedchannel_configurecryptosession-structure"></a><span data-ttu-id="b4900-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION, structure</span><span class="sxs-lookup"><span data-stu-id="b4900-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURECRYPTOSESSION structure</span></span>

<span data-ttu-id="b4900-104">Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="b4900-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) command.</span></span>

<span data-ttu-id="b4900-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="b4900-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="b4900-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4900-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  HANDLE                                  DXVA2DecodeHandle;
  HANDLE                                  CryptoSessionHandle;
  HANDLE                                  DeviceHandle;
} D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION;
```



## <a name="members"></a><span data-ttu-id="b4900-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b4900-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4900-108">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="b4900-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="b4900-109">Un [**D3DAUTHENTICATEDCHANNEL \_ configure une structure \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) qui contient le GUID de la commande et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="b4900-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="b4900-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="b4900-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b4900-111">Handle de l’appareil de décodage de DirectX Video Acceleration 2 (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="b4900-111">A handle to the DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> <dt>

<span data-ttu-id="b4900-112">**CryptoSessionHandle**</span><span class="sxs-lookup"><span data-stu-id="b4900-112">**CryptoSessionHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b4900-113">Handle de la session de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="b4900-113">A handle to the cryptographic session.</span></span>

</dd> <dt>

<span data-ttu-id="b4900-114">**DeviceHandle**</span><span class="sxs-lookup"><span data-stu-id="b4900-114">**DeviceHandle**</span></span>
</dt> <dd>

<span data-ttu-id="b4900-115">Handle du périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b4900-115">A handle to the Direct3D device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4900-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4900-116">Requirements</span></span>



| <span data-ttu-id="b4900-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4900-117">Requirement</span></span> | <span data-ttu-id="b4900-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4900-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4900-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4900-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4900-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4900-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b4900-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4900-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4900-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4900-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b4900-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4900-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4900-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4900-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4900-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4900-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4900-126">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="b4900-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="b4900-127">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="b4900-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




