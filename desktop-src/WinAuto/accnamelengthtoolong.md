---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510639"
---
# <a name="accnamelengthtoolong"></a><span data-ttu-id="a9696-103">AccNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="a9696-103">AccNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="a9696-104">Texte</span><span class="sxs-lookup"><span data-stu-id="a9696-104">Text</span></span>

<span data-ttu-id="a9696-105">Le nom de l’élément ne doit pas retourner une chaîne de plus de {0} caractères</span><span class="sxs-lookup"><span data-stu-id="a9696-105">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="a9696-106">Type</span><span class="sxs-lookup"><span data-stu-id="a9696-106">Type</span></span>

<span data-ttu-id="a9696-107">Error</span><span class="sxs-lookup"><span data-stu-id="a9696-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="a9696-108">Description</span><span class="sxs-lookup"><span data-stu-id="a9696-108">Description</span></span>

<span data-ttu-id="a9696-109">Le nom d’un élément contient trop de caractères.</span><span class="sxs-lookup"><span data-stu-id="a9696-109">The name of an element contains too many characters.</span></span> <span data-ttu-id="a9696-110">Par exemple, la méthode [**obtenir \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) utilisée pour récupérer le nom MSAA d’un élément retourne une chaîne supérieure à la limite de 32000 caractères.</span><span class="sxs-lookup"><span data-stu-id="a9696-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string greater than the limit of 32000 characters.</span></span>

<span data-ttu-id="a9696-111">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un élément peut avoir un nom non significatif et non intuitif.</span><span class="sxs-lookup"><span data-stu-id="a9696-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a9696-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="a9696-112">Possible causes</span></span>

<span data-ttu-id="a9696-113">Un nom ou une étiquette n’est pas assigné à l’élément ou à son parent.</span><span class="sxs-lookup"><span data-stu-id="a9696-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9696-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9696-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9696-115">**IAccessible :: \_ accName**</span><span class="sxs-lookup"><span data-stu-id="a9696-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="a9696-116">Propriété Name</span><span class="sxs-lookup"><span data-stu-id="a9696-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




