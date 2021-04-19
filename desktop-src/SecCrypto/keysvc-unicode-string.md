---
description: La \_ \_ structure de chaîne Unicode KEYSVC définit une chaîne Unicode et une longueur maximale pour la chaîne. Cette structure est utilisée par la fonction RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Structure KEYSVC_UNICODE_STRING (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531757"
---
# <a name="keysvc_unicode_string-structure"></a><span data-ttu-id="c3c31-104">KEYSVC \_ \_ structure de chaîne Unicode</span><span class="sxs-lookup"><span data-stu-id="c3c31-104">KEYSVC\_UNICODE\_STRING structure</span></span>

<span data-ttu-id="c3c31-105">La structure de **\_ \_ chaîne Unicode KEYSVC** définit une chaîne [*Unicode*](../secgloss/u-gly.md) et une longueur maximale pour la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c3c31-105">The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](../secgloss/u-gly.md) string and a maximum length for the string.</span></span> <span data-ttu-id="c3c31-106">Cette structure est utilisée par la fonction [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="c3c31-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c31-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3c31-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a><span data-ttu-id="c3c31-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c3c31-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3c31-109">**Durée**</span><span class="sxs-lookup"><span data-stu-id="c3c31-109">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="c3c31-110">Valeur **UShort** qui spécifie la longueur, en octets, utilisée pour la **mémoire tampon**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-110">A **USHORT** value that specifies the length, in bytes, used for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="c3c31-111">**MaximumLength**</span><span class="sxs-lookup"><span data-stu-id="c3c31-111">**MaximumLength**</span></span>
</dt> <dd>

<span data-ttu-id="c3c31-112">Valeur **UShort** qui spécifie la longueur maximale, en octets, autorisée pour la **mémoire tampon**.</span><span class="sxs-lookup"><span data-stu-id="c3c31-112">A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="c3c31-113">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="c3c31-113">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="c3c31-114">Pointeur vers un **UShort** qui représente la chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="c3c31-114">A pointer to a **USHORT** that represents the Unicode string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3c31-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3c31-115">Requirements</span></span>



| <span data-ttu-id="c3c31-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3c31-116">Requirement</span></span> | <span data-ttu-id="c3c31-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3c31-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c31-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3c31-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c31-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3c31-119">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c3c31-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3c31-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c31-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3c31-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3c31-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3c31-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c31-123"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3c31-123"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3c31-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3c31-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c31-125">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="c3c31-125">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="c3c31-126">**\_objet BLOB KEYSVC**</span><span class="sxs-lookup"><span data-stu-id="c3c31-126">**KEYSVC\_BLOB**</span></span>](keysvc-blob.md)
</dt> </dl>

 

 
