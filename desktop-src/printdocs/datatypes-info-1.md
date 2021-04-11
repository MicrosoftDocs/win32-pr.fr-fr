---
description: La structure DATATYPEs \_ info \_ 1 contient des informations sur le type de données utilisé pour enregistrer un travail d’impression.
ms.assetid: 6169006c-12d4-4608-865c-732f04107f9f
title: Structure DATATYPES_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DATATYPES_INFO_1
- _DATATYPES_INFO_1A
- _DATATYPES_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e7259f6559220697538774fef8d2460318df84c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202819"
---
# <a name="datatypes_info_1-structure"></a><span data-ttu-id="1efc9-103">Structure des informations de type de données \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="1efc9-103">DATATYPES\_INFO\_1 structure</span></span>

<span data-ttu-id="1efc9-104">La structure **DataTypes \_ info \_ 1** contient des informations sur le type de données utilisé pour enregistrer un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1efc9-104">The **DATATYPES\_INFO\_1** structure contains information about the data type used to record a print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="1efc9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1efc9-105">Syntax</span></span>


```C++
typedef struct _DATATYPES_INFO_1 {
  LPTSTR pName;
} DATATYPES_INFO_1, *PDATATYPES_INFO_1;
```



## <a name="members"></a><span data-ttu-id="1efc9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1efc9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1efc9-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="1efc9-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="1efc9-108">Pointeur vers une chaîne se terminant par un caractère null qui identifie le type de données utilisé pour enregistrer un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1efc9-108">Pointer to a null-terminated string that identifies the data type used to record a print job.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1efc9-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1efc9-109">Requirements</span></span>



| <span data-ttu-id="1efc9-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1efc9-110">Requirement</span></span> | <span data-ttu-id="1efc9-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1efc9-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1efc9-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1efc9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1efc9-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1efc9-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1efc9-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1efc9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1efc9-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1efc9-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1efc9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1efc9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1efc9-117"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1efc9-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1efc9-118">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1efc9-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1efc9-119">**\_ DataTypes \_ info \_ 1s** (Unicode) et **\_ DataTypes \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1efc9-119">**\_DATATYPES\_INFO\_1W** (Unicode) and **\_DATATYPES\_INFO\_1A** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="1efc9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1efc9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1efc9-121">Impression</span><span class="sxs-lookup"><span data-stu-id="1efc9-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1efc9-122">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="1efc9-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1efc9-123">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="1efc9-123">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> </dl>

 

 




