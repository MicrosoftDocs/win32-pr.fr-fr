---
description: Spécifie la taille de bloc d’octets chiffrés pour le chiffrement de modèle basé sur l’exemple.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: Attribut MFSampleExtension_Encryption_CryptByteBlock (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034298"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a><span data-ttu-id="659a5-103">\_Attribut CryptByteBlock de chiffrement MFSampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="659a5-103">MFSampleExtension\_Encryption\_CryptByteBlock attribute</span></span>

<span data-ttu-id="659a5-104">Spécifie la taille de bloc d’octets chiffrés pour le chiffrement de modèle basé sur l’exemple.</span><span class="sxs-lookup"><span data-stu-id="659a5-104">Specifies the encrypted byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="659a5-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="659a5-105">Data type</span></span>

<span data-ttu-id="659a5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="659a5-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="659a5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="659a5-107">Remarks</span></span>

<span data-ttu-id="659a5-108">Le nombre d’octets clairs (non chiffrés) dans le bloc de mappage de sous-échantillon est spécifié dans l’attribut [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="659a5-108">The number of clear (non-encrypted) bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) attribute.</span></span> <span data-ttu-id="659a5-109">Si l’un de ces attributs n’est pas présent ou a la valeur 0, cela signifie que les exemples de données ne sont pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="659a5-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="659a5-110">L’une ou l’autre des deux valeurs doit être différente de zéro, des valeurs positives ou les deux doivent avoir une valeur égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="659a5-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="659a5-111">Dans les cas où la source est MP4, la valeur est définie en fonction des valeurs du bloc d' \_ \_ octet de \_ chiffrement par défaut dans la zone suivre le chiffrement (« tenc ») dans l’en-tête MP4.</span><span class="sxs-lookup"><span data-stu-id="659a5-111">In cases where the Source is MP4-based, the value is set based off the values of default\_crypt\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="659a5-112">Pour plus d’informations, consultez [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="659a5-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="659a5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="659a5-113">Requirements</span></span>



| <span data-ttu-id="659a5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="659a5-114">Requirement</span></span> | <span data-ttu-id="659a5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="659a5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="659a5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="659a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="659a5-117">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="659a5-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="659a5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="659a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="659a5-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="659a5-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="659a5-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="659a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="659a5-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="659a5-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




