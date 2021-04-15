---
description: Les codes d’erreur suivants sont spécifiques à l’API d’installation.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Codes d’erreur (API du programme d’installation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485536"
---
# <a name="error-codes-setup-api"></a><span data-ttu-id="903e1-103">Codes d’erreur (API du programme d’installation)</span><span class="sxs-lookup"><span data-stu-id="903e1-103">Error Codes (Setup API)</span></span>

<span data-ttu-id="903e1-104">Les codes d’erreur suivants sont spécifiques à l’API d’installation.</span><span class="sxs-lookup"><span data-stu-id="903e1-104">The following error codes are specific to the Setup API.</span></span>



| <span data-ttu-id="903e1-105">Erreurs d’analyse INF</span><span class="sxs-lookup"><span data-stu-id="903e1-105">INF Parsing Errors</span></span>              | <span data-ttu-id="903e1-106">Description</span><span class="sxs-lookup"><span data-stu-id="903e1-106">Description</span></span>                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903e1-107">ERREUR \_ de \_ nom de section attendue \_</span><span class="sxs-lookup"><span data-stu-id="903e1-107">ERROR\_EXPECTED\_SECTION\_NAME</span></span>  | <span data-ttu-id="903e1-108">Un nom de section était attendu et introuvable.</span><span class="sxs-lookup"><span data-stu-id="903e1-108">A section name was expected and not found.</span></span>                                                                          |
| <span data-ttu-id="903e1-109">ERREUR \_ de \_ \_ ligne de nom de section erronée \_</span><span class="sxs-lookup"><span data-stu-id="903e1-109">ERROR\_BAD\_SECTION\_NAME\_LINE</span></span> | <span data-ttu-id="903e1-110">Le format du nom de la section n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="903e1-110">The section name was not of the correct format.</span></span> <span data-ttu-id="903e1-111">(Par exemple, un nom qui ne se termine pas par un crochet droit ( \] ).</span><span class="sxs-lookup"><span data-stu-id="903e1-111">(For example, a name not terminated by a right-hand bracket ( \] ).</span></span> |
| <span data-ttu-id="903e1-112">nom de section d’erreur \_ \_ \_ trop \_ long</span><span class="sxs-lookup"><span data-stu-id="903e1-112">ERROR\_SECTION\_NAME\_TOO\_LONG</span></span> | <span data-ttu-id="903e1-113">Le nom de la section a dépassé la longueur maximale du nom de la \_ coupe Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="903e1-113">The section name exceeded the maximum length of MAX\_SECT\_NAME\_LEN.</span></span>                                               |
| <span data-ttu-id="903e1-114">\_syntaxe générale de l’erreur \_</span><span class="sxs-lookup"><span data-stu-id="903e1-114">ERROR\_GENERAL\_SYNTAX</span></span>          | <span data-ttu-id="903e1-115">La syntaxe générale est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="903e1-115">The general syntax is incorrect.</span></span>                                                                                    |



 



| <span data-ttu-id="903e1-116">Erreurs d’exécution INF</span><span class="sxs-lookup"><span data-stu-id="903e1-116">INF Runtime Errors</span></span>         | <span data-ttu-id="903e1-117">Description</span><span class="sxs-lookup"><span data-stu-id="903e1-117">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903e1-118">ERREUR \_ de \_ style INF incorrect \_</span><span class="sxs-lookup"><span data-stu-id="903e1-118">ERROR\_WRONG\_INF\_STYLE</span></span>   | <span data-ttu-id="903e1-119">Le fichier INF n’est pas du type spécifié dans l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="903e1-119">The INF file is not of the type specified in the function call.</span></span> <span data-ttu-id="903e1-120">Par exemple, cette erreur peut être retournée par la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) si le fichier INF était destiné à une version antérieure de Windows.</span><span class="sxs-lookup"><span data-stu-id="903e1-120">For example, this error may be returned by the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function if the INF file was intended for an early version of Windows.</span></span> |
| <span data-ttu-id="903e1-121">\_section d' \_ erreur \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="903e1-121">ERROR\_SECTION\_NOT\_FOUND</span></span> | <span data-ttu-id="903e1-122">La section est introuvable dans le fichier INF.</span><span class="sxs-lookup"><span data-stu-id="903e1-122">The section was not found in the INF file.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="903e1-123">\_ligne d' \_ erreur \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="903e1-123">ERROR\_LINE\_NOT\_FOUND</span></span>    | <span data-ttu-id="903e1-124">La ligne est introuvable dans la section INF.</span><span class="sxs-lookup"><span data-stu-id="903e1-124">The line was not found in the INF section.</span></span>                                                                                                                                                                                                     |



 

 

 



