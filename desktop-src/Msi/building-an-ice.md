---
description: Si vous ne parvenez pas à trouver les évaluateurs de cohérence internes dont vous avez besoin parmi les actions personnalisées ICE existantes répertoriées dans la référence ICE, vous devrez préparer votre propre glace pour valider votre package.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Génération d’une glace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533852"
---
# <a name="building-an-ice"></a><span data-ttu-id="884d5-103">Génération d’une glace</span><span class="sxs-lookup"><span data-stu-id="884d5-103">Building An ICE</span></span>

<span data-ttu-id="884d5-104">Si vous ne parvenez pas à trouver les [évaluateurs de cohérence internes](internal-consistency-evaluators-ices.md) dont vous avez besoin parmi les actions personnalisées Ice existantes répertoriées dans la [référence Ice](ice-reference.md), vous devrez préparer votre propre glace pour valider votre package.</span><span class="sxs-lookup"><span data-stu-id="884d5-104">If you are unable to find the [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) you need among the existing ICE custom actions listed in the [ICE Reference](ice-reference.md), you will need to prepare your own ICE to validate your package.</span></span>

<span data-ttu-id="884d5-105">Lorsque vous créez des actions personnalisées ICE, vous devez effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="884d5-105">When authoring ICE custom actions you should do the following:</span></span>

