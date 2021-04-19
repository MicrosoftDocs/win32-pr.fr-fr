---
description: Crée une clé éphémère à utiliser pendant l’authentification qui se produit au cours de la négociation SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: faad9b3b-e476-4e61-b978-bcb517ecaeb7
title: SslCreateEphemeralKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateEphemeralKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452b0166da367bb6b1530f5669e55b7ca909e13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517650"
---
# <a name="sslcreateephemeralkey-function"></a><span data-ttu-id="e5ad4-103">SslCreateEphemeralKey fonction)</span><span class="sxs-lookup"><span data-stu-id="e5ad4-103">SslCreateEphemeralKey function</span></span>

<span data-ttu-id="e5ad4-104">La fonction **SslCreateEphemeralKey** crée une clé éphémère à utiliser pendant l’authentification qui se produit pendant la négociation SSL ( [*protocole SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="e5ad4-104">The **SslCreateEphemeralKey** function creates an ephemeral key for use during the authentication that occurs during the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ad4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5ad4-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateEphemeralKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phEphemeralKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _In_  DWORD              dwKeyBitLen,
  _In_  PBYTE              pbParams,
  _In_  DWORD              cbParams,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e5ad4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5ad4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5ad4-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-109">*phEphemeralKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-109">*phEphemeralKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-110">Handle de la clé éphémère.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-110">The handle of the ephemeral key.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-111">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-112">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="e5ad4-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-113">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-114">L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="e5ad4-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-115">*dwKeyType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-115">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-116">L’une des valeurs d' [**identificateur de type de clé du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="e5ad4-116">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="e5ad4-117">Affectez la valeur zéro à ce paramètre pour les types de clés qui ne sont pas du [*chiffrement à courbe elliptique*](/windows/desktop/SecGloss/e-gly) (ECC).</span><span class="sxs-lookup"><span data-stu-id="e5ad4-117">Set this parameter to zero for key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC).</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-118">*dwKeyBitLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-118">*dwKeyBitLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-119">Longueur, en bits, de la clé.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-119">The length, in bits, of the key.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-120">*pbParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-120">*pbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-121">Pointeur vers une mémoire tampon qui contient les paramètres de la clé qui doit être créée.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-121">A pointer to a buffer to contain parameters for the key that is to be created.</span></span> <span data-ttu-id="e5ad4-122">Si une suite de chiffrement d’algorithme d’échange de clés (dhe) [*Diffie-Hellman (éphémère)*](/windows/desktop/SecGloss/d-gly) n’est pas utilisée, affectez la valeur **null** au paramètre *pbParams* et le paramètre *cbParams* à zéro.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-122">If a [*Diffie-Hellman (ephemeral) key-exchange algorithm*](/windows/desktop/SecGloss/d-gly) (DHE) cipher suite is not used, set the *pbParams* parameter to **NULL** and the *cbParams* parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-123">*cbParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-123">*cbParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-124">Longueur, en octets, des données dans la mémoire tampon *pbParams* .</span><span class="sxs-lookup"><span data-stu-id="e5ad4-124">The length, in bytes, of the data in the *pbParams* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e5ad4-125">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5ad4-126">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5ad4-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5ad4-127">Return value</span></span>

<span data-ttu-id="e5ad4-128">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="e5ad4-129">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-129">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="e5ad4-130">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e5ad4-130">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="e5ad4-131">Description</span><span class="sxs-lookup"><span data-stu-id="e5ad4-131">Description</span></span>                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e5ad4-132"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad4-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="e5ad4-133">La mémoire est insuffisante pour allouer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-133">There is insufficient memory to allocate the buffer.</span></span><br/> |
| <dl> <span data-ttu-id="e5ad4-134"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e5ad4-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="e5ad4-135">Le descripteur *hSslProvider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-135">The *hSslProvider* handle is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="e5ad4-136"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e5ad4-136"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="e5ad4-137">L’un des paramètres fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e5ad4-137">One of the supplied parameters is not valid.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="e5ad4-138">Notes</span><span class="sxs-lookup"><span data-stu-id="e5ad4-138">Remarks</span></span>

<span data-ttu-id="e5ad4-139">Lors de l’utilisation d’une suite de chiffrement DHE, l’implémentation SSL interne transmet les paramètres Server *p* et *g* à la fonction **SslCreateEphemeralKey** dans les paramètres *pbParams* et *cbParams* .</span><span class="sxs-lookup"><span data-stu-id="e5ad4-139">When using a DHE cipher suite, the internal SSL implementation passes server *p* and *g* parameters to the **SslCreateEphemeralKey** function in the *pbParams* and *cbParams* parameters.</span></span>

<span data-ttu-id="e5ad4-140">Le format des données dans la mémoire tampon *pbParams* est le même que celui utilisé lors de la définition de la propriété de [**\_ \_ paramètres bcrypt DH**](cng-property-identifiers.md) , et il commence par une structure d' [**\_ \_ \_ en-tête de paramètre bcrypt DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="e5ad4-140">The format of the data in the *pbParams* buffer is the same as that used when setting the [**BCRYPT\_DH\_PARAMETERS**](cng-property-identifiers.md) property, and it starts with a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ad4-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5ad4-141">Requirements</span></span>



| <span data-ttu-id="e5ad4-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5ad4-142">Requirement</span></span> | <span data-ttu-id="e5ad4-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5ad4-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ad4-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5ad4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e5ad4-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-145">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e5ad4-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5ad4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e5ad4-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5ad4-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e5ad4-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5ad4-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5ad4-149"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad4-149"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e5ad4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ad4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5ad4-151"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5ad4-151"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

