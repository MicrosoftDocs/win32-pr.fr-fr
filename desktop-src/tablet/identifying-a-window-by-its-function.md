---
description: Description de l’identification d’une fenêtre par sa fonction pour le Tablet PC.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Identification d’une fenêtre par sa fonction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497f660d6690bd4dc37c252f82f2408da3e3655d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515469"
---
# <a name="identifying-a-window-by-its-function"></a><span data-ttu-id="4cb60-103">Identification d’une fenêtre par sa fonction</span><span class="sxs-lookup"><span data-stu-id="4cb60-103">Identifying a Window by Its Function</span></span>

<span data-ttu-id="4cb60-104">Identifiez chaque type de fenêtre en lui assignant une classe de fenêtre unique.</span><span class="sxs-lookup"><span data-stu-id="4cb60-104">Identify each type of window by assigning it a unique window class.</span></span> <span data-ttu-id="4cb60-105">Évitez d’avoir une classe de fenêtre unique utilisée pour un large éventail de fonctions.</span><span class="sxs-lookup"><span data-stu-id="4cb60-105">Avoid having a single window class that is used for a wide variety of functions.</span></span>

<span data-ttu-id="4cb60-106">Les aides à l’accessibilité doivent avoir cette identification pour pouvoir gérer différentes fenêtres au sein de la même application.</span><span class="sxs-lookup"><span data-stu-id="4cb60-106">Accessibility aids must have this identification in order to handle different windows within the same application.</span></span> <span data-ttu-id="4cb60-107">Il peut y avoir des instructions distinctes pour gérer ces fenêtres, telles que l’annonce de zones spécifiques lorsque le contenu change.</span><span class="sxs-lookup"><span data-stu-id="4cb60-107">There may be separate instructions for handling these windows, such as announcing specific areas when the content changes.</span></span>

<span data-ttu-id="4cb60-108">Si vous ne pouvez pas utiliser des classes de fenêtres distinctes, vous pouvez exposer les différences par le biais <entity type="reg"/> de Microsoft Active Accessibility <entity type="reg"/> ou, si nécessaire, par un message de fenêtre privée que vous documentez sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="4cb60-108">If you cannot use separate window classes, you can expose the differences through Microsoft<entity type="reg"/> Active Accessibility<entity type="reg"/>, or if necessary, by a private window message that you document on your website.</span></span>

<span data-ttu-id="4cb60-109">Pour plus d’informations sur l’exposition des classes de fenêtre à l’aide de Active Accessibility, consultez la section [accessibilité](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="4cb60-109">For more information about exposing window classes by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
