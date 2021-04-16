---
title: Constantes WINBIO_EVENT ( \_ types WINBIO. h)
description: Spécifiez les types de notifications d’événements du fournisseur de services à surveiller.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 182a4ffe254e946f1b8deca2c5034e665a58f7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508373"
---
# <a name="winbio_event-constants"></a><span data-ttu-id="a665b-103">\_Constantes d’événement WINBIO</span><span class="sxs-lookup"><span data-stu-id="a665b-103">WINBIO\_EVENT Constants</span></span>

<span data-ttu-id="a665b-104">Les constantes suivantes peuvent être utilisées dans la fonction [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) pour spécifier les types de notifications d’événements du fournisseur de services à surveiller.</span><span class="sxs-lookup"><span data-stu-id="a665b-104">The following constants can be used in the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to specify the types of service provider event notifications to monitor.</span></span>



| <span data-ttu-id="a665b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a665b-105">Constant</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="a665b-106">Description</span><span class="sxs-lookup"><span data-stu-id="a665b-106">Description</span></span>                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <span data-ttu-id="a665b-107"><dt>**\_événement WINBIO \_ FP \_ récupéré**</dt></span><span class="sxs-lookup"><span data-stu-id="a665b-107"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED**</dt></span></span> </dl>                             | <span data-ttu-id="a665b-108">Le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus.</span><span class="sxs-lookup"><span data-stu-id="a665b-108">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="a665b-109">Le Windows Biometric Framework appelle la fonction de rappel pour indiquer qu’un glissement Finger s’est produit, mais n’essaie pas d’identifier l’empreinte digitale.</span><span class="sxs-lookup"><span data-stu-id="a665b-109">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.</span></span><br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <span data-ttu-id="a665b-110"><dt>**identification de l' \_ événement WINBIO \_ FP \_ inréclamée \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a665b-110"><dt>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY**</dt></span></span> </dl> | <span data-ttu-id="a665b-111">Le capteur a détecté un glissement Finger qui n’a pas été demandé par l’application ou par la fenêtre qui a actuellement le focus.</span><span class="sxs-lookup"><span data-stu-id="a665b-111">The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="a665b-112">Le Windows Biometric Framework tente d’identifier l’empreinte digitale et transmet le résultat de ce processus à votre fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="a665b-112">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="a665b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a665b-113">Requirements</span></span>



| <span data-ttu-id="a665b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a665b-114">Requirement</span></span> | <span data-ttu-id="a665b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a665b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a665b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a665b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a665b-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a665b-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a665b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a665b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a665b-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a665b-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a665b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a665b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a665b-121"><dt>WinBio \_ types. h (include WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a665b-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a665b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a665b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a665b-123">Constantes d’application cliente</span><span class="sxs-lookup"><span data-stu-id="a665b-123">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





