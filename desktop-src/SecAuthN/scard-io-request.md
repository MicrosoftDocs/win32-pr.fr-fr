---
description: La structure des \_ demandes d’e/s en cicatrices \_ commence une structure d’informations de contrôle de protocole.
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: Structure SCARD_IO_REQUEST (Winsmcrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: fe3205311789ee51bb9b96b3b425b735e1fdf887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319105"
---
# <a name="scard_io_request-structure"></a><span data-ttu-id="4da6d-103">Structure de \_ demande d’e/s en cicatrice \_</span><span class="sxs-lookup"><span data-stu-id="4da6d-103">SCARD\_IO\_REQUEST structure</span></span>

<span data-ttu-id="4da6d-104">La structure des **\_ \_ demandes d’e/s en cicatrices** commence une structure d’informations de contrôle de protocole.</span><span class="sxs-lookup"><span data-stu-id="4da6d-104">The **SCARD\_IO\_REQUEST** structure begins a protocol control information structure.</span></span> <span data-ttu-id="4da6d-105">Toutes les informations spécifiques au protocole suivent immédiatement cette structure.</span><span class="sxs-lookup"><span data-stu-id="4da6d-105">Any protocol-specific information then immediately follows this structure.</span></span> <span data-ttu-id="4da6d-106">La longueur totale de la structure doit être alignée avec la taille de mot de l’architecture matérielle sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="4da6d-106">The entire length of the structure must be aligned with the underlying hardware architecture word size.</span></span> <span data-ttu-id="4da6d-107">Par exemple, dans Win32, la longueur de toutes les informations PCI doit être un multiple de quatre octets afin qu’il s’aligne sur une limite de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4da6d-107">For example, in Win32 the length of any PCI information must be a multiple of four bytes so that it aligns on a 32-bit boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da6d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4da6d-108">Syntax</span></span>


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a><span data-ttu-id="4da6d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4da6d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="4da6d-110">**dwProtocol**</span><span class="sxs-lookup"><span data-stu-id="4da6d-110">**dwProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="4da6d-111">Protocole en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4da6d-111">Protocol in use.</span></span>

</dd> <dt>

<span data-ttu-id="4da6d-112">**cbPciLength**</span><span class="sxs-lookup"><span data-stu-id="4da6d-112">**cbPciLength**</span></span>
</dt> <dd>

<span data-ttu-id="4da6d-113">Longueur, en octets, de la structure de **\_ \_ demande d’e/s en cicatrices** plus les informations spécifiques au PCI suivantes.</span><span class="sxs-lookup"><span data-stu-id="4da6d-113">Length, in bytes, of the **SCARD\_IO\_REQUEST** structure plus any following PCI-specific information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4da6d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4da6d-114">Requirements</span></span>



| <span data-ttu-id="4da6d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4da6d-115">Requirement</span></span> | <span data-ttu-id="4da6d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4da6d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4da6d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4da6d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4da6d-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4da6d-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4da6d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4da6d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4da6d-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4da6d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4da6d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="4da6d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da6d-122"><dt>Winsmcrd. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da6d-122"><dt>Winsmcrd.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4da6d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4da6d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4da6d-124">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="4da6d-124">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




