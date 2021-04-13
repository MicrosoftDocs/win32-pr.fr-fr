---
title: Fonctions de rappel d’application cliente
description: Deux types de signatures de rappel.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380243"
---
# <a name="client-application-callback-functions"></a><span data-ttu-id="af780-103">Fonctions de rappel d’application cliente</span><span class="sxs-lookup"><span data-stu-id="af780-103">Client Application Callback Functions</span></span>

<span data-ttu-id="af780-104">Le Windows Biometric Framework prend en charge deux types de signatures de rappel.</span><span class="sxs-lookup"><span data-stu-id="af780-104">The Windows Biometric Framework supports two types of callback signatures.</span></span> <span data-ttu-id="af780-105">À partir de Windows 8, le rappel suivant est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="af780-105">Beginning with Windows 8, the following callback is supported.</span></span> <span data-ttu-id="af780-106">Nous vous recommandons d’implémenter ce rappel pour toutes les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="af780-106">We recommend that you implement this callback for all new applications.</span></span> <span data-ttu-id="af780-107">Toutefois, ce rappel ne peut pas être utilisé dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="af780-107">This callback cannot, however, be used in Windows 7.</span></span>



| <span data-ttu-id="af780-108">Rappel</span><span class="sxs-lookup"><span data-stu-id="af780-108">Callback</span></span>                                                                                     | <span data-ttu-id="af780-109">Description</span><span class="sxs-lookup"><span data-stu-id="af780-109">Description</span></span>                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af780-110">**\_rappel d' \_ achèvement \_ asynchrone PWINBIO**</span><span class="sxs-lookup"><span data-stu-id="af780-110">**PWINBIO\_ASYNC\_COMPLETION\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | <span data-ttu-id="af780-111">Indique à l’application cliente qu’une opération asynchrone démarrée à l’aide de [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) ou de [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) est terminée.</span><span class="sxs-lookup"><span data-stu-id="af780-111">Notifies the client application that an asynchronous operation started by using [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) or [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) has completed.</span></span><br/> |



 

<span data-ttu-id="af780-112">Les fonctions de rappel suivantes ont été introduites dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="af780-112">The following callback functions were introduced in Windows 7.</span></span> <span data-ttu-id="af780-113">Nous vous recommandons de ne pas les implémenter pour les nouvelles applications qui ciblent les systèmes d’exploitation Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="af780-113">We recommend that you do not implement them for new applications that target Windows 8 and later operating systems.</span></span>



| <span data-ttu-id="af780-114">Rappel</span><span class="sxs-lookup"><span data-stu-id="af780-114">Callback</span></span>                                                                                 | <span data-ttu-id="af780-115">Description</span><span class="sxs-lookup"><span data-stu-id="af780-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af780-116">**\_rappel de capture PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="af780-116">**PWINBIO\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | <span data-ttu-id="af780-117">Retourne les résultats de la fonction asynchrone [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="af780-117">Returns results from the asynchronous [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="af780-118">**\_rappel de \_ capture d’inscription PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="af780-118">**PWINBIO\_ENROLL\_CAPTURE\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | <span data-ttu-id="af780-119">Retourne les résultats de la fonction asynchrone [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .</span><span class="sxs-lookup"><span data-stu-id="af780-119">Returns results from the asynchronous [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) function.</span></span><br/> |
| [<span data-ttu-id="af780-120">**\_rappel d’événement PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="af780-120">**PWINBIO\_EVENT\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | <span data-ttu-id="af780-121">Retourne les résultats de la fonction asynchrone [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .</span><span class="sxs-lookup"><span data-stu-id="af780-121">Returns results from the asynchronous [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function.</span></span><br/>           |
| [<span data-ttu-id="af780-122">**PWINBIO \_ identifier le \_ rappel**</span><span class="sxs-lookup"><span data-stu-id="af780-122">**PWINBIO\_IDENTIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | <span data-ttu-id="af780-123">Retourne les résultats de la fonction asynchrone [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="af780-123">Returns results from the asynchronous [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) function.</span></span><br/>           |
| [<span data-ttu-id="af780-124">**PWINBIO \_ Rechercher \_ le \_ rappel de capteur**</span><span class="sxs-lookup"><span data-stu-id="af780-124">**PWINBIO\_LOCATE\_SENSOR\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | <span data-ttu-id="af780-125">Retourne les résultats de la fonction asynchrone [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .</span><span class="sxs-lookup"><span data-stu-id="af780-125">Returns results from the asynchronous [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) function.</span></span><br/>   |
| [<span data-ttu-id="af780-126">**\_rappel de vérification de PWINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="af780-126">**PWINBIO\_VERIFY\_CALLBACK**</span></span>](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | <span data-ttu-id="af780-127">Retourne les résultats de la fonction asynchrone [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .</span><span class="sxs-lookup"><span data-stu-id="af780-127">Returns results from the asynchronous [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) function.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="af780-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af780-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af780-129">Référence de l’application cliente</span><span class="sxs-lookup"><span data-stu-id="af780-129">Client Application Reference</span></span>](client-application-reference.md)
</dt> </dl>

 

 