-   <span data-ttu-id="884d5-106">Basez le CIEM uniquement sur les actions personnalisées des types répertoriés dans le tableau indiqué.</span><span class="sxs-lookup"><span data-stu-id="884d5-106">Base the ICEs only on custom actions of types listed in the table shown.</span></span>
-   <span data-ttu-id="884d5-107">Appelez [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) et publiez un \_ message de type utilisateur INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="884d5-107">Call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and post an INSTALLMESSAGE\_USER type of message.</span></span> <span data-ttu-id="884d5-108">Lorsque vous créez vos messages ICE, suivez le format du message dans les [instructions relatives aux messages Ice](ice-message-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="884d5-108">When authoring your ICE messages follow the message format in the [ICE Message Guidelines](ice-message-guidelines.md).</span></span>
-   <span data-ttu-id="884d5-109">Écrivez votre glace de sorte qu’elle capture toutes les erreurs d’API et retourne toujours l’erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="884d5-109">Write your ICE such that it captures any API errors and always returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="884d5-110">Cela est nécessaire pour permettre aux actions personnalisées suivantes de s’exécuter après l’échec d’une glace.</span><span class="sxs-lookup"><span data-stu-id="884d5-110">This is necessary to allow subsequent custom actions to run following the failure of an ICE.</span></span>

<span data-ttu-id="884d5-111">Les actions personnalisées ICE sont limitées aux types d’actions personnalisées suivants.</span><span class="sxs-lookup"><span data-stu-id="884d5-111">ICE custom actions are limited to the following custom action types.</span></span>



| <span data-ttu-id="884d5-112">Type d’action personnalisé</span><span class="sxs-lookup"><span data-stu-id="884d5-112">Custom action type</span></span>                                 | <span data-ttu-id="884d5-113">Description</span><span class="sxs-lookup"><span data-stu-id="884d5-113">Description</span></span>               |
|----------------------------------------------------|---------------------------|
| [<span data-ttu-id="884d5-114">Type d’action personnalisé 1</span><span class="sxs-lookup"><span data-stu-id="884d5-114">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="884d5-115">DLL dans un flux binaire</span><span class="sxs-lookup"><span data-stu-id="884d5-115">DLL in binary stream</span></span>      |
| [<span data-ttu-id="884d5-116">Type d’action personnalisé 2</span><span class="sxs-lookup"><span data-stu-id="884d5-116">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="884d5-117">EXE dans un flux binaire</span><span class="sxs-lookup"><span data-stu-id="884d5-117">EXE in binary stream</span></span>      |
| [<span data-ttu-id="884d5-118">Type d’action personnalisé 5</span><span class="sxs-lookup"><span data-stu-id="884d5-118">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="884d5-119">JScript dans un flux binaire</span><span class="sxs-lookup"><span data-stu-id="884d5-119">JScript in binary stream</span></span>  |
| [<span data-ttu-id="884d5-120">Type d’action personnalisé 6</span><span class="sxs-lookup"><span data-stu-id="884d5-120">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="884d5-121">VBScript dans un flux binaire</span><span class="sxs-lookup"><span data-stu-id="884d5-121">VBScript in binary stream</span></span> |
| [<span data-ttu-id="884d5-122">Type d’action personnalisé 37</span><span class="sxs-lookup"><span data-stu-id="884d5-122">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="884d5-123">Code JScript sous forme de chaîne</span><span class="sxs-lookup"><span data-stu-id="884d5-123">JScript code as string</span></span>    |
| [<span data-ttu-id="884d5-124">Type d’action personnalisé 38</span><span class="sxs-lookup"><span data-stu-id="884d5-124">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="884d5-125">Code VBScript sous forme de chaîne</span><span class="sxs-lookup"><span data-stu-id="884d5-125">VBScript code as string</span></span>   |



 

<span data-ttu-id="884d5-126">Lors de la création d’une action personnalisée ICE, n’effectuez pas les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="884d5-126">When authoring an ICE custom action, do not do the following:</span></span>

-   <span data-ttu-id="884d5-127">Ne supposez pas que le descripteur du moteur que la glace reçoit est une instance d’installation de la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="884d5-127">Do not assume that the handle to the engine that the ICE receives is an installation instance of the installer database.</span></span> <span data-ttu-id="884d5-128">S’il ne s’agit pas d’une instance d’installation, certaines propriétés ne sont pas définies, les répertoires source et cible ne sont pas résolus et les États des fonctionnalités actuelles ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="884d5-128">If it is not a installation instance, certain properties are not defined, the source and target directories are not resolved, and current feature states are not defined.</span></span>
-   <span data-ttu-id="884d5-129">Ne vous fiez pas à l’exécution antérieure, ou non, d’une action du programme d’installation, d’une action personnalisée ou d’une autre glace.</span><span class="sxs-lookup"><span data-stu-id="884d5-129">Do not rely on the prior execution, or non-execution, of any installer action, custom action, or another ICE.</span></span> <span data-ttu-id="884d5-130">Comme une ICE précédente peut avoir créé des colonnes temporaires dans une table, les auteurs doivent référencer les colonnes par nom chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="884d5-130">Because a prior ICE may have created temporary columns in any table, authors should reference columns by name whenever possible.</span></span> <span data-ttu-id="884d5-131">Le CIEM doit nettoyer les tables ou colonnes temporaires avant de quitter.</span><span class="sxs-lookup"><span data-stu-id="884d5-131">ICEs should cleanup any temporary columns or tables before they exit.</span></span>
-   <span data-ttu-id="884d5-132">Ne partez pas du principe que les auteurs ont accès à une image du répertoire source de la base de données.</span><span class="sxs-lookup"><span data-stu-id="884d5-132">Do not assume that authors have access to an image of the source directory of the database.</span></span>
-   <span data-ttu-id="884d5-133">Ne partez pas du principe que les modifications apportées à la base de données ne sont pas conservées.</span><span class="sxs-lookup"><span data-stu-id="884d5-133">Do not assume that changes made to the database do not persist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="884d5-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="884d5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="884d5-135">Exemple de code ICE en C++</span><span class="sxs-lookup"><span data-stu-id="884d5-135">Sample ICE in C++</span></span>](sample-ice-in-c-.md)
</dt> <dt>

[<span data-ttu-id="884d5-136">Exemple de code ICE dans VBScript</span><span class="sxs-lookup"><span data-stu-id="884d5-136">Sample ICE in VBScript</span></span>](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



