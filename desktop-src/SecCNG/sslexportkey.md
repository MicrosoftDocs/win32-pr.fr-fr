---
description: Retourne une clé de session de protocole SSL (Secure Sockets Layer) (SSL) ou une clé éphémère publique dans un objet BLOB sérialisé.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: SslExportKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951676"
---
# <a name="sslexportkey-function"></a><span data-ttu-id="7d231-103">SslExportKey fonction)</span><span class="sxs-lookup"><span data-stu-id="7d231-103">SslExportKey function</span></span>

<span data-ttu-id="7d231-104">La fonction **SslExportKey** retourne une [*clé de session*](/windows/desktop/SecGloss/s-gly) de [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL) ou une clé éphémère publique dans un [*objet BLOB*](/windows/desktop/SecGloss/b-gly)sérialisé.</span><span class="sxs-lookup"><span data-stu-id="7d231-104">The **SslExportKey** function returns an [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) [*session key*](/windows/desktop/SecGloss/s-gly) or public ephemeral key into a serialized [*BLOB*](/windows/desktop/SecGloss/b-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d231-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d231-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7d231-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d231-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d231-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d231-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d231-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="7d231-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="7d231-109">*HKEY* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d231-109">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d231-110">Handle de la clé à exporter.</span><span class="sxs-lookup"><span data-stu-id="7d231-110">The handle of the key to export.</span></span>

<span data-ttu-id="7d231-111">Si vous ne spécifiez pas de clé, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="7d231-111">When you are not specifying a key, set this parameter to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="7d231-112">Un handle *HKEY* est obtenu en appelant la fonction [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="7d231-112">A *hKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="7d231-113">Les handles obtenus à partir de la fonction [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7d231-113">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="7d231-114">*pszBlobType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d231-114">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d231-115">Chaîne Unicode terminée par le caractère null qui contient un identificateur spécifiant le type d’objet BLOB à exporter.</span><span class="sxs-lookup"><span data-stu-id="7d231-115">A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export.</span></span> <span data-ttu-id="7d231-116">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d231-116">This can be one of the following values.</span></span>



| <span data-ttu-id="7d231-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d231-117">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="7d231-118">Signification</span><span class="sxs-lookup"><span data-stu-id="7d231-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="7d231-119"><dt>**\_ \_ objet BLOB public de BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d231-119"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="7d231-120">Exportez une [*clé publique*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="7d231-120">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="7d231-121">La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ \_ objet blob de clé**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) de la clé de données BCRYPT immédiatement suivie des données de clé.</span><span class="sxs-lookup"><span data-stu-id="7d231-121">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="7d231-122"><dt>**\_objet BLOB ECCPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d231-122"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="7d231-123">Exportez une clé publique ECC ( [*Elliptic Curve Cryptography*](/windows/desktop/SecGloss/e-gly) ).</span><span class="sxs-lookup"><span data-stu-id="7d231-123">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) public key.</span></span> <span data-ttu-id="7d231-124">La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immédiatement suivie des données de clé.</span><span class="sxs-lookup"><span data-stu-id="7d231-124">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="7d231-125"><dt>**\_ \_ objet blob de clé opaque BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d231-125"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="7d231-126">Exporter une clé symétrique dans un format spécifique à un [*fournisseur de services de chiffrement*](/windows/desktop/SecGloss/c-gly) (CSP) unique.</span><span class="sxs-lookup"><span data-stu-id="7d231-126">Export a symmetric key in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="7d231-127">Les objets BLOB opaques ne sont pas transférables et doivent être importés à l’aide du même *fournisseur de services de chiffrement* (CSP) qui a généré l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="7d231-127">Opaque BLOBs are not transferable and must be imported by using the same *cryptographic service provider* (CSP) that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="7d231-128"><dt>**\_objet BLOB RSAPUBLIC de BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7d231-128"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="7d231-129">Exportez une clé publique RSA.</span><span class="sxs-lookup"><span data-stu-id="7d231-129">Export an RSA public key.</span></span> <span data-ttu-id="7d231-130">La mémoire tampon *pbOutput* reçoit une structure d' [**\_ \_ objet BLOB RSAKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immédiatement suivie des données de clé.</span><span class="sxs-lookup"><span data-stu-id="7d231-130">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="7d231-131">*pbOutput* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7d231-131">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7d231-132">Adresse d’une mémoire tampon qui reçoit l' [*objet blob de clé*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="7d231-132">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="7d231-133">Le paramètre *cbOutput* contient la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="7d231-133">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="7d231-134">Si ce paramètre a la **valeur null**, cette fonction place la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="7d231-134">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7d231-135">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d231-135">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d231-136">Taille, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="7d231-136">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7d231-137">*pcbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7d231-137">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d231-138">Adresse d’une variable **DWORD** qui reçoit le nombre d’octets copiés dans la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="7d231-138">The address of a **DWORD** variable that receives the number of bytes copied to the *pbOutput* buffer.</span></span> <span data-ttu-id="7d231-139">Si le paramètre *pbOutput* a la valeur **null** lorsque la fonction est appelée, la taille requise pour la mémoire tampon *pbOutput* , en octets, est retournée dans la **valeur DWORD** désignée par ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="7d231-139">If the *pbOutput* parameter is set to **NULL** when the function is called, the required size for the *pbOutput* buffer, in bytes, is returned in the **DWORD** pointed to by this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7d231-140">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7d231-140">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d231-141">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="7d231-141">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d231-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d231-142">Return value</span></span>

<span data-ttu-id="7d231-143">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="7d231-143">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="7d231-144">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7d231-144">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="7d231-145">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="7d231-145">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7d231-146">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7d231-146">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="7d231-147">Description</span><span class="sxs-lookup"><span data-stu-id="7d231-147">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="7d231-148"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7d231-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="7d231-149">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7d231-149">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d231-150">Notes</span><span class="sxs-lookup"><span data-stu-id="7d231-150">Remarks</span></span>

<span data-ttu-id="7d231-151">La fonction **SslExportKey** facilite le transport des clés de session d’un processus à un autre, ainsi que l’exportation de la partie publique d’une clé éphémère.</span><span class="sxs-lookup"><span data-stu-id="7d231-151">The **SslExportKey** function facilitates transporting session keys from one process to another as well as exporting the public portion an ephemeral key.</span></span>

<span data-ttu-id="7d231-152">Lorsque vous exportez des clés de session, le type d’objet BLOB est opaque, ce qui signifie que le format de l’objet BLOB n’a pas d’importance tant que les fonctions **SslExportKey** et [**SslImportKey**](sslimportkey.md) peuvent l’interpréter.</span><span class="sxs-lookup"><span data-stu-id="7d231-152">When exporting session keys, the BLOB type is opaque, meaning that the format of the BLOB is irrelevant as long as both the **SslExportKey** and [**SslImportKey**](sslimportkey.md) functions can interpret it.</span></span>

<span data-ttu-id="7d231-153">Lors de l’exportation de la partie publique d’une clé éphémère, le type d’objet BLOB doit être le type approprié, par exemple, l’objet BLOB **\_ \_ public \_** ou l' **\_ \_ objet BLOB ECCPUBLIC ncrypt**.</span><span class="sxs-lookup"><span data-stu-id="7d231-153">When exporting the public portion of an ephemeral key the BLOB type must be the appropriate type, such as **NCRYPT\_DH\_PUBLIC\_BLOB** or **NCRYPT\_ECCPUBLIC\_BLOB**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d231-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d231-154">Requirements</span></span>



| <span data-ttu-id="7d231-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d231-155">Requirement</span></span> | <span data-ttu-id="7d231-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d231-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d231-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d231-157">Minimum supported client</span></span><br/> | <span data-ttu-id="7d231-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d231-158">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d231-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d231-159">Minimum supported server</span></span><br/> | <span data-ttu-id="7d231-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d231-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7d231-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d231-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d231-162"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d231-162"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="7d231-163">DLL</span><span class="sxs-lookup"><span data-stu-id="7d231-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d231-164"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d231-164"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

