---
description: Retourne un handle pour le hachage de négociation.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: SslHashHandshake, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952717"
---
# <a name="sslhashhandshake-function"></a><span data-ttu-id="e4af8-103">SslHashHandshake fonction)</span><span class="sxs-lookup"><span data-stu-id="e4af8-103">SslHashHandshake function</span></span>

<span data-ttu-id="e4af8-104">La fonction **SslHashHandshake** retourne un handle vers le hachage de négociation.</span><span class="sxs-lookup"><span data-stu-id="e4af8-104">The **SslHashHandshake** function returns a handle to the handshake hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4af8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4af8-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e4af8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4af8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4af8-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4af8-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4af8-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="e4af8-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="e4af8-109">*hHandshakeHash* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e4af8-109">*hHandshakeHash* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4af8-110">Handle de l’objet de hachage.</span><span class="sxs-lookup"><span data-stu-id="e4af8-110">The handle to the hash object.</span></span>

</dd> <dt>

<span data-ttu-id="e4af8-111">*pbInput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e4af8-111">*pbInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4af8-112">Adresse d’une mémoire tampon qui contient les données à hacher.</span><span class="sxs-lookup"><span data-stu-id="e4af8-112">The address of a buffer that contains the data to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="e4af8-113">*cbInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4af8-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4af8-114">Taille, en octets, de la mémoire tampon *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="e4af8-114">The size, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e4af8-115">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4af8-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4af8-116">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="e4af8-116">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4af8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4af8-117">Return value</span></span>

<span data-ttu-id="e4af8-118">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e4af8-118">If the function succeeds, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4af8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e4af8-119">Remarks</span></span>

<span data-ttu-id="e4af8-120">La fonction **SslHashHandshake** est l’une des trois fonctions utilisées pour générer un hachage à utiliser pendant la négociation SSL.</span><span class="sxs-lookup"><span data-stu-id="e4af8-120">The **SslHashHandshake** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="e4af8-121">La fonction [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) est appelée pour obtenir un handle de hachage.</span><span class="sxs-lookup"><span data-stu-id="e4af8-121">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="e4af8-122">La fonction **SslHashHandshake** est appelée un nombre quelconque de fois avec le handle de hachage pour ajouter des données au hachage.</span><span class="sxs-lookup"><span data-stu-id="e4af8-122">The **SslHashHandshake** function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="e4af8-123">La fonction [**SslComputeFinishedHash**](sslcomputefinishedhash.md) est appelée avec le descripteur de hachage pour obtenir le condensé des données hachées.</span><span class="sxs-lookup"><span data-stu-id="e4af8-123">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4af8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4af8-124">Requirements</span></span>



| <span data-ttu-id="e4af8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4af8-125">Requirement</span></span> | <span data-ttu-id="e4af8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4af8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4af8-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4af8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4af8-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4af8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e4af8-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4af8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4af8-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4af8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e4af8-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4af8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4af8-132"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4af8-132"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e4af8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e4af8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4af8-134"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4af8-134"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

