---
title: Instructions relatives à l’interface utilisateur pour les extensions de classe d’assistance NDF
description: Lors de la création de votre classe d’assistance, vous devrez créer du texte pour aider l’utilisateur à comprendre la cause d’un incident et les étapes de réparation possibles qui peuvent être effectuées.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104313585"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a><span data-ttu-id="4f508-103">Instructions relatives à l’interface utilisateur pour les extensions de classe d’assistance NDF</span><span class="sxs-lookup"><span data-stu-id="4f508-103">UI guidelines for NDF helper class extensions</span></span>

<span data-ttu-id="4f508-104">Lors de la création de votre classe d’assistance, vous devrez créer du texte pour aider l’utilisateur à comprendre la cause d’un incident et les étapes de réparation possibles qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="4f508-104">When building your helper class, you will need to create text to help the user understand the cause of an incident and the possible repair steps which can be taken.</span></span>

## <a name="root-cause-and-repair"></a><span data-ttu-id="4f508-105">Cause racine et réparation</span><span class="sxs-lookup"><span data-stu-id="4f508-105">Root Cause and Repair</span></span>

<span data-ttu-id="4f508-106">Lorsqu’un incident se produit, une boîte de dialogue s’affiche pour informer l’utilisateur sur ce qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="4f508-106">When an incident occurs, a dialog box will appear to inform the user about what has happened.</span></span> <span data-ttu-id="4f508-107">Le texte que vous créez apparaît dans deux zones distinctes.</span><span class="sxs-lookup"><span data-stu-id="4f508-107">The text that you create will appear in two separate areas.</span></span>

-   <span data-ttu-id="4f508-108">**Cause racine**: brève description de la cause du problème.</span><span class="sxs-lookup"><span data-stu-id="4f508-108">**Root Cause**: A brief description of the cause of the issue.</span></span> <span data-ttu-id="4f508-109">Contient des informations pour aider un administrateur ou un utilisateur expérimenté à résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="4f508-109">Contains information to help an administrator or advanced user troubleshoot the problem.</span></span>
-   <span data-ttu-id="4f508-110">**Réparation**: se développe à la cause racine pour fournir plus de détails sur les étapes qu’un utilisateur peut effectuer, sans trop dépasser.</span><span class="sxs-lookup"><span data-stu-id="4f508-110">**Repair**: Expands on the root cause to provide more details about the steps that a user can take, without getting too lengthy.</span></span>

<span data-ttu-id="4f508-111">Chaque cause racine ou réparation doit avoir un titre et une description.</span><span class="sxs-lookup"><span data-stu-id="4f508-111">Each root cause or repair should have a title and a description.</span></span> <span data-ttu-id="4f508-112">Tout le texte avant le premier \\ caractère « n » sera utilisé pour le titre.</span><span class="sxs-lookup"><span data-stu-id="4f508-112">All text before the first "\\n" character will be used for the title.</span></span> <span data-ttu-id="4f508-113">Tout le texte qui suit le premier \\ caractère « n » (y compris les sauts de ligne suivants) sera utilisé pour la description.</span><span class="sxs-lookup"><span data-stu-id="4f508-113">All text following the first "\\n" character (including any subsequent line breaks) will be used for the description.</span></span>

## <a name="title-guidelines"></a><span data-ttu-id="4f508-114">Directives relatives aux titres</span><span class="sxs-lookup"><span data-stu-id="4f508-114">Title Guidelines</span></span>

<span data-ttu-id="4f508-115">Le titre d’une cause racine ou d’une réparation doit suivre les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f508-115">The title of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="4f508-116">Doit avoir 128 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="4f508-116">Must be 128 characters or fewer.</span></span> <span data-ttu-id="4f508-117">(40 caractères ou moins est recommandé.)</span><span class="sxs-lookup"><span data-stu-id="4f508-117">(40 characters or less is recommended.)</span></span>
-   <span data-ttu-id="4f508-118">Ne doit pas se terminer par un point.</span><span class="sxs-lookup"><span data-stu-id="4f508-118">Should not end with a period.</span></span>

## <a name="description-guidelines"></a><span data-ttu-id="4f508-119">Instructions de description</span><span class="sxs-lookup"><span data-stu-id="4f508-119">Description Guidelines</span></span>

<span data-ttu-id="4f508-120">La description d’une cause racine ou d’une réparation doit suivre les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4f508-120">The description of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="4f508-121">Doit avoir 512 caractères au maximum.</span><span class="sxs-lookup"><span data-stu-id="4f508-121">Must be 512 characters or fewer.</span></span>
-   <span data-ttu-id="4f508-122">Chaque phrase doit se terminer par un point.</span><span class="sxs-lookup"><span data-stu-id="4f508-122">Each sentence should end with a period.</span></span>
-   <span data-ttu-id="4f508-123">Le \\ caractère « n » peut être utilisé pour créer un saut de ligne dans la description.</span><span class="sxs-lookup"><span data-stu-id="4f508-123">The "\\n" character may be used to create a line break in the description.</span></span>

 

 




