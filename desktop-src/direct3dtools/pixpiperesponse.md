---
description: Énumération utilisée pour envoyer des réponses du moteur de capture à Graphics Diagnostics.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération PixPipeResponse
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09ab253be5e02cc7329195016a406758b7a82e2b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515902"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span data-ttu-id="90ca8-103"><span id="vspixengine.pixpiperesponse"></span>Énumération PixPipeResponse</span><span class="sxs-lookup"><span data-stu-id="90ca8-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse enumeration</span></span>

<span data-ttu-id="90ca8-104">Énumération utilisée pour envoyer des réponses du moteur de capture à Graphics Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="90ca8-104">An enum used to send responses from the capture engine to Graphics Diagnostics.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ca8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90ca8-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="90ca8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="90ca8-106">Constants</span></span>

<span data-ttu-id="90ca8-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NOUVELLES \_ données \_ disponibles**</span><span class="sxs-lookup"><span data-stu-id="90ca8-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEW\_DATA\_AVAILABLE**</span></span>  
<span data-ttu-id="90ca8-108">Réponse qui indique que les nouvelles données ont été écrites dans le journal de graphisme et sont prêtes à être lues.</span><span class="sxs-lookup"><span data-stu-id="90ca8-108">A response which indicates that new data has been written to the graphics log and is ready to be read.</span></span>

<span data-ttu-id="90ca8-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**données d’EXPÉRIMENTation \_**</span><span class="sxs-lookup"><span data-stu-id="90ca8-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**EXPERIMENT\_DATA**</span></span>  
<span data-ttu-id="90ca8-110">Réponse qui indique les informations de configuration relatives à la session de capture.</span><span class="sxs-lookup"><span data-stu-id="90ca8-110">A response which indicates configuration information about the capture session.</span></span>

<span data-ttu-id="90ca8-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span><span class="sxs-lookup"><span data-stu-id="90ca8-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span></span>  
<span data-ttu-id="90ca8-112">Réponse indiquant que le moteur de capture a rencontré une erreur.</span><span class="sxs-lookup"><span data-stu-id="90ca8-112">A response which indicates that the capture engine has encountered an error.</span></span>

<span data-ttu-id="90ca8-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="90ca8-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span></span>  
<span data-ttu-id="90ca8-114">Réponse qui indique que le moteur de capture a démarré la capture des informations graphiques.</span><span class="sxs-lookup"><span data-stu-id="90ca8-114">A response which indicates that the capture engine has started capturing graphics information.</span></span> <span data-ttu-id="90ca8-115">Cela ne signifie pas que les données sont disponibles pour être examinées pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="90ca8-115">This does not indicate that data is available to be examined yet.</span></span>

<span data-ttu-id="90ca8-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**données PARTIELles \_**</span><span class="sxs-lookup"><span data-stu-id="90ca8-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIAL\_DATA**</span></span>  
<span data-ttu-id="90ca8-117">Réponse qui indique que des données partielles ont été écrites dans le journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="90ca8-117">A response which indicates that partial data has been written to the graphics log.</span></span>

<span data-ttu-id="90ca8-118"><span id="READY"></span><span id="ready"></span>**MONDIALISABLES**</span><span class="sxs-lookup"><span data-stu-id="90ca8-118"><span id="READY"></span><span id="ready"></span>**READY**</span></span>  
<span data-ttu-id="90ca8-119">Réponse qui indique que le moteur de capture est prêt à capturer les informations graphiques.</span><span class="sxs-lookup"><span data-stu-id="90ca8-119">A response which indicates that the capture engine is ready to start capturing graphics information.</span></span>

<span data-ttu-id="90ca8-120"><span id="DONE"></span><span id="done"></span>**CAS**</span><span class="sxs-lookup"><span data-stu-id="90ca8-120"><span id="DONE"></span><span id="done"></span>**DONE**</span></span>  
<span data-ttu-id="90ca8-121">Interne</span><span class="sxs-lookup"><span data-stu-id="90ca8-121">Internal</span></span>

<span data-ttu-id="90ca8-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span><span class="sxs-lookup"><span data-stu-id="90ca8-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span></span>  
<span data-ttu-id="90ca8-123">Réponse qui indique qu’une capture de frame a démarré.</span><span class="sxs-lookup"><span data-stu-id="90ca8-123">A response which indicates that a frame capture has started.</span></span>

<span data-ttu-id="90ca8-124"><span id="STATUS"></span><span id="status"></span>**STATU**</span><span class="sxs-lookup"><span data-stu-id="90ca8-124"><span id="STATUS"></span><span id="status"></span>**STATUS**</span></span>  
<span data-ttu-id="90ca8-125">Réponse qui indique des informations d’État sur l’application capturée ; par exemple, cadence.</span><span class="sxs-lookup"><span data-stu-id="90ca8-125">A response which indicates status information about the app being captured; for example, framerate.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ca8-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90ca8-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="90ca8-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="90ca8-127">Header</span></span></p></td><td><span data-ttu-id="90ca8-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="90ca8-128">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



