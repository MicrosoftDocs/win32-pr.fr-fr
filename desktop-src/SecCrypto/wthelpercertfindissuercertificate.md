---
description: Recherche un certificat d’émetteur à partir des magasins de certificats spécifiés qui correspondent au certificat d’objet spécifié.
ms.assetid: c724f602-fc73-4857-941f-0f22a9e472d1
title: WTHelperCertFindIssuerCertificate fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperCertFindIssuerCertificate
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 99135ac22509b288726732ca4a16248b304f294b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203035"
---
# <a name="wthelpercertfindissuercertificate-function"></a><span data-ttu-id="3b2d5-103">WTHelperCertFindIssuerCertificate fonction)</span><span class="sxs-lookup"><span data-stu-id="3b2d5-103">WTHelperCertFindIssuerCertificate function</span></span>

<span data-ttu-id="3b2d5-104">\[La fonction **WTHelperCertFindIssuerCertificate** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-104">\[The **WTHelperCertFindIssuerCertificate** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3b2d5-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="3b2d5-106">La fonction **WTHelperCertFindIssuerCertificate** recherche un certificat d’émetteur parmi les magasins de certificats spécifiés qui correspondent au certificat d’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-106">The **WTHelperCertFindIssuerCertificate** function finds an issuer certificate from the specified certificate stores that matches the specified subject certificate.</span></span>

> [!Note]  
> <span data-ttu-id="3b2d5-107">Cette fonction n’a pas de bibliothèque d’importation associée.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-107">This function has no associated import library.</span></span> <span data-ttu-id="3b2d5-108">Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Wintrust.dll.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-108">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3b2d5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b2d5-109">Syntax</span></span>


```C++
PCCERT_CONTEXT WINAPI WTHelperCertFindIssuerCertificate(
  _In_      PCCERT_CONTEXT pChildContext,
  _In_      DWORD          chStores,
  _In_      HCERTSTORE     *pahStores,
  _In_      FILETIME       *psftVerifyAsOf,
  _In_      DWORD          dwEncoding,
  _Out_opt_ DWORD          *pdwConfidence,
  _Out_     DWORD          *dwError
);
```



## <a name="parameters"></a><span data-ttu-id="3b2d5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b2d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b2d5-111">*pChildContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-111">*pChildContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2d5-112">Certificat d’objet pour lequel Rechercher un certificat d’émetteur correspondant.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-112">The subject certificate for which to find a matching issuer certificate.</span></span>

</dd> <dt>

<span data-ttu-id="3b2d5-113">*chStores* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-113">*chStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2d5-114">Nombre d’éléments dans le tableau *pahStores* .</span><span class="sxs-lookup"><span data-stu-id="3b2d5-114">The number of elements in the *pahStores* array.</span></span>

</dd> <dt>

<span data-ttu-id="3b2d5-115">*pahStores* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-115">*pahStores* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2d5-116">Tableau de magasins de certificats dans lequel effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-116">An array of certificate stores in which to search.</span></span>

</dd> <dt>

<span data-ttu-id="3b2d5-117">*psftVerifyAsOf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-117">*psftVerifyAsOf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2d5-118">Heure de vérification.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-118">The time of verification.</span></span>

</dd> <dt>

<span data-ttu-id="3b2d5-119">*dwEncoding* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-119">*dwEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2d5-120">Valeur **DWORD** qui spécifie les types d’encodage du certificat à vérifier.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-120">A **DWORD** value that specifies the encoding types of the certificate to check.</span></span> <span data-ttu-id="3b2d5-121">Pour plus d’informations sur les types d’encodage possibles, consultez [types d’encodage de message et de certificat](certificate-and-message-encoding-types.md).</span><span class="sxs-lookup"><span data-stu-id="3b2d5-121">For information about possible encoding types, see [Certificate and Message Encoding Types](certificate-and-message-encoding-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b2d5-122">*pdwConfidence* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-122">*pdwConfidence* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2d5-123">Ce paramètre peut être une combinaison d’opérations de bits de zéro ou plusieurs des valeurs de confiance suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-123">This parameter can be a bitwise combination of zero or more of the following confidence values.</span></span>



| <span data-ttu-id="3b2d5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b2d5-124">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="3b2d5-125">Signification</span><span class="sxs-lookup"><span data-stu-id="3b2d5-125">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="CERT_CONFIDENCE_SIG"></span><span id="cert_confidence_sig"></span><dl> <span data-ttu-id="3b2d5-126"><dt>**Certificat \_ CONFIANCE \_ SIG**</dt> <dt> 0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="3b2d5-126"><dt>**CERT\_CONFIDENCE\_SIG**</dt> <dt> 0x10000000</dt></span></span> </dl>                     | <span data-ttu-id="3b2d5-127">La signature du certificat est valide.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-127">The signature of the certificate is valid.</span></span><br/>                                           |
| <span id="CERT_CONFIDENCE_TIME"></span><span id="cert_confidence_time"></span><dl> <span data-ttu-id="3b2d5-128"><dt>**Certificat \_ \_Temps de confiance**</dt> <dt> 0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="3b2d5-128"><dt>**CERT\_CONFIDENCE\_TIME**</dt> <dt> 0x01000000</dt></span></span> </dl>                  | <span data-ttu-id="3b2d5-129">L’heure de l’émetteur du certificat est valide.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-129">The time of the certificate issuer is valid.</span></span><br/>                                         |
| <span id="_CERT_CONFIDENCE_TIMENEST"></span><span id="_cert_confidence_timenest"></span><dl> <span data-ttu-id="3b2d5-130"><dt> **Certificat \_ confidence \_ TIMENEST**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="3b2d5-130"><dt> **CERT\_CONFIDENCE\_TIMENEST**</dt> <dt>0x00100000</dt></span></span> </dl>    | <span data-ttu-id="3b2d5-131">L’heure du certificat est valide.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-131">The time of the certificate is valid.</span></span><br/>                                                |
| <span id="_CERT_CONFIDENCE_AUTHIDEXT"></span><span id="_cert_confidence_authidext"></span><dl> <span data-ttu-id="3b2d5-132"><dt> **Certificat \_ confidence \_ AUTHIDEXT**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="3b2d5-132"><dt> **CERT\_CONFIDENCE\_AUTHIDEXT**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="3b2d5-133">L’extension de l’ID d’autorité est valide.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-133">The authority ID extension is valid.</span></span><br/>                                                 |
| <span id="_CERT_CONFIDENCE_HYGIENE"></span><span id="_cert_confidence_hygiene"></span><dl> <span data-ttu-id="3b2d5-134"><dt> **Certificat \_ d' \_ hygiène de confiance**</dt> <dt>0x00001000</dt></span><span class="sxs-lookup"><span data-stu-id="3b2d5-134"><dt> **CERT\_CONFIDENCE\_HYGIENE**</dt> <dt>0x00001000</dt></span></span> </dl>       | <span data-ttu-id="3b2d5-135">Au minimum, la signature de l’extension Certificate and Authority ID est valide.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-135">At a minimum, the signature of the certificate and authority ID extension are valid.</span></span><br/> |
| <span id="_CERT_CONFIDENCE_HIGHEST"></span><span id="_cert_confidence_highest"></span><dl> <span data-ttu-id="3b2d5-136"><dt> **Confiance du certificat \_ \_ le plus élevé**</dt> <dt>0x11111000</dt></span><span class="sxs-lookup"><span data-stu-id="3b2d5-136"><dt> **CERT\_CONFIDENCE\_HIGHEST**</dt> <dt>0x11111000</dt></span></span> </dl>       | <span data-ttu-id="3b2d5-137">Combinaison de toutes les autres valeurs de confiance.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-137">A combination of all of the other confidence values.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="3b2d5-138">*dwError* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-138">*dwError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b2d5-139">Pointeur vers une variable **DWORD** qui contient la valeur d’erreur de ce certificat, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-139">A pointer to a **DWORD** variable that contains the error value for this certificate, if applicable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b2d5-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3b2d5-140">Return value</span></span>

<span data-ttu-id="3b2d5-141">Certificat d’émetteur qui correspond au certificat de sujet spécifié par le paramètre *pChildContext* .</span><span class="sxs-lookup"><span data-stu-id="3b2d5-141">An issuer certificate that matches the subject certificate specified by the *pChildContext* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b2d5-142">Notes</span><span class="sxs-lookup"><span data-stu-id="3b2d5-142">Remarks</span></span>

<span data-ttu-id="3b2d5-143">Pour trouver un certificat d’émetteur correspondant, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="3b2d5-143">To successfully find a matching issuer certificate, the following requirements must be met:</span></span>

-   <span data-ttu-id="3b2d5-144">La signature du certificat objet spécifié par le paramètre *pChildContext* doit être valide.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-144">The signature of the subject certificate specified by the *pChildContext* parameter must be valid.</span></span>
-   <span data-ttu-id="3b2d5-145">Le membre **rgExtension** du membre **PCertInfo** du paramètre *pChildContext* doit contenir une structure d' [**informations d' \_ ID de clé d’autorité \_ \_ \_ de certification**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) .</span><span class="sxs-lookup"><span data-stu-id="3b2d5-145">The **rgExtension** member of the **pCertInfo** member of the *pChildContext* parameter must contain a [**CERT\_AUTHORITY\_KEY\_ID\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_authority_key_id_info) structure.</span></span> <span data-ttu-id="3b2d5-146">Les membres **CertIssuer** et **CertSerialMember** de cette structure correspondent davantage aux membres correspondants pour le certificat de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-146">The **CertIssuer** and **CertSerialMember** members of this structure much match the corresponding members for the issuer certificate.</span></span>
-   <span data-ttu-id="3b2d5-147">La valeur du paramètre *psftVerifyAsOf* doit être comprise dans la période de validité du certificat du sujet.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-147">The value of the *psftVerifyAsOf* parameter must be within the period of validity of the subject certificate.</span></span>
-   <span data-ttu-id="3b2d5-148">La période de validité du certificat d’objet doit être comprise dans la période de validité du certificat de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="3b2d5-148">The period of validity of the subject certificate must be within the period of validity of the issuer certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b2d5-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b2d5-149">Requirements</span></span>



| <span data-ttu-id="3b2d5-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b2d5-150">Requirement</span></span> | <span data-ttu-id="3b2d5-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b2d5-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b2d5-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b2d5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3b2d5-153">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-153">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3b2d5-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b2d5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3b2d5-155">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b2d5-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3b2d5-156">DLL</span><span class="sxs-lookup"><span data-stu-id="3b2d5-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b2d5-157"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b2d5-157"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
