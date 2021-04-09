---
title: General, constantes (WinBio \_ types. h)
description: Spécifiez la longueur maximale des SID, des descripteurs, des ID, la longueur de chaîne maximale et la taille de mémoire tampon d’échantillon maximale.
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942125"
---
# <a name="general-constants-winbio_typesh"></a><span data-ttu-id="4bfe2-103">General, constantes (WinBio \_ types. h)</span><span class="sxs-lookup"><span data-stu-id="4bfe2-103">General Constants (Winbio\_types.h)</span></span>

<span data-ttu-id="4bfe2-104">Les constantes suivantes sont utilisées dans l’ensemble du Windows Biometric Framework.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-104">The following constants are used throughout the Windows Biometric Framework.</span></span>



| <span data-ttu-id="4bfe2-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="4bfe2-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="4bfe2-106">Description</span><span class="sxs-lookup"><span data-stu-id="4bfe2-106">Description</span></span>                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <span data-ttu-id="4bfe2-107"><dt>**\_taille maximale de \_ sid \_ de sécurité**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-107"><dt>**SECURITY\_MAX\_SID\_SIZE**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="4bfe2-108">Longueur maximale d’une valeur d’identificateur de sécurité (SID).</span><span class="sxs-lookup"><span data-stu-id="4bfe2-108">The maximum length of a security identifier (SID) value.</span></span> <span data-ttu-id="4bfe2-109">Actuellement, il s’agit de 68.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-109">Currently this is 68.</span></span><br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <span data-ttu-id="4bfe2-110"><dt>**\_ID d’unité WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-110"><dt>**WINBIO\_UNIT\_ID**</dt></span></span> </dl>                                                                                                                | <span data-ttu-id="4bfe2-111">Numéro d’identification d’une unité biométrique.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-111">ID number of a biometric unit.</span></span><br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <span data-ttu-id="4bfe2-112"><dt>**\_handle de session WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-112"><dt>**WINBIO\_SESSION\_HANDLE**</dt></span></span> </dl>                                                                                           | <span data-ttu-id="4bfe2-113">Entier long non signé qui contient le handle d’une session biométrique ouverte.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-113">An unsigned long integer that contains the handle for an open biometric session.</span></span><br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <span data-ttu-id="4bfe2-114"><dt>**\_handle de Framework WINBIO \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-114"><dt>**WINBIO\_FRAMEWORK\_HANDLE**</dt></span></span> </dl>                                                                                     | <span data-ttu-id="4bfe2-115">Entier long non signé qui contient le handle d’une session Open Framework.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-115">An unsigned long integer that contains the handle for an open framework session.</span></span><br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <span data-ttu-id="4bfe2-116"><dt>**\_UUID WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-116"><dt>**WINBIO\_UUID**</dt></span></span> </dl>                                                                                                                          | <span data-ttu-id="4bfe2-117">GUID.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-117">A GUID.</span></span><br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <span data-ttu-id="4bfe2-118"><dt>**\_chaîne WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-118"><dt>**WINBIO\_STRING**</dt></span></span> </dl>                                                                                                                    | <span data-ttu-id="4bfe2-119">Tableau d’octets qui contient une chaîne Unicode terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-119">A byte array that contains a null-terminated Unicode string.</span></span><br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <span data-ttu-id="4bfe2-120"><dt>**WINBIO \_ \_ \_ longueur maximale** de la chaîne</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-120"><dt>**WINBIO\_MAX\_STRING\_LEN** </dt></span></span> </dl>                                                                                       | <span data-ttu-id="4bfe2-121">Longueur maximale d’une valeur **de \_ chaîne WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="4bfe2-121">The maximum length of a **WINBIO\_STRING** value.</span></span> <span data-ttu-id="4bfe2-122">Actuellement, il s’agit de 256.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-122">Currently this is 256.</span></span><br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <span data-ttu-id="4bfe2-123"><dt>**WINBIO \_ Taille maximale de la \_ \_ mémoire \_ tampon d’échantillonnage**</dt> <dt>0x7FFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-123"><dt>**WINBIO\_MAX\_SAMPLE\_BUFFER\_SIZE**</dt> <dt>0x7FFFFFFF</dt></span></span> </dl> | <span data-ttu-id="4bfe2-124">Nombre maximal d’octets dans une seule capture de données biométriques.</span><span class="sxs-lookup"><span data-stu-id="4bfe2-124">The maximum number of bytes in a single biometric data capture.</span></span><br/>                  |



## <a name="requirements"></a><span data-ttu-id="4bfe2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bfe2-125">Requirements</span></span>



| <span data-ttu-id="4bfe2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bfe2-126">Requirement</span></span> | <span data-ttu-id="4bfe2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bfe2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfe2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bfe2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfe2-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bfe2-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="4bfe2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bfe2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfe2-131">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bfe2-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4bfe2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4bfe2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bfe2-133"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bfe2-133"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bfe2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bfe2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfe2-135">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="4bfe2-135">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





