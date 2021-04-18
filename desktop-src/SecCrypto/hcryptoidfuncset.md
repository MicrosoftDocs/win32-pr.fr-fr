---
description: Représente un handle vers un ensemble de fonctions installables d’identificateur d’objet (OID).
ms.assetid: 83b76466-dc55-4269-91a3-17c2e6102126
title: HCRYPTOIDFUNCSET (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 437511de32de97d4fb226d299f224427267381ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526206"
---
# <a name="hcryptoidfuncset"></a><span data-ttu-id="06935-103">HCRYPTOIDFUNCSET</span><span class="sxs-lookup"><span data-stu-id="06935-103">HCRYPTOIDFUNCSET</span></span>

<span data-ttu-id="06935-104">Le type de données **HCRYPTOIDFUNCSET** représente un descripteur d’un ensemble de fonctions d' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) installables.</span><span class="sxs-lookup"><span data-stu-id="06935-104">The **HCRYPTOIDFUNCSET** data type represents a handle to a set of [*object identifier*](../secgloss/o-gly.md) (OID) installable functions.</span></span> <span data-ttu-id="06935-105">Les fonctions [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)et [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) utilisent ce type de données.</span><span class="sxs-lookup"><span data-stu-id="06935-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress), and [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset) functions use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCSET;
```



## <a name="requirements"></a><span data-ttu-id="06935-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06935-106">Requirements</span></span>



| <span data-ttu-id="06935-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06935-107">Requirement</span></span> | <span data-ttu-id="06935-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="06935-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06935-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06935-109">Minimum supported client</span></span><br/> | <span data-ttu-id="06935-110">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06935-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06935-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06935-111">Minimum supported server</span></span><br/> | <span data-ttu-id="06935-112">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06935-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06935-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="06935-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="06935-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="06935-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
