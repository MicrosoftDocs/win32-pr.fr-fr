---
description: Les considérations suivantes relatives au thread de Tablet PC sont spécifiques à la bibliothèque managée.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considérations sur les threads de bibliothèque managée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543724"
---
# <a name="managed-library-threading-considerations"></a><span data-ttu-id="059cb-103">Considérations sur les threads de bibliothèque managée</span><span class="sxs-lookup"><span data-stu-id="059cb-103">Managed Library Threading Considerations</span></span>

<span data-ttu-id="059cb-104">Les considérations suivantes relatives au thread de Tablet PC sont spécifiques à la bibliothèque managée.</span><span class="sxs-lookup"><span data-stu-id="059cb-104">The following Tablet PC threading considerations are specific to the Managed Library.</span></span>

-   [<span data-ttu-id="059cb-105">Sécurité des threads</span><span class="sxs-lookup"><span data-stu-id="059cb-105">Thread-Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="059cb-106">Applications STA et MTA</span><span class="sxs-lookup"><span data-stu-id="059cb-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="059cb-107">Considérations relatives au Threading Windows Forms</span><span class="sxs-lookup"><span data-stu-id="059cb-107">Windows Forms Threading Considerations</span></span>](#windows-forms-threading-considerations)
-   [<span data-ttu-id="059cb-108">Considérations sur le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="059cb-108">Clipboard Considerations</span></span>](#clipboard-considerations)
-   [<span data-ttu-id="059cb-109">Exceptions dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="059cb-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="059cb-110">Suppression d’objets et de contrôles</span><span class="sxs-lookup"><span data-stu-id="059cb-110">Disposing Objects and Controls</span></span>](#disposing-objects-and-controls)
-   [<span data-ttu-id="059cb-111">API StylusInput</span><span class="sxs-lookup"><span data-stu-id="059cb-111">StylusInput APIs</span></span>](#stylusinput-apis)

## <a name="thread-safety"></a><span data-ttu-id="059cb-112">Thread-Safety</span><span class="sxs-lookup"><span data-stu-id="059cb-112">Thread-Safety</span></span>

<span data-ttu-id="059cb-113">Les classes de la bibliothèque managée de la plateforme Tablet PC ne sont généralement pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="059cb-113">The Tablet PC Platform's Managed Library classes are not generally thread-safe.</span></span> <span data-ttu-id="059cb-114">Les collections suivantes sont thread-safe au niveau du membre ; Toutefois, ces collections ne garantissent pas qu’un énumérateur est protégé si un autre thread opère simultanément sur la collection :</span><span class="sxs-lookup"><span data-stu-id="059cb-114">The following collections are thread-safe at the member level; however, these collections do not guarantee that an enumerator is protected if another thread operates on the collection simultaneously:</span></span>

-   <span data-ttu-id="059cb-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="059cb-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span></span>
-   <span data-ttu-id="059cb-116">[Curseurs](/previous-versions/ms839493(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="059cb-116">[Cursors](/previous-versions/ms839493(v=msdn.10))</span></span>
-   <span data-ttu-id="059cb-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="059cb-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span></span>
-   <span data-ttu-id="059cb-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="059cb-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span></span>
-   <span data-ttu-id="059cb-119">[Modules de reconnaissance](/previous-versions/ms828520(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="059cb-119">[Recognizers](/previous-versions/ms828520(v=msdn.10))</span></span>
-   <span data-ttu-id="059cb-120">[Tablettes](/previous-versions/ms827599(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="059cb-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="059cb-121">Applications STA et MTA</span><span class="sxs-lookup"><span data-stu-id="059cb-121">STA and MTA Applications</span></span>

<span data-ttu-id="059cb-122">Les applications managées créées à l’aide des assistants contenus dans Microsoft Visual Studio .NET sont des threads cloisonnés (STA) par défaut.</span><span class="sxs-lookup"><span data-stu-id="059cb-122">Managed applications created by using the wizards contained in Microsoft Visual Studio .NET are single-threaded apartment (STA) by default.</span></span> <span data-ttu-id="059cb-123">Vous pouvez modifier le cloisonnement de votre application en définissant le thread STA ou l’attribut de thread du cloisonnement multithread (MTA) sur le point d’entrée de votre application.</span><span class="sxs-lookup"><span data-stu-id="059cb-123">You can change the apartment for your application by setting the STA thread or multithreaded apartment (MTA) thread attribute on the entry point of your application.</span></span>

<span data-ttu-id="059cb-124">Si votre application s’exécute dans un MTA, vous devez écrire du code thread-safe. Toutefois, en procédant ainsi, vous pouvez améliorer certains problèmes de performances de gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="059cb-124">If your application runs in an MTA, you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

<span data-ttu-id="059cb-125">Pour plus d’informations sur les attributs du thread STA et du thread MTA, consultez la classe [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) et la classe [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="059cb-125">For more information about the STA thread and MTA thread attributes, see [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) class and [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span></span>

## <a name="windows-forms-threading-considerations"></a><span data-ttu-id="059cb-126">Considérations relatives au Threading Windows Forms</span><span class="sxs-lookup"><span data-stu-id="059cb-126">Windows Forms Threading Considerations</span></span>

<span data-ttu-id="059cb-127">Les contrôles [InkPicture](/previous-versions/aa514604(v=msdn.10)) et [InkEdit](/previous-versions/ms552265(v=vs.100)) étendent Windows Forms contrôles.</span><span class="sxs-lookup"><span data-stu-id="059cb-127">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls extend Windows Forms controls.</span></span> <span data-ttu-id="059cb-128">Les contrôles Windows Forms utilisent le modèle STA (Single-Threaded Apartment), car Windows Forms sont basés sur des fenêtres Win32 natives qui sont intrinsèquement des threads uniques.</span><span class="sxs-lookup"><span data-stu-id="059cb-128">Windows Forms controls use the single-threaded apartment (STA) model because Windows Forms are based on native Win32 windows that are inherently single threaded.</span></span> <span data-ttu-id="059cb-129">Dans le code managé, les contrôles d’encre doivent être créés dans le même thread que le thread principal pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="059cb-129">In managed code, ink controls should be created in the same thread as the main thread for the form.</span></span>

<span data-ttu-id="059cb-130">Dans une application STA, certains événements se produisent sur un thread autre que le thread d’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="059cb-130">In an STA application, certain events happen on a thread other than the application's user interface (UI) thread.</span></span> <span data-ttu-id="059cb-131">Lors de l’appel d’un objet ou d’un contrôle Windows Forms, y compris les contrôles [InkPicture](/previous-versions/aa514604(v=msdn.10)) et [InkEdit](/previous-versions/ms552265(v=vs.100)) , à partir d’un gestionnaire d’événements Tablet PC, utilisez la méthode [Control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) héritée de l’objet ou du contrôle.</span><span class="sxs-lookup"><span data-stu-id="059cb-131">When calling any Windows Forms object or control, including the [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls, from within a Tablet PC event handler, use the object or control's inherited [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) method.</span></span> <span data-ttu-id="059cb-132">La propriété [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , héritée de la classe Control, peut être utilisée pour déterminer si cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="059cb-132">The [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property, inherited from the Control class, can be used to determine if this is necessary.</span></span>

<span data-ttu-id="059cb-133">Par exemple, dans le gestionnaire d’événements suivant pour l’événement de [reconnaissance](/previous-versions/ms829424(v=msdn.10)) , la propriété [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) est testée et, si la **valeur est true**, le gestionnaire d’événements est à nouveau appelé à partir du thread d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="059cb-133">For example, in the following event handler for the [Recognition](/previous-versions/ms829424(v=msdn.10)) event, the [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property is tested and if **TRUE**, the event handler is re-invoked from the user interface thread.</span></span>


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



<span data-ttu-id="059cb-134">Si vous placez un [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) sur awebpagein un navigateur (consultez [contrôles Web](web-controls.md)), il s’exécute en tant qu’application STA.</span><span class="sxs-lookup"><span data-stu-id="059cb-134">If you put a [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) onto awebpagein a browser (see [Web Controls](web-controls.md)), then it runs as an STA application.</span></span> <span data-ttu-id="059cb-135">Pour les applications Smart client (voir [aucun déploiement Touch](no-touch-deployment.md)), le développeur a un contrôle total sur le [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="059cb-135">For smart client applications (see [No Touch Deployment](no-touch-deployment.md)), the developer has full control over the [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span></span> <span data-ttu-id="059cb-136">(La valeur par défaut est généralement STA, mais peut être MTA, en fonction de votre version de CLR.) Pour les problèmes de Threading impliquant l' [**RealTimeStylus**](realtimestylus-class.md), consultez [Considérations sur les threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="059cb-136">(The default is generally STA, but may be MTA, depending on your version of CLR.) For threading issues involving the [**RealTimeStylus**](realtimestylus-class.md), see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="059cb-137">Pour plus d’informations sur l’appel d’Windows Forms à partir d’une application MTA, consultez [exemple de contrôle multithread Windows Forms](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="059cb-137">For more information about calling Windows Forms from an MTA application, see [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span></span>

## <a name="clipboard-considerations"></a><span data-ttu-id="059cb-138">Considérations sur le presse-papiers</span><span class="sxs-lookup"><span data-stu-id="059cb-138">Clipboard Considerations</span></span>

<span data-ttu-id="059cb-139">L’objet [Clipboard](../dataxchg/clipboard.md) ne fonctionne qu’à partir d’un thread STA.</span><span class="sxs-lookup"><span data-stu-id="059cb-139">The [Clipboard](../dataxchg/clipboard.md) object works only from an STA thread.</span></span> <span data-ttu-id="059cb-140">Lors d’une tentative de copie ou de collage à partir du presse-papiers à partir d’un thread qui n’est pas STA, vous recevez un [ThreadStateException](/previous-versions/windows/).</span><span class="sxs-lookup"><span data-stu-id="059cb-140">When trying to copy to or paste from the Clipboard from a thread that is not STA, you get a [ThreadStateException](/previous-versions/windows/).</span></span> <span data-ttu-id="059cb-141">Si votre application est MTA, créez un thread STA pour gérer les appels de méthode du presse-papiers et certains des autres aspects de l’interface utilisateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="059cb-141">If your application is MTA, create an STA thread to handle the Clipboard's method calls and some of the other UI aspects of your application.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="059cb-142">Exceptions dans les gestionnaires d’événements</span><span class="sxs-lookup"><span data-stu-id="059cb-142">Exceptions within Event Handlers</span></span>

<span data-ttu-id="059cb-143">Les exceptions ne peuvent pas être levées à partir des gestionnaires d’événements Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="059cb-143">Exceptions cannot be thrown from within Tablet PC event handlers.</span></span> <span data-ttu-id="059cb-144">Par exemple, si un délégué de gestionnaire d’événements pour un objet ou une collection Tablet PC a trois gestionnaires inscrits et que le premier lève une exception, la séquence suivante se produit :</span><span class="sxs-lookup"><span data-stu-id="059cb-144">For example, if an event handler delegate for a Tablet PC object or collection has three registered handlers and the first one throws an exception, then the following sequence occurs:</span></span>

1.  <span data-ttu-id="059cb-145">Le premier gestionnaire se termine.</span><span class="sxs-lookup"><span data-stu-id="059cb-145">The first handler exits.</span></span>
2.  <span data-ttu-id="059cb-146">L’exception est perdue.</span><span class="sxs-lookup"><span data-stu-id="059cb-146">The exception is lost.</span></span>
3.  <span data-ttu-id="059cb-147">Les gestionnaires restants ne sont pas appelés.</span><span class="sxs-lookup"><span data-stu-id="059cb-147">The remaining handlers are not invoked.</span></span>

## <a name="disposing-objects-and-controls"></a><span data-ttu-id="059cb-148">Suppression d’objets et de contrôles</span><span class="sxs-lookup"><span data-stu-id="059cb-148">Disposing Objects and Controls</span></span>

<span data-ttu-id="059cb-149">Pour éviter une fuite de mémoire, vous devez appeler explicitement la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) sur tout objet ou contrôle Tablet PC auquel un gestionnaire d’événements a été attaché avant que l’objet ou le contrôle ne soit hors de portée.</span><span class="sxs-lookup"><span data-stu-id="059cb-149">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="059cb-150">Pour améliorer les performances de votre application, supprimez manuellement tout objet ou contrôle Tablet PC qui implémente la méthode [dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) lorsque l’objet ou le contrôle n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="059cb-150">To improve performance in your application, manually dispose of any Tablet PC object or control that implements the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method when the object or control is no longer needed.</span></span>

## <a name="stylusinput-apis"></a><span data-ttu-id="059cb-151">API StylusInput</span><span class="sxs-lookup"><span data-stu-id="059cb-151">StylusInput APIs</span></span>

<span data-ttu-id="059cb-152">Pour plus d’informations sur les considérations relatives aux threads pour l’objet [**RealTimeStylus**](realtimestylus-class.md) et les interfaces de programmation d’applications (API) StylusInput, consultez [Considérations sur les threads pour les API StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="059cb-152">For information about threading considerations for the [**RealTimeStylus**](realtimestylus-class.md) object and the StylusInput application programming interfaces (APIs) see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

 

 
