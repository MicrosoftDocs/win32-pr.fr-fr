---
description: Le type de données HCRYPTKEY est utilisé pour représenter les descripteurs des clés de chiffrement.
ms.assetid: d62f1d40-4f42-4684-96d7-de88db67dceb
title: HCRYPTKEY (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56bda14169aa2f4d7c6e502d3444473ea0f00408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530158"
---
# <a name="hcryptkey"></a><span data-ttu-id="2810a-103">HCRYPTKEY</span><span class="sxs-lookup"><span data-stu-id="2810a-103">HCRYPTKEY</span></span>

<span data-ttu-id="2810a-104">Le type de données **HCRYPTKEY** est utilisé pour représenter les descripteurs des [*clés de chiffrement*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2810a-104">The **HCRYPTKEY** data type is used to represent handles to [*cryptographic keys*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2810a-105">Ces descripteurs sont utilisés pour indiquer au module CSP quelle clé est utilisée dans une opération spécifique.</span><span class="sxs-lookup"><span data-stu-id="2810a-105">These handles are used to indicate to the CSP module which key is being used in a specific operation.</span></span> <span data-ttu-id="2810a-106">Le module CSP n’autorise pas l’accès direct aux valeurs de clé.</span><span class="sxs-lookup"><span data-stu-id="2810a-106">The CSP module does not enable direct access to the key values.</span></span> <span data-ttu-id="2810a-107">Au lieu de cela, l’utilisateur exécute des fonctions à l’aide de la valeur de clé par le biais du handle de clé.</span><span class="sxs-lookup"><span data-stu-id="2810a-107">Instead, the user performs functions by using the key value through the key handle.</span></span>


```C++
typedef ULONG_PTR HCRYPTKEY;
```



## <a name="requirements"></a><span data-ttu-id="2810a-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2810a-108">Requirements</span></span>



| <span data-ttu-id="2810a-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2810a-109">Requirement</span></span> | <span data-ttu-id="2810a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2810a-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2810a-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2810a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="2810a-112">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2810a-112">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2810a-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2810a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="2810a-114">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2810a-114">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2810a-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="2810a-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="2810a-116"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="2810a-116"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
