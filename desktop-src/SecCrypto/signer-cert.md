---
description: Spécifie un certificat utilisé pour signer un document. Le certificat peut être stocké dans un fichier SPC (Software Publisher Certificate) ou dans un magasin de certificats.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Structure SIGNER_CERT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209867"
---
# <a name="signer_cert-structure"></a><span data-ttu-id="de431-104">Structure du \_ certificat du signataire</span><span class="sxs-lookup"><span data-stu-id="de431-104">SIGNER\_CERT structure</span></span>

<span data-ttu-id="de431-105">La structure du certificat du **signataire \_** spécifie un [*certificat*](../secgloss/c-gly.md) utilisé pour signer un document.</span><span class="sxs-lookup"><span data-stu-id="de431-105">The **SIGNER\_CERT** structure specifies a [*certificate*](../secgloss/c-gly.md) used to sign a document.</span></span> <span data-ttu-id="de431-106">Le certificat peut être stocké dans un fichier SPC ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) ou dans un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="de431-106">The certificate can be stored in a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) file or in a [*certificate store*](../secgloss/c-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="de431-107">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="de431-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="de431-108">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="de431-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="de431-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de431-109">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a><span data-ttu-id="de431-110">Membres</span><span class="sxs-lookup"><span data-stu-id="de431-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="de431-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="de431-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="de431-112">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="de431-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="de431-113">**dwCertChoice**</span><span class="sxs-lookup"><span data-stu-id="de431-113">**dwCertChoice**</span></span>
</dt> <dd>

<span data-ttu-id="de431-114">Spécifie comment le certificat est stocké.</span><span class="sxs-lookup"><span data-stu-id="de431-114">Specifies how the certificate is stored.</span></span> <span data-ttu-id="de431-115">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="de431-115">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="de431-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="de431-116">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="de431-117">Signification</span><span class="sxs-lookup"><span data-stu-id="de431-117">Meaning</span></span>                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <span data-ttu-id="de431-118"><dt>**Signataire \_ \_ \_ Fichier CPS du certificat**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="de431-118"><dt>**SIGNER\_CERT\_SPC\_FILE**</dt> <dt>1</dt></span></span> </dl>    | <span data-ttu-id="de431-119">Le certificat est stocké dans un fichier SPC.</span><span class="sxs-lookup"><span data-stu-id="de431-119">The certificate is stored in an SPC file.</span></span> <span data-ttu-id="de431-120">Le membre **pwszSpcFile** contient le chemin d’accès et le nom de fichier du fichier SPC.</span><span class="sxs-lookup"><span data-stu-id="de431-120">The **pwszSpcFile** member contains the path and file name of the SPC file.</span></span><br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <span data-ttu-id="de431-121"><dt>**Signataire \_ \_Magasin de certificats**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="de431-121"><dt>**SIGNER\_CERT\_STORE**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="de431-122">Le certificat est stocké dans un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="de431-122">The certificate is stored in a certificate store.</span></span> <span data-ttu-id="de431-123">Le membre **pCertStoreInfo** contient un pointeur vers une structure d' [**\_ \_ \_ informations du magasin**](signer-cert-store-info.md) du certificat du signataire qui spécifie le magasin de certificats dans lequel le certificat est stocké.</span><span class="sxs-lookup"><span data-stu-id="de431-123">The **pCertStoreInfo** member contains a pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span><br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <span data-ttu-id="de431-124"><dt>**Signataire \_ CERTIFICAT \_ SPC \_ chaîne**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="de431-124"><dt>**SIGNER\_CERT\_SPC\_CHAIN**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="de431-125">Le certificat est stocké dans un fichier SPC et est associé à une chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="de431-125">The certificate is stored in an SPC file and is associated with a certificate chain.</span></span> <span data-ttu-id="de431-126">Le membre **pSpcChainInfo** contient un pointeur vers une structure d' [**\_ \_ \_ informations de chaîne SPC du signataire**](signer-spc-chain-info.md) qui contient les informations de chaîne du certificat.</span><span class="sxs-lookup"><span data-stu-id="de431-126">The **pSpcChainInfo** member contains a pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="de431-127">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="de431-127">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="de431-128">Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le chemin d’accès et le nom de fichier du fichier SPC dans lequel le certificat est stocké.</span><span class="sxs-lookup"><span data-stu-id="de431-128">A pointer to a null-terminated Unicode string that contains the path and file name of the SPC file in which the certificate is stored.</span></span> <span data-ttu-id="de431-129">Ce membre est utilisé uniquement si le membre **dwCertChoice** contient le **\_ \_ \_ fichier SPC du certificat du signataire**.</span><span class="sxs-lookup"><span data-stu-id="de431-129">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_FILE**.</span></span>

</dd> <dt>

<span data-ttu-id="de431-130">**pCertStoreInfo**</span><span class="sxs-lookup"><span data-stu-id="de431-130">**pCertStoreInfo**</span></span>
</dt> <dd>

<span data-ttu-id="de431-131">Pointeur vers une structure d' [**\_ \_ \_ informations du magasin**](signer-cert-store-info.md) du certificat du signataire qui spécifie le magasin de certificats dans lequel le certificat est stocké.</span><span class="sxs-lookup"><span data-stu-id="de431-131">A pointer to a [**SIGNER\_CERT\_STORE\_INFO**](signer-cert-store-info.md) structure that specifies the certificate store in which the certificate is stored.</span></span> <span data-ttu-id="de431-132">Ce membre est utilisé uniquement si le membre **dwCertChoice** contient le **\_ \_ magasin de certificats de signataire**.</span><span class="sxs-lookup"><span data-stu-id="de431-132">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_STORE**.</span></span>

</dd> <dt>

<span data-ttu-id="de431-133">**pSpcChainInfo**</span><span class="sxs-lookup"><span data-stu-id="de431-133">**pSpcChainInfo**</span></span>
</dt> <dd>

<span data-ttu-id="de431-134">Pointeur vers une structure d' [**\_ \_ \_ informations de chaîne SPC du signataire**](signer-spc-chain-info.md) qui contient les informations de chaîne du certificat.</span><span class="sxs-lookup"><span data-stu-id="de431-134">A pointer to a [**SIGNER\_SPC\_CHAIN\_INFO**](signer-spc-chain-info.md) structure that contains the chain information for the certificate.</span></span> <span data-ttu-id="de431-135">Ce membre est utilisé uniquement si le membre **dwCertChoice** contient le **certificat du signataire du \_ certificat \_ SPC \_**.</span><span class="sxs-lookup"><span data-stu-id="de431-135">This member is only used if the **dwCertChoice** member contains **SIGNER\_CERT\_SPC\_CHAIN**.</span></span>

</dd> <dt>

<span data-ttu-id="de431-136">**HWND**</span><span class="sxs-lookup"><span data-stu-id="de431-136">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="de431-137">Handle de la fenêtre à utiliser comme propriétaire de toutes les boîtes de dialogue affichées.</span><span class="sxs-lookup"><span data-stu-id="de431-137">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="de431-138">Ce membre n’est pas actuellement utilisé et est ignoré.</span><span class="sxs-lookup"><span data-stu-id="de431-138">This member is not currently used and is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de431-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de431-139">Requirements</span></span>



| <span data-ttu-id="de431-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de431-140">Requirement</span></span> | <span data-ttu-id="de431-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="de431-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="de431-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de431-142">Minimum supported client</span></span><br/> | <span data-ttu-id="de431-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de431-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="de431-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de431-144">Minimum supported server</span></span><br/> | <span data-ttu-id="de431-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de431-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="de431-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de431-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de431-147">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="de431-147">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="de431-148">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="de431-148">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
