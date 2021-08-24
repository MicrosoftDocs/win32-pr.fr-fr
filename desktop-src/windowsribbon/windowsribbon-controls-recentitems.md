---
title: Éléments récents
description: La liste éléments récents est un volet du menu de l’application qui affiche les éléments utilisés récemment (MRU) pour une application.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1d67c38e1eb9014cfd3349881ed2849755ebc89489cc925052aa690f54adc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810877"
---
# <a name="recent-items"></a>Éléments récents

La liste éléments récents est un volet du menu de l' [application](windowsribbon-controls-applicationmenu.md) qui affiche les éléments utilisés récemment (MRU) pour une application.

-   [Détails](#details)
-   [Propriétés des éléments récents](#recent-items-properties)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="details"></a>Détails

la capture d’écran suivante illustre une liste d’éléments récents de WordPad pour Windows 7).

![capture d’écran de la liste des éléments récents dans le ruban Microsoft Paint.](images/controls/recentitems.png)

Le [menu application](windowsribbon-controls-applicationmenu.md) ne peut avoir qu’une seule liste [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , représentée par un élément **ApplicationMenu. RecentItems** , pour afficher les documents récents, les images, les films et les autres projets sur lesquels un utilisateur a travaillé. Le nombre d’éléments listés est compris entre zéro et le nombre maximal spécifié dans le balisage, avec une valeur par défaut de 10. Les éléments récents s’affichent sous la forme d’une liste numérotée de chaînes indiquant les noms de fichiers. Il est recommandé d’utiliser la propriété [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) pour fournir le chemin d’accès complet de l’emplacement du fichier, comme illustré dans la capture d’écran suivante.

![capture d’écran d’une liste d’éléments récents dans un menu d’application.](images/overviews/applicationmenu-menurecentitems.png)

L’élément [**RecentItems**](windowsribbon-element-recentitems.md) a un attribut *EnablePinning* qui, s’il est défini sur `true` , affiche une icône d’épingle à droite de chaque élément de la liste, comme illustré dans la capture d’écran suivante.

> [!Note]  
> L’épinglage est activé par défaut si l’attribut *EnablePinning* n’est pas spécifié.

 

![capture d’écran de l’épinglage d’éléments récents dans un menu d’application.](images/overviews/applicationmenu-menurecentitemspinned.png)

L’algorithme épinglé est conçu pour empêcher les éléments de tomber dans la liste des **éléments récents** . L’algorithme produit le comportement suivant :

-   Un nouvel élément est toujours ajouté en haut de la liste des **éléments récents** .
-   Les éléments se déplacent dans la liste au fil du temps. Une fois la liste complète (atteint le nombre maximal d’éléments spécifiés dans le balisage), les éléments les plus anciens se trouvent en bas de la liste à mesure que de nouveaux éléments sont ajoutés en haut de la liste.
-   Si un élément figure déjà dans la liste, mais fait l’objet d’un nouvel accès, il revient en haut de la liste.
-   Si un élément est épinglé, il continue de parcourir la liste, mais il ne se situe pas en bas. Au lieu de cela, une fois que la liste est pleine, le premier élément non épinglé au-dessus de l’élément épinglé s’arrête lorsqu’un nouvel élément est ajouté à la liste.
-   Si le nombre d’éléments épinglés atteint toujours le nombre maximal d’éléments, aucun nouvel élément n’est ajouté à la liste tant qu’un élément n’est pas épinglé.

## <a name="recent-items-properties"></a>Propriétés des éléments récents

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle d’éléments récents.

En général, une propriété Items récente est mise à jour dans l’interface ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle éléments récents.



| Clé de propriété                                                                       | Notes                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)           | Peut uniquement être mis à jour par le biais d’une invalidation. |
| [IU \_ \_ RecentItems](windowsribbon-reference-properties-uipkey-recentitems.md) | Peut uniquement être mis à jour par le biais d’une invalidation. |



 

## <a name="remarks"></a>Remarques

la méthode [IApplicationDocumentLists :: GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) peut être utilisée pour récupérer la liste des derniers fichiers de l’interpréteur de commandes Windows pour l’application ruban. L’objet récupéré par cette méthode peut ensuite être utilisé par l’application pour créer les données requises par l’infrastructure du ruban pour remplir la liste des **éléments récents** du menu de l' [application](windowsribbon-controls-applicationmenu.md).

> [!Note]  
> Lors de l’utilisation de cette méthode, *ListType* doit avoir la valeur `ADLT_RECENT` .

 

Pour obtenir un exemple d’implémentation d’une liste d’éléments MRU dans une application de Framework de ruban, consultez l' [exemple HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage des éléments récents**](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 