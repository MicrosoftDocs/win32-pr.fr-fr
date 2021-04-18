---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511850"
---
# <a name="accnamecontainsinvalidstring"></a><span data-ttu-id="7ae21-103">AccNameContainsInvalidString</span><span class="sxs-lookup"><span data-stu-id="7ae21-103">AccNameContainsInvalidString</span></span>

## <a name="text"></a><span data-ttu-id="7ae21-104">Texte</span><span class="sxs-lookup"><span data-stu-id="7ae21-104">Text</span></span>

<span data-ttu-id="7ae21-105">accName ne doit pas contenir la chaîne {0}</span><span class="sxs-lookup"><span data-stu-id="7ae21-105">accName should not contain the string {0}</span></span>

## <a name="type"></a><span data-ttu-id="7ae21-106">Type</span><span class="sxs-lookup"><span data-stu-id="7ae21-106">Type</span></span>

<span data-ttu-id="7ae21-107">Error</span><span class="sxs-lookup"><span data-stu-id="7ae21-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7ae21-108">Description</span><span class="sxs-lookup"><span data-stu-id="7ae21-108">Description</span></span>

<span data-ttu-id="7ae21-109">Le nom d’un élément contient des caractères non valides (ces caractères sont remplacés par AccChecker).</span><span class="sxs-lookup"><span data-stu-id="7ae21-109">The name of an element contains invalid characters (these characters are replaced by AccChecker).</span></span> <span data-ttu-id="7ae21-110">Par exemple, la méthode [**obtenir \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) utilisée pour récupérer le nom MSAA d’un élément retourne une chaîne qui contient des caractères de tabulation, de saut de ligne ou de caractère.</span><span class="sxs-lookup"><span data-stu-id="7ae21-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string that contains tab, newline, or ampersand characters.</span></span>

<span data-ttu-id="7ae21-111">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément peut avoir un nom non significatif et non intuitif.</span><span class="sxs-lookup"><span data-stu-id="7ae21-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7ae21-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="7ae21-112">Possible causes</span></span>

<span data-ttu-id="7ae21-113">Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.</span><span class="sxs-lookup"><span data-stu-id="7ae21-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ae21-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7ae21-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae21-115">**IAccessible :: \_ accName**</span><span class="sxs-lookup"><span data-stu-id="7ae21-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="7ae21-116">Propriété Name</span><span class="sxs-lookup"><span data-stu-id="7ae21-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




