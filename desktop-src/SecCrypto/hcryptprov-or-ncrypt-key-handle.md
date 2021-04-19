---
description: Est utilisé comme handle d’un fournisseur de services de chiffrement CryptoAPI (CSP) ou CSP CNG.
ms.assetid: 1ad77adb-5960-4965-bddb-5967b982b034
title: HCRYPTPROV_OR_NCRYPT_KEY_HANDLE (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bbd442b93cdb9ba7479878aa9fcad095b7903af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532142"
---
# <a name="hcryptprov_or_ncrypt_key_handle"></a><span data-ttu-id="3619a-103">\_handle de clé HCRYPTPROV ou \_ NCRYPT \_ \_</span><span class="sxs-lookup"><span data-stu-id="3619a-103">HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE</span></span>

<span data-ttu-id="3619a-104">Le type de données du **\_ handle de clé HCRYPTPROV ou \_ NCRYPT \_ \_** est utilisé comme handle d’un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) CryptoAPI ou d’un CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="3619a-104">The **HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE** data type is used as a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> <span data-ttu-id="3619a-105">Ce handle doit être un handle [**HCRYPTPROV**](hcryptprov.md) qui a été créé à l’aide de la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) ou d’un handle de **\_ \_ handle de clé NCRYPT** créé à l’aide de la fonction [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) .</span><span class="sxs-lookup"><span data-stu-id="3619a-105">This handle must be an [**HCRYPTPROV**](hcryptprov.md) handle that has been created by using the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function or an **NCRYPT\_KEY\_HANDLE** handle that has been created by using the [**NCryptOpenKey**](/windows/win32/api/ncrypt/nf-ncrypt-ncryptopenkey) function.</span></span> <span data-ttu-id="3619a-106">Les nouvelles applications doivent toujours passer le descripteur de **\_ \_ handle de clé NCRYPT** à un CSP CNG.</span><span class="sxs-lookup"><span data-stu-id="3619a-106">New applications should always pass in the **NCRYPT\_KEY\_HANDLE** handle to a CNG CSP.</span></span>


```C++
typedef ULONG_PTR HCRYPTPROV_OR_NCRYPT_KEY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="3619a-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3619a-107">Requirements</span></span>



| <span data-ttu-id="3619a-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3619a-108">Requirement</span></span> | <span data-ttu-id="3619a-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="3619a-109">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3619a-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3619a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="3619a-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3619a-111">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3619a-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3619a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="3619a-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3619a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3619a-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="3619a-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="3619a-115"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="3619a-115"><dt>Wincrypt.h</dt></span></span> </dl> |



 

 
