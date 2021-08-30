---
title: Groupe de menus
description: Le groupe de menus organise les commandes et les contrôles connexes dans un menu ou une barre d’outils.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f734b852df94bf953ccc8b89581da0253e070f33e9af6bec516dd4c923bd6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933292"
---
# <a name="menu-group"></a>Groupe de menus

Le groupe de menus organise les commandes et les contrôles connexes dans un menu ou une barre d’outils.

-   [Introduction](#introduction)
-   [Propriétés du groupe de menus](#menu-group-properties)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Le contrôle de groupe de menus, exposé via l’élément de balisage [**MenuGroup**](windowsribbon-element-menugroup.md) , est un conteneur logique pour les groupes d’éléments ou de commandes dans les contrôles basés sur des menus, y compris la mini-barre d’outils [contextuelle](windowsribbon-controls-contextpopup.md) .

Une étiquette peut être spécifiée pour un groupe de menus via l’attribut *LabelTitle* ou la propriété [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) d’une déclaration de commande associée. La valeur assignée à *LabelTitle* est rendue sous la forme d’un en-tête de catégorie.

L’exemple suivant illustre le balisage de commande pour un contrôle [bouton partagé](windowsribbon-controls-splitbutton.md) qui comprend deux déclarations de commande de groupe de menus.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



L’exemple suivant illustre le balisage requis pour un élément [**SplitButton**](windowsribbon-element-splitbutton.md) avec trois déclarations d’élément [**MenuGroup**](windowsribbon-element-menugroup.md) , deux d’entre elles étant associées aux commandes de groupe de menus de l’exemple précédent. L’attribut *Class* de l’élément **MenuGroup** est utilisé pour spécifier la taille des éléments de menu.


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



La capture d’écran suivante illustre le menu (avec trois contrôles de groupe de menus) généré à partir du balisage dans les exemples précédents.

![capture d’écran d’un menu avec trois contrôles de groupe de menus.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a>Propriétés du groupe de menus

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de groupe de menus.

En général, une propriété de groupe de menus est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle de groupe de menus.



| Clé de propriété                                                                                     | Remarques                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IU-au-dessus \_ \_ activé](windowsribbon-reference-properties-uipkey-enabled.md)                       | Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)                           | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |
| [IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément de balisage MenuGroup**](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 