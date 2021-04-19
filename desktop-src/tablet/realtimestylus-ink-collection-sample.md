---
description: Cette application montre la collecte et le rendu d’entrée manuscrite lors de l’utilisation de la classe RealTimeStylus.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: Exemple de collection d’encres RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24fe67ed59ea1a69f5d0d9a2656169f2df88a450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534657"
---
# <a name="realtimestylus-ink-collection-sample"></a><span data-ttu-id="89fbe-103">Exemple de collection d’encres RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="89fbe-103">RealTimeStylus Ink Collection Sample</span></span>

<span data-ttu-id="89fbe-104">Cette application montre la collecte et le rendu d’entrée manuscrite lors de l’utilisation de la classe [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-104">This application demonstrates ink collection and rendering when using the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="the-inkcollection-project"></a><span data-ttu-id="89fbe-105">Projet InkCollection</span><span class="sxs-lookup"><span data-stu-id="89fbe-105">The InkCollection Project</span></span>

<span data-ttu-id="89fbe-106">Cet exemple se compose d’une solution unique qui contient un projet, InkCollection.</span><span class="sxs-lookup"><span data-stu-id="89fbe-106">This sample consists of a single solution that contains one project, InkCollection.</span></span> <span data-ttu-id="89fbe-107">L’application définit l' `InkCollection` espace de noms qui contient une seule classe, également appelée `InkCollection` .</span><span class="sxs-lookup"><span data-stu-id="89fbe-107">The application defines the `InkCollection` namespace that contains a single class, also called `InkCollection`.</span></span> <span data-ttu-id="89fbe-108">La classe hérite de la classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) et implémente l’interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-108">The class inherits from the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



<span data-ttu-id="89fbe-109">La classe InkCollection définit un ensemble de constantes privées utilisées pour spécifier différentes épaisseurs d’encre.</span><span class="sxs-lookup"><span data-stu-id="89fbe-109">The InkCollection Class defines a set of private constants used to specify various ink thickness.</span></span> <span data-ttu-id="89fbe-110">La classe déclare également des instances privées de la classe [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , la classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` , et la classe de [convertisseur](/previous-versions/ms828481(v=msdn.10)) `myRenderer` .</span><span class="sxs-lookup"><span data-stu-id="89fbe-110">The class also declares private instances of the [**RealTimeStylus**](realtimestylus-class.md) class, `myRealTimeStylus`, the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class, `myDynamicRenderer`, and the [Renderer](/previous-versions/ms828481(v=msdn.10)) class `myRenderer`.</span></span> <span data-ttu-id="89fbe-111">Le **DynamicRenderer** restitue le [trait](/previous-versions/ms552692(v=vs.100)) qui est actuellement collecté.</span><span class="sxs-lookup"><span data-stu-id="89fbe-111">The **DynamicRenderer** renders the [Stroke](/previous-versions/ms552692(v=vs.100)) that is currently being collected.</span></span> <span data-ttu-id="89fbe-112">L’objet de convertisseur, `myRenderer` , restitue les objets Stroke qui ont déjà été collectés.</span><span class="sxs-lookup"><span data-stu-id="89fbe-112">The Renderer object, `myRenderer`, renders Stroke objects that have already been collected.</span></span>


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



<span data-ttu-id="89fbe-113">La classe déclare également un objet [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , qui est utilisé pour stocker les données de paquets collectées par un ou plusieurs objets [curseur](/previous-versions/ms552104(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-113">The class also declares a [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) object, `myPackets`, which is used to store packet data that is being collected by one or more [Cursor](/previous-versions/ms552104(v=vs.100)) objects.</span></span> <span data-ttu-id="89fbe-114">Les valeurs d' [ID](/previous-versions/ms824826(v=msdn.10)) de l’objet de [stylet](/previous-versions/ms824824(v=msdn.10)) sont utilisées comme clé de la Hashtable pour identifier de manière unique les données de paquet collectées pour un objet curseur donné.</span><span class="sxs-lookup"><span data-stu-id="89fbe-114">The [Stylus](/previous-versions/ms824824(v=msdn.10)) object's [Id](/previous-versions/ms824826(v=msdn.10)) values are used as the hashtable key to uniquely identify the packet data collected for a given Cursor object.</span></span>

<span data-ttu-id="89fbe-115">Une instance privée de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) `myInk` stocke les objets [Stroke](/previous-versions/ms552692(v=vs.100)) collectés par `myRealTimeStylus` .</span><span class="sxs-lookup"><span data-stu-id="89fbe-115">A private instance of the [Ink](/previous-versions/aa515768(v=msdn.10)) object, `myInk`, stores [Stroke](/previous-versions/ms552692(v=vs.100)) objects collected by `myRealTimeStylus`.</span></span>


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a><span data-ttu-id="89fbe-116">Événement de chargement de formulaire</span><span class="sxs-lookup"><span data-stu-id="89fbe-116">The Form Load Event</span></span>

<span data-ttu-id="89fbe-117">Dans le gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire, `myDynamicRenderer` est instancié à l’aide du [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) qui prend un contrôle comme argument et `myRenderer` est construit avec un constructeur sans argument.</span><span class="sxs-lookup"><span data-stu-id="89fbe-117">In the [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler for the form, `myDynamicRenderer` is instantiated by using the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) that takes a control as an argument, and `myRenderer` is constructed with a no-argument constructor.</span></span>


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



<span data-ttu-id="89fbe-118">Faites attention au commentaire qui suit l’instanciation des convertisseurs, car `myDynamicRenderer` utilise les valeurs par défaut pour [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) lors du rendu de l’encre.</span><span class="sxs-lookup"><span data-stu-id="89fbe-118">Pay attention to the comment that follows the instantiation of the renderers, because `myDynamicRenderer` uses the default values for [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) when rendering the ink.</span></span> <span data-ttu-id="89fbe-119">Il s’agit du comportement standard.</span><span class="sxs-lookup"><span data-stu-id="89fbe-119">This is standard behavior.</span></span> <span data-ttu-id="89fbe-120">Toutefois, si vous souhaitez donner à l’encre un rendu `myDynamicRenderer` différent de l’encre rendue par `myRenderer` , vous pouvez modifier la propriété [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) sur `myDynamicRenderer` .</span><span class="sxs-lookup"><span data-stu-id="89fbe-120">However, if you wish to give the ink rendered by `myDynamicRenderer` a different look from ink rendered by `myRenderer`, you can change the [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) property on `myDynamicRenderer`.</span></span> <span data-ttu-id="89fbe-121">Pour ce faire, supprimez les marques de commentaire des lignes suivantes avant de générer et d’exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="89fbe-121">To do so, uncomment the following lines before you build and run the application.</span></span>


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



<span data-ttu-id="89fbe-122">Ensuite, l’application crée l’objet [**RealTimeStylus**](realtimestylus-class.md) qui est utilisé pour recevoir des notifications de stylet et ajoute l’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) à la file d’attente de notification de plug-in synchrone.</span><span class="sxs-lookup"><span data-stu-id="89fbe-122">Next, the application creates the [**RealTimeStylus**](realtimestylus-class.md) object that is used to receive stylus notifications and adds the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object to the synchronous plug-in notification queue.</span></span> <span data-ttu-id="89fbe-123">Plus précisément, `myRealTimeStylus` ajoute `myDynamicRenderer` à la propriété [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-123">Specifically, `myRealTimeStylus` adds `myDynamicRenderer` to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property.</span></span>


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



<span data-ttu-id="89fbe-124">Le formulaire est ensuite ajouté à la file d’attente de notification du plug-in asynchrone.</span><span class="sxs-lookup"><span data-stu-id="89fbe-124">The form is then added to the asynchronous plug-in notification queue.</span></span> <span data-ttu-id="89fbe-125">Plus précisément, `InkCollection` est ajouté à la propriété [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-125">Specifically, `InkCollection` is added to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property.</span></span> <span data-ttu-id="89fbe-126">Enfin, `myRealTimeStylus` et `myDynamicRenderer` sont activés, et MyPackets et myInk sont instanciés.</span><span class="sxs-lookup"><span data-stu-id="89fbe-126">Finally, `myRealTimeStylus` and `myDynamicRenderer` are enabled, and myPackets and myInk are instantiated.</span></span>


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



<span data-ttu-id="89fbe-127">Hormis le raccordement des gestionnaires de menus pour modifier la couleur et la taille de l’encre, un bloc de code plus bref est requis avant d’implémenter l’interface.</span><span class="sxs-lookup"><span data-stu-id="89fbe-127">Aside from hooking up the menu handlers for changing ink color and size, one more brief block of code is required before implementing the interface.</span></span> <span data-ttu-id="89fbe-128">L’exemple doit gérer l’événement [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="89fbe-128">The sample must handle the form's [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event.</span></span> <span data-ttu-id="89fbe-129">Dans le gestionnaire d’événements, l’application doit `myDynamicRenderer` être actualisée, car il est possible qu’un objet [Stroke](/previous-versions/ms552692(v=vs.100)) soit collecté au moment où l’événement Paint se produit.</span><span class="sxs-lookup"><span data-stu-id="89fbe-129">In the event handler, the application must refresh `myDynamicRenderer` because it is possible that a [Stroke](/previous-versions/ms552692(v=vs.100)) object is being collected at the time the Paint event occurs.</span></span> <span data-ttu-id="89fbe-130">Dans ce cas, la partie de l’objet Stroke qui a déjà été collectée doit être redessinée.</span><span class="sxs-lookup"><span data-stu-id="89fbe-130">In that case, the portion of the Stroke object that has already been collected needs to be redrawn.</span></span> <span data-ttu-id="89fbe-131">Le [convertisseur](/previous-versions/ms828481(v=msdn.10)) statique est utilisé pour redessiner les objets Stroke qui ont déjà été collectés.</span><span class="sxs-lookup"><span data-stu-id="89fbe-131">The static [Renderer](/previous-versions/ms828481(v=msdn.10)) is used to re-draw Stroke objects that have already been collected.</span></span> <span data-ttu-id="89fbe-132">Ces traits se trouvent dans l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) , car ils sont placés là où ils sont dessinés, comme indiqué dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="89fbe-132">These strokes are in the [Ink](/previous-versions/aa515768(v=msdn.10)) object because they are placed there when drawn, as shown in the next section.</span></span>


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a><span data-ttu-id="89fbe-133">Implémentation de l’interface IStylusAsyncPlugin</span><span class="sxs-lookup"><span data-stu-id="89fbe-133">Implementing the IStylusAsyncPlugin Interface</span></span>

<span data-ttu-id="89fbe-134">L’exemple d’application définit les types de notifications qu’il a intérêt à recevoir dans l’implémentation de la propriété [DataInterest](/previous-versions/ms824769(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-134">The sample application defines the types of notifications it has interest in receiving in the implementation of the [DataInterest](/previous-versions/ms824769(v=msdn.10)) property.</span></span> <span data-ttu-id="89fbe-135">La propriété DataInterest définit donc les notifications transférées par l’objet [**RealTimeStylus**](realtimestylus-class.md) au formulaire.</span><span class="sxs-lookup"><span data-stu-id="89fbe-135">The DataInterest property therefore defines which notifications that the [**RealTimeStylus**](realtimestylus-class.md) object forwards to the form.</span></span> <span data-ttu-id="89fbe-136">Pour cet exemple, la propriété DataInterest définit l’intérêt pour les **StylusDown**, les **paquets**, les **StylusUp** et les notifications d' **erreur** par le biais de l’énumération [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-136">For this sample, the DataInterest property defines interest in the **StylusDown**, **Packets**, **StylusUp**, and **Error** notifications through the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span>


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
```



<span data-ttu-id="89fbe-137">La notification [StylusDown](/previous-versions/ms824779(v=msdn.10)) se produit lorsque le stylet touche la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="89fbe-137">The [StylusDown](/previous-versions/ms824779(v=msdn.10)) notification occurs when the pen touches the digitizer surface.</span></span> <span data-ttu-id="89fbe-138">Dans ce cas, l’exemple alloue un tableau qui est utilisé pour stocker les données du paquet pour l’objet de [stylet](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-138">When this happens, the sample allocates an array that is used to store the packet data for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="89fbe-139">Le [StylusDownData](/previous-versions/ms824107(v=msdn.10)) de la méthode StylusDown est ajouté au tableau et le tableau est inséré dans la table de hachage en utilisant la propriété [ID](/previous-versions/ms824826(v=msdn.10)) de l’objet Stylus comme clé.</span><span class="sxs-lookup"><span data-stu-id="89fbe-139">The [StylusDownData](/previous-versions/ms824107(v=msdn.10)) from the StylusDown method is added to the array, and the array is inserted into the hashtable by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as a key.</span></span>


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



<span data-ttu-id="89fbe-140">La notification de [paquets](/previous-versions/ms824773(v=msdn.10)) se produit lorsque le stylet se déplace sur la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="89fbe-140">The [Packets](/previous-versions/ms824773(v=msdn.10)) notification occurs when the pen moves on the digitizer surface.</span></span> <span data-ttu-id="89fbe-141">Lorsque cela se produit, l’application ajoute de nouvelles [StylusDownData](/previous-versions/ms824107(v=msdn.10)) dans le tableau de paquets pour l’objet [Stylus](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="89fbe-141">When this occurs, the application adds new [StylusDownData](/previous-versions/ms824107(v=msdn.10)) into the packet array for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="89fbe-142">Pour ce faire, il utilise la propriété [ID](/previous-versions/ms824826(v=msdn.10)) de l’objet Stylus comme clé pour récupérer le tableau de paquets du stylet à partir de la table de hachage.</span><span class="sxs-lookup"><span data-stu-id="89fbe-142">It does this by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as the key to retrieve the packet array for the stylus from the hashtable.</span></span> <span data-ttu-id="89fbe-143">Les nouvelles données de paquet sont ensuite insérées dans le tableau récupéré.</span><span class="sxs-lookup"><span data-stu-id="89fbe-143">The new packet data is then inserted into the retrieved array.</span></span>


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



<span data-ttu-id="89fbe-144">La notification [StylusUp](/previous-versions/ms824782(v=msdn.10)) se produit lorsque le stylet quitte la surface du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="89fbe-144">The [StylusUp](/previous-versions/ms824782(v=msdn.10)) notification occurs when the pen leaves the digitizer surface.</span></span> <span data-ttu-id="89fbe-145">Lorsque cette notification se produit, l’exemple récupère le tableau de paquets pour cet objet de [stylet](/previous-versions/ms824824(v=msdn.10)) à partir de la table de hachage, en le supprimant de la table de hachage, car il n’est plus nécessaire, ajoute les nouvelles données de paquet et utilise le tableau de données de paquet pour créer un nouvel objet [Stroke](/previous-versions/ms552692(v=vs.100)) `stroke` .</span><span class="sxs-lookup"><span data-stu-id="89fbe-145">When this notification occurs, the sample retrieves the packet array for this [Stylus](/previous-versions/ms824824(v=msdn.10)) object from the hashtable-removing it from the hashtable as it is no longer needed, adds in the new packet data, and uses the array of packet data to create a new [Stroke](/previous-versions/ms552692(v=vs.100)) object, `stroke`.</span></span>


```C++
public void StylusUp(RealTimeStylus sender, StylusUpData data)
{
    ArrayList collectedPackets = (ArrayList)myPackets[data.Stylus.Id];
    myPackets.Remove(data.Stylus.Id);

    collectedPackets.AddRange(data.GetData());

    int[] packets = (int[])(collectedPackets.ToArray(typeof(int)));
    TabletPropertyDescriptionCollection tabletProperties =
        myRealTimeStylus.GetTabletPropertyDescriptionCollection(data.Stylus.TabletContextId);

    Stroke stroke = myInk.CreateStroke(packets, tabletProperties);
    if (stroke != null) 
    {
         stroke.DrawingAttributes.Color = myDynamicRenderer.DrawingAttributes.Color;
         stroke.DrawingAttributes.Width = myDynamicRenderer.DrawingAttributes.Width;
    } 
}
```



<span data-ttu-id="89fbe-146">Pour obtenir un exemple qui illustre une utilisation plus robuste de la classe [**RealTimeStylus**](realtimestylus-class.md) , y compris l’utilisation de la création d’un plug-in personnalisé, consultez [exemple de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md).</span><span class="sxs-lookup"><span data-stu-id="89fbe-146">For an example that shows more robust use of the [**RealTimeStylus**](realtimestylus-class.md) class, including the use of custom plug-in creation, see [RealTimeStylus Plug-in Sample](realtimestylus-plug-in-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89fbe-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89fbe-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="89fbe-148">[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="89fbe-148">[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="89fbe-149">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="89fbe-149">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="89fbe-150">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="89fbe-150">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="89fbe-151">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="89fbe-151">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="89fbe-152">Accès et manipulation de l’entrée du stylet</span><span class="sxs-lookup"><span data-stu-id="89fbe-152">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
