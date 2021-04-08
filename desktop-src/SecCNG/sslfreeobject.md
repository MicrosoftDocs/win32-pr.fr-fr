---
description: Libère un objet de clé, de hachage ou de fournisseur.
ms.assetid: 73fa0a08-4654-4515-bdb2-9951936b689a
title: SslFreeObject, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslFreeObject
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e7d10059942080e7794da7e6b87613189dcf9844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864209"
---
# <a name="sslfreeobject-function"></a><span data-ttu-id="02190-103">SslFreeObject fonction)</span><span class="sxs-lookup"><span data-stu-id="02190-103">SslFreeObject function</span></span>

<span data-ttu-id="02190-104">La fonction **SslFreeObject** libère un objet de clé, de hachage ou de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="02190-104">The **SslFreeObject** function frees a key, hash, or provider object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02190-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02190-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslFreeObject(
  _In_ NCRYPT_HANDLE hObject,
  _In_ DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="02190-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02190-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02190-107">*hObject* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02190-107">*hObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02190-108">Handle de l’objet à libérer.</span><span class="sxs-lookup"><span data-stu-id="02190-108">The handle of the object to free.</span></span>

</dd> <dt>

<span data-ttu-id="02190-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02190-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02190-110">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="02190-110">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02190-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02190-111">Return value</span></span>

<span data-ttu-id="02190-112">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="02190-112">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="02190-113">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="02190-113">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="02190-114">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="02190-114">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="02190-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="02190-115">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="02190-116">Description</span><span class="sxs-lookup"><span data-stu-id="02190-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="02190-117"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02190-117"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="02190-118">Un descripteur interne n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="02190-118">An internal handle is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="02190-119"><dt>**État \_ \_Handle 0XC0000008L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02190-119"><dt>**STATUS\_INVALID\_HANDLE**</dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="02190-120">Le handle fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="02190-120">The provided handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02190-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02190-121">Requirements</span></span>



| <span data-ttu-id="02190-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02190-122">Requirement</span></span> | <span data-ttu-id="02190-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="02190-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02190-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02190-124">Minimum supported client</span></span><br/> | <span data-ttu-id="02190-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02190-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="02190-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02190-126">Minimum supported server</span></span><br/> | <span data-ttu-id="02190-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02190-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="02190-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="02190-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="02190-129"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="02190-129"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="02190-130">DLL</span><span class="sxs-lookup"><span data-stu-id="02190-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02190-131"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02190-131"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

 




