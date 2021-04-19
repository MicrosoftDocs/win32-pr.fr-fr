---
description: La \_ structure d’objet BLOB KEYSVC définit un objet blob de service de clé. Cette structure est utilisée par la fonction RKeyPFXInstall.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Structure KEYSVC_BLOB (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532309"
---
# <a name="keysvc_blob-structure"></a><span data-ttu-id="b1a03-104">KEYSVC, \_ structure BLOB</span><span class="sxs-lookup"><span data-stu-id="b1a03-104">KEYSVC\_BLOB structure</span></span>

<span data-ttu-id="b1a03-105">La structure d' **\_ objet BLOB KEYSVC** définit un objet blob de service de clé.</span><span class="sxs-lookup"><span data-stu-id="b1a03-105">The **KEYSVC\_BLOB** structure defines a key service BLOB.</span></span> <span data-ttu-id="b1a03-106">Cette structure est utilisée par la fonction [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="b1a03-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a03-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1a03-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a><span data-ttu-id="b1a03-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b1a03-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1a03-109">**libéré**</span><span class="sxs-lookup"><span data-stu-id="b1a03-109">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="b1a03-110">Valeur **ULong** qui spécifie la taille, en octets, de **PB**.</span><span class="sxs-lookup"><span data-stu-id="b1a03-110">A **ULONG** value that specifies the size, in bytes, of **pb**.</span></span>

</dd> <dt>

<span data-ttu-id="b1a03-111">**gérés**</span><span class="sxs-lookup"><span data-stu-id="b1a03-111">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="b1a03-112">Pointeur vers un **octet** qui contient l’objet BLOB, au format [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b1a03-112">A pointer to a **BYTE** that contains the BLOB, in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1a03-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1a03-113">Requirements</span></span>



| <span data-ttu-id="b1a03-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1a03-114">Requirement</span></span> | <span data-ttu-id="b1a03-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1a03-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a03-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1a03-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a03-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1a03-117">None supported</span></span><br/>                                                             |
| <span data-ttu-id="b1a03-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1a03-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a03-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1a03-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1a03-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1a03-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a03-121"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a03-121"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1a03-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1a03-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a03-123">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="b1a03-123">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="b1a03-124">**\_chaîne Unicode \_ KEYSVC**</span><span class="sxs-lookup"><span data-stu-id="b1a03-124">**KEYSVC\_UNICODE\_STRING**</span></span>](keysvc-unicode-string.md)
</dt> </dl>

 

 
