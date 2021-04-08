---
description: 'Il y a quatre couches dans la bibliothèque d’analyse d’encre : Windows Forms, WPF, COM et la couche de base. Cette section explique quand utiliser chaque couche.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Utilisation de l’API analyse de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951011"
---
# <a name="ink-analysis-api-usage"></a><span data-ttu-id="85b07-104">Utilisation de l’API analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="85b07-104">Ink Analysis API Usage</span></span>

<span data-ttu-id="85b07-105">Il y a quatre couches dans la bibliothèque d’analyse d’encre : Windows Forms, WPF, COM et la couche de base.</span><span class="sxs-lookup"><span data-stu-id="85b07-105">There are four layers to the Ink Analysis library: Windows Forms, WPF, COM, and the base layer.</span></span> <span data-ttu-id="85b07-106">Cette section explique quand utiliser chaque couche.</span><span class="sxs-lookup"><span data-stu-id="85b07-106">This section describes when to use each layer.</span></span>

## <a name="ink-analysis-api-overview"></a><span data-ttu-id="85b07-107">Vue d’ensemble de l’API d’analyse d’encre</span><span class="sxs-lookup"><span data-stu-id="85b07-107">Ink Analysis API Overview</span></span>

<span data-ttu-id="85b07-108">Les bibliothèques d’analyse de l’encre sont conçues pour être utilisées dans un large éventail d’environnements de programmation pris en charge.</span><span class="sxs-lookup"><span data-stu-id="85b07-108">The Ink Analysis libraries are designed to be used in a variety of supported programming environments.</span></span> <span data-ttu-id="85b07-109">Il existe quatre couches de base par lesquelles votre application peut utiliser l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="85b07-109">There are four basic layers through which your application can make use of Ink Analysis.</span></span> <span data-ttu-id="85b07-110">Ces couches sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b07-110">These layers are:</span></span>

-   <span data-ttu-id="85b07-111">Couche Windows Forms</span><span class="sxs-lookup"><span data-stu-id="85b07-111">The Windows Forms layer</span></span>
-   <span data-ttu-id="85b07-112">Couche WPF</span><span class="sxs-lookup"><span data-stu-id="85b07-112">The WPF layer</span></span>
-   <span data-ttu-id="85b07-113">Couche COM</span><span class="sxs-lookup"><span data-stu-id="85b07-113">The COM layer</span></span>
-   <span data-ttu-id="85b07-114">Couche de base</span><span class="sxs-lookup"><span data-stu-id="85b07-114">The base layer</span></span>

### <a name="windows-forms-applications"></a><span data-ttu-id="85b07-115">Applications Windows Forms</span><span class="sxs-lookup"><span data-stu-id="85b07-115">Windows Forms Applications</span></span>

<span data-ttu-id="85b07-116">Vous pouvez utiliser l’API d’analyse d’encre dans votre projet managé en ajoutant une référence aux bibliothèques suivantes :</span><span class="sxs-lookup"><span data-stu-id="85b07-116">You can use the Ink Analysis API in your managed project by adding a reference to the following libraries:</span></span>

-   <span data-ttu-id="85b07-117">Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)</span><span class="sxs-lookup"><span data-stu-id="85b07-117">Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)</span></span>
-   <span data-ttu-id="85b07-118">Bibliothèque d’analyse de documents manuscrits (IACore.dll)</span><span class="sxs-lookup"><span data-stu-id="85b07-118">Ink Document Analysis Library (IACore.dll)</span></span>

<span data-ttu-id="85b07-119">Dans Windows Forms applications, vous utiliserez très probablement les bibliothèques conjointement avec les objets de plateforme Tablet PC standard qui se trouvent dans l’assembly v 1.7 de l’API Microsoft Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="85b07-119">In Windows Forms applications, you will most likely use the libraries in conjunction with the standard Tablet PC platform objects found in the Microsoft Tablet PC API v1.7 assembly.</span></span> <span data-ttu-id="85b07-120">Vérifiez que vous avez également une référence à :</span><span class="sxs-lookup"><span data-stu-id="85b07-120">Be sure you also have a reference to:</span></span>

-   <span data-ttu-id="85b07-121">API Microsoft Tablet PC v 1.7.2600.2180 (Microsoft.Ink.dll)</span><span class="sxs-lookup"><span data-stu-id="85b07-121">Microsoft Tablet PC API v1.7.2600.2180 (Microsoft.Ink.dll)</span></span>

### <a name="windows-presentation-framework-applications"></a><span data-ttu-id="85b07-122">Applications Windows Presentation Framework</span><span class="sxs-lookup"><span data-stu-id="85b07-122">Windows Presentation Framework Applications</span></span>

