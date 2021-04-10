---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197145"
---
# <a name="incorrectroundtrip"></a><span data-ttu-id="fdca8-103">IncorrectRoundTrip</span><span class="sxs-lookup"><span data-stu-id="fdca8-103">IncorrectRoundTrip</span></span>

## <a name="text"></a><span data-ttu-id="fdca8-104">Texte</span><span class="sxs-lookup"><span data-stu-id="fdca8-104">Text</span></span>

<span data-ttu-id="fdca8-105">Appelez accNavigate ((cliquez sur répéter pour être rappelé dans :), 1, NAVDIR \_ suivant), puis accNavigate ((ouvrir), 2, NAVDIR \_ précédent). l’opération doit être retournée. cliquez sur répéter pour être rappelé dans : (childID = 1), mais retournée cliquez sur répéter pour être rappelé dans :</span><span class="sxs-lookup"><span data-stu-id="fdca8-105">Call to accNavigate((Click Snooze to be reminded again in:), 1, NAVDIR\_NEXT), then accNavigate((Open), 2, NAVDIR\_PREVIOUS), should have returned Click Snooze to be reminded again in:(ChildId=1), but returned Click Snooze to be reminded again in:</span></span>

## <a name="type"></a><span data-ttu-id="fdca8-106">Type</span><span class="sxs-lookup"><span data-stu-id="fdca8-106">Type</span></span>

<span data-ttu-id="fdca8-107">Error</span><span class="sxs-lookup"><span data-stu-id="fdca8-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="fdca8-108">Description</span><span class="sxs-lookup"><span data-stu-id="fdca8-108">Description</span></span>

<span data-ttu-id="fdca8-109">l’utilisation de [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) pour traverser l’arborescence d’éléments de la cible de vérification ne retourne pas le même élément de départ lorsque la direction de traversée est inversée.</span><span class="sxs-lookup"><span data-stu-id="fdca8-109">using [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to traverse the element tree of the verification target does not return the same starting element when the direction of traversal is reversed.</span></span>

![exemple d’implémentation MSAA non valide qui a provoqué une navigation aller-retour incorrecte](images/accchecker-invalid-round-trip.png)

<span data-ttu-id="fdca8-111">Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car le parcours des éléments peut être erratique et imprévisible.</span><span class="sxs-lookup"><span data-stu-id="fdca8-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="fdca8-112">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="fdca8-112">Possible causes</span></span>

<span data-ttu-id="fdca8-113">Implémentation MSAA incorrecte ou non valide.</span><span class="sxs-lookup"><span data-stu-id="fdca8-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdca8-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fdca8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdca8-115">**IAccessible :: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="fdca8-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




