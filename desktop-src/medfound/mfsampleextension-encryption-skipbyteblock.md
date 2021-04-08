---
description: Spécifie la taille de bloc d’octets Clear (non chiffrée) pour le chiffrement de modèle basé sur un échantillon.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: Attribut MFSampleExtension_Encryption_SkipByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863970"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a><span data-ttu-id="4a536-103">\_Attribut SkipByteBlock de chiffrement MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="4a536-103">MFSampleExtension\_Encryption\_SkipByteBlock attribute</span></span>

<span data-ttu-id="4a536-104">Spécifie la taille de bloc d’octets Clear (non chiffrée) pour le chiffrement de modèle basé sur un échantillon.</span><span class="sxs-lookup"><span data-stu-id="4a536-104">Specifies the clear (non-encrypted) byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="4a536-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="4a536-105">Data type</span></span>

<span data-ttu-id="4a536-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4a536-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4a536-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4a536-107">Remarks</span></span>

<span data-ttu-id="4a536-108">Le nombre d’octets chiffrés dans le bloc de mappage de sous-échantillon est spécifié dans l’attribut [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="4a536-108">The number of encrypted bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) attribute.</span></span> <span data-ttu-id="4a536-109">Si l’un de ces attributs n’est pas présent ou a la valeur 0, cela signifie que les exemples de données ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="4a536-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="4a536-110">L’une ou l’autre des deux valeurs doit être différente de zéro, des valeurs positives ou les deux doivent avoir une valeur égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="4a536-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="4a536-111">Dans les cas où la source est MP4, la valeur est définie en fonction des valeurs de bloc d' \_ octets ignorés par défaut \_ \_ dans la zone suivre le chiffrement (« tenc ») dans l’en-tête MP4.</span><span class="sxs-lookup"><span data-stu-id="4a536-111">In cases where the Source is MP4-based, the value is set based off the values of default\_skip\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="4a536-112">Pour plus d’informations, consultez [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="4a536-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4a536-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a536-113">Requirements</span></span>



| <span data-ttu-id="4a536-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a536-114">Requirement</span></span> | <span data-ttu-id="4a536-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a536-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a536-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a536-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4a536-117">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a536-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4a536-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a536-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4a536-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a536-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="4a536-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a536-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a536-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a536-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




