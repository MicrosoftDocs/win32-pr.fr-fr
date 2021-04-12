---
title: Énumération WINBIO_CREDENTIAL_STATE ( \_ types WINBIO. h)
description: Définit des valeurs qui spécifient si des informations d’identification ont été associées aux données biométriques pour un utilisateur final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- API Windows Biometric Framework de l’énumération WINBIO_CREDENTIAL_STATE
- API du pointeur d’énumération PWINBIO_CREDENTIAL_STATE Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317146"
---
# <a name="winbio_credential_state-enumeration"></a><span data-ttu-id="b44c1-105">\_Énumération de l’état des informations d’identification WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="b44c1-105">WINBIO\_CREDENTIAL\_STATE enumeration</span></span>

<span data-ttu-id="b44c1-106">Définit des valeurs qui spécifient si des informations d’identification ont été associées aux données biométriques pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="b44c1-106">Defines values that specify whether a credential has been associated with the biometric data for an end user.</span></span> <span data-ttu-id="b44c1-107">Cette énumération est utilisée par la fonction [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="b44c1-107">This enumeration is used by the [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b44c1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b44c1-108">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a><span data-ttu-id="b44c1-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="b44c1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b44c1-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_informations d’identification WINBIO \_ non \_ définies**</span><span class="sxs-lookup"><span data-stu-id="b44c1-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**WINBIO\_CREDENTIAL\_NOT\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="b44c1-111">Des informations d’identification ont été associées à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="b44c1-111">A credential has been associated with the end user.</span></span>

</dd> <dt>

<span data-ttu-id="b44c1-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_jeu d’informations d’identification WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="b44c1-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO\_CREDENTIAL\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="b44c1-113">Les informations d’identification n’ont pas été associées à l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="b44c1-113">A credential has not been associated with the end user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b44c1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b44c1-114">Requirements</span></span>



| <span data-ttu-id="b44c1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b44c1-115">Requirement</span></span> | <span data-ttu-id="b44c1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b44c1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b44c1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b44c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b44c1-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b44c1-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b44c1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b44c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b44c1-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b44c1-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b44c1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b44c1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b44c1-122"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b44c1-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b44c1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b44c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b44c1-124">Énumérations des applications clientes</span><span class="sxs-lookup"><span data-stu-id="b44c1-124">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="b44c1-125">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="b44c1-125">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





