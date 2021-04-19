---
title: Structure de DDS_PIXELFORMAT (DDS. h)
description: Format de pixel de surface.
ms.assetid: 39c5e48d-cf20-4d77-80d5-a67f04de4883
keywords:
- DDS_PIXELFORMAT de la structure DDS
topic_type:
- apiref
api_name:
- DDS_PIXELFORMAT
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd909d62a1be212f9ed4ef9af243a27f28be818
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106539866"
---
# <a name="dds_pixelformat-structure"></a><span data-ttu-id="359e0-104">\_Structure DDS PIXELFORMAT</span><span class="sxs-lookup"><span data-stu-id="359e0-104">DDS\_PIXELFORMAT structure</span></span>

<span data-ttu-id="359e0-105">Format de pixel de surface.</span><span class="sxs-lookup"><span data-stu-id="359e0-105">Surface pixel format.</span></span>

## <a name="syntax"></a><span data-ttu-id="359e0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="359e0-106">Syntax</span></span>


```C++
struct DDS_PIXELFORMAT {
  DWORD dwSize;
  DWORD dwFlags;
  DWORD dwFourCC;
  DWORD dwRGBBitCount;
  DWORD dwRBitMask;
  DWORD dwGBitMask;
  DWORD dwBBitMask;
  DWORD dwABitMask;
};
```



## <a name="members"></a><span data-ttu-id="359e0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="359e0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="359e0-108">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="359e0-108">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-109">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-109">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-110">Taille de la structure ; Affectez la valeur 32 (octets).</span><span class="sxs-lookup"><span data-stu-id="359e0-110">Structure size; set to 32 (bytes).</span></span>

</dd> <dt>

<span data-ttu-id="359e0-111">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="359e0-111">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-112">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-112">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-113">Valeurs qui indiquent le type de données dans la surface.</span><span class="sxs-lookup"><span data-stu-id="359e0-113">Values which indicate what type of data is in the surface.</span></span>



