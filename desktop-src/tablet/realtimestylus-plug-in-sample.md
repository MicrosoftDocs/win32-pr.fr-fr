---
description: Cette application illustre l’utilisation de la classe RealTimeStylus.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Exemple de plug-in RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404757"
---
# <a name="realtimestylus-plug-in-sample"></a>Exemple de plug-in RealTimeStylus

Cette application illustre l’utilisation de la classe [**RealTimeStylus**](realtimestylus-class.md) . Pour obtenir une vue d’ensemble détaillée des API StylusInput, y compris la classe **RealTimeStylus** , consultez [accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md). Pour plus d’informations sur les plug-ins synchrones et asynchrones, consultez [plug-ins et la classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="overview-of-the-sample"></a>Vue d’ensemble de l’exemple

Les plug-ins, objets qui implémentent l’interface [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) ou [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) peuvent être ajoutés à un objet [**RealTimeStylus**](realtimestylus-class.md) . Cet exemple d’application utilise plusieurs types de plug-in :

-   Plug-in de filtre de paquets : modifie les paquets. Dans cet exemple, le plug-in de filtre de paquets modifie les informations de paquets en limitant toutes les données de paquet (x, y) au sein d’une zone rectangulaire.
-   Plug-in de rendu dynamique personnalisé : modifie les qualités de rendu dynamiques. Dans cet exemple, le plug-in de rendu dynamique personnalisé modifie la façon dont l’encre est rendue en dessinant un petit cercle autour de chaque point (x, y) sur un trait.
-   Plug-in de rendu dynamique : modifie les qualités de rendu dynamiques. Cet exemple illustre l’utilisation de l’objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) en tant que plug-in pour gérer le rendu dynamique de l’encre.
-   Plug-in de module de reconnaissance de mouvement : reconnaît les gestes d’application. Cet exemple illustre l’utilisation de l’objet [**GestureRecognizer**](gesturerecognizer-class.md) en tant que plug-in pour reconnaître les gestes d’application (en cas d’exécution sur un système sur lequel le module de reconnaissance de mouvement Microsoft est présent).

En outre, cet exemple fournit une interface utilisateur qui permet à l’utilisateur d’ajouter, de supprimer et de modifier l’ordre de chaque plug-in de la collection. L’exemple de solution contient deux projets, RealTimeStylusPluginApp et RealTimeStylusPlugins. RealTimeStylusPluginApp contient l’interface utilisateur de l’exemple. RealTimeStylusPlugins contient les implémentations des plug-ins. Le projet RealTimeStylusPlugins définit l’espace de noms RealTimeStylusPlugins, qui contient les plug-ins filtre de paquets et convertisseur dynamique personnalisé. Cet espace de noms est référencé par le projet RealTimeStylusPluginApp. Le projet RealTimeStylusPlugins utilise les espaces de noms [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))et [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .

Pour obtenir une vue d’ensemble des espaces de noms [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) et [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) , consultez [architecture des API StylusInput](architecture-of-the-stylusinput-apis.md).

## <a name="packet-filter-plug-in"></a>Plug-in de filtre de paquets

Le plug-in de filtre de paquets est un plug-in synchrone qui illustre la modification de paquets. Plus précisément, il définit un rectangle sur le formulaire. Tous les paquets qui sont dessinés en dehors de la région sont rendus à l’intérieur de la région. La classe de plug-in, `PacketFilterPlugin` , s’inscrit pour la notification des `StylusDown` `StylusUp` `Packets` événements d’entrée de stylet, et. La classe implémente les méthodes [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10))et [Packets](/previous-versions/ms824756(v=msdn.10)) définies sur la classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .

Le constructeur public pour `PacketFilterPlugin` requiert une structure [rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) . Ce rectangle définit la zone rectangulaire, en coordonnées d’espace d’encre (. 01mm = 1 unité HIMETRIC), dans laquelle les paquets seront contenus. Le rectangle est conservé dans un champ privé, `rectangle` .


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



La `PacketFilterPlugin` classe s’inscrit pour les notifications d’événements en implémentant l’accesseur get pour la propriété [DataInterest](/previous-versions/ms824752(v=msdn.10)) . Dans ce cas, le plug-in s’intéresse à répondre aux `StylusDown` `Packets` `StylusUp` notifications,, et `Error` . L’exemple retourne ces valeurs telles qu’elles sont définies dans l’énumération [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) . La méthode [StylusDown](/previous-versions/ms824761(v=msdn.10)) est appelée lorsque l’info-bulle du stylet contacte la surface du digitaliseur. La méthode [StylusUp](/previous-versions/ms824764(v=msdn.10)) est appelée lorsque la pointe du stylet quitte la surface du digitaliseur. La méthode [Packets](/previous-versions/ms824756(v=msdn.10)) est appelée lorsque l’objet [**RealTimeStylus**](realtimestylus-class.md) reçoit des paquets. La méthode d' [erreur](/previous-versions/ms585069(v=vs.100)) est appelée quand le plug-in actuel ou un plug-in précédent lève une exception.


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



