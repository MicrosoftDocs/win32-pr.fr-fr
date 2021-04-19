---
description: La structure DIBDATA contient des informations sur une image bitmap indépendante du périphérique (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: DIBDATA, structure (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543263"
---
# <a name="dibdata-structure"></a><span data-ttu-id="5d7d8-103">DIBDATA, structure</span><span class="sxs-lookup"><span data-stu-id="5d7d8-103">DIBDATA structure</span></span>

<span data-ttu-id="5d7d8-104">La `DIBDATA` structure contient des informations sur une image bitmap indépendante du périphérique (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="5d7d8-104">The `DIBDATA` structure contains information about a GDI device-independent bitmap (DIB).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7d8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d7d8-105">Syntax</span></span>


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a><span data-ttu-id="5d7d8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5d7d8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d7d8-107">**PaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="5d7d8-107">**PaletteVersion**</span></span>
</dt> <dd>

<span data-ttu-id="5d7d8-108">Ce membre doit être incrémenté à chaque modification de la palette.</span><span class="sxs-lookup"><span data-stu-id="5d7d8-108">This member should be incremented whenever the palette changes.</span></span>

</dd> <dt>

<span data-ttu-id="5d7d8-109">**DibSection**</span><span class="sxs-lookup"><span data-stu-id="5d7d8-109">**DibSection**</span></span>
</dt> <dd>

<span data-ttu-id="5d7d8-110">Structure **DIBSECTION** qui contient des informations sur le dib.</span><span class="sxs-lookup"><span data-stu-id="5d7d8-110">**DIBSECTION** structure that contains information about the DIB.</span></span> <span data-ttu-id="5d7d8-111">Pour plus d’informations, consultez la documentation GDI.</span><span class="sxs-lookup"><span data-stu-id="5d7d8-111">See the GDI documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="5d7d8-112">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="5d7d8-112">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="5d7d8-113">Handle de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="5d7d8-113">Handle to the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="5d7d8-114">**hMapping**</span><span class="sxs-lookup"><span data-stu-id="5d7d8-114">**hMapping**</span></span>
</dt> <dd>

<span data-ttu-id="5d7d8-115">Handle vers un objet de mappage de fichiers utilisé pour partager la mémoire entre GDI et un objet [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="5d7d8-115">Handle to a file-mapping object that is used to share memory between GDI and a [**CImageSample**](cimagesample.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="5d7d8-116">**pBase**</span><span class="sxs-lookup"><span data-stu-id="5d7d8-116">**pBase**</span></span>
</dt> <dd>

<span data-ttu-id="5d7d8-117">Adresse de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="5d7d8-117">Address of the bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d7d8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d7d8-118">Requirements</span></span>



| <span data-ttu-id="5d7d8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d7d8-119">Requirement</span></span> | <span data-ttu-id="5d7d8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d7d8-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d7d8-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d7d8-121">Header</span></span><br/> | <dl> <span data-ttu-id="5d7d8-122"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d7d8-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl> |



 

 




