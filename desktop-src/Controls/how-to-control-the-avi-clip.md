---
title: Comment contrôler le clip AVI
description: Cette rubrique montre comment utiliser les macros de contrôle d’animation pour lire, arrêter et fermer un clip Audio-Video entrelacé (AVI) associé.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463966"
---
# <a name="how-to-control-the-avi-clip"></a><span data-ttu-id="244e0-103">Comment contrôler le clip AVI</span><span class="sxs-lookup"><span data-stu-id="244e0-103">How to Control the AVI Clip</span></span>

<span data-ttu-id="244e0-104">Cette rubrique montre comment utiliser les macros de contrôle d’animation pour lire, arrêter et fermer un clip Audio-Video entrelacé (AVI) associé.</span><span class="sxs-lookup"><span data-stu-id="244e0-104">This topic demonstrates how to use the animation control macros to play, stop, and close an associated Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="244e0-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="244e0-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="244e0-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="244e0-106">Technologies</span></span>

-   [<span data-ttu-id="244e0-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="244e0-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="244e0-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="244e0-108">Prerequisites</span></span>

-   <span data-ttu-id="244e0-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="244e0-109">C/C++</span></span>
-   <span data-ttu-id="244e0-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="244e0-110">Windows User Interface Programming</span></span>
-   <span data-ttu-id="244e0-111">Fichiers AVI</span><span class="sxs-lookup"><span data-stu-id="244e0-111">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="244e0-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="244e0-112">Instructions</span></span>


<span data-ttu-id="244e0-113">Créez une fonction qui prend comme paramètre un handle vers le contrôle d’animation et un indicateur qui indique l’action à effectuer sur le clip AVI associé.</span><span class="sxs-lookup"><span data-stu-id="244e0-113">Create a function that takes as parameters a handle to the animation control and a flag that indicates the action to be performed on the associated AVI clip.</span></span>

<span data-ttu-id="244e0-114">La fonction de l’exemple C++ suivant appelle l’une des trois macros de contrôle d’animation ([**animer \_ lire**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**animer \_ arrêter**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**animer \_ Fermer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) en fonction de la valeur du paramètre *nsortie* .</span><span class="sxs-lookup"><span data-stu-id="244e0-114">The function in the following C++ example calls one of three animation control macros ([**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) based on the value of the *nAction* parameter.</span></span> <span data-ttu-id="244e0-115">Le handle du contrôle d’animation associé au clip AVI est passé via le paramètre *hwndAnim* .</span><span class="sxs-lookup"><span data-stu-id="244e0-115">The handle to the animation control that is associated with the AVI clip is passed via the *hwndAnim* parameter.</span></span>


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a><span data-ttu-id="244e0-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="244e0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="244e0-117">À propos des contrôles d’animation</span><span class="sxs-lookup"><span data-stu-id="244e0-117">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="244e0-118">Référence de contrôle d’animation</span><span class="sxs-lookup"><span data-stu-id="244e0-118">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="244e0-119">Utilisation de contrôles d’animation</span><span class="sxs-lookup"><span data-stu-id="244e0-119">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="244e0-120">Contrôle d’animation</span><span class="sxs-lookup"><span data-stu-id="244e0-120">Animation Control</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




