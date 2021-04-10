---
description: Le type de données HCRYPTHASH est utilisé pour représenter les descripteurs des objets de hachage.
ms.assetid: 3b872bf0-cf1b-465b-82a2-c6fd154e1125
title: HCRYPTHASH (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a009350ed910627c1e6ec9ae33997ed20c7fec2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867413"
---
# <a name="hcrypthash"></a><span data-ttu-id="0cfd3-103">HCRYPTHASH</span><span class="sxs-lookup"><span data-stu-id="0cfd3-103">HCRYPTHASH</span></span>

<span data-ttu-id="0cfd3-104">Le type de données **HCRYPTHASH** est utilisé pour représenter les descripteurs des [*objets de hachage*](../secgloss/h-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0cfd3-104">The **HCRYPTHASH** data type is used to represent handles to [*hash objects*](../secgloss/h-gly.md).</span></span> <span data-ttu-id="0cfd3-105">Ces handles indiquent au module CSP le hachage utilisé dans une opération particulière.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-105">These handles indicate to the CSP module which hash is being used in a particular operation.</span></span> <span data-ttu-id="0cfd3-106">Le module CSP n’active pas la manipulation directe des valeurs de hachage.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-106">The CSP module does not enable direct manipulation of the hash values.</span></span> <span data-ttu-id="0cfd3-107">Au lieu de cela, l’utilisateur manipule les valeurs de hachage par le biais du handle de hachage.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-107">Instead, the user manipulates the hash values through the hash handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTHASH;
```



## <a name="requirements"></a><span data-ttu-id="0cfd3-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cfd3-108">Requirements</span></span>



| <span data-ttu-id="0cfd3-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cfd3-109">Requirement</span></span> | <span data-ttu-id="0cfd3-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cfd3-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfd3-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfd3-111">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfd3-112">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfd3-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0cfd3-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfd3-113">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfd3-114">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfd3-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cfd3-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cfd3-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cfd3-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfd3-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
