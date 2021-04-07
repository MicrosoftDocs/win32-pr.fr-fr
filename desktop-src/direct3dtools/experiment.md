---
description: Représente des informations sur une expérience (capture).
MS-HAID: vspixengine.Experiment
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Structure d’expérimentation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 632F1F92-3E32-4B0A-8E38-2613694C267F
api_name:
- Experiment
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e932d2f2b60a72ca167f3f6edd7f4ddae9b68710
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746444"
---
# <a name="span-idvspixengineexperimentspanexperiment-structure"></a><span data-ttu-id="b920e-103"><span id="vspixengine.experiment"></span>Structure d’expérimentation</span><span class="sxs-lookup"><span data-stu-id="b920e-103"><span id="vspixengine.experiment"></span>Experiment structure</span></span>

<span data-ttu-id="b920e-104">Représente des informations sur une expérience (capture).</span><span class="sxs-lookup"><span data-stu-id="b920e-104">Represents information about an experiment (capture).</span></span>

## <a name="syntax"></a><span data-ttu-id="b920e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b920e-105">Syntax</span></span>


```C++
} Experiment;
```

## <a name="members"></a><span data-ttu-id="b920e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b920e-106">Members</span></span>

<span data-ttu-id="b920e-107">**processId**</span><span class="sxs-lookup"><span data-stu-id="b920e-107">**processId**</span></span>  
<span data-ttu-id="b920e-108">ID de processus associé.</span><span class="sxs-lookup"><span data-stu-id="b920e-108">The associated process ID.</span></span>

<span data-ttu-id="b920e-109">**applicationName**</span><span class="sxs-lookup"><span data-stu-id="b920e-109">**applicationName**</span></span>  
<span data-ttu-id="b920e-110">Chaîne COM contenant le nom de l’application sur laquelle exécuter l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b920e-110">A COM string containing the name of the application to run the experiment on.</span></span>

<span data-ttu-id="b920e-111">**commandLineArguments**</span><span class="sxs-lookup"><span data-stu-id="b920e-111">**commandLineArguments**</span></span>  
<span data-ttu-id="b920e-112">Chaîne COM contenant les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b920e-112">A COM string containing the command line arguments.</span></span>

<span data-ttu-id="b920e-113">**workingDirectory**</span><span class="sxs-lookup"><span data-stu-id="b920e-113">**workingDirectory**</span></span>  
<span data-ttu-id="b920e-114">Chaîne COM contenant le chemin d’accès du répertoire de travail.</span><span class="sxs-lookup"><span data-stu-id="b920e-114">A COM string containing the path of the working directory.</span></span>

<span data-ttu-id="b920e-115">**tempPixRunFile**</span><span class="sxs-lookup"><span data-stu-id="b920e-115">**tempPixRunFile**</span></span>  
<span data-ttu-id="b920e-116">Chaîne COM contenant le chemin d’accès du fichier temporaire utilisé pour effectuer l’expérimentation.</span><span class="sxs-lookup"><span data-stu-id="b920e-116">A COM string containing the filepath of the temporary file used to perform the experiment.</span></span>

<span data-ttu-id="b920e-117">**startOption**</span><span class="sxs-lookup"><span data-stu-id="b920e-117">**startOption**</span></span>  
<span data-ttu-id="b920e-118">Option Start associée à l’expérience.</span><span class="sxs-lookup"><span data-stu-id="b920e-118">The start option associated with the experiment.</span></span>

<span data-ttu-id="b920e-119">**experimentType**</span><span class="sxs-lookup"><span data-stu-id="b920e-119">**experimentType**</span></span>  
<span data-ttu-id="b920e-120">Type d’expérience (capture).</span><span class="sxs-lookup"><span data-stu-id="b920e-120">The kind of experiment (capture).</span></span>

<span data-ttu-id="b920e-121">**uiLocale**</span><span class="sxs-lookup"><span data-stu-id="b920e-121">**uiLocale**</span></span>  
<span data-ttu-id="b920e-122">ID des paramètres régionaux utilisés pour les éléments de superposition de l’interface utilisateur pendant le experiement (capture).</span><span class="sxs-lookup"><span data-stu-id="b920e-122">The ID of the locale used for UI overlay elements during the experiement (capture).</span></span> <span data-ttu-id="b920e-123">Cette valeur est transmise à partir de l’hôte (par exemple, Visual Studio Graphics Diagnostics) au moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="b920e-123">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

<span data-ttu-id="b920e-124">**registryRoot**</span><span class="sxs-lookup"><span data-stu-id="b920e-124">**registryRoot**</span></span>  
<span data-ttu-id="b920e-125">Chaîne COM contenant la racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="b920e-125">A COM string containing the registry root.</span></span> <span data-ttu-id="b920e-126">Cette valeur est transmise à partir de l’hôte (par exemple, Visual Studio Graphics Diagnostics) au moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="b920e-126">This is passed from the host (such as Visual Studio Graphics Diagnostics) to the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b920e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b920e-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b920e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b920e-128">Header</span></span></p></td><td><span data-ttu-id="b920e-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b920e-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



