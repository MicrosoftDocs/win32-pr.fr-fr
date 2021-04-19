---
description: Spécifie le magasin de certificats utilisé pour signer un document.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Structure SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518546"
---
# <a name="signer_cert_store_info-structure"></a><span data-ttu-id="eae23-103">Structure d' \_ \_ informations du magasin du certificat du signataire \_</span><span class="sxs-lookup"><span data-stu-id="eae23-103">SIGNER\_CERT\_STORE\_INFO structure</span></span>

<span data-ttu-id="eae23-104">La structure d' **\_ \_ \_ informations du magasin** de certificats du signataire spécifie le magasin de certificats utilisé pour signer un document.</span><span class="sxs-lookup"><span data-stu-id="eae23-104">The **SIGNER\_CERT\_STORE\_INFO** structure specifies the certificate store used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="eae23-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="eae23-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="eae23-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="eae23-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eae23-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eae23-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a><span data-ttu-id="eae23-108">Membres</span><span class="sxs-lookup"><span data-stu-id="eae23-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eae23-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="eae23-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="eae23-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="eae23-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="eae23-111">**pSigningCert**</span><span class="sxs-lookup"><span data-stu-id="eae23-111">**pSigningCert**</span></span>
</dt> <dd>

<span data-ttu-id="eae23-112">Pointeur vers une structure [**de \_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificat pour le certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="eae23-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the signing certificate.</span></span>

</dd> <dt>

<span data-ttu-id="eae23-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="eae23-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="eae23-114">Spécifie la manière dont les certificats sont ajoutés à la signature.</span><span class="sxs-lookup"><span data-stu-id="eae23-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="eae23-115">Pour trouver la chaîne de certificats, les magasins MY, CA, ROOT et SPC, en plus du magasin spécifié par le membre **hCertStore** , sont activés.</span><span class="sxs-lookup"><span data-stu-id="eae23-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="eae23-116">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eae23-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="eae23-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="eae23-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="eae23-118">Signification</span><span class="sxs-lookup"><span data-stu-id="eae23-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="eae23-119"><dt>**Signataire \_ \_ \_ Chaîne de stratégie de certificat**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="eae23-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="eae23-120">Ajoutez uniquement des certificats dans la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="eae23-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="eae23-121"><dt>**Signataire \_ Chaîne de stratégie de certificat \_ \_ \_ non \_ racine**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="eae23-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="eae23-122">Ajoutez uniquement des certificats dans la chaîne de certificats, à l’exclusion du certificat racine.</span><span class="sxs-lookup"><span data-stu-id="eae23-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="eae23-123"><dt>**Signataire \_ \_ \_ Magasin de stratégies de certificat**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="eae23-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="eae23-124">Ajoutez tous les certificats dans le magasin spécifié par le membre **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="eae23-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="eae23-125">Cet indicateur peut être **une combinaison or au niveau** du bit avec l’une des autres valeurs possibles pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="eae23-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eae23-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="eae23-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="eae23-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="eae23-127">Optional.</span></span> <span data-ttu-id="eae23-128">Handle d’un magasin de certificats supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="eae23-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eae23-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eae23-129">Requirements</span></span>



| <span data-ttu-id="eae23-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eae23-130">Requirement</span></span> | <span data-ttu-id="eae23-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="eae23-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eae23-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eae23-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eae23-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eae23-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="eae23-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eae23-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eae23-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eae23-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eae23-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eae23-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eae23-137">**certificat du signataire \_**</span><span class="sxs-lookup"><span data-stu-id="eae23-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 




