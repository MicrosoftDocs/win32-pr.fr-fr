---
description: Cette application illustre l’utilisation de la classe RealTimeStylus.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Exemple de plug-in RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210823"
---
# <a name="realtimestylus-plug-in-sample"></a><span data-ttu-id="438e1-103">Exemple de plug-in RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="438e1-103">RealTimeStylus Plug-in Sample</span></span>

<span data-ttu-id="438e1-104">Cette application illustre l’utilisation de la classe [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="438e1-104">This application demonstrates working with the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span> <span data-ttu-id="438e1-105">Pour obtenir une vue d’ensemble détaillée des API StylusInput, y compris la classe **RealTimeStylus** , consultez [accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="438e1-105">For a detailed overview of the StylusInput APIs, including the **RealTimeStylus** class, see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span> <span data-ttu-id="438e1-106">Pour plus d’informations sur les plug-ins synchrones et asynchrones, consultez [plug-ins et la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="438e1-106">For information about synchronous and asynchronous plug-ins, see [Plug-ins and the RealTimeStylus Class](plug-ins-and-the-realtimestylus-class.md).</span></span>

## <a name="overview-of-the-sample"></a><span data-ttu-id="438e1-107">Vue d’ensemble de l’exemple</span><span class="sxs-lookup"><span data-stu-id="438e1-107">Overview of the Sample</span></span>

<span data-ttu-id="438e1-108">Les plug-ins, objets qui implémentent l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) peuvent être ajoutés à un objet [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="438e1-108">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface can be added to a [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="438e1-109">Cet exemple d’application utilise plusieurs types de plug-in :</span><span class="sxs-lookup"><span data-stu-id="438e1-109">This sample application uses several types of plug-in:</span></span>

-   <span data-ttu-id="438e1-110">Plug-in de filtre de paquets : modifie les paquets.</span><span class="sxs-lookup"><span data-stu-id="438e1-110">Packet Filter Plug-in: Modifies packets.</span></span> <span data-ttu-id="438e1-111">Dans cet exemple, le plug-in de filtre de paquets modifie les informations de paquets en limitant toutes les données de paquet (x, y) au sein d’une zone rectangulaire.</span><span class="sxs-lookup"><span data-stu-id="438e1-111">The packet filter plug-in in this sample modifies packet information by constraining all (x,y) packet data within a rectangular area.</span></span>
-   <span data-ttu-id="438e1-112">Plug-in de rendu dynamique personnalisé : modifie les qualités de rendu dynamiques.</span><span class="sxs-lookup"><span data-stu-id="438e1-112">Custom Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="438e1-113">Dans cet exemple, le plug-in de rendu dynamique personnalisé modifie la façon dont l’encre est rendue en dessinant un petit cercle autour de chaque point (x, y) sur un trait.</span><span class="sxs-lookup"><span data-stu-id="438e1-113">The custom dynamic rendering plug-in in this sample modifies the way ink is rendered by drawing a small circle around each (x,y) point on a stroke.</span></span>
-   <span data-ttu-id="438e1-114">Plug-in de rendu dynamique : modifie les qualités de rendu dynamiques.</span><span class="sxs-lookup"><span data-stu-id="438e1-114">Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="438e1-115">Cet exemple illustre l’utilisation de l’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) en tant que plug-in pour gérer le rendu dynamique de l’encre.</span><span class="sxs-lookup"><span data-stu-id="438e1-115">This sample demonstrates use of the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object as a plug-in to handle dynamic rendering of ink.</span></span>
-   <span data-ttu-id="438e1-116">Plug-in de module de reconnaissance de mouvement : reconnaît les gestes d’application.</span><span class="sxs-lookup"><span data-stu-id="438e1-116">Gesture Recognizer Plug-in: Recognizes application gestures.</span></span> <span data-ttu-id="438e1-117">Cet exemple illustre l’utilisation de l’objet [**GestureRecognizer**](gesturerecognizer-class.md) en tant que plug-in pour reconnaître les gestes d’application (en cas d’exécution sur un système sur lequel le module de reconnaissance de mouvement Microsoft est présent).</span><span class="sxs-lookup"><span data-stu-id="438e1-117">This sample demonstrates use of the [**GestureRecognizer**](gesturerecognizer-class.md) object as a plug-in to recognize application gestures (when running on a system with the Microsoft gesture recognizer present).</span></span>

<span data-ttu-id="438e1-118">En outre, cet exemple fournit une interface utilisateur qui permet à l’utilisateur d’ajouter, de supprimer et de modifier l’ordre de chaque plug-in de la collection.</span><span class="sxs-lookup"><span data-stu-id="438e1-118">In addition, this sample provides a user interface that enables the user to add, remove, and change the order of each plug-in in the collection.</span></span> <span data-ttu-id="438e1-119">L’exemple de solution contient deux projets, RealTimeStylusPluginApp et RealTimeStylusPlugins.</span><span class="sxs-lookup"><span data-stu-id="438e1-119">The sample solution contains two projects, RealTimeStylusPluginApp and RealTimeStylusPlugins.</span></span> <span data-ttu-id="438e1-120">RealTimeStylusPluginApp contient l’interface utilisateur de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="438e1-120">RealTimeStylusPluginApp contains the user interface for the sample.</span></span> <span data-ttu-id="438e1-121">RealTimeStylusPlugins contient les implémentations des plug-ins. Le projet RealTimeStylusPlugins définit l’espace de noms RealTimeStylusPlugins, qui contient les plug-ins filtre de paquets et convertisseur dynamique personnalisé. Cet espace de noms est référencé par le projet RealTimeStylusPluginApp.</span><span class="sxs-lookup"><span data-stu-id="438e1-121">RealTimeStylusPlugins contains the implementations of the plug-ins. The RealTimeStylusPlugins project defines the RealTimeStylusPlugins namespace, which contains the packet filter and custom dynamic renderer plug-ins. This namespace is referenced by the RealTimeStylusPluginApp project.</span></span> <span data-ttu-id="438e1-122">Le projet RealTimeStylusPlugins utilise les espaces de noms [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))et [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="438e1-122">The RealTimeStylusPlugins project uses the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)), and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span>

<span data-ttu-id="438e1-123">Pour obtenir une vue d’ensemble des espaces de noms [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) et [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) , consultez [architecture des API StylusInput](architecture-of-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="438e1-123">For an overview of the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces see [Architecture of the StylusInput APIs](architecture-of-the-stylusinput-apis.md).</span></span>

## <a name="packet-filter-plug-in"></a><span data-ttu-id="438e1-124">Plug-in de filtre de paquets</span><span class="sxs-lookup"><span data-stu-id="438e1-124">Packet Filter Plug-in</span></span>

<span data-ttu-id="438e1-125">Le plug-in de filtre de paquets est un plug-in synchrone qui illustre la modification de paquets.</span><span class="sxs-lookup"><span data-stu-id="438e1-125">The packet filter plug-in is a synchronous plug-in that demonstrates packet modification.</span></span> <span data-ttu-id="438e1-126">Plus précisément, il définit un rectangle sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="438e1-126">Specifically, it defines a rectangle on the form.</span></span> <span data-ttu-id="438e1-127">Tous les paquets qui sont dessinés en dehors de la région sont rendus à l’intérieur de la région.</span><span class="sxs-lookup"><span data-stu-id="438e1-127">Any packets that are drawn outside the region are rendered inside the region.</span></span> <span data-ttu-id="438e1-128">La classe de plug-in, `PacketFilterPlugin` , s’inscrit pour la notification des `StylusDown` `StylusUp` `Packets` événements d’entrée de stylet, et.</span><span class="sxs-lookup"><span data-stu-id="438e1-128">The plug-in class, `PacketFilterPlugin`, registers for notification of `StylusDown`, `StylusUp`, and `Packets` pen input events.</span></span> <span data-ttu-id="438e1-129">La classe implémente les méthodes [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10))et [Packets](/previous-versions/ms824756(v=msdn.10)) définies sur la classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="438e1-129">The class implements the [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10)), and [Packets](/previous-versions/ms824756(v=msdn.10)) methods defined on [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class.</span></span>

<span data-ttu-id="438e1-130">Le constructeur public pour `PacketFilterPlugin` requiert une structure [rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="438e1-130">The public constructor for `PacketFilterPlugin` requires a [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) structure.</span></span> <span data-ttu-id="438e1-131">Ce rectangle définit la zone rectangulaire, en coordonnées d’espace d’encre (. 01mm = 1 unité HIMETRIC), dans laquelle les paquets seront contenus.</span><span class="sxs-lookup"><span data-stu-id="438e1-131">This rectangle defines the rectangular area, in ink space coordinates (.01mm = 1 HIMETRIC unit), in which packets will be contained.</span></span> <span data-ttu-id="438e1-132">Le rectangle est conservé dans un champ privé, `rectangle` .</span><span class="sxs-lookup"><span data-stu-id="438e1-132">The rectangle is held in a private field, `rectangle`.</span></span>


```C++
public class PacketFilterPlugin:IStylusSyncPlugin  
{
    private System.Drawing.Rectangle rectangle = System.Drawing.Rectangle.Empty;
    public PacketFilterPlugin(Rectangle r)
    {
        rectangle = r;
    }
    // ...
```



<span data-ttu-id="438e1-133">La `PacketFilterPlugin` classe s’inscrit pour les notifications d’événements en implémentant l’accesseur get pour la propriété [DataInterest](/previous-versions/ms824752(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="438e1-133">The `PacketFilterPlugin` class registers for event notifications by implementing the get accessor for the [DataInterest](/previous-versions/ms824752(v=msdn.10)) property.</span></span> <span data-ttu-id="438e1-134">Dans ce cas, le plug-in s’intéresse à répondre aux `StylusDown` `Packets` `StylusUp` notifications,, et `Error` .</span><span class="sxs-lookup"><span data-stu-id="438e1-134">In this case, the plug-in has interested in responding to the `StylusDown`, `Packets`, `StylusUp`, and `Error` notifications.</span></span> <span data-ttu-id="438e1-135">L’exemple retourne ces valeurs telles qu’elles sont définies dans l’énumération [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="438e1-135">The sample returns these values as defined in the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span> <span data-ttu-id="438e1-136">La méthode [StylusDown](/previous-versions/ms824761(v=msdn.10)) est appelée lorsque l’info-bulle du stylet contacte la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="438e1-136">The [StylusDown](/previous-versions/ms824761(v=msdn.10)) method is called when the pen tip contacts the digitizer surface.</span></span> <span data-ttu-id="438e1-137">La méthode [StylusUp](/previous-versions/ms824764(v=msdn.10)) est appelée lorsque la pointe du stylet quitte la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="438e1-137">The [StylusUp](/previous-versions/ms824764(v=msdn.10)) method is called when the pen tip leaves the digitizer surface.</span></span> <span data-ttu-id="438e1-138">La méthode [Packets](/previous-versions/ms824756(v=msdn.10)) est appelée lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) reçoit des paquets.</span><span class="sxs-lookup"><span data-stu-id="438e1-138">The [Packets](/previous-versions/ms824756(v=msdn.10)) method is called when the [**RealTimeStylus**](realtimestylus-class.md) object receives packets.</span></span> <span data-ttu-id="438e1-139">La méthode d' [erreur](/previous-versions/ms585069(v=vs.100)) est appelée quand le plug-in actuel ou un plug-in précédent lève une exception.</span><span class="sxs-lookup"><span data-stu-id="438e1-139">The [Error](/previous-versions/ms585069(v=vs.100)) method is called when the current plug-in or a previous plug-in throws an exception.</span></span>


```C++
public DataInterestMask DataInterest
{
    get
    {
        return DataInterestMask.StylusDown | 
               DataInterestMask.Packets | 
               DataInterestMask.StylusUp | 
               DataInterestMask.Error;
    }
}           
    //...
```



<span data-ttu-id="438e1-140">La `PacketFilterPlugin` classe gère la plupart de ces notifications dans une méthode d’assistance, `ModifyPacketData` .</span><span class="sxs-lookup"><span data-stu-id="438e1-140">The `PacketFilterPlugin` class handles most of these notifications in a helper method, `ModifyPacketData`.</span></span> <span data-ttu-id="438e1-141">La `ModifyPacketData` méthode obtient les valeurs x et y de chaque nouveau paquet de la classe [PacketsData](/previous-versions/ms824590(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="438e1-141">The `ModifyPacketData` method gets the x and y values for each new packet from the [PacketsData](/previous-versions/ms824590(v=msdn.10)) class.</span></span> <span data-ttu-id="438e1-142">Si l’une des valeurs est à l’extérieur du rectangle, la méthode remplace la valeur par le point le plus proche qui se trouve toujours dans le rectangle.</span><span class="sxs-lookup"><span data-stu-id="438e1-142">If either value is outside the rectangle, the method replaces the value with the nearest point that still falls within the rectangle.</span></span> <span data-ttu-id="438e1-143">Il s’agit d’un exemple de la façon dont un plug-in peut remplacer des données de paquets au fur et à mesure de leur réception à partir du flux d’entrée de stylet.</span><span class="sxs-lookup"><span data-stu-id="438e1-143">This is an example of how a plug-in can replace packet data as it is received from the pen-input stream.</span></span>


```C++
private void ModifyPacketData(StylusDataBase data)
{
    for (int i = 0; i < data.Count ; i += data.PacketPropertyCount)
    {
        // packet data always has x followed by y followed by the rest
        int x = data[i];
        int y = data[i+1];

        // Constrain points to the input rectangle
        x = Math.Max(x, rectangle.Left);
        x = Math.Min(x, rectangle.Right);
        y = Math.Max(y, rectangle.Top);
        y = Math.Min(y, rectangle.Bottom);

        // If necessary, modify the x,y packet data
        if (x != data[i])
        {
            data[i] = x;
        }
        if (y != data[i+1])
        {
            data[i+1] = y;
        } 
    }
}
```



## <a name="custom-dynamic-renderer-plug-in"></a><span data-ttu-id="438e1-144">Plug-in de rendu dynamique personnalisé</span><span class="sxs-lookup"><span data-stu-id="438e1-144">Custom Dynamic Renderer Plug-in</span></span>

<span data-ttu-id="438e1-145">La `CustomDynamicRenderer` classe implémente également la classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) pour recevoir des notifications d’entrée de stylet.</span><span class="sxs-lookup"><span data-stu-id="438e1-145">The `CustomDynamicRenderer` class also implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class to receive pen-input notifications.</span></span> <span data-ttu-id="438e1-146">Il gère ensuite la `Packets` notification pour dessiner un petit cercle autour de chaque nouveau point de paquet.</span><span class="sxs-lookup"><span data-stu-id="438e1-146">It then handles the `Packets` notification to draw a small circle around each new packet point.</span></span>

<span data-ttu-id="438e1-147">La classe contient une variable [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) qui contient une référence à l’objet Graphics passé dans le constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="438e1-147">The class contains a [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) variable that holds a reference to the graphics object passed into the class constructor.</span></span> <span data-ttu-id="438e1-148">Il s’agit de l’objet Graphics utilisé pour le rendu dynamique.</span><span class="sxs-lookup"><span data-stu-id="438e1-148">This is the graphics object used for dynamic rendering.</span></span>


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



<span data-ttu-id="438e1-149">Lorsque le plug-in de rendu dynamique personnalisé reçoit une notification de paquets, il extrait les données (x, y) et dessine un petit cercle vert autour du point.</span><span class="sxs-lookup"><span data-stu-id="438e1-149">When the custom dynamic renderer plug-in receives a Packets notification, it extracts the (x,y) data and draws a small green circle around the point.</span></span> <span data-ttu-id="438e1-150">Il s’agit d’un exemple de rendu personnalisé basé sur le flux d’entrée de stylet.</span><span class="sxs-lookup"><span data-stu-id="438e1-150">This is an example of custom rendering based on the pen-input stream.</span></span>


```C++
public void Packets(RealTimeStylus sender,  PacketsData data)
{           
    for (int i = 0; i < data.Count; i += data.PacketPropertyCount)
    {
        // Packet data always has x followed by y followed by the rest
        Point point = new Point(data[i], data[i+1]);

        // Since the packet data is in Ink Space coordinates, we need to convert to Pixels...
        point.X = (int)Math.Round((float)point.X * (float)myGraphics.DpiX/2540.0F);
        point.Y = (int)Math.Round((float)point.Y * (float)myGraphics.DpiY/2540.0F);

        // Draw a circle corresponding to the packet
        myGraphics.DrawEllipse(Pens.Green, point.X - 2, point.Y - 2, 4, 4);
    }
}
```



## <a name="the-realtimestyluspluginapp-project"></a><span data-ttu-id="438e1-151">Projet RealTimeStylusPluginApp</span><span class="sxs-lookup"><span data-stu-id="438e1-151">The RealTimeStylusPluginApp Project</span></span>

<span data-ttu-id="438e1-152">Le projet RealTimeStylusPluginApp illustre les plug-ins décrits précédemment, ainsi que les plug-ins [**GestureRecognizer**](gesturerecognizer-class.md) et [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . L’interface utilisateur du projet se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="438e1-152">The RealTimeStylusPluginApp project demonstrates the plug-ins previously described, as well as the [**GestureRecognizer**](gesturerecognizer-class.md) and [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) plug-ins. The project's user interface consists of:</span></span>

-   <span data-ttu-id="438e1-153">Formulaire qui contient un contrôle [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) utilisé pour définir la zone d’entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="438e1-153">A Form that contains a [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) control used to define the ink entry area.</span></span>
-   <span data-ttu-id="438e1-154">Un contrôle [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) pour répertorier et sélectionner les plug-ins disponibles.</span><span class="sxs-lookup"><span data-stu-id="438e1-154">A [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) control to list and select the available plug-ins.</span></span>
-   <span data-ttu-id="438e1-155">Paire d' [objets bouton](/dotnet/api/system.windows.forms.button?view=netcore-3.1) qui permet de réorganiser les plug-ins.</span><span class="sxs-lookup"><span data-stu-id="438e1-155">A pair of [Button objects](/dotnet/api/system.windows.forms.button?view=netcore-3.1) to enable re-ordering the plug-ins.</span></span>

<span data-ttu-id="438e1-156">Le projet définit une structure, `PlugInListItem` , pour faciliter la gestion des plug-ins utilisés dans le projet.</span><span class="sxs-lookup"><span data-stu-id="438e1-156">The project defines a structure, `PlugInListItem`, to make managing the plug-ins used in the project easier.</span></span> <span data-ttu-id="438e1-157">La `PlugInListItem` structure contient le plug-in et une description.</span><span class="sxs-lookup"><span data-stu-id="438e1-157">The `PlugInListItem` structure contains the plug-in and a description.</span></span>

<span data-ttu-id="438e1-158">La `RealTimeStylusPluginApp` classe elle-même implémente la classe [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="438e1-158">The `RealTimeStylusPluginApp` class itself implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) class.</span></span> <span data-ttu-id="438e1-159">Cela est nécessaire afin que la `RealTimeStylusPluginApp` classe puisse être notifiée lorsque le plug-in [**GestureRecognizer**](gesturerecognizer-class.md) ajoute des données de mouvement à la file d’attente de sortie.</span><span class="sxs-lookup"><span data-stu-id="438e1-159">This is necessary so that the `RealTimeStylusPluginApp` class can be notified when the [**GestureRecognizer**](gesturerecognizer-class.md) plug-in adds gesture data to the output queue.</span></span> <span data-ttu-id="438e1-160">L’application s’inscrit à la notification de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="438e1-160">The application registers for notification of [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span></span> <span data-ttu-id="438e1-161">Une fois les données de mouvement reçues, `RealTimeStylusPluginApp` les insèrent une description dans la barre d’État en bas du formulaire.</span><span class="sxs-lookup"><span data-stu-id="438e1-161">When gesture data is received, `RealTimeStylusPluginApp` places a description of it on the status bar at the bottom of the form.</span></span>


```C++
public void CustomStylusDataAdded(RealTimeStylus sender, CustomStylusData data)
{
    if (data.CustomDataId == GestureRecognizer.GestureRecognitionDataGuid)
    {
        GestureRecognitionData grd = data.Data as GestureRecognitionData;
        if (grd != null)
        {
            if (grd.Count > 0)
            {
                GestureAlternate ga = grd[0];
                sbGesture.Text = "Gesture=" + ga.Id + ", Confidence=" + ga.Confidence;
            }
        }
    }
}
```



> [!Note]  
> Dans l’implémentation [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) , il est intéressant de pouvoir identifier les données de mouvement personnalisées dans la file d’attente de sortie par GUID (à l’aide du champ [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ) ou par type (à l’aide du résultat de l’instruction As). L’exemple utilise les deux techniques d’identification à des fins de démonstration. <span data-ttu-id="438e1-164">L’une ou l’autre approche est également valide.</span><span class="sxs-lookup"><span data-stu-id="438e1-164">Either approach alone is also valid.</span></span>

 

<span data-ttu-id="438e1-165">Dans le gestionnaire d’événements Load du formulaire, l’application crée des instances `PacketFilter` des `CustomDynamicRenderer` classes et, puis les ajoute à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="438e1-165">In the Form's Load event handler, the application creates instances of the `PacketFilter` and `CustomDynamicRenderer` classes and adds them to the list box.</span></span> <span data-ttu-id="438e1-166">L’application tente ensuite de créer une instance de la classe [**GestureRecognizer**](gesturerecognizer-class.md) et, en cas de réussite, l’ajoute à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="438e1-166">The application then attempts to create an instance of the [**GestureRecognizer**](gesturerecognizer-class.md) class and, if successful, adds it to the list box.</span></span> <span data-ttu-id="438e1-167">Cela échoue si le module de reconnaissance de mouvement n’est pas présent sur le système.</span><span class="sxs-lookup"><span data-stu-id="438e1-167">This fails if the gesture recognizer is not present on the system.</span></span> <span data-ttu-id="438e1-168">Ensuite, l’application instancie un objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) et l’ajoute à la zone de liste.</span><span class="sxs-lookup"><span data-stu-id="438e1-168">Next, the application instantiates a [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object and adds it to the list box.</span></span> <span data-ttu-id="438e1-169">Enfin, l’application active chacun des plug-ins et l’objet [**RealTimeStylus**](realtimestylus-class.md) lui-même.</span><span class="sxs-lookup"><span data-stu-id="438e1-169">Finally, the application enables each of the plug-ins and the [**RealTimeStylus**](realtimestylus-class.md) object itself.</span></span>

<span data-ttu-id="438e1-170">Il est également important de noter que dans les méthodes d’assistance, l’objet [**RealTimeStylus**](realtimestylus-class.md) est désactivé avant l’ajout ou la suppression de plug-ins, puis réactivé une fois l’ajout ou la suppression terminé.</span><span class="sxs-lookup"><span data-stu-id="438e1-170">Another important thing to note about the sample is that in the helper methods, the [**RealTimeStylus**](realtimestylus-class.md) object is first disabled before plug-ins are added or removed and then re-enabled after the addition or removal is complete.</span></span>


```C++
private void RemoveFromPluginCollection(int index)
{
    IStylusSyncPlugin plugin = ((PluginListItem)chklbPlugins.Items[index]).Plugin;

    bool rtsEnabled = myRealTimeStylus.Enabled;
    myRealTimeStylus.Enabled = false;
    myRealTimeStylus.SyncPluginCollection.Remove(plugin);
    myRealTimeStylus.Enabled = rtsEnabled;
}
```



## <a name="related-topics"></a><span data-ttu-id="438e1-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="438e1-171">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="438e1-172">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="438e1-172">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="438e1-173">[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="438e1-173">[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="438e1-174">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="438e1-174">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="438e1-175">[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="438e1-175">[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="438e1-176">[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="438e1-176">[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="438e1-177">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="438e1-177">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="438e1-178">[Microsoft. StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="438e1-178">[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="438e1-179">Accès et manipulation de l’entrée du stylet</span><span class="sxs-lookup"><span data-stu-id="438e1-179">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[<span data-ttu-id="438e1-180">Plug-ins et classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="438e1-180">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="438e1-181">Exemple de collection d’encres RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="438e1-181">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
