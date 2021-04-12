---
description: Représente des informations sur un fichier de code source.
MS-HAID: vspixengine.SourceFileInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: SourceFileInfo, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A5222610-36ED-4F3B-BD95-A4F8611CC557
api_name:
- SourceFileInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3e0528e61e830872a3e3b1c0555e541fc41d9d39
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481992"
---
# <a name="span-idvspixenginesourcefileinfospansourcefileinfo-structure"></a><span data-ttu-id="8ee92-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo, structure</span><span class="sxs-lookup"><span data-stu-id="8ee92-103"><span id="vspixengine.sourcefileinfo"></span>SourceFileInfo structure</span></span>

<span data-ttu-id="8ee92-104">Représente des informations sur un fichier de code source.</span><span class="sxs-lookup"><span data-stu-id="8ee92-104">Represents information about a source code file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ee92-105">Syntax</span></span>


```C++
} SourceFileInfo;
```

## <a name="members"></a><span data-ttu-id="8ee92-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8ee92-106">Members</span></span>

<span data-ttu-id="8ee92-107">**fileName**</span><span class="sxs-lookup"><span data-stu-id="8ee92-107">**fileName**</span></span>  
<span data-ttu-id="8ee92-108">Chaîne COM comtaining le chemin d’accès du fichier source associé.</span><span class="sxs-lookup"><span data-stu-id="8ee92-108">A COM string comtaining the filepath of the associated source file.</span></span>

<span data-ttu-id="8ee92-109">**checksumByteCount**</span><span class="sxs-lookup"><span data-stu-id="8ee92-109">**checksumByteCount**</span></span>  
<span data-ttu-id="8ee92-110">Nombre d’octets dans la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8ee92-110">The number of bytes in the checksum.</span></span> <span data-ttu-id="8ee92-111">Lorsque checkSumAlgorithm est égal à CHECKSUMALGORITHM :: MD5, checkSumByteCount est 16.</span><span class="sxs-lookup"><span data-stu-id="8ee92-111">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::md5, checkSumByteCount is 16.</span></span> <span data-ttu-id="8ee92-112">Lorsque checkSumAlgorithm est égal à CHECKSUMALGORITHM :: SHA1, checkSumByteCount est 20.</span><span class="sxs-lookup"><span data-stu-id="8ee92-112">When checkSumAlgorithm is equal to CHECKSUMALGORITHM::sha1, checkSumByteCount is 20.</span></span>

<span data-ttu-id="8ee92-113">**checkSumAlgorithm**</span><span class="sxs-lookup"><span data-stu-id="8ee92-113">**checkSumAlgorithm**</span></span>  
<span data-ttu-id="8ee92-114">Spécifie l’algorithme utilisé pour générer la somme de contrôle du fichier.</span><span class="sxs-lookup"><span data-stu-id="8ee92-114">Specifies the algorithm used to generate the checksum of the file.</span></span> <span data-ttu-id="8ee92-115">Les algorithmes pris en charge sont MD5 et SHA1.</span><span class="sxs-lookup"><span data-stu-id="8ee92-115">Supported algorithms are MD5 and SHA1.</span></span> <span data-ttu-id="8ee92-116">Pour plus d’informations, consultez l’énumération CHECKSUMALGORITHM.</span><span class="sxs-lookup"><span data-stu-id="8ee92-116">For more information, see the CHECKSUMALGORITHM enum.</span></span>

<span data-ttu-id="8ee92-117">**checkSumFirstPart**</span><span class="sxs-lookup"><span data-stu-id="8ee92-117">**checkSumFirstPart**</span></span>  
<span data-ttu-id="8ee92-118">Première partie de 8 octets de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8ee92-118">The first 8 byte portion of the checksum.</span></span>

<span data-ttu-id="8ee92-119">**checkSumSecondPart**</span><span class="sxs-lookup"><span data-stu-id="8ee92-119">**checkSumSecondPart**</span></span>  
<span data-ttu-id="8ee92-120">Deuxième partie de 8 octets de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8ee92-120">The second 8 byte portion of the checksum.</span></span>

<span data-ttu-id="8ee92-121">**checkSumThirdPart**</span><span class="sxs-lookup"><span data-stu-id="8ee92-121">**checkSumThirdPart**</span></span>  
<span data-ttu-id="8ee92-122">Troisième partie de 8 octets de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8ee92-122">The third 8 byte portion of the checksum.</span></span>

<span data-ttu-id="8ee92-123">**checkSumFourthPart**</span><span class="sxs-lookup"><span data-stu-id="8ee92-123">**checkSumFourthPart**</span></span>  
<span data-ttu-id="8ee92-124">Quatrième partie de 8 octets de la somme de contrôle.</span><span class="sxs-lookup"><span data-stu-id="8ee92-124">The fourth 8 byte portion of the checksum.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee92-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ee92-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8ee92-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ee92-126">Header</span></span></p></td><td><span data-ttu-id="8ee92-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8ee92-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



