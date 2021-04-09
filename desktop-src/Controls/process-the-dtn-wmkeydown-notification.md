---
title: Comment traiter la notification de DTN_WMKEYDOWN
description: Cette rubrique montre comment traiter une notification DTN \_ WMKEYDOWN. La gestion de ce code de notification permet au propriétaire du contrôle de fournir des réponses spécifiques aux séquences de touches dans les champs de rappel du contrôle.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842909"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a><span data-ttu-id="0c287-104">Comment traiter la notification DTN \_ WMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="0c287-104">How to Process the DTN\_WMKEYDOWN Notification</span></span>

<span data-ttu-id="0c287-105">Cette rubrique montre comment traiter une notification [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="0c287-105">This topic demonstrates how to process a [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span> <span data-ttu-id="0c287-106">La gestion de ce code de notification permet au propriétaire du contrôle de fournir des réponses spécifiques aux séquences de touches dans les champs de rappel du contrôle.</span><span class="sxs-lookup"><span data-stu-id="0c287-106">Handling this notification code allows the owner of the control to provide specific responses to keystrokes within the callback fields of the control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="0c287-107">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="0c287-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="0c287-108">Technologies</span><span class="sxs-lookup"><span data-stu-id="0c287-108">Technologies</span></span>

-   [<span data-ttu-id="0c287-109">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="0c287-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="0c287-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="0c287-110">Prerequisites</span></span>

-   <span data-ttu-id="0c287-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0c287-111">C/C++</span></span>
-   <span data-ttu-id="0c287-112">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="0c287-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="0c287-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="0c287-113">Instructions</span></span>


<span data-ttu-id="0c287-114">Les contrôles de sélecteur de date et d’heure (PAO) envoient le message [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) pour signaler que l’utilisateur a entré une entrée dans un champ de rappel.</span><span class="sxs-lookup"><span data-stu-id="0c287-114">Date and time picker (DTP) controls send the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) message to report that the user has typed input in a callback field.</span></span> <span data-ttu-id="0c287-115">Si vous souhaitez émuler les mêmes réponses de clavier que celles prises en charge pour les champs de PAO standard ou fournir des réponses personnalisées, votre application doit inclure du code pour gérer cette notification.</span><span class="sxs-lookup"><span data-stu-id="0c287-115">If you want to emulate the same keyboard responses that are supported for standard DTP fields or provide custom responses, your application must include code to handle this notification.</span></span>

<span data-ttu-id="0c287-116">L’exemple de code C++ suivant est une fonction définie par l’application qui traite la notification [ \_ WMKEYDOWN DTN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="0c287-116">The following C++ code example is an application-defined function that processes the [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification.</span></span>

<span data-ttu-id="0c287-117">**Avertissement de sécurité :** L’utilisation incorrecte de **lstrcmp** peut compromettre la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="0c287-117">**Security Warning:** Using **lstrcmp** incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="0c287-118">Par exemple, avant d’appeler **lstrcmp** dans l’exemple de code suivant, vous devez vous assurer que les deux chaînes se terminent par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="0c287-118">For example, before calling **lstrcmp** in the following code example, you should make sure the two strings are null-terminated.</span></span> <span data-ttu-id="0c287-119">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="0c287-119">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="0c287-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c287-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c287-121">Utilisation des contrôles de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="0c287-121">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="0c287-122">Référence de contrôle de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="0c287-122">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0c287-123">Sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="0c287-123">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




