---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS structure (WinBio \_ adapter. h)
description: Contient des informations supplémentaires nécessaires à un adaptateur de moteur pour créer un modèle d’inscription.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- API de Windows Biometric Framework de structure de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
- API du pointeur de structure PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS Windows Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464607"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a><span data-ttu-id="02f3d-105">\_Structure des \_ paramètres d’inscription étendue WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="02f3d-105">WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS structure</span></span>

<span data-ttu-id="02f3d-106">La structure des **\_ \_ \_ paramètres d’inscription étendue WINBIO** contient des informations supplémentaires nécessaires à un adaptateur de moteur pour créer un modèle d’inscription.</span><span class="sxs-lookup"><span data-stu-id="02f3d-106">The **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure contains additional information that an engine adapter needs to create an enrollment template.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f3d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02f3d-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="02f3d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="02f3d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="02f3d-109">**Taille**</span><span class="sxs-lookup"><span data-stu-id="02f3d-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="02f3d-110">Taille (en octets) de la structure **des \_ \_ \_ paramètres d’inscription étendue WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="02f3d-110">The size (in bytes) of the **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="02f3d-111">**Sous-fait**</span><span class="sxs-lookup"><span data-stu-id="02f3d-111">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="02f3d-112">L’une des [**\_ \_ constantes de sous-type biométrique WINBIO**](winbio-biometric-subtype-constants.md) qui fournit des informations supplémentaires sur l’inscription.</span><span class="sxs-lookup"><span data-stu-id="02f3d-112">One of the [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md) values that provides additional information about the enrollment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02f3d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="02f3d-113">Remarks</span></span>

<span data-ttu-id="02f3d-114">Le Windows Biometric Framework passe cette structure à la méthode [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) lors d’une opération d’inscription.</span><span class="sxs-lookup"><span data-stu-id="02f3d-114">The Windows Biometric Framework passes this structure to the [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) method during an enrollment operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f3d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02f3d-115">Requirements</span></span>



| <span data-ttu-id="02f3d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02f3d-116">Requirement</span></span> | <span data-ttu-id="02f3d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="02f3d-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f3d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02f3d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="02f3d-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02f3d-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="02f3d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02f3d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="02f3d-121">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02f3d-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="02f3d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="02f3d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="02f3d-123"><dt>WinBio \_ adaptateur. h (include WinBio \_ adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02f3d-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





