---
description: Cette application montre la collecte et le rendu d’entrée manuscrite lors de l’utilisation de la classe RealTimeStylus.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: Exemple de collection d’encres RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11065a40118c83be2451f9b2ac2431e5d7edb6cf31808030861d9f059774bf78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708386"
---
# <a name="realtimestylus-ink-collection-sample"></a>Exemple de collection d’encres RealTimeStylus

Cette application montre la collecte et le rendu d’entrée manuscrite lors de l’utilisation de la classe [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="the-inkcollection-project"></a>InkCollection Project

Cet exemple se compose d’une solution unique qui contient un projet, InkCollection. L’application définit l' `InkCollection` espace de noms qui contient une seule classe, également appelée `InkCollection` . La classe hérite de la classe [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) et implémente l’interface [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



La classe InkCollection définit un ensemble de constantes privées utilisées pour spécifier différentes épaisseurs d’encre. La classe déclare également des instances privées de la classe [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , la classe [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` , et la classe de [convertisseur](/previous-versions/ms828481(v=msdn.10)) `myRenderer` . Le **DynamicRenderer** restitue le [trait](/previous-versions/ms552692(v=vs.100)) qui est actuellement collecté. L’objet de convertisseur, `myRenderer` , restitue les objets Stroke qui ont déjà été collectés.


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



La classe déclare également un objet [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , qui est utilisé pour stocker les données de paquets collectées par un ou plusieurs objets [curseur](/previous-versions/ms552104(v=vs.100)) . Les valeurs d' [ID](/previous-versions/ms824826(v=msdn.10)) de l’objet de [stylet](/previous-versions/ms824824(v=msdn.10)) sont utilisées comme clé de la Hashtable pour identifier de manière unique les données de paquet collectées pour un objet curseur donné.

Une instance privée de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) `myInk` stocke les objets [Stroke](/previous-versions/ms552692(v=vs.100)) collectés par `myRealTimeStylus` .


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>Événement de chargement de formulaire

Dans le gestionnaire d’événements [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) du formulaire, `myDynamicRenderer` est instancié à l’aide du [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) qui prend un contrôle comme argument et `myRenderer` est construit avec un constructeur sans argument.


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



Faites attention au commentaire qui suit l’instanciation des convertisseurs, car `myDynamicRenderer` utilise les valeurs par défaut pour [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) lors du rendu de l’encre. Il s’agit du comportement standard. Toutefois, si vous souhaitez donner à l’encre un rendu `myDynamicRenderer` différent de l’encre rendue par `myRenderer` , vous pouvez modifier la propriété [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) sur `myDynamicRenderer` . Pour ce faire, supprimez les marques de commentaire des lignes suivantes avant de générer et d’exécuter l’application.


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



Ensuite, l’application crée l’objet [**RealTimeStylus**](realtimestylus-class.md) qui est utilisé pour recevoir des notifications de stylet et ajoute l’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) à la file d’attente de notification de plug-in synchrone. Plus précisément, `myRealTimeStylus` ajoute `myDynamicRenderer` à la propriété [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



Le formulaire est ensuite ajouté à la file d’attente de notification du plug-in asynchrone. Plus précisément, `InkCollection` est ajouté à la propriété [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) . Enfin, `myRealTimeStylus` et `myDynamicRenderer` sont activés, et MyPackets et myInk sont instanciés.


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



Hormis le raccordement des gestionnaires de menus pour modifier la couleur et la taille de l’encre, un bloc de code plus bref est requis avant d’implémenter l’interface. l’exemple doit gérer l’événement [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) du formulaire. dans le gestionnaire d’événements, l’application doit `myDynamicRenderer` être actualisée, car il est possible qu’un objet [Stroke](/previous-versions/ms552692(v=vs.100)) soit collecté au moment où se produit l’événement Paint. Dans ce cas, la partie de l’objet Stroke qui a déjà été collectée doit être redessinée. Le [convertisseur](/previous-versions/ms828481(v=msdn.10)) statique est utilisé pour redessiner les objets Stroke qui ont déjà été collectés. Ces traits se trouvent dans l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) , car ils sont placés là où ils sont dessinés, comme indiqué dans la section suivante.


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>Implémentation de l’interface IStylusAsyncPlugin

L’exemple d’application définit les types de notifications qu’il a intérêt à recevoir dans l’implémentation de la propriété [DataInterest](/previous-versions/ms824769(v=msdn.10)) . La propriété DataInterest définit donc les notifications transférées par l’objet [**RealTimeStylus**](realtimestylus-class.md) au formulaire. Pour cet exemple, la propriété DataInterest définit l’intérêt pour les **StylusDown**, les **paquets**, les **StylusUp** et les notifications d' **erreur** par le biais de l’énumération [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .


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



La notification [StylusDown](/previous-versions/ms824779(v=msdn.10)) se produit lorsque le stylet touche la surface du digitaliseur. Dans ce cas, l’exemple alloue un tableau qui est utilisé pour stocker les données du paquet pour l’objet de [stylet](/previous-versions/ms824824(v=msdn.10)) . Le [StylusDownData](/previous-versions/ms824107(v=msdn.10)) de la méthode StylusDown est ajouté au tableau et le tableau est inséré dans la table de hachage en utilisant la propriété [ID](/previous-versions/ms824826(v=msdn.10)) de l’objet Stylus comme clé.


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



La notification de [paquets](/previous-versions/ms824773(v=msdn.10)) se produit lorsque le stylet se déplace sur la surface du digitaliseur. Lorsque cela se produit, l’application ajoute de nouvelles [StylusDownData](/previous-versions/ms824107(v=msdn.10)) dans le tableau de paquets pour l’objet [Stylus](/previous-versions/ms824824(v=msdn.10)) . Pour ce faire, il utilise la propriété [ID](/previous-versions/ms824826(v=msdn.10)) de l’objet Stylus comme clé pour récupérer le tableau de paquets du stylet à partir de la table de hachage. Les nouvelles données de paquet sont ensuite insérées dans le tableau récupéré.


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



La notification [StylusUp](/previous-versions/ms824782(v=msdn.10)) se produit lorsque le stylet quitte la surface du digitaliseur. Lorsque cette notification se produit, l’exemple récupère le tableau de paquets pour cet objet de [stylet](/previous-versions/ms824824(v=msdn.10)) à partir de la table de hachage, en le supprimant de la table de hachage, car il n’est plus nécessaire, ajoute les nouvelles données de paquet et utilise le tableau de données de paquet pour créer un nouvel objet [Stroke](/previous-versions/ms552692(v=vs.100)) `stroke` .


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



Pour obtenir un exemple qui illustre une utilisation plus robuste de la classe [**RealTimeStylus**](realtimestylus-class.md) , y compris l’utilisation de la création d’un plug-in personnalisé, consultez [exemple de plug-in RealTimeStylus](realtimestylus-plug-in-sample.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
