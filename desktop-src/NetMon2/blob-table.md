---
description: Contient un tableau d’objets BLOB.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Structure de BLOB_TABLE (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202731"
---
# <a name="blob_table-structure"></a><span data-ttu-id="f5ace-103">Structure de table d’objets BLOB \_</span><span class="sxs-lookup"><span data-stu-id="f5ace-103">BLOB\_TABLE structure</span></span>

<span data-ttu-id="f5ace-104">La structure de la **\_ table d’objets BLOB** contient un tableau d’objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5ace-104">The **BLOB\_TABLE** structure contains an array of BLOBs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ace-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5ace-105">Syntax</span></span>


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a><span data-ttu-id="f5ace-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f5ace-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5ace-107">**dwNumBlobs**</span><span class="sxs-lookup"><span data-stu-id="f5ace-107">**dwNumBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="f5ace-108">Indicateur que de nombreux objets BLOB suivent.</span><span class="sxs-lookup"><span data-stu-id="f5ace-108">Indicator that many BLOBs follow.</span></span>

</dd> <dt>

<span data-ttu-id="f5ace-109">**hBlobs**</span><span class="sxs-lookup"><span data-stu-id="f5ace-109">**hBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="f5ace-110">Handle vers le tableau d’objets BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5ace-110">Handle to the BLOB array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5ace-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5ace-111">Requirements</span></span>



| <span data-ttu-id="f5ace-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5ace-112">Requirement</span></span> | <span data-ttu-id="f5ace-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5ace-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ace-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ace-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ace-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5ace-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f5ace-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5ace-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ace-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5ace-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f5ace-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5ace-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ace-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ace-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




