---
description: Définit une paire d’algorithmes d’authentification et de chiffrement 802,11 qui peuvent être activés en même temps sur la station 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Structure DOT11_AUTH_CIPHER_PAIR (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544929"
---
# <a name="dot11_auth_cipher_pair-structure"></a><span data-ttu-id="18329-103">\_Structure de \_ paire de chiffrement d’authentification DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="18329-103">DOT11\_AUTH\_CIPHER\_PAIR structure</span></span>

<span data-ttu-id="18329-104">La structure de **\_ \_ \_ paire de chiffrement** d’authentification DOT11 définit une paire d’algorithmes d’authentification et de chiffrement de 802,11 qui peut être activée en même temps sur la station 802,11.</span><span class="sxs-lookup"><span data-stu-id="18329-104">The **DOT11\_AUTH\_CIPHER\_PAIR** structure defines a pair of 802.11 authentication and cipher algorithms that can be enabled at the same time on the 802.11 station.</span></span>

## <a name="syntax"></a><span data-ttu-id="18329-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="18329-105">Syntax</span></span>


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a><span data-ttu-id="18329-106">Membres</span><span class="sxs-lookup"><span data-stu-id="18329-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="18329-107">**AuthAlgoId**</span><span class="sxs-lookup"><span data-stu-id="18329-107">**AuthAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="18329-108">Algorithme d’authentification qui utilise un type énuméré d' [**\_ \_ algorithme**](dot11-auth-algorithm.md) d’authentification DOT11.</span><span class="sxs-lookup"><span data-stu-id="18329-108">An authentication algorithm that uses a [**DOT11\_AUTH\_ALGORITHM**](dot11-auth-algorithm.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="18329-109">**CipherAlgoId**</span><span class="sxs-lookup"><span data-stu-id="18329-109">**CipherAlgoId**</span></span>
</dt> <dd>

<span data-ttu-id="18329-110">Algorithme de chiffrement qui utilise un type énuméré de l' [**\_ \_ algorithme de chiffrement DOT11**](dot11-cipher-algorithm.md) .</span><span class="sxs-lookup"><span data-stu-id="18329-110">A cipher algorithm that uses a [**DOT11\_CIPHER\_ALGORITHM**](dot11-cipher-algorithm.md) enumerated type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18329-111">Notes</span><span class="sxs-lookup"><span data-stu-id="18329-111">Remarks</span></span>

<span data-ttu-id="18329-112">La \_ structure de \_ paire de chiffrement d’authentification DOT11 \_ définit un algorithme d’authentification et de chiffrement qui peut être activé ensemble pour les connexions réseau BSS (Basic Service Set).</span><span class="sxs-lookup"><span data-stu-id="18329-112">The DOT11\_AUTH\_CIPHER\_PAIR structure defines an authentication and cipher algorithm that can be enabled together for basic service set (BSS) network connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="18329-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18329-113">Requirements</span></span>



| <span data-ttu-id="18329-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18329-114">Requirement</span></span> | <span data-ttu-id="18329-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="18329-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18329-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18329-116">Minimum supported client</span></span><br/> | <span data-ttu-id="18329-117">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18329-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="18329-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18329-118">Minimum supported server</span></span><br/> | <span data-ttu-id="18329-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="18329-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="18329-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="18329-120">Redistributable</span></span><br/>          | <span data-ttu-id="18329-121">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="18329-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="18329-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="18329-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18329-123"><dt>Wlantypes. h (inclure Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18329-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18329-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18329-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18329-125">**\_Algorithme d’authentification DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="18329-125">**DOT11\_AUTH\_ALGORITHM**</span></span>](dot11-auth-algorithm.md)
</dt> <dt>

[<span data-ttu-id="18329-126">**\_Algorithme de chiffrement DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="18329-126">**DOT11\_CIPHER\_ALGORITHM**</span></span>](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




