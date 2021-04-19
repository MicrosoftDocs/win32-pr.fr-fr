---
description: La \_ \_ structure d’en-tête brut WIA définit une image au format de données brutes d’un appareil et permet aux applications d’utiliser le format RAW dans les transferts WIA (Windows Image Acquisition).
ms.assetid: c7b50816-d596-4c62-a00e-cd8d6e303e42
title: Structure WIA_RAW_HEADER (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_RAW_HEADER
api_type:
- HeaderDef
api_location:
- Wiadef.h
ms.openlocfilehash: 8da33f0b257168712f1b16fb7f940df5db862d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515037"
---
# <a name="wia_raw_header-structure"></a><span data-ttu-id="e9ea6-103">\_Structure d' \_ en-tête brut WIA</span><span class="sxs-lookup"><span data-stu-id="e9ea6-103">WIA\_RAW\_HEADER structure</span></span>

<span data-ttu-id="e9ea6-104">La structure d' **\_ \_ en-tête brut WIA** définit une image au format de données brutes d’un appareil et permet aux applications d’utiliser le format RAW dans les transferts WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="e9ea6-104">The **WIA\_RAW\_HEADER** structure defines an image in the RAW data format of a device and enables applications to use RAW format in Windows Image Acquisition (WIA) transfers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ea6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9ea6-105">Syntax</span></span>


```C++
typedef struct _WIA_RAW_HEADER {
  DWORD Tag;
  DWORD Version;
  DWORD HeaderSize;
  DWORD XRes;
  DWORD YRes;
  DWORD XExtent;
  DWORD YExtent;
  DWORD BytesPerLine;
  DWORD BitsPerPixel;
  DWORD ChannelsPerPixel;
  DWORD DataType;
  BYTE  BitsPerChannel[8];
  DWORD Compression;
  DWORD PhotometricInterp;
  DWORD LineOrder;
  DWORD RawDataOffset;
  DWORD RawDataSize;
  DWORD PaletteOffset;
  DWORD PaletteSize;
} WIA_RAW_HEADER;
```



## <a name="members"></a><span data-ttu-id="e9ea6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e9ea6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e9ea6-107">**Tag**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-107">**Tag**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-108">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-109">Nom du format.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-109">The name of the format.</span></span> <span data-ttu-id="e9ea6-110">Il doit s’agir du littéral « WRAW » (quatre caractères ASCII sur un seul octet).</span><span class="sxs-lookup"><span data-stu-id="e9ea6-110">This must be the literal 'WRAW' (four single byte ASCII characters).</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-111">**Version**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-111">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-112">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-112">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-113">Version du format brut.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-113">The version of the RAW format.</span></span> <span data-ttu-id="e9ea6-114">Utilisez toujours 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-114">Always use 0x00010000.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-115">**HeaderSize**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-115">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-116">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-117">Nombre total d’octets valides dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-117">The total valid bytes in the header.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-118">**XRes**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-118">**XRes**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-119">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-119">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-120">La résolution horizontale en points par pouce.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-120">The horizontal resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-121">**YRes**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-121">**YRes**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-122">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-123">La résolution verticale en points par pouce.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-123">The vertical resolution in dots per inch.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-124">**XExtent**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-124">**XExtent**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-125">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-125">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-126">Largeur de l’image en pixels.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-126">The width of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-127">**YExtent**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-127">**YExtent**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-128">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-128">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-129">Hauteur de l’image en pixels.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-129">The height of the image in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-130">**BytesPerLine**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-130">**BytesPerLine**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-131">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-132">Nombre d’octets dans une ligne d’une image non compressée.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-132">The number of bytes in a line of an uncompressed image.</span></span> <span data-ttu-id="e9ea6-133">Utilisez 0 lorsque les données sont compressées pour signaler que le nombre d’octets par ligne est inconnu.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-133">Use 0 when the data is compressed to signal that the number of bytes per line is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-134">**BitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-134">**BitsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-135">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-135">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-136">Nombre total de bits par pixel pour tous les canaux du pixel.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-136">The total number of bits per pixel for all the pixel's channels.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-137">**ChannelsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-137">**ChannelsPerPixel**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-138">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-139">Nombre de canaux de couleur dans un pixel.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-139">The number of color channels in a pixel.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-140">**DataType**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-140">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-141">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-141">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-142">\_ \_ Type de données WIA de la loi WIA de l’image.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-142">The WIA\_IPA\_DATATYPE of the image.</span></span> <span data-ttu-id="e9ea6-143">Étant donné \_ que \_ le format WIA WIA est défini sur WiaImgFmt \_ RAW, il s’agit d’une liste de valeurs autorisées que l’application choisit.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-143">Since WIA\_IPA\_FORMAT is set to WiaImgFmt\_RAW, this is a list of allowed values from which the application picks.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-144">**BitsPerChannel \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-144">**BitsPerChannel\[8\]**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-145">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-145">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-146">Nombre de bits dans un canal, jusqu’à un maximum de 8.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-146">The number of bits in a channel, up to a maximum of 8.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-147">**Compression**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-147">**Compression**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-148">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-148">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-149">\_ \_ Valeur de compression WIA de la Loi d’images qui spécifie le type de compression utilisé, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-149">A WIA\_IPA\_COMPRESSION value specifying the type of compression used, if any.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-150">**PhotometricInterp**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-150">**PhotometricInterp**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-151">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-151">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-152">\_ \_ Valeur interp photométrique WIA \_ de la loi WIA spécifiant l’interprétation photométrique de l’image.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-152">A WIA\_IPA\_PHOTOMETRIC\_INTERP value specifying the photometric interpretation of the image.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-153">**LineOrder**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-153">**LineOrder**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-154">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-154">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-155">Valeur représentant l’ordre des lignes de l’image.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-155">A value representing the image line order.</span></span> <span data-ttu-id="e9ea6-156">Il s’agit toujours de l' \_ ordre des lignes WIA \_ \_ \_ de haut en bas ou de l’ordre des \_ \_ lignes WIA \_ \_ \_ de bas en \_ haut.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-156">This is always either WIA\_LINE\_ORDER\_TOP\_TO\_BOTTOM or WIA\_LINE\_ORDER\_BOTTOM\_TO\_TOP.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-157">**RawDataOffset**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-157">**RawDataOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-158">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-158">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-159">Position des données d’image brutes en octets, à partir de la position à laquelle l’en-tête se termine ou de la position à laquelle la palette se termine.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-159">The position of the raw image data in bytes, starting from position where the header ends or the position where the palette ends.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-160">**RawDataSize**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-160">**RawDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-161">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-161">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-162">Taille, en octets, des données d’image brutes.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-162">The size, in bytes, of the raw image data.</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-163">**PaletteOffset**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-163">**PaletteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-164">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-165">Position de la palette en octets, à partir de la position à laquelle l’en-tête se termine ou de la position à laquelle les données se terminent.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-165">The position of the palette in bytes, starting from the position where the header ends or the position where the data ends.</span></span> <span data-ttu-id="e9ea6-166">(Cette valeur est 0, s’il n’y a aucune palette.)</span><span class="sxs-lookup"><span data-stu-id="e9ea6-166">(This value is 0, if there is no palette.)</span></span>

</dd> <dt>

<span data-ttu-id="e9ea6-167">**PaletteSize**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-167">**PaletteSize**</span></span>
</dt> <dd>

<span data-ttu-id="e9ea6-168">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e9ea6-168">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e9ea6-169">Taille, en octets, de la table de palettes.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-169">The size, in bytes, of the palette table.</span></span> <span data-ttu-id="e9ea6-170">(Il s’agit de 0, s’il n’y a aucune palette.)</span><span class="sxs-lookup"><span data-stu-id="e9ea6-170">(This is 0, if there is no palette.)</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ea6-171">Notes</span><span class="sxs-lookup"><span data-stu-id="e9ea6-171">Remarks</span></span>

<span data-ttu-id="e9ea6-172">Étant donné qu’il ne s’agit pas d’un format de fichier, utilisez une chaîne vide pour la propriété d’extension de fichier WIA de la \_ Loi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e9ea6-172">Because this is not a file format, use an empty string for the WIA\_IPA\_FILE\_EXTENSION property.</span></span>

<span data-ttu-id="e9ea6-173">La palette et les données peuvent être dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-173">The palette and the data can come in either order.</span></span>

<span data-ttu-id="e9ea6-174">**RawDataSize** n’inclut ni l’en-tête ni la palette.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-174">**RawDataSize** does not include either the header or the palette.</span></span> <span data-ttu-id="e9ea6-175">Utilisez ce champ pour vérifier que le transfert de l’image a réussi.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-175">Use this field to verify that the transfer of the image has been successful.</span></span>

<span data-ttu-id="e9ea6-176">**PaletteSize** est le nombre d’octets, et non le nombre d’entrées dans la palette.</span><span class="sxs-lookup"><span data-stu-id="e9ea6-176">**PaletteSize** is bytes, not the number of entries in the palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ea6-177">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9ea6-177">Requirements</span></span>



| <span data-ttu-id="e9ea6-178">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9ea6-178">Requirement</span></span> | <span data-ttu-id="e9ea6-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9ea6-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ea6-180">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9ea6-180">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ea6-181">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9ea6-181">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e9ea6-182">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9ea6-182">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ea6-183">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9ea6-183">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e9ea6-184">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9ea6-184">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ea6-185"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ea6-185"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




