---
description: Importe une clé dans le fournisseur de protocole du protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: SslImportKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519054"
---
# <a name="sslimportkey-function"></a><span data-ttu-id="2595c-103">SslImportKey fonction)</span><span class="sxs-lookup"><span data-stu-id="2595c-103">SslImportKey function</span></span>

<span data-ttu-id="2595c-104">La fonction **SslImportKey** importe une clé dans le fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="2595c-104">The **SslImportKey** function imports a key into the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="2595c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2595c-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2595c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2595c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2595c-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2595c-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2595c-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="2595c-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="2595c-109">*phKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2595c-109">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2595c-110">Pointeur vers le handle de la [*clé de chiffrement*](/windows/desktop/SecGloss/c-gly) pour recevoir la clé importée.</span><span class="sxs-lookup"><span data-stu-id="2595c-110">A pointer to the handle of the [*cryptographic key*](/windows/desktop/SecGloss/c-gly) to receive the imported key.</span></span>

</dd> <dt>

<span data-ttu-id="2595c-111">*pszBlobType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2595c-111">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2595c-112">Chaîne Unicode terminée par le caractère null qui contient un identificateur spécifiant le type d' [*objet BLOB*](/windows/desktop/SecGloss/b-gly) contenu dans la mémoire tampon *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="2595c-112">A null-terminated Unicode string that contains an identifier that specifies the type of [*BLOB*](/windows/desktop/SecGloss/b-gly) that is contained in the *pbInput* buffer.</span></span> <span data-ttu-id="2595c-113">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2595c-113">This can be one of the following values.</span></span>



| <span data-ttu-id="2595c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2595c-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="2595c-115">Signification</span><span class="sxs-lookup"><span data-stu-id="2595c-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="2595c-116"><dt>**\_ \_ objet BLOB public de BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2595c-116"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="2595c-117">Exportez une [*clé publique*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="2595c-117">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="2595c-118">La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ \_ objet blob de clé**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) de la clé de données BCRYPT immédiatement suivie des données de clé.</span><span class="sxs-lookup"><span data-stu-id="2595c-118">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="2595c-119"><dt>**\_objet BLOB ECCPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2595c-119"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="2595c-120">Exportez une [*clé publique*](/windows/desktop/SecGloss/p-gly)ECC ( [*Elliptic Curve Cryptography*](/windows/desktop/SecGloss/e-gly) ).</span><span class="sxs-lookup"><span data-stu-id="2595c-120">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="2595c-121">La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immédiatement suivie des données de clé.</span><span class="sxs-lookup"><span data-stu-id="2595c-121">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="2595c-122"><dt>**\_ \_ objet blob de clé opaque BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2595c-122"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="2595c-123">Exporter une [*clé symétrique*](/windows/desktop/SecGloss/s-gly) dans un format spécifique à un [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) unique.</span><span class="sxs-lookup"><span data-stu-id="2595c-123">Export a [*symmetric key*](/windows/desktop/SecGloss/s-gly) in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="2595c-124">Les objets BLOB opaques ne sont pas transférables et doivent être importés à l’aide du CSP qui a généré l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="2595c-124">Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="2595c-125"><dt>**\_objet BLOB RSAPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2595c-125"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="2595c-126">Exportez une clé publique [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="2595c-126">Export an [*RSA*](/windows/desktop/SecGloss/r-gly) public key.</span></span> <span data-ttu-id="2595c-127">La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB RSAKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immédiatement suivie des données de clé.</span><span class="sxs-lookup"><span data-stu-id="2595c-127">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="2595c-128">*pbKeyBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2595c-128">*pbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2595c-129">Pointeur vers la mémoire tampon qui contient l' [*objet blob de clé*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="2595c-129">A pointer to the buffer that contains the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span>

</dd> <dt>

<span data-ttu-id="2595c-130">*cbKeyBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2595c-130">*cbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2595c-131">Taille, en octets, de la mémoire tampon *pbKeyBlob* .</span><span class="sxs-lookup"><span data-stu-id="2595c-131">The size, in bytes, of the *pbKeyBlob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2595c-132">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2595c-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2595c-133">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2595c-133">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2595c-134">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2595c-134">Return value</span></span>

<span data-ttu-id="2595c-135">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="2595c-135">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="2595c-136">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2595c-136">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="2595c-137">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="2595c-137">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="2595c-138">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2595c-138">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="2595c-139">Description</span><span class="sxs-lookup"><span data-stu-id="2595c-139">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2595c-140"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="2595c-140"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="2595c-141">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2595c-141">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="2595c-142"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2595c-142"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="2595c-143">Le descripteur *hSslProvider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2595c-143">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="2595c-144"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2595c-144"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="2595c-145">Le paramètre *phKey* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2595c-145">The *phKey* parameter is **NULL**.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="2595c-146">Notes</span><span class="sxs-lookup"><span data-stu-id="2595c-146">Remarks</span></span>

<span data-ttu-id="2595c-147">Vous pouvez utiliser la fonction **SslImportKey** pour importer des clés de session dans le cadre du processus de transfert des clés de session d’un processus à un autre.</span><span class="sxs-lookup"><span data-stu-id="2595c-147">You can use the **SslImportKey** function to import session keys as a part of the process of transferring session keys from one process to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="2595c-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2595c-148">Requirements</span></span>



| <span data-ttu-id="2595c-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2595c-149">Requirement</span></span> | <span data-ttu-id="2595c-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="2595c-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2595c-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2595c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="2595c-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2595c-152">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2595c-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2595c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="2595c-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2595c-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2595c-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="2595c-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="2595c-156"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="2595c-156"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="2595c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="2595c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2595c-158"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2595c-158"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

