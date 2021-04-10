---
title: Énumération WINBIO_CREDENTIAL_FORMAT ( \_ types WINBIO. h)
description: Définit des indicateurs qui peuvent être utilisés pour spécifier le format des informations d’identification de l’utilisateur final.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_CREDENTIAL_FORMAT
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103696"
---
# <a name="winbio_credential_format-enumeration"></a><span data-ttu-id="5848c-104">\_Énumération du format des informations d’identification WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="5848c-104">WINBIO\_CREDENTIAL\_FORMAT enumeration</span></span>

<span data-ttu-id="5848c-105">Définit des indicateurs qui peuvent être utilisés pour spécifier le format des informations d’identification de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="5848c-105">Defines flags that can be used to specify the end-user credential format.</span></span> <span data-ttu-id="5848c-106">Cette énumération est utilisée par la fonction [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .</span><span class="sxs-lookup"><span data-stu-id="5848c-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="5848c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5848c-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="5848c-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5848c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5848c-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**\_mot de passe WINBIO \_ générique**</span><span class="sxs-lookup"><span data-stu-id="5848c-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO\_PASSWORD\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="5848c-110">Le mot de passe est dans un format générique.</span><span class="sxs-lookup"><span data-stu-id="5848c-110">The password is in a generic format.</span></span>

</dd> <dt>

<span data-ttu-id="5848c-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO \_ mot de passe \_ condensé**</span><span class="sxs-lookup"><span data-stu-id="5848c-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO\_PASSWORD\_PACKED**</span></span>
</dt> <dd>

<span data-ttu-id="5848c-112">Le mot de passe est dans un format compressé.</span><span class="sxs-lookup"><span data-stu-id="5848c-112">The password is in a compressed format.</span></span>

</dd> <dt>

<span data-ttu-id="5848c-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ protégé par mot de passe \_**</span><span class="sxs-lookup"><span data-stu-id="5848c-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO\_PASSWORD\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="5848c-114">Les informations d’identification du mot de passe ont été encapsulées avec [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span><span class="sxs-lookup"><span data-stu-id="5848c-114">The password credential was wrapped with [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5848c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5848c-115">Requirements</span></span>



| <span data-ttu-id="5848c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5848c-116">Requirement</span></span> | <span data-ttu-id="5848c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5848c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5848c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5848c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5848c-119">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5848c-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="5848c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5848c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5848c-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5848c-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5848c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5848c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5848c-123"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5848c-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5848c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5848c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5848c-125">Énumérations des applications clientes</span><span class="sxs-lookup"><span data-stu-id="5848c-125">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="5848c-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="5848c-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

