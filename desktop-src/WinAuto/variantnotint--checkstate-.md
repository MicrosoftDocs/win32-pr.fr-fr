---
title: VariantNotInt (CheckState)
description: VariantNotInt (CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196785"
---
# <a name="variantnotint-checkstate"></a><span data-ttu-id="1ee8e-103">VariantNotInt (CheckState)</span><span class="sxs-lookup"><span data-stu-id="1ee8e-103">VariantNotInt (CheckState)</span></span>

## <a name="text"></a><span data-ttu-id="1ee8e-104">Texte</span><span class="sxs-lookup"><span data-stu-id="1ee8e-104">Text</span></span>

<span data-ttu-id="1ee8e-105">La variante retournée par {0} doit être un {1} , mais est un {2} .</span><span class="sxs-lookup"><span data-stu-id="1ee8e-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="1ee8e-106">Type</span><span class="sxs-lookup"><span data-stu-id="1ee8e-106">Type</span></span>

<span data-ttu-id="1ee8e-107">Error</span><span class="sxs-lookup"><span data-stu-id="1ee8e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="1ee8e-108">Description</span><span class="sxs-lookup"><span data-stu-id="1ee8e-108">Description</span></span>

<span data-ttu-id="1ee8e-109">Un élément signale un État MSAA non valide.</span><span class="sxs-lookup"><span data-stu-id="1ee8e-109">An element is reporting an invalid MSAA state.</span></span> <span data-ttu-id="1ee8e-110">Par exemple, la méthode [**obtenir \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) utilisée pour récupérer l’État MSAA d’un élément doit retourner une valeur entière qui représente l’une des constantes d’État MSAA, mais qui retourne une autre variante à la place.</span><span class="sxs-lookup"><span data-stu-id="1ee8e-110">For example, the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method used to retrieve the MSAA state of an element should return an integer value that represents one of the MSAA state constants, but is returning another variant instead.</span></span>

<span data-ttu-id="1ee8e-111">Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car un état d’élément incorrect peut être signalé à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1ee8e-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="1ee8e-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="1ee8e-112">Possible causes</span></span>

<span data-ttu-id="1ee8e-113">L’État MSAA de l’élément ou de son parent est incorrect.</span><span class="sxs-lookup"><span data-stu-id="1ee8e-113">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ee8e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ee8e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ee8e-115">**IAccessible :: \_ accState**</span><span class="sxs-lookup"><span data-stu-id="1ee8e-115">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="1ee8e-116">**Constantes d’état d’objet**</span><span class="sxs-lookup"><span data-stu-id="1ee8e-116">**Object State Constants**</span></span>](object-state-constants.md)
</dt> </dl>

 

 