| <span data-ttu-id="359e0-114">Indicateur</span><span class="sxs-lookup"><span data-stu-id="359e0-114">Flag</span></span>              | <span data-ttu-id="359e0-115">Description</span><span class="sxs-lookup"><span data-stu-id="359e0-115">Description</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="359e0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="359e0-116">Value</span></span>   |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|
| <span data-ttu-id="359e0-117">DDPF \_ ALPHAPIXELS</span><span class="sxs-lookup"><span data-stu-id="359e0-117">DDPF\_ALPHAPIXELS</span></span> | <span data-ttu-id="359e0-118">La texture contient des données alpha ; **dwRGBAlphaBitMask** contient des données valides.</span><span class="sxs-lookup"><span data-stu-id="359e0-118">Texture contains alpha data; **dwRGBAlphaBitMask** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="359e0-119">0x1</span><span class="sxs-lookup"><span data-stu-id="359e0-119">0x1</span></span>     |
| <span data-ttu-id="359e0-120">DDPF \_ alpha</span><span class="sxs-lookup"><span data-stu-id="359e0-120">DDPF\_ALPHA</span></span>       | <span data-ttu-id="359e0-121">Utilisé dans certains fichiers DDS plus anciens pour les données non compressées du canal alpha (dwRGBBitCount contient le canal alpha bitCount ; dwABitMask contient des données valides)</span><span class="sxs-lookup"><span data-stu-id="359e0-121">Used in some older DDS files for alpha channel only uncompressed data (dwRGBBitCount contains the alpha channel bitcount; dwABitMask contains valid data)</span></span>                                                                                  | <span data-ttu-id="359e0-122">0x2</span><span class="sxs-lookup"><span data-stu-id="359e0-122">0x2</span></span>     |
| <span data-ttu-id="359e0-123">DDPF \_ FourCC</span><span class="sxs-lookup"><span data-stu-id="359e0-123">DDPF\_FOURCC</span></span>      | <span data-ttu-id="359e0-124">La texture contient des données RVB compressées ; **dwFourCC** contient des données valides.</span><span class="sxs-lookup"><span data-stu-id="359e0-124">Texture contains compressed RGB data; **dwFourCC** contains valid data.</span></span>                                                                                                                                                                    | <span data-ttu-id="359e0-125">0x4</span><span class="sxs-lookup"><span data-stu-id="359e0-125">0x4</span></span>     |
| <span data-ttu-id="359e0-126">DDPF \_ RGB</span><span class="sxs-lookup"><span data-stu-id="359e0-126">DDPF\_RGB</span></span>         | <span data-ttu-id="359e0-127">La texture contient des données RVB non compressées ; **dwRGBBitCount** et les masques RGB (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contiennent des données valides.</span><span class="sxs-lookup"><span data-stu-id="359e0-127">Texture contains uncompressed RGB data; **dwRGBBitCount** and the RGB masks (**dwRBitMask**, **dwGBitMask**, **dwBBitMask**) contain valid data.</span></span>                                                                                           | <span data-ttu-id="359e0-128">0x40</span><span class="sxs-lookup"><span data-stu-id="359e0-128">0x40</span></span>    |
| <span data-ttu-id="359e0-129">DDPF \_ YUV</span><span class="sxs-lookup"><span data-stu-id="359e0-129">DDPF\_YUV</span></span>         | <span data-ttu-id="359e0-130">Utilisé dans certains fichiers DDS plus anciens pour les données non compressées YUV (dwRGBBitCount contient le nombre de bits YUV ; dwRBitMask contient le masque Y, dwGBitMask contient le masque U, dwBBitMask contient le masque V)</span><span class="sxs-lookup"><span data-stu-id="359e0-130">Used in some older DDS files for YUV uncompressed data (dwRGBBitCount contains the YUV bit count; dwRBitMask contains the Y mask, dwGBitMask contains the U mask, dwBBitMask contains the V mask)</span></span>                                          | <span data-ttu-id="359e0-131">0x200</span><span class="sxs-lookup"><span data-stu-id="359e0-131">0x200</span></span>   |
| <span data-ttu-id="359e0-132">\_luminance DDPF</span><span class="sxs-lookup"><span data-stu-id="359e0-132">DDPF\_LUMINANCE</span></span>   | <span data-ttu-id="359e0-133">Utilisé dans certains fichiers DDS plus anciens pour les données non compressées de couleur de canal unique (dwRGBBitCount contient le nombre de bits de canal luminance ; dwRBitMask contient le masque de canal).</span><span class="sxs-lookup"><span data-stu-id="359e0-133">Used in some older DDS files for single channel color uncompressed data (dwRGBBitCount contains the luminance channel bit count; dwRBitMask contains the channel mask).</span></span> <span data-ttu-id="359e0-134">Peut être combiné avec DDPF \_ ALPHAPIXELS pour un fichier DDS à deux canaux.</span><span class="sxs-lookup"><span data-stu-id="359e0-134">Can be combined with DDPF\_ALPHAPIXELS for a two channel DDS file.</span></span> | <span data-ttu-id="359e0-135">0x20000</span><span class="sxs-lookup"><span data-stu-id="359e0-135">0x20000</span></span> |



 

</dd> <dt>

<span data-ttu-id="359e0-136">**dwFourCC**</span><span class="sxs-lookup"><span data-stu-id="359e0-136">**dwFourCC**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-137">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-137">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-138">Codes à quatre caractères pour spécifier des formats compressés ou personnalisés.</span><span class="sxs-lookup"><span data-stu-id="359e0-138">Four-character codes for specifying compressed or custom formats.</span></span> <span data-ttu-id="359e0-139">Les valeurs possibles sont les suivantes : *DXT1*, *DXT2*, *DXT3*, *DXT4* ou *DXT5*.</span><span class="sxs-lookup"><span data-stu-id="359e0-139">Possible values include: *DXT1*, *DXT2*, *DXT3*, *DXT4*, or *DXT5*.</span></span> <span data-ttu-id="359e0-140">Un FourCC de facilement indique prescense de l’en [**-tête DDS \_ \_ DXT10**](dds-header-dxt10.md) en-tête étendu, et le membre dxgiFormat de cette structure indique le format réel.</span><span class="sxs-lookup"><span data-stu-id="359e0-140">A FourCC of DX10 indicates the prescense of the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extended header, and the dxgiFormat member of that structure indicates the true format.</span></span> <span data-ttu-id="359e0-141">Lorsque vous utilisez un code à quatre caractères, dwFlags doit inclure *DDPF \_ FourCC*.</span><span class="sxs-lookup"><span data-stu-id="359e0-141">When using a four-character code, dwFlags must include *DDPF\_FOURCC*.</span></span>

</dd> <dt>

<span data-ttu-id="359e0-142">**dwRGBBitCount**</span><span class="sxs-lookup"><span data-stu-id="359e0-142">**dwRGBBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-143">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-143">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-144">Nombre de bits dans un format RVB (éventuellement, y compris alpha).</span><span class="sxs-lookup"><span data-stu-id="359e0-144">Number of bits in an RGB (possibly including alpha) format.</span></span> <span data-ttu-id="359e0-145">Valide lorsque **dwFlags** comprend *DDPF \_ RGB*, *DDPF \_ luminance* ou *DDPF \_ YUV*.</span><span class="sxs-lookup"><span data-stu-id="359e0-145">Valid when **dwFlags** includes *DDPF\_RGB*, *DDPF\_LUMINANCE*, or *DDPF\_YUV*.</span></span>

</dd> <dt>

<span data-ttu-id="359e0-146">**dwRBitMask**</span><span class="sxs-lookup"><span data-stu-id="359e0-146">**dwRBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-147">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-147">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-148">Masque rouge (ou lumiannce ou Y) pour la lecture des données de couleur.</span><span class="sxs-lookup"><span data-stu-id="359e0-148">Red (or lumiannce or Y) mask for reading color data.</span></span> <span data-ttu-id="359e0-149">Par exemple, étant donné le format A8R8G8B8, le masque rouge est 0x00FF0000.</span><span class="sxs-lookup"><span data-stu-id="359e0-149">For instance, given the A8R8G8B8 format, the red mask would be 0x00ff0000.</span></span>

</dd> <dt>

<span data-ttu-id="359e0-150">**dwGBitMask**</span><span class="sxs-lookup"><span data-stu-id="359e0-150">**dwGBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-151">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-151">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-152">Masque vert (ou U) pour la lecture des données de couleur.</span><span class="sxs-lookup"><span data-stu-id="359e0-152">Green (or U) mask for reading color data.</span></span> <span data-ttu-id="359e0-153">Par exemple, étant donné le format A8R8G8B8, le masque vert est 0x0000ff00.</span><span class="sxs-lookup"><span data-stu-id="359e0-153">For instance, given the A8R8G8B8 format, the green mask would be 0x0000ff00.</span></span>

</dd> <dt>

<span data-ttu-id="359e0-154">**dwBBitMask**</span><span class="sxs-lookup"><span data-stu-id="359e0-154">**dwBBitMask**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-155">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-155">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-156">Masque bleu (ou V) pour la lecture des données de couleur.</span><span class="sxs-lookup"><span data-stu-id="359e0-156">Blue (or V) mask for reading color data.</span></span> <span data-ttu-id="359e0-157">Par exemple, étant donné le format A8R8G8B8, le masque bleu est 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="359e0-157">For instance, given the A8R8G8B8 format, the blue mask would be 0x000000ff.</span></span>

</dd> <dt>

<span data-ttu-id="359e0-158">**dwABitMask**</span><span class="sxs-lookup"><span data-stu-id="359e0-158">**dwABitMask**</span></span>
</dt> <dd>

<span data-ttu-id="359e0-159">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="359e0-159">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="359e0-160">Masque Alpha pour la lecture des données alpha.</span><span class="sxs-lookup"><span data-stu-id="359e0-160">Alpha mask for reading alpha data.</span></span> <span data-ttu-id="359e0-161">dwFlags doit inclure *DDPF \_ ALPHAPIXELS* ou *DDPF \_ alpha*.</span><span class="sxs-lookup"><span data-stu-id="359e0-161">dwFlags must include *DDPF\_ALPHAPIXELS* or *DDPF\_ALPHA*.</span></span> <span data-ttu-id="359e0-162">Par exemple, étant donné le format A8R8G8B8, le masque Alpha est 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="359e0-162">For instance, given the A8R8G8B8 format, the alpha mask would be 0xff000000.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="359e0-163">Notes</span><span class="sxs-lookup"><span data-stu-id="359e0-163">Remarks</span></span>

<span data-ttu-id="359e0-164">Pour stocker des formats DXGI tels que des données à virgule flottante, utilisez un **dwFlags** de DDPF \_ FourCC et définissez **dwFourCC** sur’d', 'X', ' 1 ', ' 0 '.</span><span class="sxs-lookup"><span data-stu-id="359e0-164">To store DXGI formats such as floating-point data, use a **dwFlags** of DDPF\_FOURCC and set **dwFourCC** to 'D','X','1','0'.</span></span> <span data-ttu-id="359e0-165">Utilisez l’en-tête d’extension DXT10 de l' [**\_ en-tête \_ DDS**](dds-header-dxt10.md) pour stocker le format dxgi dans le membre **dxgiFormat** .</span><span class="sxs-lookup"><span data-stu-id="359e0-165">Use the [**DDS\_HEADER\_DXT10**](dds-header-dxt10.md) extension header to store the DXGI format in the **dxgiFormat** member.</span></span>

<span data-ttu-id="359e0-166">Notez qu’il existe des variantes de fichiers DDS non standard pour lesquelles **dwFlags** a DDPF \_ FourCC et la valeur **dwFourCC** est directement définie sur une valeur d' \_ énumération de format D3DFORMAT ou DXGI.</span><span class="sxs-lookup"><span data-stu-id="359e0-166">Note that there are non-standard variants of DDS files where **dwFlags** has DDPF\_FOURCC and the **dwFourCC** value is set directly to a D3DFORMAT or DXGI\_FORMAT enumeration value.</span></span> <span data-ttu-id="359e0-167">Il n’est pas possible de lever l’ambiguïté entre les valeurs de format D3DFORMAT et DXGI \_ à l’aide de ce schéma non standard. par conséquent, l’en-tête d’extension facilement est recommandé à la place.</span><span class="sxs-lookup"><span data-stu-id="359e0-167">It is not possible to disambiguate the D3DFORMAT versus DXGI\_FORMAT values using this non-standard scheme, so the DX10 extension header is recommended instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="359e0-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="359e0-168">Requirements</span></span>



| <span data-ttu-id="359e0-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="359e0-169">Requirement</span></span> | <span data-ttu-id="359e0-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="359e0-170">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="359e0-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="359e0-171">Header</span></span><br/> | <dl> <span data-ttu-id="359e0-172"><dt>DDS. h</dt></span><span class="sxs-lookup"><span data-stu-id="359e0-172"><dt>Dds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="359e0-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="359e0-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="359e0-174">Référence pour DDS</span><span class="sxs-lookup"><span data-stu-id="359e0-174">Reference for DDS</span></span>](dx-graphics-dds-reference.md)
</dt> </dl>

 

