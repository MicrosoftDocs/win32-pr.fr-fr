---
description: Représente un handle vers une fonction d’installation d’identificateur d’objet (OID).
ms.assetid: 06492b94-9717-40e0-be96-f97f42ac34af
title: HCRYPTOIDFUNCADDR (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4f083d87234e598e8464491f2968868fa2b3c8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530683"
---
# <a name="hcryptoidfuncaddr"></a><span data-ttu-id="23c2c-103">HCRYPTOIDFUNCADDR</span><span class="sxs-lookup"><span data-stu-id="23c2c-103">HCRYPTOIDFUNCADDR</span></span>

<span data-ttu-id="23c2c-104">Le type de données **HCRYPTOIDFUNCADDR** représente un handle vers une fonction d’installation d' [*identificateur d’objet*](../secgloss/o-gly.md) (OID).</span><span class="sxs-lookup"><span data-stu-id="23c2c-104">The **HCRYPTOIDFUNCADDR** data type represents a handle to an [*object identifier*](../secgloss/o-gly.md) (OID) installable function.</span></span> <span data-ttu-id="23c2c-105">Les fonctions [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)et [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) , ainsi que la structure d' [**\_ \_ \_ informations Prov Store store**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) , utilisent ce type de données.</span><span class="sxs-lookup"><span data-stu-id="23c2c-105">The [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress), [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress), and [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress) functions, and the [**CERT\_STORE\_PROV\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_info) structure use this data type.</span></span>


```C++
typedef void* HCRYPTOIDFUNCADDR;
```



## <a name="requirements"></a><span data-ttu-id="23c2c-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23c2c-106">Requirements</span></span>



| <span data-ttu-id="23c2c-107">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23c2c-107">Requirement</span></span> | <span data-ttu-id="23c2c-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="23c2c-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23c2c-109">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23c2c-109">Minimum supported client</span></span><br/> | <span data-ttu-id="23c2c-110">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23c2c-110">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="23c2c-111">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23c2c-111">Minimum supported server</span></span><br/> | <span data-ttu-id="23c2c-112">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23c2c-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23c2c-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="23c2c-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="23c2c-114"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c2c-114"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
