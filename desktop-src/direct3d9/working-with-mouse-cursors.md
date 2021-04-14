---
description: Les méthodes de curseur de la souris permettent à l’application de spécifier un curseur de couleur en fournissant une surface qui contient une image.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Utilisation des curseurs de souris (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14855e2d17c9d23f078297840d951b8db338d613
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482416"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a><span data-ttu-id="8f71d-103">Utilisation des curseurs de souris (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8f71d-103">Working with Mouse Cursors (Direct3D 9)</span></span>

<span data-ttu-id="8f71d-104">Les méthodes de curseur de la souris permettent à l’application de spécifier un curseur de couleur en fournissant une surface qui contient une image.</span><span class="sxs-lookup"><span data-stu-id="8f71d-104">The mouse cursor methods enable the application to specify a color cursor by providing a surface that contains an image.</span></span> <span data-ttu-id="8f71d-105">Le système s’assure que ce curseur sera mis à jour à la moitié du taux d’affichage ou plus si la fréquence d’images de l’application est lente.</span><span class="sxs-lookup"><span data-stu-id="8f71d-105">The system will ensure that this cursor will be updated at half the display rate or more if the application's frame rate is slow.</span></span> <span data-ttu-id="8f71d-106">Toutefois, le curseur n’est jamais mis à jour plus fréquemment que la fréquence d’actualisation de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="8f71d-106">However, the cursor will never be updated more frequently than the display refresh rate.</span></span>

<span data-ttu-id="8f71d-107">La position du curseur de la souris est liée au curseur système, mise à l’échelle de manière appropriée pour la résolution spatiale en mode d’affichage actuelle, mais elle peut être déplacée explicitement par l’application.</span><span class="sxs-lookup"><span data-stu-id="8f71d-107">The mouse cursor position is tied to the system cursor, appropriately scaled for the current display mode spatial resolution, but it can be moved explicitly by the application.</span></span> <span data-ttu-id="8f71d-108">Cela est analogue au comportement du curseur de souris système pris en charge par l’API Win32.</span><span class="sxs-lookup"><span data-stu-id="8f71d-108">This is analogous to the behavior of the Win32 API - supported system mouse cursor.</span></span> <span data-ttu-id="8f71d-109">Pour plus d’informations sur l’utilisation d’un curseur de souris dans votre application Direct3D, consultez les rubriques de référence suivantes.</span><span class="sxs-lookup"><span data-stu-id="8f71d-109">For more information about how to use a mouse cursor in your Direct3D application, see the following reference topics.</span></span>

-   [<span data-ttu-id="8f71d-110">**IDirect3DDevice9::ShowCursor**</span><span class="sxs-lookup"><span data-stu-id="8f71d-110">**IDirect3DDevice9::ShowCursor**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [<span data-ttu-id="8f71d-111">**IDirect3DDevice9::SetCursorPosition**</span><span class="sxs-lookup"><span data-stu-id="8f71d-111">**IDirect3DDevice9::SetCursorPosition**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [<span data-ttu-id="8f71d-112">**IDirect3DDevice9::SetCursorProperties**</span><span class="sxs-lookup"><span data-stu-id="8f71d-112">**IDirect3DDevice9::SetCursorProperties**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

<span data-ttu-id="8f71d-113">Direct3D garantit que la souris est prise en charge par les implémentations matérielles ou par le runtime Direct3D qui effectue des opérations blitting accélérées par le matériel lors de l’appel de [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="8f71d-113">Direct3D ensures that the mouse is supported either by hardware implementations or by the Direct3D run time that performs hardware-accelerated blitting operations when calling [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f71d-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8f71d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f71d-115">Conseils de programmation</span><span class="sxs-lookup"><span data-stu-id="8f71d-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
