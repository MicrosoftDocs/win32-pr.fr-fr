---
title: Comment implémenter des info-bulles pour les icônes de barre d’État
description: Une méthode non intrusive pour afficher un message explicatif pour une icône de barre d’état consiste à implémenter une info-bulle. L’info-bulle disparaît lorsque vous cliquez dessus, mais vous pouvez également spécifier une valeur de délai d’attente.
ms.assetid: AA7F17F2-63A4-4954-9DAB-788B73984628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 277fb8d15654ae51565c1a461a9a8414d3e9213c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463786"
---
# <a name="how-to-implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="8571d-104">Comment implémenter des info-bulles pour les icônes de barre d’État</span><span class="sxs-lookup"><span data-stu-id="8571d-104">How to Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="8571d-105">Une méthode non intrusive pour afficher un message explicatif pour une icône de barre d’état consiste à implémenter une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="8571d-105">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="8571d-106">L’info-bulle disparaît lorsque vous cliquez dessus, mais vous pouvez également spécifier une valeur de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="8571d-106">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8571d-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="8571d-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8571d-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="8571d-108">Technologies</span></span>

-   [<span data-ttu-id="8571d-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="8571d-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8571d-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="8571d-110">Prerequisites</span></span>

-   <span data-ttu-id="8571d-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="8571d-111">C/C++</span></span>
-   <span data-ttu-id="8571d-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="8571d-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8571d-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="8571d-113">Instructions</span></span>

### <a name="implement-tooltips-for-status-bar-icons"></a><span data-ttu-id="8571d-114">Implémenter des info-bulles pour les icônes de barre d’État</span><span class="sxs-lookup"><span data-stu-id="8571d-114">Implement Tooltips for Status Bar Icons</span></span>

<span data-ttu-id="8571d-115">Le fragment de code suivant montre comment ajouter une info-bulle à une icône de barre d’État.</span><span class="sxs-lookup"><span data-stu-id="8571d-115">The following code fragment illustrates how to add a balloon tooltip to a status bar icon.</span></span>


```C++
#define ARRAYSIZE(a) (sizeof(a)/sizeof(a[0]))

NOTIFYICONDATA IconData = {0};

IconData.cbSize = sizeof(IconData);
IconData.hWnd   = hwndNI;
IconData.uFlags = NIF_INFO;

HRESULT hr = StringCchCopy(IconData.szInfo, 
                           ARRAYSIZE(IconData.szInfo), 
                           TEXT("Your message text goes here."));

if(FAILED(hr))
{
  // TODO: Write an error handler in case the call to StringCchCopy fails.
}
IconData.uTimeout = 15000; // in milliseconds

Shell_NotifyIcon(NIM_MODIFY, &IconData);
            
```



## <a name="remarks"></a><span data-ttu-id="8571d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8571d-116">Remarks</span></span>

<span data-ttu-id="8571d-117">Pour obtenir une présentation détaillée de la barre d’État, consultez [la barre des tâches](/windows/desktop/shell/taskbar).</span><span class="sxs-lookup"><span data-stu-id="8571d-117">For a detailed discussion of the status bar, see [The Taskbar](/windows/desktop/shell/taskbar).</span></span>

<span data-ttu-id="8571d-118">Pour afficher une info-bulle, vous devez définir l' \_ indicateur d’informations NSI dans la structure [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) et utiliser les membres **szInfo** et **uTimeout** pour spécifier le texte d’info-bulle et la durée du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="8571d-118">To display a balloon tooltip, you need to set the NIF\_INFO flag in the [**NOTIFYICONDATA**](/windows/desktop/api/shellapi/ns-shellapi-notifyicondataa) structure, and use the **szInfo** and **uTimeout** members to specify the tooltip text and time-out duration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8571d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8571d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8571d-120">Utilisation des contrôles ToolTip</span><span class="sxs-lookup"><span data-stu-id="8571d-120">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 