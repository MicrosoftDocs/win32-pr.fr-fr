---
description: Une fois l’encre collectée, les applications peuvent gérer, manipuler et/ou transférer ces données vers d’autres médias.
ms.assetid: 5a8c370e-79cb-47f0-a7b3-a631874ad757
title: Données manuscrites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55f62f566e48859ba2aea7013783b3ccc8c825b8559fdec34e24438d68b6ee65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939409"
---
# <a name="ink-data"></a>Données manuscrites

Une fois l’encre collectée, les applications peuvent gérer, manipuler et/ou transférer ces données vers d’autres médias. Les actions de sélection, de copie, de déplacement, d’enregistrement, d’affichage et de modification de l’encre se produisent sur l’objet [**Ink**](inkdisp-class.md) et les membres qu’il contient, [**comme les objets Stroke et**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .

> [!Note]  
> À l’aide de Real-Time stylet, les applications peuvent choisir de conserver les données dans leur propre format (par exemple, enregistrer des traits).

 

## <a name="ink-strokes-and-packets"></a>Encre, traits et paquets

Un objet [**Ink**](inkdisp-class.md) est le type de données fondamental qui gère, manipule et stocke l’entrée collectée à partir de l’objet [**InkCollector**](inkcollector-class.md) . Un objet **Ink** contient un ou plusieurs objets [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) et des méthodes et des propriétés communes pour gérer et manipuler ces traits. Un trait est défini en tant que jeu de données capturées dans une séquence de stylet, de déplacement et de stylet vers le haut unique. Les données de trait contiennent une collection de paquets. Un paquet est l’ensemble de données que le périphérique tablette envoie à chaque point d’échantillonnage. Ces données contiennent des informations telles que les coordonnées, la pression du stylet, l’angle du stylet et tout autre point que le matériel peut transmettre. La propriété [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) de l’objet **Stroke** décrit les paquets générés par une [**tablette**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) .

## <a name="strokes"></a>Traits

Vous pouvez obtenir un instantané des traits dans un objet [**Ink**](inkdisp-class.md) à l’aide de la propriété [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) de l’objet **Ink** . La propriété **Strokes** est une collection de références aux traits dans l’objet **Ink** au moment où la propriété **Strokes** est lue. Si des traits sont par la suite ajoutés ou supprimés de l’objet **Ink** , une collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) précédemment obtenue n’est pas mise à jour. En outre, la propriété **Strokes** est une valeur et, comme n’importe quelle valeur, est hors de portée, sauf si elle est assignée à une variable.

Pour conserver une propriété [**Strokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_strokes) synchronisée avec un objet [**Ink**](inkdisp-class.md) , encapsulez-la dans un gestionnaire d’événements pour les événements [**StrokesAdded**](inkstrokes-strokesadded.md) et [**StrokesRemoved**](inkstrokes-strokesremoved.md) sur la collection [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) . Le gestionnaire doit obtenir une nouvelle copie de la propriété **Strokes** lorsque l’un ou l’autre événement est déclenché. Veillez à ne pas ajouter le gestionnaire d’événements à une collection de **traits** qui est hors de portée avant le déclenchement de l’événement.

Notez dans cet exemple que `theAddedStrokesIDs` est mis à jour avec une nouvelle copie de la propriété Strokes dans le `StrokesAdded_Event` Gestionnaire.


```C++
public void StrokesAdded_Event(object sender, StrokesEventArgs e)
{
    int [] theAddedStrokesIDs = e.StrokeIds;
    theListBox.Items.Clear();
    foreach (int i in theAddedStrokesIDs)
    {
        theListBox.Items.Add("Added Stroke ID: " + i.ToString());
    }
}
```



## <a name="packetdescription-property"></a>Propriété PacketDescription

La propriété [**PacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_packetdescription) de l’objet [**Ink**](inkdisp-class.md) définit le jeu d’informations dans chaque paquet que l’application obtient à partir d’un périphérique Tablet PC. Les informations incluent généralement des coordonnées, mais elles peuvent inclure des informations bien plus détaillées (en fonction des capacités du digitaliseur Tablet PC), telles que la pression du stylet ou l’angle du stylet. En définissant des descriptions de paquets sur l’objet [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) avant la collecte de toute entrée manuscrite (à l’aide de la propriété DesiredPacketDescription), vous avez un contrôle total sur les propriétés des périphériques Tablet PC que vous souhaitez recevoir.

## <a name="extended-properties"></a>Propriétés étendues

Les propriétés étendues fournissent un mécanisme pour attacher les données définies par l’application à l' [**encre**](inkdisp-class.md) et à d’autres objets. Pour plus d’informations sur les propriétés étendues, consultez la collection [**ExtendedProperties**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties) .

## <a name="ink-rendering"></a>Rendu d’encre

L’objet de [**convertisseur**](inkrenderer-class.md) est responsable du rendu de l' [**encre**](inkdisp-class.md). À partir d’un contexte tablette approprié, l’objet de **convertisseur** peut mapper les coordonnées de l’espace manuscrit aux pixels, appliquer les transformations de vue et afficher l’encre sur les écrans et les imprimantes. Les méthodes [**Draw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) et [**DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke) sont les principales méthodes de rendu de l’encre. Pour plus d’informations sur l’affichage de l’encre dans une fenêtre, consultez l’objet **Renderer** .

## <a name="cusps"></a>Sommets

Un trait commence normalement lorsque le stylet est abaissé à la surface de dessin et se termine lorsque le stylet est déclenché. Au sein d’un trait, les pics, les angles et les changements Radicals de direction sont appelés sommets. Les points de terminaison d’un trait sont également considérés comme des sommets. Par exemple, la lettre majuscule « L » a trois sommets, l’un au milieu et l’autre à chaque extrémité.

Lorsqu’un trait est entré, il est normalement lissé et rendu à l’aide d’une courbe de Bézier (ou polyligne). Les courbes de Bézier peuvent transformer les fronces en petites boucles. Par exemple, le pic de la lettre « i » cursive peut être lissé pour ressembler à « e » cursive. Pour éviter cela, les convertisseurs Microsoft ont une phase de pré-Bézier qui gère les sommets différemment.

Les sommets peuvent également être utilisés pour subdiviser les objets [**Stroke**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en unités effaçable. Par exemple, la sélection de la partie verticale d’un « L » majuscule peut indiquer l’effacement de ce côté. La partie du trait à effacer serait la partie comprise entre deux sommets.

 

 
