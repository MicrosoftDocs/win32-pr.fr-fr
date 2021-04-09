---
description: CABINETDLLVERSIONINFO contient les informations de version pour Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: CABINETDLLVERSIONINFO, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861009"
---
# <a name="cabinetdllversioninfo-structure"></a><span data-ttu-id="b75db-103">CABINETDLLVERSIONINFO, structure</span><span class="sxs-lookup"><span data-stu-id="b75db-103">CABINETDLLVERSIONINFO structure</span></span>

<span data-ttu-id="b75db-104">\[Cette structure contient des informations requises uniquement lors de l’utilisation de la fonction **DllGetVersion** , ce qui n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b75db-104">\[This structure contains information required only when using the **DllGetVersion** function, which is not supported.</span></span> <span data-ttu-id="b75db-105">Cette documentation est fournie à titre d’information uniquement.\]</span><span class="sxs-lookup"><span data-stu-id="b75db-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="b75db-106">**CABINETDLLVERSIONINFO** contient les informations de version pour Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="b75db-106">The **CABINETDLLVERSIONINFO** contains the version information for Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b75db-107">Syntax</span></span>


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="b75db-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b75db-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b75db-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="b75db-109">**cbStruct**</span></span>
</dt> <dd>

<span data-ttu-id="b75db-110">Taille de cette structure, en octets.</span><span class="sxs-lookup"><span data-stu-id="b75db-110">The size of this structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b75db-111">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="b75db-111">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="b75db-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b75db-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b75db-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="b75db-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="b75db-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="b75db-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b75db-115">**dwFileVersionMS**</span><span class="sxs-lookup"><span data-stu-id="b75db-115">**dwFileVersionMS**</span></span>
</dt> <dd>

<span data-ttu-id="b75db-116">Contient les bits les plus significatifs des informations sur la version.</span><span class="sxs-lookup"><span data-stu-id="b75db-116">Contains the most significant bits of the version information.</span></span> <span data-ttu-id="b75db-117">Bits 0-15 contient la version mineure et bits 16-31 contient la version principale.</span><span class="sxs-lookup"><span data-stu-id="b75db-117">Bits 0-15 contain the minor version, and bits 16-31 contain the major version.</span></span>

</dd> <dt>

<span data-ttu-id="b75db-118">**dwFileVersionLS**</span><span class="sxs-lookup"><span data-stu-id="b75db-118">**dwFileVersionLS**</span></span>
</dt> <dd>

<span data-ttu-id="b75db-119">Contient les bits les moins significatifs des informations de version.</span><span class="sxs-lookup"><span data-stu-id="b75db-119">Contains the least significant bits of the version information.</span></span> <span data-ttu-id="b75db-120">Bits 0-15 contiennent le numéro de révision, et les bits 16-31 contiennent le numéro de Build.</span><span class="sxs-lookup"><span data-stu-id="b75db-120">Bits 0-15 contain the revision number, and bits 16-31 contain the build number.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b75db-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b75db-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75db-122">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="b75db-122">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 



