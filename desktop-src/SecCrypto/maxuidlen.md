---
description: Constante numérique qui spécifie le nombre maximal de caractères que certains des fournisseurs de services de chiffrement Microsoft utiliseront lors de l’obtention de l’ID utilisateur.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: MAXUIDLEN (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514035"
---
# <a name="maxuidlen"></a><span data-ttu-id="e0811-103">MAXUIDLEN</span><span class="sxs-lookup"><span data-stu-id="e0811-103">MAXUIDLEN</span></span>

<span data-ttu-id="e0811-104">MAXUIDLEN est une constante numérique qui spécifie le nombre maximal de caractères que certains des fournisseurs de services de chiffrement Microsoft utiliseront lors de l’obtention de l’ID utilisateur. MAXUIDLEN est défini dans wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="e0811-104">MAXUIDLEN is a numeric constant that specifies the maximum number of characters that some of the Microsoft cryptographic providers will use when obtaining the user ID.MAXUIDLEN is defined in Wincrypt.h.</span></span>



| <span data-ttu-id="e0811-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="e0811-105">Constant/value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="e0811-106">Description</span><span class="sxs-lookup"><span data-stu-id="e0811-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <span data-ttu-id="e0811-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="e0811-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span></span> </dl> | <span data-ttu-id="e0811-108">Lorsque le paramètre *pszContainer* de la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) a la **valeur null**, certains des fournisseurs de services de chiffrement Microsoft utilisent le nom d’ouverture de session de l’utilisateur actuellement connecté comme nom de conteneur de clé.</span><span class="sxs-lookup"><span data-stu-id="e0811-108">When the *pszContainer* parameter of the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function is **NULL**, some of the Microsoft cryptographic providers use the logon name of the currently logged on user as the key container name.</span></span> <span data-ttu-id="e0811-109">MAXUIDLEN spécifie le nombre maximal de caractères, y compris le caractère **null** de fin, que ces fournisseurs utiliseront pour le nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e0811-109">MAXUIDLEN specifies the maximum number of characters, including the terminating **NULL** character, that these providers will use for the user name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e0811-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0811-110">Requirements</span></span>



| <span data-ttu-id="e0811-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0811-111">Requirement</span></span> | <span data-ttu-id="e0811-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0811-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0811-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0811-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e0811-114">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0811-114">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e0811-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0811-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e0811-116">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0811-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0811-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0811-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0811-118"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0811-118"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0811-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0811-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0811-120">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="e0811-120">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[<span data-ttu-id="e0811-121">**CPAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="e0811-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




