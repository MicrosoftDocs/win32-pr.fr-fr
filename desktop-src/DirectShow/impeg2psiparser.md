---
description: L’implémentation de cette interface est fournie en tant qu’exemple de code avec le kit de développement logiciel (SDK) DirectShow.
ms.assetid: a18fc6b6-f37e-4c87-9150-0504333d33c2
title: Interface IMpeg2PsiParser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser
api_type:
- COM
api_location: ''
ms.openlocfilehash: 51f0f3373c67da75c50ecc2f6bc234e0351f5dc3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517148"
---
# <a name="impeg2psiparser-interface"></a><span data-ttu-id="48651-103">Interface IMpeg2PsiParser</span><span class="sxs-lookup"><span data-stu-id="48651-103">IMpeg2PsiParser interface</span></span>

<span data-ttu-id="48651-104">L’implémentation de cette interface est fournie en tant qu’exemple de code avec le kit de développement logiciel (SDK) DirectShow.</span><span class="sxs-lookup"><span data-stu-id="48651-104">The implementation of this interface is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="48651-105">Il ne s’agit pas d’une API DirectShow prise en charge.</span><span class="sxs-lookup"><span data-stu-id="48651-105">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="48651-106">L' `IMpeg2PsiParser` interface récupère les informations spécifiques au programme (psi) à partir du filtre de l’analyseur psi, fourni dans le kit de développement logiciel (SDK) DirectShow sous la forme d’un exemple de filtre.</span><span class="sxs-lookup"><span data-stu-id="48651-106">The `IMpeg2PsiParser` interface retrieves Program Specific Information (PSI) from the PSI Parser filter, which is provided in the DirectShow SDK as a sample filter.</span></span> <span data-ttu-id="48651-107">Une application peut utiliser ce filtre pour mapper les ID de programme (PID) sur le filtre de démultiplexage MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="48651-107">An application can use this filter to map program IDs (PIDs) on the MPEG-2 Demultiplexer filter.</span></span>

## <a name="members"></a><span data-ttu-id="48651-108">Membres</span><span class="sxs-lookup"><span data-stu-id="48651-108">Members</span></span>

<span data-ttu-id="48651-109">L’interface **IMpeg2PsiParser** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="48651-109">The **IMpeg2PsiParser** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="48651-110">**IMpeg2PsiParser** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="48651-110">**IMpeg2PsiParser** also has these types of members:</span></span>

-   [<span data-ttu-id="48651-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="48651-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="48651-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="48651-112">Methods</span></span>

<span data-ttu-id="48651-113">L’interface **IMpeg2PsiParser** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="48651-113">The **IMpeg2PsiParser** interface has these methods.</span></span>



| <span data-ttu-id="48651-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="48651-114">Method</span></span>                                                                             | <span data-ttu-id="48651-115">Description</span><span class="sxs-lookup"><span data-stu-id="48651-115">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="48651-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48651-116">[**FindRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd407137(v=vs.85))</span></span>         | <span data-ttu-id="48651-117">Recherche le PID d’un programme, en fonction du numéro de programme.</span><span class="sxs-lookup"><span data-stu-id="48651-117">Finds the Program Map Table (PMT) PID for a program, given the program number.</span></span><br/> |
| [<span data-ttu-id="48651-118">**GetCountOfElementaryStreams**</span><span class="sxs-lookup"><span data-stu-id="48651-118">**GetCountOfElementaryStreams**</span></span>](impeg2psiparser-getcountofelementarystreams.md) | <span data-ttu-id="48651-119">Récupère le nombre de flux élémentaires dans un programme spécifié.</span><span class="sxs-lookup"><span data-stu-id="48651-119">Retrieves the number of elementary streams in a specified program.</span></span><br/>             |
| [<span data-ttu-id="48651-120">**GetCountOfPrograms**</span><span class="sxs-lookup"><span data-stu-id="48651-120">**GetCountOfPrograms**</span></span>](impeg2psiparser-getcountofprograms.md)                   | <span data-ttu-id="48651-121">Récupère le nombre de programmes dans le flux de transport.</span><span class="sxs-lookup"><span data-stu-id="48651-121">Retrieves the number of programs in the transport stream.</span></span><br/>                      |
| [<span data-ttu-id="48651-122">**GetPatVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="48651-122">**GetPatVersionNumber**</span></span>](impeg2psiparser-getpatversionnumber.md)                 | <span data-ttu-id="48651-123">Récupère le champ du \_ numéro de version de la table d’association de programmes (Pat).</span><span class="sxs-lookup"><span data-stu-id="48651-123">Retrieves the version\_number field from the Program Association Table (PAT).</span></span><br/>  |
| [<span data-ttu-id="48651-124">**GetPmtVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="48651-124">**GetPmtVersionNumber**</span></span>](impeg2psiparser-getpmtversionnumber.md)                 | <span data-ttu-id="48651-125">Récupère le champ du \_ numéro de version à partir d’un PMT spécifié.</span><span class="sxs-lookup"><span data-stu-id="48651-125">Retrieves the version\_number field from a specified PMT.</span></span><br/>                      |
| <span data-ttu-id="48651-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48651-126">[**GetRecordElementaryPid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85))</span></span>           | <span data-ttu-id="48651-127">Récupère l’attribution de PID pour un flux élémentaire spécifié dans un programme.</span><span class="sxs-lookup"><span data-stu-id="48651-127">Retrieves the PID assignment for a specified elementary stream in a program.</span></span><br/>   |
| <span data-ttu-id="48651-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48651-128">[**GetRecordProgramMapPid**](/previous-versions/windows/desktop/legacy/dd376624(v=vs.85))</span></span>           | <span data-ttu-id="48651-129">Récupère l’attribution de PID pour un PMT spécifié.</span><span class="sxs-lookup"><span data-stu-id="48651-129">Retrieves the PID assignment for a specified PMT.</span></span><br/>                              |
| [<span data-ttu-id="48651-130">**GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="48651-130">**GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)           | <span data-ttu-id="48651-131">Récupère le numéro de programme d’un programme spécifié.</span><span class="sxs-lookup"><span data-stu-id="48651-131">Retrieves the program number for a specified program.</span></span><br/>                          |
| <span data-ttu-id="48651-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="48651-132">[**GetRecordStreamType**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85))</span></span>                 | <span data-ttu-id="48651-133">Récupère le type de flux pour un flux élémentaire spécifié dans un programme.</span><span class="sxs-lookup"><span data-stu-id="48651-133">Retrieves the stream type for a specified elementary stream in a program.</span></span><br/>      |
| [<span data-ttu-id="48651-134">**GetTransportStreamId**</span><span class="sxs-lookup"><span data-stu-id="48651-134">**GetTransportStreamId**</span></span>](impeg2psiparser-gettransportstreamid.md)               | <span data-ttu-id="48651-135">Récupère le \_ \_ champ d’ID de flux de transport à partir de Pat.</span><span class="sxs-lookup"><span data-stu-id="48651-135">Retrieves the transport\_stream\_id field from the PAT.</span></span><br/>                        |



 

## <a name="see-also"></a><span data-ttu-id="48651-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48651-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48651-137">Exemple de filtre de l’analyseur PSI</span><span class="sxs-lookup"><span data-stu-id="48651-137">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 
