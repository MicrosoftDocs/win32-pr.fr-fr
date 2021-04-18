---
description: Les structures de données utilisées par TSPI sont identiques à celles définies dans les structures TAPI, à l’exception de TUISPICREATEDIALOGINSTANCEPARAMS.
ms.assetid: 99d966ea-49b5-4a84-83a1-99dc8465c751
title: Structures TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e3468171bc160ca03ac9f5501a9eba7fd9221ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519886"
---
# <a name="tspi-structures"></a><span data-ttu-id="5d3fa-103">Structures TSPI</span><span class="sxs-lookup"><span data-stu-id="5d3fa-103">TSPI Structures</span></span>

<span data-ttu-id="5d3fa-104">Les structures de données utilisées par TSPI sont identiques à celles définies dans les [structures TAPI](./tapi-structures.md), à l’exception de [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span><span class="sxs-lookup"><span data-stu-id="5d3fa-104">The data structures TSPI uses are identical to those defined in [TAPI Structures](./tapi-structures.md), with the exception of [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams).</span></span>

<span data-ttu-id="5d3fa-105">Dans le cas de la plupart des structures de données les plus volumineuses, la responsabilité de remplir les membres est divisée entre le fournisseur de services et TAPI.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-105">In the case of most of the larger data structures, the responsibility for filling in members is divided between the service provider and TAPI.</span></span> <span data-ttu-id="5d3fa-106">Le fournisseur de services doit conserver les valeurs présentes dans les membres appartenant à l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-106">The service provider must preserve the values present in members owned by TAPI.</span></span> <span data-ttu-id="5d3fa-107">La description des membres qui doivent être définis par le fournisseur de services et qui doivent être préservés est fournie dans la section Functions dans les fonctions qui font référence à cette structure de données.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-107">The description of which members must be set by the service provider and which must be preserved is provided in the Functions section in the functions that refer to that data structure.</span></span>

<span data-ttu-id="5d3fa-108">Pour chaque structure, la section de référence répertorie les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="5d3fa-108">For each structure, the reference section lists the following items:</span></span>

-   <span data-ttu-id="5d3fa-109">L’objectif de la structure</span><span class="sxs-lookup"><span data-stu-id="5d3fa-109">The purpose of the structure</span></span>
-   <span data-ttu-id="5d3fa-110">Description des valeurs ou des champs</span><span class="sxs-lookup"><span data-stu-id="5d3fa-110">A description of the values or fields</span></span>
-   <span data-ttu-id="5d3fa-111">Description de l’extensibilité de la structure</span><span class="sxs-lookup"><span data-stu-id="5d3fa-111">A description of the structure's extensibility</span></span>
-   <span data-ttu-id="5d3fa-112">Commentaires facultatifs sur l’utilisation de la structure</span><span class="sxs-lookup"><span data-stu-id="5d3fa-112">Optional comments about using the structure</span></span>
-   <span data-ttu-id="5d3fa-113">Références facultatives à d’autres fonctions, messages, constantes ou structures.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-113">Optional references to other functions, messages, constants, or structures.</span></span>

<span data-ttu-id="5d3fa-114">La mémoire pour toutes les structures de données dont la représentation est publiée et partagée par TAPI et le fournisseur de services est allouée par TAPI ou une application utilisant TAPI.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-114">Memory for all data structures whose representation is published and shared by both TAPI and the service provider is allocated by TAPI or an application using TAPI.</span></span> <span data-ttu-id="5d3fa-115">L’interface TAPI transmet un pointeur vers la fonction TSPI qui retourne les informations.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-115">TAPI passes a pointer to the TSPI function that returns the information.</span></span> <span data-ttu-id="5d3fa-116">TSPI remplit la structure de données avec les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-116">TSPI fills the data structure with the requested information.</span></span> <span data-ttu-id="5d3fa-117">Si l’opération est asynchrone, les informations ne sont pas disponibles tant que le rappel de réponse asynchrone n’indique pas la réussite.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-117">If the operation is asynchronous, the information is not available until the asynchronous reply callback indicates success.</span></span>

> [!Note]  
> <span data-ttu-id="5d3fa-118">Certaines structures incluent des champs de taille et de décalage pour définir l’emplacement et la longueur des chaînes dans la partie variable de la structure.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-118">Some structures include Size and Offset fields for defining the location and length of strings in the variable portion of the structure.</span></span> <span data-ttu-id="5d3fa-119">Si le fournisseur de services est invité à ajouter une chaîne alors qu’aucune chaîne n’est disponible, le fournisseur de services doit indiquer cette condition de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d3fa-119">If the service provider is requested to add a string but no string is available, the service provider must indicate this condition in one of these ways:</span></span>
>
> -   <span data-ttu-id="5d3fa-120">Affectez la valeur 0 aux champs taille et décalage.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-120">Set both the Size and Offset fields to 0.</span></span>
> -   <span data-ttu-id="5d3fa-121">Définissez le champ décalage sur une valeur différente de zéro, mais dimensionnez-la sur 0.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-121">Set the Offset field to nonzero but Size to 0.</span></span>
> -   <span data-ttu-id="5d3fa-122">Définissez le champ décalage sur une valeur différente de zéro, la taille sur 1 et l’octet au décalage à 0.</span><span class="sxs-lookup"><span data-stu-id="5d3fa-122">Set the Offset field to nonzero, Size to 1, and the byte at the Offset to 0.</span></span>

 

 

 
