---
description: Cet attribut mesure le remplissage de la barre de l’indicateur de progression.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Progress (attribut de contrôle)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525710"
---
# <a name="progress-control-attribute"></a><span data-ttu-id="8a945-103">Progress (attribut de contrôle)</span><span class="sxs-lookup"><span data-stu-id="8a945-103">Progress Control Attribute</span></span>

<span data-ttu-id="8a945-104">Cet attribut mesure le remplissage de la barre de l’indicateur de progression.</span><span class="sxs-lookup"><span data-stu-id="8a945-104">This attribute measures how far the progress indicator bar is filled.</span></span> <span data-ttu-id="8a945-105">L’enregistrement contient deux entiers et une chaîne.</span><span class="sxs-lookup"><span data-stu-id="8a945-105">The record contains two integers and a string.</span></span> <span data-ttu-id="8a945-106">Le premier nombre correspond à la progression, le deuxième nombre à la plage (le nombre maximal possible de la progression).</span><span class="sxs-lookup"><span data-stu-id="8a945-106">The first number is the progress, the second number is the range (the maximal possible number for the progress).</span></span> <span data-ttu-id="8a945-107">Sur le paramètre, les entiers peuvent être entrés en tant que champs entiers ou chaînes contenant les entiers.</span><span class="sxs-lookup"><span data-stu-id="8a945-107">On setting, the integers can be entered as integer fields or strings containing the integers.</span></span> <span data-ttu-id="8a945-108">Si le deuxième nombre est manquant, il est supposé être la valeur par défaut (1024).</span><span class="sxs-lookup"><span data-stu-id="8a945-108">If the second number is missing it is assumed to be the default (1024).</span></span> <span data-ttu-id="8a945-109">Si la progression est supérieure à la plage, elle est remplacée par la plage.</span><span class="sxs-lookup"><span data-stu-id="8a945-109">If the progress is larger than the range then it is changed to be the range.</span></span> <span data-ttu-id="8a945-110">Le troisième champ est une chaîne, le nom de l’action dont la progression est affichée.</span><span class="sxs-lookup"><span data-stu-id="8a945-110">The third field is a string, the name of the action whose progress is displayed.</span></span>

<span data-ttu-id="8a945-111">Pour obtenir des informations connexes, consultez [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md)et [Ajout d’actions personnalisées au ProgressBar](adding-custom-actions-to-the-progressbar.md).</span><span class="sxs-lookup"><span data-stu-id="8a945-111">For related information, see [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), and [Adding Custom Actions to the ProgressBar](adding-custom-actions-to-the-progressbar.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="8a945-112">Contrôles valides</span><span class="sxs-lookup"><span data-stu-id="8a945-112">Valid Controls</span></span>

[<span data-ttu-id="8a945-113">Barre de progression</span><span class="sxs-lookup"><span data-stu-id="8a945-113">ProgressBar</span></span>](progressbar-control.md)

## <a name="associated-bit-flags"></a><span data-ttu-id="8a945-114">Indicateurs binaires associés</span><span class="sxs-lookup"><span data-stu-id="8a945-114">Associated Bit Flags</span></span>

<span data-ttu-id="8a945-115">Cet attribut n’utilise pas d’indicateurs binaires.</span><span class="sxs-lookup"><span data-stu-id="8a945-115">This attribute does not use bit flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a945-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8a945-116">Remarks</span></span>

<span data-ttu-id="8a945-117">Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).</span><span class="sxs-lookup"><span data-stu-id="8a945-117">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



