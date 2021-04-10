---
title: Constantes WINBIO_DB ( \_ types WINBIO. h)
description: Spécifiez la base de données à utiliser pour un pool système.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104368"
---
# <a name="winbio_db-constants"></a><span data-ttu-id="e4239-103">\_Constantes WINBIO DB</span><span class="sxs-lookup"><span data-stu-id="e4239-103">WINBIO\_DB Constants</span></span>

<span data-ttu-id="e4239-104">Les constantes suivantes peuvent être utilisées lors de l’appel de [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour spécifier la base de données à utiliser pour un pool système.</span><span class="sxs-lookup"><span data-stu-id="e4239-104">The following constants can be used when calling [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) to specify the database to be used for a system pool.</span></span>



| <span data-ttu-id="e4239-105">Constante</span><span class="sxs-lookup"><span data-stu-id="e4239-105">Constant</span></span>                                                                                                                                                                         | <span data-ttu-id="e4239-106">Description</span><span class="sxs-lookup"><span data-stu-id="e4239-106">Description</span></span>                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <span data-ttu-id="e4239-107"><dt>**WINBIO \_ DB \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="e4239-107"><dt>**WINBIO\_DB\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="e4239-108">Chaque unité biométrique du pool de capteurs utilise la base de données par défaut spécifiée dans la configuration d’unité biométrique par défaut.</span><span class="sxs-lookup"><span data-stu-id="e4239-108">Each biometric unit in the sensor pool uses the default database specified in the default biometric unit configuration.</span></span><br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <span data-ttu-id="e4239-109"><dt>**démarrage de WINBIO \_ DB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e4239-109"><dt>**WINBIO\_DB\_BOOTSTRAP**</dt></span></span> </dl> | <span data-ttu-id="e4239-110">Peut être utilisé pour les scénarios avant le démarrage de Windows.</span><span class="sxs-lookup"><span data-stu-id="e4239-110">Can be used for scenarios prior to starting Windows.</span></span> <span data-ttu-id="e4239-111">En règle générale, la base de données fait partie de la puce de capteur ou fait partie du BIOS et ne peut être utilisée que pour l’inscription et la suppression d’un modèle.</span><span class="sxs-lookup"><span data-stu-id="e4239-111">Typically, the database is part of the sensor chip or is part of the BIOS and can only be used for template enrollment and deletion.</span></span><br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <span data-ttu-id="e4239-112"><dt>**WINBIO \_ DB \_ ONCHIP**</dt></span><span class="sxs-lookup"><span data-stu-id="e4239-112"><dt>**WINBIO\_DB\_ONCHIP**</dt></span></span> </dl>          | <span data-ttu-id="e4239-113">La base de données réside sur la puce du capteur.</span><span class="sxs-lookup"><span data-stu-id="e4239-113">The database resides on the sensor chip.</span></span><br/>                                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="e4239-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4239-114">Requirements</span></span>



| <span data-ttu-id="e4239-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4239-115">Requirement</span></span> | <span data-ttu-id="e4239-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4239-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4239-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4239-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e4239-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4239-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e4239-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4239-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e4239-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4239-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e4239-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4239-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4239-122"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4239-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4239-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4239-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4239-124">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="e4239-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





