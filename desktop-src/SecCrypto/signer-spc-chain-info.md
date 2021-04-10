---
description: Spécifie un certificat SPC (Software Publisher Certificate) et une chaîne de certificats utilisés pour signer un document.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: Structure SIGNER_SPC_CHAIN_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115534"
---
# <a name="signer_spc_chain_info-structure"></a><span data-ttu-id="35387-103">Structure des \_ informations de la chaîne SPC du signataire \_ \_</span><span class="sxs-lookup"><span data-stu-id="35387-103">SIGNER\_SPC\_CHAIN\_INFO structure</span></span>

<span data-ttu-id="35387-104">La structure des informations de la **\_ \_ chaîne \_ du signataire SPC** spécifie un certificat SPC ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) et une chaîne de certificats utilisés pour signer un document.</span><span class="sxs-lookup"><span data-stu-id="35387-104">The **SIGNER\_SPC\_CHAIN\_INFO** structure specifies a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) and certificate chain used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="35387-105">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="35387-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="35387-106">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="35387-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="35387-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35387-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a><span data-ttu-id="35387-108">Membres</span><span class="sxs-lookup"><span data-stu-id="35387-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="35387-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="35387-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="35387-110">Taille, en octets, de la structure.</span><span class="sxs-lookup"><span data-stu-id="35387-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="35387-111">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="35387-111">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="35387-112">Nom du fichier SPC à utiliser pour signer un document.</span><span class="sxs-lookup"><span data-stu-id="35387-112">The name of the SPC file to use to sign a document.</span></span>

</dd> <dt>

<span data-ttu-id="35387-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="35387-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="35387-114">Spécifie la manière dont les certificats sont ajoutés à la signature.</span><span class="sxs-lookup"><span data-stu-id="35387-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="35387-115">Pour trouver la chaîne de certificats, les magasins MY, CA, ROOT et SPC, en plus du magasin spécifié par le membre **hCertStore** , sont activés.</span><span class="sxs-lookup"><span data-stu-id="35387-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="35387-116">Ce membre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="35387-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="35387-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="35387-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="35387-118">Signification</span><span class="sxs-lookup"><span data-stu-id="35387-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="35387-119"><dt>**Signataire \_ \_ \_ Chaîne de stratégie de certificat**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="35387-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="35387-120">Ajoutez uniquement des certificats dans la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="35387-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="35387-121"><dt>**Signataire \_ Chaîne de stratégie de certificat \_ \_ \_ non \_ racine**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="35387-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="35387-122">Ajoutez uniquement des certificats dans la chaîne de certificats, à l’exclusion du certificat racine.</span><span class="sxs-lookup"><span data-stu-id="35387-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="35387-123"><dt>**Signataire \_ \_ \_ Magasin de stratégies de certificat**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="35387-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="35387-124">Ajoutez tous les certificats dans le magasin spécifié par le membre **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="35387-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="35387-125">Cet indicateur peut être **une combinaison or au niveau** du bit avec l’une des autres valeurs possibles pour ce membre.</span><span class="sxs-lookup"><span data-stu-id="35387-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="35387-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="35387-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="35387-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="35387-127">Optional.</span></span> <span data-ttu-id="35387-128">Handle d’un magasin de certificats supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="35387-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35387-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35387-129">Requirements</span></span>



| <span data-ttu-id="35387-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35387-130">Requirement</span></span> | <span data-ttu-id="35387-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="35387-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35387-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35387-132">Minimum supported client</span></span><br/> | <span data-ttu-id="35387-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35387-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="35387-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35387-134">Minimum supported server</span></span><br/> | <span data-ttu-id="35387-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35387-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35387-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35387-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35387-137">**certificat du signataire \_**</span><span class="sxs-lookup"><span data-stu-id="35387-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 
