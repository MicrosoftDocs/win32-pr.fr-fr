---
description: Ce guide de démarrage rapide montre comment déclencher une notification toast à partir d’une application de bureau.
title: Envoi d’une notification toast à partir du Bureau
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866149"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a><span data-ttu-id="5b76a-103">Démarrage rapide : envoi d’une notification toast à partir du Bureau</span><span class="sxs-lookup"><span data-stu-id="5b76a-103">Quickstart: Sending a toast notification from the desktop</span></span>

<span data-ttu-id="5b76a-104">Ce guide de démarrage rapide montre comment déclencher une notification toast à partir d’une application de bureau.</span><span class="sxs-lookup"><span data-stu-id="5b76a-104">This quickstart shows how to raise a toast notification from a desktop app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b76a-105">Prérequis</span><span class="sxs-lookup"><span data-stu-id="5b76a-105">Prerequisites</span></span>

-   <span data-ttu-id="5b76a-106">Bibliothèques</span><span class="sxs-lookup"><span data-stu-id="5b76a-106">Libraries</span></span>
    -   <span data-ttu-id="5b76a-107">C++ : Runtime. Object. lib</span><span class="sxs-lookup"><span data-stu-id="5b76a-107">C++: Runtime.object.lib</span></span>
    -   <span data-ttu-id="5b76a-108">C \# : Windows. Winmd</span><span class="sxs-lookup"><span data-stu-id="5b76a-108">C\#: Windows.Winmd</span></span>
