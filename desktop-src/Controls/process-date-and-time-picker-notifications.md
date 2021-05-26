---
title: Comment traiter les notifications de sélecteur de date et d’heure
description: Cette section montre comment traiter les notifications de sélecteur de date et d’heure.
ms.assetid: DBF624F0-89E0-435B-BE96-60B7A4CEDA61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa1214ebd671b4ae222990bde4b44586e6d7b11
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424179"
---
# <a name="how-to-process-date-and-time-picker-notifications"></a><span data-ttu-id="38400-103">Comment traiter les notifications de sélecteur de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="38400-103">How to Process Date and Time Picker Notifications</span></span>

<span data-ttu-id="38400-104">Cette section montre comment traiter les notifications de sélecteur de date et d’heure.</span><span class="sxs-lookup"><span data-stu-id="38400-104">This section demonstrates how to process date and time picker notifications.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="38400-105">Ce que vous devez savoir</span><span class="sxs-lookup"><span data-stu-id="38400-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="38400-106">Technologies</span><span class="sxs-lookup"><span data-stu-id="38400-106">Technologies</span></span>

-   [<span data-ttu-id="38400-107">Contrôles Windows</span><span class="sxs-lookup"><span data-stu-id="38400-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="38400-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="38400-108">Prerequisites</span></span>

-   <span data-ttu-id="38400-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="38400-109">C/C++</span></span>
-   <span data-ttu-id="38400-110">Programmation de l’interface utilisateur Windows</span><span class="sxs-lookup"><span data-stu-id="38400-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="38400-111">Instructions</span><span class="sxs-lookup"><span data-stu-id="38400-111">Instructions</span></span>


<span data-ttu-id="38400-112">Un contrôle de sélecteur de date et heure (PAO) envoie des messages de notification à la fenêtre parente lorsque des événements, généralement déclenchés par une entrée de l’utilisateur, se produisent dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="38400-112">A date and time picker (DTP) control sends notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="38400-113">Votre application doit inclure du code pour déterminer le type de message de notification et répondre de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="38400-113">Your application must include code to determine the type of notification message and respond appropriately.</span></span>

<span data-ttu-id="38400-114">Si vous envisagez d’utiliser des champs de rappel avec les contrôles de PAO dans votre application, vous devez être prêt à gérer les codes de notification [DTN \_ FORMATQUERY](dtn-formatquery.md), [DTN \_ ](dtn-format.md)et [DTN \_ WMKEYDOWN](dtn-wmkeydown.md) .</span><span class="sxs-lookup"><span data-stu-id="38400-114">If you plan to use callback fields with the DTP controls in your application, you must be prepared to handle [DTN\_FORMATQUERY](dtn-formatquery.md), [DTN\_FORMAT](dtn-format.md), and [DTN\_WMKEYDOWN](dtn-wmkeydown.md) notification codes.</span></span> <span data-ttu-id="38400-115">Pour plus d’informations sur les champs de rappel, consultez [champs de rappel](date-and-time-picker-controls.md).</span><span class="sxs-lookup"><span data-stu-id="38400-115">For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).</span></span>

<span data-ttu-id="38400-116">L’exemple de code C++ suivant identifie le message de notification envoyé par un contrôle de PAO et appelle la fonction appropriée définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="38400-116">The following C++ code example identifies the notification message sent by a DTP control and calls the appropriate application-defined function.</span></span> <span data-ttu-id="38400-117">Reportez-vous aux rubriques suivantes pour obtenir des exemples de code qui illustrent comment traiter les notifications qui s’affichent dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="38400-117">Refer to the following topics for code examples that illustrate how to process the notifications that appear in this example.</span></span>

|   <span data-ttu-id="38400-118">Rubriques</span><span class="sxs-lookup"><span data-stu-id="38400-118">Topics</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38400-119">Comment traiter la notification DTN \_ DATETIMECHANGE</span><span class="sxs-lookup"><span data-stu-id="38400-119">How to Process the DTN\_DATETIMECHANGE Notification</span></span>](process-the-dtn-datetimechange-notification.md) |
| [<span data-ttu-id="38400-120">Comment traiter la notification DTN \_ FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="38400-120">How to Process the DTN\_FORMATQUERY Notification</span></span>](process-the-dtn-formatquery-notification.md)       |
| [<span data-ttu-id="38400-121">Comment traiter la notification au \_ format DTN</span><span class="sxs-lookup"><span data-stu-id="38400-121">How to Process the DTN\_FORMAT Notification</span></span>](process-the-dtn-format-notfication.md)                  |
| [<span data-ttu-id="38400-122">Comment traiter la notification DTN \_ WMKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="38400-122">How to Process the DTN\_WMKEYDOWN Notification</span></span>](process-the-dtn-wmkeydown-notification.md)           |



 



```C++
BOOL WINAPI DoNotify(HWND hwnd, WPARAM wParam, LPARAM lParam)
{
    LPNMHDR hdr = (LPNMHDR)lParam;

    switch(hdr->code){

        case DTN_DATETIMECHANGE:{
            LPNMDATETIMECHANGE lpChange = (LPNMDATETIMECHANGE)lParam;
            DoDateTimeChange(lpChange);
        }
        break;

        case DTN_FORMATQUERY:{
            LPNMDATETIMEFORMATQUERY lpDTFQuery = (LPNMDATETIMEFORMATQUERY)lParam;

            // Process DTN_FORMATQUERY to ensure that the control
            // displays callback information properly.
            DoFormatQuery(hdr->hwndFrom, lpDTFQuery);
        }
        break;

        case DTN_FORMAT:{
            LPNMDATETIMEFORMAT lpNMFormat = (LPNMDATETIMEFORMAT) lParam;

            // Process DTN_FORMAT to supply information about callback
            // fields (fields) in the DTP control.
            DoFormat(hdr->hwndFrom, lpNMFormat);
        }
        break;

        case DTN_WMKEYDOWN:{
            LPNMDATETIMEWMKEYDOWN lpDTKeystroke = 
                            (LPNMDATETIMEWMKEYDOWN)lParam;

            // Process DTN_WMKEYDOWN to respond to a user's keystroke in
            // a callback field.
            DoWMKeydown(hdr->hwndFrom, lpDTKeystroke);
        }
        break;
    }

    // All of the above notifications require the owner to return zero.
    return FALSE;
}
```



## <a name="related-topics"></a><span data-ttu-id="38400-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38400-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38400-124">Notifications du sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="38400-124">Date and Time Picker Notifications</span></span>](bumper-date-and-time-picker-control-reference-notifications.md)
</dt> <dt>

[<span data-ttu-id="38400-125">Référence de contrôle de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="38400-125">Date and Time Picker Control Reference</span></span>](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[<span data-ttu-id="38400-126">Utilisation des contrôles de sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="38400-126">Using Date and Time Picker Controls</span></span>](using-date-and-time-picker.md)
</dt> <dt>

[<span data-ttu-id="38400-127">Sélecteur de date et heure</span><span class="sxs-lookup"><span data-stu-id="38400-127">Date and Time Picker</span></span>](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




