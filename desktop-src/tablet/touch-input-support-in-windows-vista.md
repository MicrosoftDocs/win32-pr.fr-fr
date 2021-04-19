---
description: À compter de Windows Vista, la technologie Tablet PC prend en charge l’entrée tactile sur les Tablet PC avec des digitaliseurs compatibles avec les fonctions tactiles. Cette prise en charge comprend une interface utilisateur améliorée qui vous aide à cibler et à utiliser les fenêtres de commande lors de l’utilisation d’un doigt pour l’entrée.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: Prise en charge des entrées tactiles dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b623630c93c33b846ab1bb491fc56fe46dfe825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534332"
---
# <a name="touch-input-support-in-windows-vista"></a><span data-ttu-id="901cc-104">Prise en charge des entrées tactiles dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="901cc-104">Touch Input Support in Windows Vista</span></span>

<span data-ttu-id="901cc-105">À compter de Windows Vista, la technologie Tablet PC prend en charge l’entrée tactile sur les Tablet PC avec des digitaliseurs compatibles avec les fonctions tactiles.</span><span class="sxs-lookup"><span data-stu-id="901cc-105">Starting with Windows Vista, Tablet PC Technology has support for touch input on Tablet PC's with touch capable digitizers.</span></span> <span data-ttu-id="901cc-106">Cette prise en charge comprend une interface utilisateur améliorée qui vous aide à cibler et à utiliser les fenêtres de commande lors de l’utilisation d’un doigt pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="901cc-106">This support includes an enhanced user interface to aid in targeting and commanding Windows when using a finger for input.</span></span>

## <a name="touch-digitizer-support"></a><span data-ttu-id="901cc-107">Prise en charge du digitaliseur tactile</span><span class="sxs-lookup"><span data-stu-id="901cc-107">Touch Digitizer Support</span></span>

### <a name="pen-and-touch-input-not-exclusive"></a><span data-ttu-id="901cc-108">Entrée Pen et Touch non exclusive</span><span class="sxs-lookup"><span data-stu-id="901cc-108">Pen and Touch Input Not Exclusive</span></span>

<span data-ttu-id="901cc-109">Ne supposez pas que les entrées de stylet et de toucher s’excluent mutuellement dans les applications [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)et [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="901cc-109">Do not assume pen and touch input are mutually exclusive in [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md), and [**RealTimeStylus**](realtimestylus-class.md) applications.</span></span>

<span data-ttu-id="901cc-110">Dans Windows Vista, lorsque le système reconnaît un stylet, il ignore l’entrée tactile.</span><span class="sxs-lookup"><span data-stu-id="901cc-110">In Windows Vista, when the system recognizes a pen it ignores touch input.</span></span> <span data-ttu-id="901cc-111">Autrement dit, le trait tactile se termine et le trait du stylet commence.</span><span class="sxs-lookup"><span data-stu-id="901cc-111">That is, the touch stroke ends and the pen stroke begins.</span></span> <span data-ttu-id="901cc-112">Étant donné que cela peut changer à l’avenir, votre code ne doit pas supposer que les entrées de stylet et de toucher s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="901cc-112">Because this could possibly change in the future, your code should not assume pen and touch input are mutually exclusive.</span></span>

### <a name="other-mouse-message-sources"></a><span data-ttu-id="901cc-113">Autres sources de message de souris</span><span class="sxs-lookup"><span data-stu-id="901cc-113">Other Mouse Message Sources</span></span>

<span data-ttu-id="901cc-114">Il y a d’autres sources de messages de souris, même lorsque l’utilisateur interagit uniquement à l’aide d’un doigt ou d’un stylet.</span><span class="sxs-lookup"><span data-stu-id="901cc-114">There are other sources of mouse messages even when the user is only interacting using finger or pen.</span></span> <span data-ttu-id="901cc-115">Les sources incluent des pavés tactiles, ainsi que le mouvement destiné à permettre à une application derrière une fenêtre superposée de savoir que la souris se déplace au-dessus de l’application.</span><span class="sxs-lookup"><span data-stu-id="901cc-115">Sources include touchpads, as well as movement intended to let an application behind a layered window be aware that the mouse is moving above the application.</span></span>

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a><span data-ttu-id="901cc-116">Activation et désactivation de l’interface utilisateur d’entrée tactile</span><span class="sxs-lookup"><span data-stu-id="901cc-116">Enabling and Disabling the Touch Input User Interface</span></span>

<span data-ttu-id="901cc-117">Vous pouvez activer ou désactiver l’interface utilisateur d’entrée tactile en fonction des exigences de votre application.</span><span class="sxs-lookup"><span data-stu-id="901cc-117">You may wish to enable or disable the touch input user interface depending on the requirements of your application.</span></span> <span data-ttu-id="901cc-118">Pour ce faire, interceptez les messages de fenêtre du système d’exploitation dans une procédure de fenêtre et modifiez le message Windows.</span><span class="sxs-lookup"><span data-stu-id="901cc-118">To accomplish this, intercept operating system window messages in a window procedure and modify the Windows message.</span></span> <span data-ttu-id="901cc-119">Remplacez [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) dans votre application pour intercepter ces messages.</span><span class="sxs-lookup"><span data-stu-id="901cc-119">Override [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) in your application to intercept these messages.</span></span> <span data-ttu-id="901cc-120">Le \# Pseudo-code C suivant illustre l’activation et la désactivation de l’interface utilisateur d’entrée tactile.</span><span class="sxs-lookup"><span data-stu-id="901cc-120">The following C\# pseudo-code shows how to enable and disable the touch input user interface.</span></span> <span data-ttu-id="901cc-121">Le code illustre également l’utilisation de la même technique pour désactiver le mouvement de pression et de blocage.</span><span class="sxs-lookup"><span data-stu-id="901cc-121">The code also shows using the same technique to disable the press-and-hold gesture.</span></span> <span data-ttu-id="901cc-122">Cette méthode fonctionne également pour désactiver le stylet.</span><span class="sxs-lookup"><span data-stu-id="901cc-122">This method also works for disabling the stylus.</span></span>


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="901cc-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="901cc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="901cc-124">Tactile Windows</span><span class="sxs-lookup"><span data-stu-id="901cc-124">Windows Touch</span></span>](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
