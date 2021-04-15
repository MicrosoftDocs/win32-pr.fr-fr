---
description: Introduction à l’utilisation de contrôles sans propriétés de légende pour Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Contrôles sans propriétés de légende
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6c9a52d7c6c89e7233e32f7f5d7dc295bc289e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524380"
---
# <a name="controls-without-caption-properties"></a><span data-ttu-id="62807-103">Contrôles sans propriétés de légende</span><span class="sxs-lookup"><span data-stu-id="62807-103">Controls Without Caption Properties</span></span>

<span data-ttu-id="62807-104">Lorsqu’un contrôle n’a pas sa propre propriété Caption, effectuez les étapes suivantes pour garantir que les aides à l’accessibilité peuvent identifier les contrôles :</span><span class="sxs-lookup"><span data-stu-id="62807-104">When a control does not have its own caption property, take the following steps to ensure that accessibility aids can identify the controls:</span></span>

-   <span data-ttu-id="62807-105">Créez un contrôle de texte statique avec un nom explicite et descriptif.</span><span class="sxs-lookup"><span data-stu-id="62807-105">Create a static text control with a meaningful and descriptive name.</span></span>
-   <span data-ttu-id="62807-106">Placez l’étiquette statique de manière à ce qu’elle précède immédiatement le contrôle référencé, dans l’ordre de tabulation.</span><span class="sxs-lookup"><span data-stu-id="62807-106">Place the static label so it immediately precedes the referenced control, in tab order.</span></span>
-   <span data-ttu-id="62807-107">Assurez-vous que le texte de l’étiquette se termine par un signe deux-points, par exemple, « paramètres : »</span><span class="sxs-lookup"><span data-stu-id="62807-107">Ensure that the label text ends with a colon, for example, "Settings:"</span></span>
-   <span data-ttu-id="62807-108">Placez le texte de l’étiquette immédiatement à gauche ou avant le contrôle référencé.</span><span class="sxs-lookup"><span data-stu-id="62807-108">Position the label text immediately to the left or preceding the referenced control.</span></span>
-   <span data-ttu-id="62807-109">Rendez le texte statique invisible s’il n’est pas approprié de l’afficher visuellement.</span><span class="sxs-lookup"><span data-stu-id="62807-109">Make the static text invisible if it is not appropriate to display it visually.</span></span> <span data-ttu-id="62807-110">Pour ce faire, affectez l’attribut approprié dans le script de ressources.</span><span class="sxs-lookup"><span data-stu-id="62807-110">Do this by assigning the appropriate attribute in the resource script.</span></span> <span data-ttu-id="62807-111">Cela peut être approprié lorsque le nom ou la fonction d’un contrôle est fourni visuellement par d’autres moyens que le contrôle de texte statique, tel qu’un graphique ou une case d’option associée.</span><span class="sxs-lookup"><span data-stu-id="62807-111">This may be appropriate when the name or function of a control is visually provided by means other than static text control, such as a graphic or a related radio button.</span></span>

<span data-ttu-id="62807-112">L’utilisation correcte des contrôles statiques est la seule façon d’implémenter correctement les clés d’accès soulignées pour les contrôles qui n’ont pas d’étiquette intrinsèque.</span><span class="sxs-lookup"><span data-stu-id="62807-112">The proper use of static controls is the only way to correctly implement underlined access keys for controls that do not have intrinsic labels.</span></span> <span data-ttu-id="62807-113">Pour plus d’informations sur l’utilisation de contrôles qui n’ont pas de propriétés de légende, consultez la section [accessibilité](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="62807-113">For more information about using controls that do not have caption properties, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
