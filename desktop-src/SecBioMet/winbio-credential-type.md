---
title: Énumération WINBIO_CREDENTIAL_TYPE ( \_ types WINBIO. h)
description: Définit des indicateurs qui peuvent être utilisés pour filtrer sur le type d’informations d’identification.
ms.assetid: 7ef2d4b3-e1f9-46a0-8fc2-0e8660805ac3
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_CREDENTIAL_TYPE
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_TYPE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae41693db264308d33bc30191bdb73007b6b2dba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844321"
---
# <a name="winbio_credential_type-enumeration"></a><span data-ttu-id="7bb1d-104">\_Énumération des types d’informations d’identification WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="7bb1d-104">WINBIO\_CREDENTIAL\_TYPE enumeration</span></span>

<span data-ttu-id="7bb1d-105">Définit des indicateurs qui peuvent être utilisés pour filtrer sur le type d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="7bb1d-105">Defines flags that can be used to filter on the credential type.</span></span> <span data-ttu-id="7bb1d-106">Cette énumération est utilisée par les fonctions [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)et [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="7bb1d-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential), [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential), and [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb1d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bb1d-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_TYPE { 
  WINBIO_CREDENTIAL_PASSWORD  = 0x00000001,
  WINBIO_CREDENTIAL_ALL       = 0xffffffff
} WINBIO_CREDENTIAL_TYPE;
```



## <a name="constants"></a><span data-ttu-id="7bb1d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="7bb1d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7bb1d-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**\_ \_ mot de passe des informations d’identification WINBIO**</span><span class="sxs-lookup"><span data-stu-id="7bb1d-109"><span id="WINBIO_CREDENTIAL_PASSWORD"></span><span id="winbio_credential_password"></span>**WINBIO\_CREDENTIAL\_PASSWORD**</span></span>
</dt> <dd>

<span data-ttu-id="7bb1d-110">Filtre les informations d’identification du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="7bb1d-110">Filters password credentials.</span></span>

</dd> <dt>

<span data-ttu-id="7bb1d-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO \_ tous les informations d’identification \_**</span><span class="sxs-lookup"><span data-stu-id="7bb1d-111"><span id="WINBIO_CREDENTIAL_ALL"></span><span id="winbio_credential_all"></span>**WINBIO\_CREDENTIAL\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="7bb1d-112">Filtre toutes les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="7bb1d-112">Filters all credentials.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bb1d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bb1d-113">Requirements</span></span>



| <span data-ttu-id="7bb1d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bb1d-114">Requirement</span></span> | <span data-ttu-id="7bb1d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bb1d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb1d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bb1d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb1d-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bb1d-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="7bb1d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bb1d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb1d-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bb1d-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7bb1d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bb1d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bb1d-121"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bb1d-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb1d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bb1d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb1d-123">Énumérations des applications clientes</span><span class="sxs-lookup"><span data-stu-id="7bb1d-123">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="7bb1d-124">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="7bb1d-124">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> <dt>

[<span data-ttu-id="7bb1d-125">**WinBioRemoveCredential**</span><span class="sxs-lookup"><span data-stu-id="7bb1d-125">**WinBioRemoveCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
</dt> <dt>

[<span data-ttu-id="7bb1d-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="7bb1d-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

 





