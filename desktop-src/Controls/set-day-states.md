---
title: Comment définir les États des jours
description: Cette rubrique montre comment définir les informations d’État du jour. Le contrôle Month Calendar utilise les informations d’État du jour pour déterminer comment il dessine des jours spécifiques dans le contrôle.
ms.assetid: EA92D858-BC80-4D08-9768-29A2BBDF900C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa1fc105c94a15e1a658218013dca00129c883c2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941507"
---
# <a name="how-to-set-day-states"></a><span data-ttu-id="fe89b-104">Comment définir les États des jours</span><span class="sxs-lookup"><span data-stu-id="fe89b-104">How to Set Day States</span></span>

<span data-ttu-id="fe89b-105">Cette rubrique montre comment définir les informations d’État du jour.</span><span class="sxs-lookup"><span data-stu-id="fe89b-105">This topic demonstrates how to set day state information.</span></span> <span data-ttu-id="fe89b-106">Le contrôle Month Calendar utilise les informations d’État du jour pour déterminer comment il dessine des jours spécifiques dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="fe89b-106">The month calendar control uses day state information to determine how it draws specific days within the control.</span></span>

<span data-ttu-id="fe89b-107">Les contrôles de calendrier mensuel qui utilisent les États du jour du support de style [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fe89b-107">Month calendar controls that use the [**MCS\_DAYSTATE**](month-calendar-control-styles.md) style support day states.</span></span> <span data-ttu-id="fe89b-108">Les informations d’État du jour sont exprimées sous la forme d’un type de données 32 bits, [**MONTHDAYSTATE**](monthdaystate.md).</span><span class="sxs-lookup"><span data-stu-id="fe89b-108">Day state information is expressed as a 32-bit data type, [**MONTHDAYSTATE**](monthdaystate.md).</span></span> <span data-ttu-id="fe89b-109">Chaque bit dans un champ de bits **MONTHDAYSTATE** (0 à 30) spécifie l’état d’un jour dans un mois.</span><span class="sxs-lookup"><span data-stu-id="fe89b-109">Each bit in a **MONTHDAYSTATE** bitfield (0 through 30) specifies the state of a day in a month.</span></span> <span data-ttu-id="fe89b-110">Si un bit est activé, le jour correspondant est affiché en gras.</span><span class="sxs-lookup"><span data-stu-id="fe89b-110">If a bit is on, the corresponding day is displayed in bold.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="fe89b-111">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="fe89b-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fe89b-112">Technologies</span><span class="sxs-lookup"><span data-stu-id="fe89b-112">Technologies</span></span>

-   [<span data-ttu-id="fe89b-113">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="fe89b-113">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fe89b-114">Prérequis</span><span class="sxs-lookup"><span data-stu-id="fe89b-114">Prerequisites</span></span>

-   <span data-ttu-id="fe89b-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="fe89b-115">C/C++</span></span>
-   <span data-ttu-id="fe89b-116">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="fe89b-116">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fe89b-117">Instructions</span><span class="sxs-lookup"><span data-stu-id="fe89b-117">Instructions</span></span>


<span data-ttu-id="fe89b-118">Une application peut définir explicitement des informations d’état de jour en envoyant le message [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) ou en utilisant la macro correspondante, [**calendrier monthcal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="fe89b-118">An application can explicitly set day state information by sending the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message or by using the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="fe89b-119">Toutefois, les informations d’État du jour sont généralement définies en réponse au code de notification [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , qui est envoyé chaque fois que le contrôle doit être actualisé car, par exemple, un autre mois a fait défiler la vue.</span><span class="sxs-lookup"><span data-stu-id="fe89b-119">However, day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed because, for example, a different month has scrolled into view.</span></span>

<span data-ttu-id="fe89b-120">L’exemple de code suivant montre comment traiter le code de notification [MCN \_ GETDAYSTATE](mcn-getdaystate.md) dans un gestionnaire de messages [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fe89b-120">The following example code shows how to process the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code in a [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="fe89b-121">Il traite MCN \_ GETDAYSTATE en spécifiant que le premier et le quinzième jour de chaque mois visible doivent être mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="fe89b-121">It processes MCN\_GETDAYSTATE by specifying that the first and fifteenth day of each visible month should be highlighted.</span></span> <span data-ttu-id="fe89b-122">Le membre **cDayState** de la structure [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) spécifie le nombre de valeurs [**MONTHDAYSTATE**](monthdaystate.md) nécessaires dans le tableau, qui reçoit une taille maximale arbitraire.</span><span class="sxs-lookup"><span data-stu-id="fe89b-122">The **cDayState** member of the [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) structure specifies the number of [**MONTHDAYSTATE**](monthdaystate.md) values that are needed in the array, which is given an arbitrary maximum size.</span></span> <span data-ttu-id="fe89b-123">Le code effectue ensuite une boucle pour définir les bits appropriés dans chaque élément valide du tableau, à l’aide de la macro **BOLDDAY** définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="fe89b-123">The code then loops to set the appropriate bits in each valid element of the array, using the application-defined **BOLDDAY** macro.</span></span>



```C++
    #define BOLDDAY(ds, iDay)  \
        if (iDay > 0 && iDay < 32)(ds) |= (0x00000001 << (iDay - 1))

    case WM_NOTIFY:
            if (((LPNMHDR)lParam)->code == MCN_GETDAYSTATE)
            {
                MONTHDAYSTATE rgMonths[12] = { 0 };
                int cMonths = ((NMDAYSTATE*)lParam)->cDayState;
                for (int i = 0; i < cMonths; i++)
                {
                    BOLDDAY(rgMonths[i], 1);
                    BOLDDAY(rgMonths[i], 15);
                }
                ((NMDAYSTATE*)lParam)->prgDayState = rgMonths;
                return TRUE;
            }
            break;
```



## <a name="related-topics"></a><span data-ttu-id="fe89b-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe89b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe89b-125">Référence du contrôle Month Calendar</span><span class="sxs-lookup"><span data-stu-id="fe89b-125">Month Calendar Control Reference</span></span>](bumper-month-calendar-month-calendar-control-reference.md)
</dt> <dt>

[<span data-ttu-id="fe89b-126">À propos des contrôles Month Calendar</span><span class="sxs-lookup"><span data-stu-id="fe89b-126">About Month Calendar Controls</span></span>](month-calendar-controls.md)
</dt> <dt>

[<span data-ttu-id="fe89b-127">Utilisation des contrôles Month Calendar</span><span class="sxs-lookup"><span data-stu-id="fe89b-127">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 




