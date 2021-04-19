---
description: Appelé lorsque le certificat retourné par le rappel CertStoreProvFindCert n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: CertStoreProvFreeFindCert fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529346"
---
# <a name="certstoreprovfreefindcert-callback-function"></a><span data-ttu-id="4e20e-103">CertStoreProvFreeFindCert fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="4e20e-103">CertStoreProvFreeFindCert callback function</span></span>

<span data-ttu-id="4e20e-104">La fonction de rappel **CertStoreProvFreeFindCert** est appelée lorsque le certificat retourné par le rappel [**CertStoreProvFindCert**](certstoreprovfindcert.md) n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à **CertStoreProvFindCert**.</span><span class="sxs-lookup"><span data-stu-id="4e20e-104">The **CertStoreProvFreeFindCert** callback function is called when the certificate returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCert**.</span></span> <span data-ttu-id="4e20e-105">Avant d’appeler le rappel de fermeture, tous les certificats retournés par le rappel [**CertStoreProvFindCert**](certstoreprovfindcert.md) doivent être libérés par le fournisseur à l’aide de **CertStoreProvFindCert** ou **CertStoreProvFreeFindCert**.</span><span class="sxs-lookup"><span data-stu-id="4e20e-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCert**](certstoreprovfindcert.md) callback must be released by the provider using **CertStoreProvFindCert** or **CertStoreProvFreeFindCert**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e20e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e20e-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4e20e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e20e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e20e-108">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e20e-109">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4e20e-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e20e-110">*pCertContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-110">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e20e-111">Pointeur vers un [**\_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="4e20e-111">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="4e20e-112">*pvStoreProvFindInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e20e-113">Pointeur vers une mémoire tampon qui contient des informations de recherche.</span><span class="sxs-lookup"><span data-stu-id="4e20e-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="4e20e-114">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e20e-115">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="4e20e-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e20e-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e20e-116">Return value</span></span>

<span data-ttu-id="4e20e-117">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="4e20e-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e20e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e20e-118">Requirements</span></span>



| <span data-ttu-id="4e20e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e20e-119">Requirement</span></span> | <span data-ttu-id="4e20e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e20e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4e20e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e20e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4e20e-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4e20e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e20e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4e20e-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e20e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e20e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e20e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e20e-126">**contexte du certificat \_**</span><span class="sxs-lookup"><span data-stu-id="4e20e-126">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="4e20e-127">**CertStoreProvFindCert**</span><span class="sxs-lookup"><span data-stu-id="4e20e-127">**CertStoreProvFindCert**</span></span>](certstoreprovfindcert.md)
</dt> </dl>

 

 