<span data-ttu-id="85b07-123">Vous pouvez utiliser l’API d’analyse d’encre dans votre projet WPF en ajoutant une référence aux membres de l’analyse d’encre qui sont définis dans l’espace de noms System. Windows. Ink dans l’assembly IAWinFX.dll.</span><span class="sxs-lookup"><span data-stu-id="85b07-123">You can use the Ink Analysis API in your WPF project by adding a reference to the Ink Analysis members that are defined in the System.Windows.Ink namespace in the IAWinFX.dll assembly.</span></span> <span data-ttu-id="85b07-124">Cet assembly est installé par le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="85b07-124">This assembly is installed by the SDK.</span></span>

### <a name="com-applications"></a><span data-ttu-id="85b07-125">Applications COM</span><span class="sxs-lookup"><span data-stu-id="85b07-125">COM Applications</span></span>

<span data-ttu-id="85b07-126">Les applications COM non-Automation doivent utiliser la couche COM des API d’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="85b07-126">Non-Automation COM applications should use the COM layer of the Ink Analysis APIs.</span></span>

<span data-ttu-id="85b07-127">Les objets [ContextNode](/previous-versions/ms551996(v=vs.100)) spécifiques de type, tels que [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))et others, ne sont pas utilisés dans la couche com.</span><span class="sxs-lookup"><span data-stu-id="85b07-127">Type specific [ContextNode](/previous-versions/ms551996(v=vs.100)) objects-such as [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100)), and others-are not used in the COM layer.</span></span> <span data-ttu-id="85b07-128">Au lieu de cela, vous devez utiliser [**IContextNode :: AddPropertyData**](icontextnode-addpropertydata.md) sur l’interface [**IContextNode**](icontextnode.md) standard.</span><span class="sxs-lookup"><span data-stu-id="85b07-128">Rather, you should use the [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) on the standard [**IContextNode**](icontextnode.md) interface.</span></span>

<span data-ttu-id="85b07-129">Vous devez \# inclure « IACom. h ».</span><span class="sxs-lookup"><span data-stu-id="85b07-129">You must \#include "IACom.h".</span></span> <span data-ttu-id="85b07-130">Vous utiliserez très probablement les bibliothèques dans le cadre de l’objet Ink de plateforme Tablet PC. par conséquent, vous devez également \# inclure « msinkaut. h ».</span><span class="sxs-lookup"><span data-stu-id="85b07-130">You will most likely use the libraries in conjunction wit the Tablet PC platform Ink object, so you should also \#include "msinkaut.h".</span></span>

### <a name="rts-and-other-applications"></a><span data-ttu-id="85b07-131">RTS et d’autres applications</span><span class="sxs-lookup"><span data-stu-id="85b07-131">RTS and Other Applications</span></span>

<span data-ttu-id="85b07-132">La couche de base de l’analyse d’encre fonctionne différemment des autres en ce sens qu’elle prend des données de point pour l’analyse plutôt que des objets [Stroke](/previous-versions/ms552692(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="85b07-132">The Ink Analysis base layer works differently than the others in that it takes point data for analysis rather than [Stroke](/previous-versions/ms552692(v=vs.100)) objects.</span></span> <span data-ttu-id="85b07-133">Parmi les exemples d’utilisation directe de la couche de base plutôt que d’utiliser les couches Windows Forms ou COM, citons les applications qui n’utilisent pas les objets Ink de plateforme Tablet PC de première génération, ou les applications qui utilisent les API [**RealTimeStylus**](realtimestylus-class.md) pour gérer l’entrée de stylet au lieu d’utiliser les objets [Ink](/previous-versions/ms583670(v=vs.100)) de plateforme Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="85b07-133">Examples of where you would work with the Base layer directly rather than using the Windows forms or COM layers include applications that do not use first generation Tablet PC Platform Ink objects, or applications that use the [**RealTimeStylus**](realtimestylus-class.md) APIs to manage stylus input rather than using the Tablet PC Platform [Ink](/previous-versions/ms583670(v=vs.100)) objects.</span></span>

## <a name="32-bit-support-only"></a><span data-ttu-id="85b07-134">32 bits pris en charge uniquement</span><span class="sxs-lookup"><span data-stu-id="85b07-134">32-bit Support Only</span></span>

<span data-ttu-id="85b07-135">Notez que les bibliothèques d’analyse de l’encre sont uniquement prises en charge dans les processus 32 bits.</span><span class="sxs-lookup"><span data-stu-id="85b07-135">Note that the Ink Analysis libraries are only supported in 32-bit processes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85b07-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85b07-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b07-137">Présentation de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="85b07-137">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="85b07-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="85b07-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 
