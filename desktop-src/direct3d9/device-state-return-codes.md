---
description: Liste de certains des codes de retour possibles pour les méthodes et les fonctions.
ms.assetid: 391b56a1-d0aa-4d35-8dba-cf7de66513d8
title: S_PRESENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6cd860fcc8268bf2b63a9498b9960da359ca210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999336"
---
# <a name="s_present"></a><span data-ttu-id="e4a0c-103">\_présente</span><span class="sxs-lookup"><span data-stu-id="e4a0c-103">S\_PRESENT</span></span>

<span data-ttu-id="e4a0c-104">Liste de certains des codes de retour possibles pour les méthodes et les fonctions.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-104">A list of some of the possible return codes for methods and functions.</span></span>



| <span data-ttu-id="e4a0c-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="e4a0c-105">\#define</span></span>                  | <span data-ttu-id="e4a0c-106">Description</span><span class="sxs-lookup"><span data-stu-id="e4a0c-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4a0c-107">\_OK</span><span class="sxs-lookup"><span data-stu-id="e4a0c-107">S\_OK</span></span>                     | <span data-ttu-id="e4a0c-108">L’appareil s’exécute normalement et peut être utilisé pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-108">The device is running normally and can be used for rendering.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e4a0c-109">\_bloqués présente \_</span><span class="sxs-lookup"><span data-stu-id="e4a0c-109">S\_PRESENT\_OCCLUDED</span></span>      | <span data-ttu-id="e4a0c-110">La zone de présentation est bloqués.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-110">The presentation area is occluded.</span></span> <span data-ttu-id="e4a0c-111">L’occlusion signifie que la fenêtre de présentation est réduite ou qu’un autre périphérique est passé en mode plein écran sur le même moniteur que la fenêtre de présentation et que la fenêtre de présentation est entièrement sur ce moniteur.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-111">Occlusion means that the presentation window is minimized or another device entered the fullscreen mode on the same monitor as the presentation window and the presentation window is completely on that monitor.</span></span> <span data-ttu-id="e4a0c-112">L’occlusion ne se produira pas si la zone cliente est couverte par une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-112">Occlusion will not occur if the client area is covered by another Window.</span></span><br/> <span data-ttu-id="e4a0c-113">Les applications bloqués peuvent continuer le rendu et tous les appels échouent, mais la fenêtre de présentation bloqués ne sera pas mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-113">Occluded applications can continue rendering and all calls will succeed, but the occluded presentation window will not be updated.</span></span> <span data-ttu-id="e4a0c-114">De préférence, l’application doit arrêter le rendu dans la fenêtre de présentation à l’aide de l’appareil et continuer l’appel de [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) jusqu’à ce que la valeur de l’appel de la \_ méthode s OK ou du \_ \_ mode actuel \_</span><span class="sxs-lookup"><span data-stu-id="e4a0c-114">Preferably the application should stop rendering to the presentation window using the device and keep calling [**CheckDeviceState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate) until S\_OK or S\_PRESENT\_MODE\_CHANGED returns.</span></span><br/> |
| <span data-ttu-id="e4a0c-115">le \_ mode actuel des S est \_ \_ modifié</span><span class="sxs-lookup"><span data-stu-id="e4a0c-115">S\_PRESENT\_MODE\_CHANGED</span></span> | <span data-ttu-id="e4a0c-116">Le mode d’affichage du Bureau a été modifié.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-116">The desktop display mode has been changed.</span></span> <span data-ttu-id="e4a0c-117">L’application peut continuer le rendu, mais il peut y avoir une conversion/étirement de couleurs.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-117">The application can continue rendering, but there might be color conversion/stretching.</span></span> <span data-ttu-id="e4a0c-118">Choisissez un format de mémoire tampon d’arrière-plan similaire au mode d’affichage actuel et appelez Reset pour recréer les chaînes de permutation.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-118">Pick a back buffer format similar to the current display mode, and call Reset to recreate the swap chains.</span></span> <span data-ttu-id="e4a0c-119">L’appareil restera dans cet État après l’appel d’une réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="e4a0c-119">The device will leave this state after a Reset is called.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

<span data-ttu-id="e4a0c-120">Les autres codes d’erreur sont contenus dans [D3DERR](d3derr.md).</span><span class="sxs-lookup"><span data-stu-id="e4a0c-120">Other error codes are contained in [D3DERR](d3derr.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4a0c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e4a0c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4a0c-122">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="e4a0c-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




