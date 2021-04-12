---
description: Contient une signature de liste de révocation globale (GRL).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: Structure MF_SIGNATURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210365"
---
# <a name="mf_signature-structure"></a><span data-ttu-id="16321-103">\_Structure de signature MF</span><span class="sxs-lookup"><span data-stu-id="16321-103">MF\_SIGNATURE structure</span></span>

<span data-ttu-id="16321-104">Contient une signature de liste de révocation globale (GRL).</span><span class="sxs-lookup"><span data-stu-id="16321-104">Contains a global revocation list (GRL) signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="16321-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16321-105">Syntax</span></span>


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a><span data-ttu-id="16321-106">Membres</span><span class="sxs-lookup"><span data-stu-id="16321-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="16321-107">**dwSignVer**</span><span class="sxs-lookup"><span data-stu-id="16321-107">**dwSignVer**</span></span>
</dt> <dd>

<span data-ttu-id="16321-108">Numéro de version de la signature.</span><span class="sxs-lookup"><span data-stu-id="16321-108">The signature version number.</span></span>

</dd> <dt>

<span data-ttu-id="16321-109">**cbSign**</span><span class="sxs-lookup"><span data-stu-id="16321-109">**cbSign**</span></span>
</dt> <dd>

<span data-ttu-id="16321-110">Taille de la signature en octets.</span><span class="sxs-lookup"><span data-stu-id="16321-110">The size of the signature in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="16321-111">**rgSign**</span><span class="sxs-lookup"><span data-stu-id="16321-111">**rgSign**</span></span>
</dt> <dd>

<span data-ttu-id="16321-112">Tableau d’octets de taille **cbSign** qui contient la signature.</span><span class="sxs-lookup"><span data-stu-id="16321-112">A byte array of size **cbSign** that contains the signature.</span></span> <span data-ttu-id="16321-113">La taille réelle du tableau est supérieure à la taille spécifiée dans la déclaration de la structure.</span><span class="sxs-lookup"><span data-stu-id="16321-113">The actual array size is larger than the size given in the structure declaration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16321-114">Notes</span><span class="sxs-lookup"><span data-stu-id="16321-114">Remarks</span></span>

<span data-ttu-id="16321-115">Cette structure n’est pas déclarée dans un en-tête SDK.</span><span class="sxs-lookup"><span data-stu-id="16321-115">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="16321-116">Pour utiliser cette structure, ajoutez la déclaration indiquée ici à votre code source.</span><span class="sxs-lookup"><span data-stu-id="16321-116">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="16321-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16321-117">Requirements</span></span>



| <span data-ttu-id="16321-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16321-118">Requirement</span></span> | <span data-ttu-id="16321-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="16321-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="16321-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16321-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16321-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16321-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="16321-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16321-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16321-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="16321-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="16321-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16321-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16321-125">Révocation de certificat OPM</span><span class="sxs-lookup"><span data-stu-id="16321-125">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="16321-126">Structures OPM</span><span class="sxs-lookup"><span data-stu-id="16321-126">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




