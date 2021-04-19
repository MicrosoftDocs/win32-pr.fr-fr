---
description: Définit l’état de Output Protection Manager (OPM).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Énumération MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 73585bf63bc559f30ce114730274e30518497b05
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106538953"
---
# <a name="mf_media_engine_opm_status-enumeration"></a><span data-ttu-id="611c6-103">Énumération de l’état de l' \_ \_ \_ État OPM Media Engine \_</span><span class="sxs-lookup"><span data-stu-id="611c6-103">MF\_MEDIA\_ENGINE\_OPM\_STATUS enumeration</span></span>

<span data-ttu-id="611c6-104">Définit l’état de [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="611c6-104">Defines the status of the [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

## <a name="syntax"></a><span data-ttu-id="611c6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="611c6-105">Syntax</span></span>


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a><span data-ttu-id="611c6-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="611c6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="611c6-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**le \_ moteur multimédia MF \_ \_ OPM \_ n’est pas \_ demandé**</span><span class="sxs-lookup"><span data-stu-id="611c6-107"><span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**MF\_MEDIA\_ENGINE\_OPM\_NOT\_REQUESTED**</span></span>
</dt> <dd>

<span data-ttu-id="611c6-108">État par défaut.</span><span class="sxs-lookup"><span data-stu-id="611c6-108">Default status.</span></span> <span data-ttu-id="611c6-109">Utilisé pour retourner l’état correct lorsque le contenu n’est pas protégé.</span><span class="sxs-lookup"><span data-stu-id="611c6-109">Used to return the correct status when the content is unprotected.</span></span>

</dd> <dt>

<span data-ttu-id="611c6-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**\_Media \_ Engine de \_ la \_ MF**</span><span class="sxs-lookup"><span data-stu-id="611c6-110"><span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**MF\_MEDIA\_ENGINE\_OPM\_ESTABLISHED**</span></span>
</dt> <dd>

<span data-ttu-id="611c6-111">OPM correctement établi.</span><span class="sxs-lookup"><span data-stu-id="611c6-111">OPM successfully established.</span></span>

</dd> <dt>

<span data-ttu-id="611c6-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ machine virtuelle Media Engine OPM \_ ayant échoué \_**</span><span class="sxs-lookup"><span data-stu-id="611c6-112"><span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_VM**</span></span>
</dt> <dd>

<span data-ttu-id="611c6-113">Échec de OPM en raison de l’exécution dans une machine virtuelle (VM).</span><span class="sxs-lookup"><span data-stu-id="611c6-113">OPM failed because running in a virtual machined (VM).</span></span>

</dd> <dt>

<span data-ttu-id="611c6-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**échec de la \_ \_ OPM Media Engine \_ OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="611c6-114"><span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_BDA**</span></span>
</dt> <dd>

<span data-ttu-id="611c6-115">Échec de OPM, car il n’existe aucun pilote graphique et le système utilise la carte d’affichage de base (BDA).</span><span class="sxs-lookup"><span data-stu-id="611c6-115">OPM failed because there is no graphics driver and the system is using Basic Display Adapter (BDA).</span></span>

</dd> <dt>

<span data-ttu-id="611c6-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**\_ \_ \_ \_ \_ pilote non signé Media Engine OPM avec échec \_**</span><span class="sxs-lookup"><span data-stu-id="611c6-116"><span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED\_UNSIGNED\_DRIVER**</span></span>
</dt> <dd>

<span data-ttu-id="611c6-117">Échec de OPM, car le pilote Graphics n’est pas PE signé, ce qui revient à WARP.</span><span class="sxs-lookup"><span data-stu-id="611c6-117">OPM failed because the graphics driver is not PE signed, falling back to WARP.</span></span>

</dd> <dt>

<span data-ttu-id="611c6-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**\_échec de \_ OPM Media Engine \_ OPM \_**</span><span class="sxs-lookup"><span data-stu-id="611c6-118"><span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF\_MEDIA\_ENGINE\_OPM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="611c6-119">Échec de OPM pour d’autres raisons.</span><span class="sxs-lookup"><span data-stu-id="611c6-119">OPM failed for other reasons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="611c6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="611c6-120">Requirements</span></span>



| <span data-ttu-id="611c6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="611c6-121">Requirement</span></span> | <span data-ttu-id="611c6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="611c6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="611c6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="611c6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="611c6-124">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="611c6-124">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="611c6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="611c6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="611c6-126">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="611c6-126">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="611c6-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="611c6-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="611c6-128"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="611c6-128"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="611c6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="611c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="611c6-130">Énumérations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="611c6-130">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




