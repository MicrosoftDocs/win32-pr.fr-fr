---
description: Contient un objet BLOB signé.
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: Structure SIGNER_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ebc7d5380438fc6cd28a43136273387c1919713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521171"
---
# <a name="signer_context-structure"></a><span data-ttu-id="fe93f-103">Structure du \_ contexte du signataire</span><span class="sxs-lookup"><span data-stu-id="fe93f-103">SIGNER\_CONTEXT structure</span></span>

<span data-ttu-id="fe93f-104">La structure du **\_ contexte du signataire** contient un [*objet BLOB*](../secgloss/b-gly.md)signé.</span><span class="sxs-lookup"><span data-stu-id="fe93f-104">The **SIGNER\_CONTEXT** structure contains a signed [*BLOB*](../secgloss/b-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="fe93f-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="fe93f-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="fe93f-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe93f-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fe93f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe93f-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a><span data-ttu-id="fe93f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="fe93f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe93f-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="fe93f-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="fe93f-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="fe93f-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe93f-111">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="fe93f-111">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="fe93f-112">Taille, en octets, du membre **pbBlob** .</span><span class="sxs-lookup"><span data-stu-id="fe93f-112">The size, in bytes, of the **pbBlob** member.</span></span>

</dd> <dt>

<span data-ttu-id="fe93f-113">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="fe93f-113">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="fe93f-114">Pointeur vers l’objet BLOB signé.</span><span class="sxs-lookup"><span data-stu-id="fe93f-114">A pointer to the signed BLOB.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe93f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe93f-115">Requirements</span></span>



| <span data-ttu-id="fe93f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe93f-116">Requirement</span></span> | <span data-ttu-id="fe93f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe93f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe93f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe93f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe93f-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe93f-119">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fe93f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe93f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe93f-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe93f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe93f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe93f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe93f-123">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="fe93f-123">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="fe93f-124">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="fe93f-124">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
