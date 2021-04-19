---
description: La \_ structure d’élément KSMULTIPLE décrit la taille et le nombre de propriétés de longueur variable sur les broches en mode noyau.
ms.assetid: aedbf7bc-393d-4ab5-afcd-d8822b925f07
title: KSMULTIPLE_ITEM, structure (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSMULTIPLE_ITEM
api_type:
- HeaderDef
api_location:
- ks.h
ms.openlocfilehash: 62e26b1aa8804514588e66c1d02e1f0643e97bcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543253"
---
# <a name="ksmultiple_item-structure"></a><span data-ttu-id="68516-103">Structure de l' \_ élément KSMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="68516-103">KSMULTIPLE\_ITEM structure</span></span>

<span data-ttu-id="68516-104">La `KSMULTIPLE_ITEM` structure décrit la taille et le nombre de propriétés de longueur variable sur les broches en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="68516-104">The `KSMULTIPLE_ITEM` structure describes the size and count of variable-length properties on kernel-mode pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="68516-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68516-105">Syntax</span></span>


```C++
typedef struct {
  ULONG Size;
  ULONG Count;
} KSMULTIPLE_ITEM, *PKSMULTIPLE_ITEM;
```



## <a name="members"></a><span data-ttu-id="68516-106">Membres</span><span class="sxs-lookup"><span data-stu-id="68516-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="68516-107">**Taille**</span><span class="sxs-lookup"><span data-stu-id="68516-107">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="68516-108">Taille du bloc de mémoire retourné, en octets.</span><span class="sxs-lookup"><span data-stu-id="68516-108">Size of the returned memory block, in bytes.</span></span> <span data-ttu-id="68516-109">La taille comprend la structure de l' **\_ élément KSMULTIPLE** et les éléments qui le suivent.</span><span class="sxs-lookup"><span data-stu-id="68516-109">The size includes the **KSMULTIPLE\_ITEM** structure and the items that follow it.</span></span>

</dd> <dt>

<span data-ttu-id="68516-110">**Count**</span><span class="sxs-lookup"><span data-stu-id="68516-110">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="68516-111">Spécifie le nombre total d’éléments qui suivent cette structure.</span><span class="sxs-lookup"><span data-stu-id="68516-111">Specifies the total number of items that follow this structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68516-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68516-112">Requirements</span></span>



| <span data-ttu-id="68516-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68516-113">Requirement</span></span> | <span data-ttu-id="68516-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="68516-114">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="68516-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="68516-115">Header</span></span><br/> | <dl> <span data-ttu-id="68516-116"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="68516-116"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68516-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68516-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68516-118">Structures DirectShow</span><span class="sxs-lookup"><span data-stu-id="68516-118">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="68516-119">**IKsPin::KsQueryMediums**</span><span class="sxs-lookup"><span data-stu-id="68516-119">**IKsPin::KsQueryMediums**</span></span>](ikspin-ksquerymediums.md)
</dt> <dt>

[<span data-ttu-id="68516-120">**REGPINMEDIUM**</span><span class="sxs-lookup"><span data-stu-id="68516-120">**REGPINMEDIUM**</span></span>](/windows/desktop/api/strmif/ns-strmif-regpinmedium)
</dt> </dl>

 

 




