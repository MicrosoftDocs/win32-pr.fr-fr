---
title: Comment traiter la notification de DTN_DATETIMECHANGE
description: Cette rubrique montre comment traiter la notification des modifications apportées par l’utilisateur au contrôle de sélecteur de date et d’heure (PAO).
ms.assetid: AE029962-E9D3-47BC-A24F-312B54137F18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434c7ebbda673f76a757375e9a3d23504483d42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941511"
---
# <a name="how-to-process-the-dtn_datetimechange-notification"></a><span data-ttu-id="241d5-103">Comment traiter la notification DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="241d5-103">How to Process the DTN\_DATETIMECHANGE Notification</span></span>

<span data-ttu-id="241d5-104">Cette rubrique montre comment traiter la notification des modifications apportées par l’utilisateur au contrôle de sélecteur de date et d’heure (PAO).</span><span class="sxs-lookup"><span data-stu-id="241d5-104">This topic demonstrates how to process notification of changes, made by the user, to the date and time picker (DTP) control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="241d5-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="241d5-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="241d5-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="241d5-106">Technologies</span></span>

-   [<span data-ttu-id="241d5-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="241d5-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="241d5-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="241d5-108">Prerequisites</span></span>

-   <span data-ttu-id="241d5-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="241d5-109">C/C++</span></span>
-   <span data-ttu-id="241d5-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="241d5-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="241d5-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="241d5-111">Instructions</span></span>


<span data-ttu-id="241d5-112">Un contrôle de PAO envoie le code de notification [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) à chaque fois qu’une modification se produit.</span><span class="sxs-lookup"><span data-stu-id="241d5-112">A DTP control sends the [DTN\_DATETIMECHANGE](dtn-datetimechange.md) notification code whenever a change occurs.</span></span> <span data-ttu-id="241d5-113">Par exemple, cette notification est générée lorsque l’utilisateur modifie l’un des champs du contrôle ou, dans le cas où le contrôle est défini sur le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) , lorsque l’utilisateur modifie l’état de la case à cocher du contrôle.</span><span class="sxs-lookup"><span data-stu-id="241d5-113">For example, this notification will be generated when the user changes one of the fields in the control or, in the case where the control is set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style, when the user changes the state of the control's check box.</span></span>

<span data-ttu-id="241d5-114">Votre application doit inclure du code pour traiter \_ les messages DTN DATETIMECHANGE qui sont envoyés par le contrôle PAO.</span><span class="sxs-lookup"><span data-stu-id="241d5-114">Your application must include code to process DTN\_DATETIMECHANGE messages that are sent by the DTP control.</span></span>

<span data-ttu-id="241d5-115">L’exemple de code C++ suivant est une fonction définie par l’application conçue pour indiquer l’état d’un contrôle PAO défini sur le style **DTS \_ SHOWNONE** .</span><span class="sxs-lookup"><span data-stu-id="241d5-115">The following C++ code example is an application-defined function designed to indicate the state of a DTP control that is set to the **DTS\_SHOWNONE** style.</span></span>



```C++
void WINAPI DoDateTimeChange(LPNMDATETIMECHANGE lpChange)
{
    // If the user has unchecked the DTP's check box, change the
    // text in a static control to show the appropriate message.
    //
    // g_hwndDlg - a program-global address of a dialog box.

    if(lpChange->dwFlags == GDT_NONE)
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Disabled");
    else
        SetDlgItemText(g_hwndDlg, IDC_STATUS, L"Active");
}
```



## <a name="related-topics"></a><span data-ttu-id="241d5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="241d5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="241d5-117">Utilisation des contrôles de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="241d5-117">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="241d5-118">Référence de contrôle de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="241d5-118">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="241d5-119">Sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="241d5-119">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




