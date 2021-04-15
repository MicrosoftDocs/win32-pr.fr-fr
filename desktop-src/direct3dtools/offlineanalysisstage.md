---
description: Énumération utilisée pour indiquer les étapes de la progression de l’analyse des frames.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération OFFLINEANALYSISSTAGE
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85D0288C-113A-4ABE-8EDB-ABB8F009956A
api_name:
- OFFLINEANALYSISSTAGE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf12b70acf70a654fe74b23d4bd3a196467797fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521372"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span data-ttu-id="ab077-103"><span id="vspixengine.offlineanalysisstage"></span>Énumération OFFLINEANALYSISSTAGE</span><span class="sxs-lookup"><span data-stu-id="ab077-103"><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE enumeration</span></span>

<span data-ttu-id="ab077-104">Énumération utilisée pour indiquer les étapes de la progression de l’analyse des frames.</span><span class="sxs-lookup"><span data-stu-id="ab077-104">An enum used to indicate stages of progress in frame analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab077-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab077-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="ab077-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ab077-106">Constants</span></span>

<span data-ttu-id="ab077-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage \_ NotStarted**</span><span class="sxs-lookup"><span data-stu-id="ab077-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage\_NotStarted**</span></span>  
<span data-ttu-id="ab077-108">L’analyse des frames n’a pas encore démarré.</span><span class="sxs-lookup"><span data-stu-id="ab077-108">Frame analysis not yet started.</span></span>

<span data-ttu-id="ab077-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**Initialisation de OfflineAnalysisStage \_**</span><span class="sxs-lookup"><span data-stu-id="ab077-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage\_Initializing**</span></span>  
<span data-ttu-id="ab077-110">Initialisation de l’analyse des frames (demande émise).</span><span class="sxs-lookup"><span data-stu-id="ab077-110">Frame analysis initializing (request issued).</span></span>

<span data-ttu-id="ab077-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage \_ initialisation de \_ LinkOk**</span><span class="sxs-lookup"><span data-stu-id="ab077-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage\_Initializing\_LinkOk**</span></span>  
<span data-ttu-id="ab077-112">Initialisation de l’analyse des frames (lien établi).</span><span class="sxs-lookup"><span data-stu-id="ab077-112">Frame analysis initializing (link established).</span></span>

<span data-ttu-id="ab077-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage \_ initialisation de \_ ManifestOk**</span><span class="sxs-lookup"><span data-stu-id="ab077-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage\_Initializing\_ManifestOk**</span></span>  
<span data-ttu-id="ab077-114">Initialisation de l’analyse des frames (manifeste analysé avec succès).</span><span class="sxs-lookup"><span data-stu-id="ab077-114">Frame analysis initializing (manifest parsed successfully).</span></span>

<span data-ttu-id="ab077-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage \_ initialisation de \_ ToolOk**</span><span class="sxs-lookup"><span data-stu-id="ab077-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage\_Initializing\_ToolOk**</span></span>  
<span data-ttu-id="ab077-116">Initialisation de l’analyse des frames (chargement de l’analyseur).</span><span class="sxs-lookup"><span data-stu-id="ab077-116">Frame analysis initializing (analyzer loading).</span></span>

<span data-ttu-id="ab077-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**\_Analyse OfflineAnalysisStage**</span><span class="sxs-lookup"><span data-stu-id="ab077-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage\_Analyzing**</span></span>  
<span data-ttu-id="ab077-118">L’analyse des frames est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ab077-118">Frame analysis is running.</span></span>

<span data-ttu-id="ab077-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage \_ AnalysisCompleted**</span><span class="sxs-lookup"><span data-stu-id="ab077-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage\_AnalysisCompleted**</span></span>  
<span data-ttu-id="ab077-120">Analyse du frame terminée (événement « terminé » envoyé).</span><span class="sxs-lookup"><span data-stu-id="ab077-120">Frame analysis completed ('complete' event sent).</span></span>

<span data-ttu-id="ab077-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ réussi**</span><span class="sxs-lookup"><span data-stu-id="ab077-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage\_AnalysisCompleted\_Successful**</span></span>  
<span data-ttu-id="ab077-122">L’analyse des frames s’est terminée correctement.</span><span class="sxs-lookup"><span data-stu-id="ab077-122">Frame analysis completed successfully.</span></span>

<span data-ttu-id="ab077-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ OutputFileExists**</span><span class="sxs-lookup"><span data-stu-id="ab077-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage\_AnalysisCompleted\_OutputFileExists**</span></span>  
<span data-ttu-id="ab077-124">L’analyse des frames s’est terminée et le fichier de sortie existe.</span><span class="sxs-lookup"><span data-stu-id="ab077-124">Frame analysis completed and output file exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab077-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab077-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ab077-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab077-126">Header</span></span></p></td><td><span data-ttu-id="ab077-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ab077-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