La `PacketFilterPlugin` classe gère la plupart de ces notifications dans une méthode d’assistance, `ModifyPacketData` . La `ModifyPacketData` méthode obtient les valeurs x et y de chaque nouveau paquet de la classe [PacketsData](/previous-versions/ms824590(v=msdn.10)) . Si l’une des valeurs est à l’extérieur du rectangle, la méthode remplace la valeur par le point le plus proche qui se trouve toujours dans le rectangle. Il s’agit d’un exemple de la façon dont un plug-in peut remplacer des données de paquets au fur et à mesure de leur réception à partir du flux d’entrée de stylet.


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



## <a name="custom-dynamic-renderer-plug-in"></a>Plug-in de rendu dynamique personnalisé

La `CustomDynamicRenderer` classe implémente également la classe [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) pour recevoir des notifications d’entrée de stylet. Il gère ensuite la `Packets` notification pour dessiner un petit cercle autour de chaque nouveau point de paquet.

La classe contient une variable [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) qui contient une référence à l’objet Graphics passé dans le constructeur de classe. Il s’agit de l’objet Graphics utilisé pour le rendu dynamique.


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



Lorsque le plug-in de rendu dynamique personnalisé reçoit une notification de paquets, il extrait les données (x, y) et dessine un petit cercle vert autour du point. Il s’agit d’un exemple de rendu personnalisé basé sur le flux d’entrée de stylet.


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



## <a name="the-realtimestyluspluginapp-project"></a>RealTimeStylusPluginApp Project

Le projet RealTimeStylusPluginApp illustre les plug-ins décrits précédemment, ainsi que les plug-ins [**GestureRecognizer**](gesturerecognizer-class.md) et [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . L’interface utilisateur du projet se compose des éléments suivants :

-   Formulaire qui contient un contrôle [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) utilisé pour définir la zone d’entrée manuscrite.
-   Un contrôle [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) pour répertorier et sélectionner les plug-ins disponibles.
-   Paire d' [objets bouton](/dotnet/api/system.windows.forms.button?view=netcore-3.1) qui permet de réorganiser les plug-ins.

Le projet définit une structure, `PlugInListItem` , pour faciliter la gestion des plug-ins utilisés dans le projet. La `PlugInListItem` structure contient le plug-in et une description.

La `RealTimeStylusPluginApp` classe elle-même implémente la classe [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Cela est nécessaire afin que la `RealTimeStylusPluginApp` classe puisse être notifiée lorsque le plug-in [**GestureRecognizer**](gesturerecognizer-class.md) ajoute des données de mouvement à la file d’attente de sortie. L’application s’inscrit à la notification de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)). Une fois les données de mouvement reçues, `RealTimeStylusPluginApp` les insèrent une description dans la barre d’État en bas du formulaire.


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
> Dans l’implémentation [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) , il est intéressant de pouvoir identifier les données de mouvement personnalisées dans la file d’attente de sortie par GUID (à l’aide du champ [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ) ou par type (à l’aide du résultat de l’instruction As). L’exemple utilise les deux techniques d’identification à des fins de démonstration. L’une ou l’autre approche est également valide.

 

Dans le gestionnaire d’événements Load du formulaire, l’application crée des instances `PacketFilter` des `CustomDynamicRenderer` classes et, puis les ajoute à la zone de liste. L’application tente ensuite de créer une instance de la classe [**GestureRecognizer**](gesturerecognizer-class.md) et, en cas de réussite, l’ajoute à la zone de liste. Cela échoue si le module de reconnaissance de mouvement n’est pas présent sur le système. Ensuite, l’application instancie un objet [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) et l’ajoute à la zone de liste. Enfin, l’application active chacun des plug-ins et l’objet [**RealTimeStylus**](realtimestylus-class.md) lui-même.

Il est également important de noter que dans les méthodes d’assistance, l’objet [**RealTimeStylus**](realtimestylus-class.md) est désactivé avant l’ajout ou la suppression de plug-ins, puis réactivé une fois l’ajout ou la suppression terminé.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[Accès et manipulation de l’entrée du stylet](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[Plug-ins et classe RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[Exemple de collection d’encres RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