-   <span data-ttu-id="5b76a-109">Un raccourci vers votre application, avec un [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), doit être installé sur l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="5b76a-109">A shortcut to your app, with a [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), must be installed to the Start screen.</span></span> <span data-ttu-id="5b76a-110">Notez, cependant, qu’il n’est pas nécessaire d’épingler à l’écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="5b76a-110">Note, however, that it does not need to be pinned to the Start screen.</span></span> <span data-ttu-id="5b76a-111">Pour plus d’informations, consultez [Comment activer les notifications de Toast de bureau par le biais d’une AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span><span class="sxs-lookup"><span data-stu-id="5b76a-111">For more information, see [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).</span></span>
-   <span data-ttu-id="5b76a-112">Une version de Microsoft Visual Studio qui prend en charge au moins Windows 8</span><span class="sxs-lookup"><span data-stu-id="5b76a-112">A version of Microsoft Visual Studio that supports at least Windows 8</span></span>

## <a name="instructions"></a><span data-ttu-id="5b76a-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="5b76a-113">Instructions</span></span>

### <a name="1-create-your-toast-content"></a><span data-ttu-id="5b76a-114">1. créer votre contenu Toast</span><span class="sxs-lookup"><span data-stu-id="5b76a-114">1. Create your toast content</span></span>

> [!Note]  
> <span data-ttu-id="5b76a-115">Lorsque vous spécifiez un modèle de Toast qui comprend une image, sachez que les applications de bureau peuvent utiliser uniquement des images locales. les images Web ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5b76a-115">When you specify a toast template that includes an image, be aware that desktop apps can use only local images; web images are not supported.</span></span> <span data-ttu-id="5b76a-116">En outre, le chemin d’accès au fichier image local doit être fourni sous la forme d’un chemin d’accès absolu (non relatif).</span><span class="sxs-lookup"><span data-stu-id="5b76a-116">Also, the path to the local image file must be provided as an absolute (not relative) path.</span></span>

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a><span data-ttu-id="5b76a-117">2. créer et attacher les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="5b76a-117">2. Create and attach the event handlers</span></span>

<span data-ttu-id="5b76a-118">Inscrire des gestionnaires pour les événements Toast : activé, ignoré et échec.</span><span class="sxs-lookup"><span data-stu-id="5b76a-118">Register handlers for the toast events: Activated, Dismissed, and Failed.</span></span> <span data-ttu-id="5b76a-119">Une application de bureau doit au moins s’abonner à l’événement activé pour pouvoir gérer l’activation attendue de l’application à partir du Toast lorsque l’utilisateur la sélectionne.</span><span class="sxs-lookup"><span data-stu-id="5b76a-119">A desktop app must at least subscribe to the Activated event so that it can handle the expected activation of the app from the toast when the user selects it.</span></span>


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a><span data-ttu-id="5b76a-120">3. envoyer le Toast</span><span class="sxs-lookup"><span data-stu-id="5b76a-120">3. Send the toast</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b76a-121">Vous devez inclure la [AppUserModelID](../properties/props-system-appusermodel-id.md) du raccourci de votre application sur l’écran de démarrage chaque fois que vous appelez [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="5b76a-121">You must include the [AppUserModelID](../properties/props-system-appusermodel-id.md) of your app's shortcut on the Start screen each time that you call [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041).</span></span> <span data-ttu-id="5b76a-122">Si vous ne le faites pas, votre toast ne s’affichera pas.</span><span class="sxs-lookup"><span data-stu-id="5b76a-122">If you fail to do this, your toast will not be displayed.</span></span>

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a><span data-ttu-id="5b76a-123">4. gérer les rappels</span><span class="sxs-lookup"><span data-stu-id="5b76a-123">4. Handle the callbacks</span></span>

<span data-ttu-id="5b76a-124">Placez la fenêtre de votre application au premier plan si elle reçoit un rappel « activé » de la notification Toast.</span><span class="sxs-lookup"><span data-stu-id="5b76a-124">Bring your app's window to the foreground if it receives an "activated" callback from the toast notification.</span></span> <span data-ttu-id="5b76a-125">Lorsqu’un utilisateur sélectionne un toast, l’attente est que l’application est lancée vers une vue relative au contenu de ce Toast.</span><span class="sxs-lookup"><span data-stu-id="5b76a-125">When a user selects a toast, the expectation is that the app will be launched to a view related to the content of that toast..</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b76a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b76a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b76a-127">Exemple d’envoi de notifications toast à partir d’applications de bureau</span><span class="sxs-lookup"><span data-stu-id="5b76a-127">Sending toast notifications from desktop apps sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[<span data-ttu-id="5b76a-128">Guide pratique pour activer les notifications toast de bureau via un AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="5b76a-128">How to enable desktop toast notifications through an AppUserModelID</span></span>](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[<span data-ttu-id="5b76a-129">Schéma de Toast XML</span><span class="sxs-lookup"><span data-stu-id="5b76a-129">Toast XML schema</span></span>](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

<span data-ttu-id="5b76a-130">[Présentation des notifications Toast](/previous-versions/windows/apps/hh779727(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-130">[Toast notification overview](/previous-versions/windows/apps/hh779727(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="5b76a-131">[Démarrage rapide : envoi d’une notification Toast](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-131">[Quickstart: Sending a toast notification](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="5b76a-132">[Démarrage rapide : envoi d’une notification push Toast](/previous-versions/windows/hh761487(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-132">[Quickstart: Sending a toast push notification](/previous-versions/windows/hh761487(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="5b76a-133">Instructions et liste de vérification pour les notifications Toast</span><span class="sxs-lookup"><span data-stu-id="5b76a-133">Guidelines and checklist for toast notifications</span></span>](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

<span data-ttu-id="5b76a-134">[Comment choisir et utiliser un modèle de Toast](/previous-versions/windows/apps/hh465448(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-134">[How to choose and use a toast template](/previous-versions/windows/apps/hh465448(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="5b76a-135">[Comment gérer l’activation à partir d’une notification Toast](/previous-versions/windows/apps/hh761468(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-135">[How to handle activation from a toast notification](/previous-versions/windows/apps/hh761468(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="5b76a-136">[Comment s’abonner aux notifications Toast](/previous-versions/windows/apps/hh781238(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-136">[How to opt in for toast notifications](/previous-versions/windows/apps/hh781238(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="5b76a-137">[Choix d’un modèle de Toast](/previous-versions/windows/apps/hh761494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-137">[Choosing a toast template](/previous-versions/windows/apps/hh761494(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="5b76a-138">[Options audio Toast](/previous-versions/windows/apps/hh761492(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="5b76a-138">[Toast audio options](/previous-versions/windows/apps/hh761492(v=win.10))</span></span>
</dt> </dl>

 

 
