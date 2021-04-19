---
description: ICE42 valide que les serveurs InProc ne sont pas liés aux fichiers EXE dans la table de classe. Il vérifie également que seules les classes LocalServer et LocalServer32 ont des arguments et des valeurs DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539108"
---
# <a name="ice42"></a><span data-ttu-id="7b18b-104">ICE42</span><span class="sxs-lookup"><span data-stu-id="7b18b-104">ICE42</span></span>

<span data-ttu-id="7b18b-105">ICE42 valide que les serveurs InProc ne sont pas liés aux fichiers EXE dans la [table de classe](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b18b-105">ICE42 validates that InProc servers are not linked to EXE files in the [Class table](class-table.md).</span></span> <span data-ttu-id="7b18b-106">Il vérifie également que seules les classes LocalServer et LocalServer32 ont des arguments et des valeurs DefInProc.</span><span class="sxs-lookup"><span data-stu-id="7b18b-106">It also validates that only LocalServer and LocalServer32 classes have arguments and DefInProc values.</span></span>

## <a name="result"></a><span data-ttu-id="7b18b-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="7b18b-107">Result</span></span>

<span data-ttu-id="7b18b-108">ICE42 publie une erreur si des serveurs InProc sont liés à des fichiers EXE dans la table de classe.</span><span class="sxs-lookup"><span data-stu-id="7b18b-108">ICE42 posts an error if there are InProc servers linked to EXE files in the Class table.</span></span>

## <a name="example"></a><span data-ttu-id="7b18b-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="7b18b-109">Example</span></span>

<span data-ttu-id="7b18b-110">ICE42 signale les erreurs suivantes pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="7b18b-110">ICE42 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="7b18b-111">Erreur ICE42</span><span class="sxs-lookup"><span data-stu-id="7b18b-111">ICE42 error</span></span>                                                                                                                             | <span data-ttu-id="7b18b-112">Description</span><span class="sxs-lookup"><span data-stu-id="7b18b-112">Description</span></span>                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b18b-113">Le CLSID « {GUID1} » est un serveur INPROC, mais le composant d’implémentation « Composant1 » a un EXE (« test.exe ») comme keyfile.</span><span class="sxs-lookup"><span data-stu-id="7b18b-113">CLSID '{GUID1}' is an InProc server, but the implementing component 'Component1' has an EXE ('test.exe') as its KeyFile.</span></span>                | <span data-ttu-id="7b18b-114">Un fichier exécutable est spécifié en tant que serveur INPROC.</span><span class="sxs-lookup"><span data-stu-id="7b18b-114">There is an executable file specified as an InProc server.</span></span> <span data-ttu-id="7b18b-115">Les fichiers EXE ne peuvent pas être des serveurs InProc.</span><span class="sxs-lookup"><span data-stu-id="7b18b-115">EXE files cannot be InProc servers.</span></span>                                                                                                                            |
| <span data-ttu-id="7b18b-116">Le CLSID « {GUID1} » dans le contexte « InProcServer32 » a un argument.</span><span class="sxs-lookup"><span data-stu-id="7b18b-116">CLSID '{GUID1}' in context 'InProcServer32' has an argument.</span></span> <span data-ttu-id="7b18b-117">Seuls les contextes LocalServer peuvent avoir des arguments.</span><span class="sxs-lookup"><span data-stu-id="7b18b-117">Only LocalServer contexts can have arguments.</span></span>                              | <span data-ttu-id="7b18b-118">Pour corriger cette erreur, supprimez l’argument.</span><span class="sxs-lookup"><span data-stu-id="7b18b-118">To fix this error, remove the argument.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="7b18b-119">Le CLSID « {GUID1} » dans le contexte « InProcServer32 » spécifie une valeur InProc par défaut.</span><span class="sxs-lookup"><span data-stu-id="7b18b-119">CLSID '{GUID1}' in context 'InProcServer32' specifies a default InProc value.</span></span> <span data-ttu-id="7b18b-120">Seuls les contextes LocalServer peuvent avoir des valeurs InProc par défaut.</span><span class="sxs-lookup"><span data-stu-id="7b18b-120">Only LocalServer contexts can have default InProc values.</span></span> | <span data-ttu-id="7b18b-121">Il existe un objet avec une valeur InProc par défaut qui n’est pas un objet opérant dans les contextes LocalServer ou LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="7b18b-121">There is an object with a default InProc value that is not an object operating in the LocalServer or LocalServer32 contexts.</span></span> <span data-ttu-id="7b18b-122">Pour corriger cette erreur, supprimez la valeur DeflnProc ou modifiez le contexte de la classe.</span><span class="sxs-lookup"><span data-stu-id="7b18b-122">To fix this error, remove the DeflnProc value or change the context of the class.</span></span><br/> |



 

<span data-ttu-id="7b18b-123">[Table de classe](class-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="7b18b-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="7b18b-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="7b18b-124">CLSID</span></span>   | <span data-ttu-id="7b18b-125">Context</span><span class="sxs-lookup"><span data-stu-id="7b18b-125">Context</span></span>        | <span data-ttu-id="7b18b-126">-\_</span><span class="sxs-lookup"><span data-stu-id="7b18b-126">Component\_</span></span> | <span data-ttu-id="7b18b-127">DefInProcHandler</span><span class="sxs-lookup"><span data-stu-id="7b18b-127">DefInProcHandler</span></span> | <span data-ttu-id="7b18b-128">Argument</span><span class="sxs-lookup"><span data-stu-id="7b18b-128">Argument</span></span> |
|---------|----------------|-------------|------------------|----------|
| <span data-ttu-id="7b18b-129">GUID1</span><span class="sxs-lookup"><span data-stu-id="7b18b-129">{GUID1}</span></span> | <span data-ttu-id="7b18b-130">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="7b18b-130">InProcServer32</span></span> | <span data-ttu-id="7b18b-131">Composant1</span><span class="sxs-lookup"><span data-stu-id="7b18b-131">Component1</span></span>  | <span data-ttu-id="7b18b-132">InProcServer</span><span class="sxs-lookup"><span data-stu-id="7b18b-132">InProcServer</span></span>     | <span data-ttu-id="7b18b-133">Donnée</span><span class="sxs-lookup"><span data-stu-id="7b18b-133">Arg</span></span>      |



 

<span data-ttu-id="7b18b-134">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="7b18b-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="7b18b-135">Composant</span><span class="sxs-lookup"><span data-stu-id="7b18b-135">Component</span></span>  | <span data-ttu-id="7b18b-136">KeyPath</span><span class="sxs-lookup"><span data-stu-id="7b18b-136">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="7b18b-137">Composant1</span><span class="sxs-lookup"><span data-stu-id="7b18b-137">Component1</span></span> | <span data-ttu-id="7b18b-138">Fichier1</span><span class="sxs-lookup"><span data-stu-id="7b18b-138">File1</span></span>   |



 

<span data-ttu-id="7b18b-139">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="7b18b-139">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="7b18b-140">Fichier</span><span class="sxs-lookup"><span data-stu-id="7b18b-140">File</span></span>  | <span data-ttu-id="7b18b-141">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="7b18b-141">Filename</span></span> |
|-------|----------|
| <span data-ttu-id="7b18b-142">Fichier1</span><span class="sxs-lookup"><span data-stu-id="7b18b-142">File1</span></span> | <span data-ttu-id="7b18b-143">test.exe</span><span class="sxs-lookup"><span data-stu-id="7b18b-143">test.exe</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7b18b-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b18b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b18b-145">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="7b18b-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




