---
title: Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle
description: Les contrôles hébergés dans la barre de commandes du ruban sont soumis aux règles de disposition appliquées par l’infrastructure du ruban Windows et basées sur une combinaison de comportements par défaut et de modèles de disposition (à la fois définis par l’infrastructure et personnalisées) comme déclaré dans le balisage du ruban. Ces règles définissent les comportements de disposition adaptative de l’infrastructure du ruban qui influencent la manière dont les contrôles de la barre de commandes s’adaptent aux différentes tailles de ruban au moment de l’exécution.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Ruban Windows, personnalisation
- Ruban, personnalisation
- Ruban Windows, modèles SizeDefinition
- Ruban, modèles SizeDefinition
- Ruban Windows, modèles personnalisés
- Ruban, modèles personnalisés
- personnalisation du ruban Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6576a672aa8c3d328a341370a7568595e988908
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444140"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle

Les contrôles hébergés dans la barre de commandes du ruban sont soumis aux règles de disposition appliquées par l’infrastructure du ruban Windows et basées sur une combinaison de comportements par défaut et de modèles de disposition (à la fois définis par l’infrastructure et personnalisées) comme déclaré dans le balisage du ruban. Ces règles définissent les comportements de disposition adaptative de l’infrastructure du ruban qui influencent la manière dont les contrôles de la barre de commandes s’adaptent aux différentes tailles de ruban au moment de l’exécution.

-   [Introduction](#introduction)
    -   [Modèles SizeDefinition du ruban](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Modèles personnalisés](#custom-templates)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

La disposition adaptative, telle que définie par l’infrastructure du ruban, est la capacité de tous les contrôles dans l’interface utilisateur du ruban à ajuster dynamiquement leur organisation, leur taille, leur format et leur échelle relative en fonction des modifications apportées à la taille du ruban au moment de l’exécution.

L’infrastructure expose les fonctionnalités de disposition adaptative via un ensemble d’éléments de balisage dédiés à la spécification et à la personnalisation de divers comportements de disposition. Une collection de modèles, appelée [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), est définie par l’infrastructure, qui prend en charge différents scénarios de contrôle et de mise en page. Toutefois, le Framework prend également en charge les modèles personnalisés si les modèles prédéfinis ne fournissent pas l’expérience de l’interface utilisateur ou les dispositions requises par une application.

Pour afficher les contrôles dans une disposition par défaut à une taille de ruban particulière, les modèles prédéfinis et les modèles personnalisés fonctionnent conjointement avec l’élément [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) . Cet élément contient un manifeste des préférences de taille que l’infrastructure utilise comme guide lors du rendu du ruban.

> [!Note]  
> L’infrastructure du ruban fournit des comportements de disposition par défaut basés sur un ensemble d’heuristiques intégrées pour l’organisation et la présentation des contrôles au moment de l’exécution sans avoir besoin des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) prédéfinis. Toutefois, cette fonctionnalité est destinée uniquement à des fins de prototypage.

 

### <a name="ribbon-sizedefinition-templates"></a>Modèles SizeDefinition du ruban

L’infrastructure du ruban fournit un ensemble complet de modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) qui spécifient le comportement de taille et de disposition pour un [Groupe](windowsribbon-controls-group.md) de contrôles de ruban. Ces modèles couvrent la plupart des scénarios courants d’organisation des contrôles dans une application de ruban.

Pour garantir une expérience utilisateur cohérente entre les applications du ruban, chaque modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impose des restrictions sur les contrôles ou la famille de contrôles qu’il prend en charge.

Par exemple, la famille de contrôles Button comprend les éléments suivants :

-   [Button](windowsribbon-controls-button.md)
-   [Bouton bascule](windowsribbon-controls-togglebutton.md)
-   [Bouton déroulant](windowsribbon-controls-dropdownbutton.md)
-   [Bouton partagé](windowsribbon-controls-splitbutton.md)
-   [Galerie déroulante](windowsribbon-controls-dropdowngallery.md)
-   [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md)
-   [Sélecteur de couleurs déroulantes](windowsribbon-controls-dropdowncolorpicker.md)

La famille de contrôles d’entrée comprend les éléments suivants :

-   [Zone de liste déroulante](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

La case [à cocher](windowsribbon-controls-checkbox.md) et la [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md) n’appartiennent ni à la famille de boutons, ni à la famille d’entrée. Ces deux contrôles peuvent être utilisés uniquement lorsqu’ils sont explicitement indiqués dans un modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

La liste suivante répertorie les modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) avec une description de la disposition et des contrôles autorisés par chaque modèle.

> [!IMPORTANT]
> Si les contrôles déclarés dans le balisage ne sont pas mappés exactement au type de contrôle, à l’ordre et à la quantité définis dans le modèle associé, une [erreur de validation](windowsribbon-compilationerrors.md) est journalisée par le [compilateur de balisage](windowsribbon-intentcl.md) et la compilation est terminée.

 



OneButton

Un contrôle de famille de bouton.<br/> Seule la taille de groupe importante est prise en charge.<br/>

![image du modèle oneButton sizedefinition.](images/overviews/sizedefinition-onebutton.png)

TwoButtons

Deux contrôles de famille de boutons.<br/> Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.<br/>

![image du modèle twobuttons large sizedefinition.](images/overviews/sizedefinition-twobuttons-large.png)

![image du modèle twobuttons Medium sizedefinition.](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

Trois contrôles de la famille de boutons.<br/> Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.<br/>

![image du modèle threebuttons large sizedefinition.](images/overviews/sizedefinition-threebuttons-large.png)

![image du modèle threebuttons Medium sizedefinition.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Trois contrôles de la famille de boutons.<br/> Le premier bouton est présenté de façon visible dans les trois tailles.<br/>

![image du modèle de grand sizedefinition threebuttons-onebigandtwosmall.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![image du modèle threebuttons-onebigandtwosmall Medium sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![image du modèle threebuttons-onebigandtwosmall Small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

Trois contrôles de famille de boutons accompagnés d’un seul contrôle CheckBox.<br/> Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.<br/>

![image du modèle threebuttonsandonecheckbox large sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![image du modèle threebuttonsandonecheckbox Medium sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

Quatre contrôles de la famille de boutons.<br/>

![image du modèle fourbuttons large sizedefinition.](images/overviews/sizedefinition-fourbuttons-large.png)

![image du modèle fourbuttons Medium sizedefinition.](images/overviews/sizedefinition-fourbuttons-medium.png)

![image du modèle fourbuttons Small sizedefinition.](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

Cinq contrôles de famille de boutons.<br/>

![image du modèle fivebuttons large sizedefinition.](images/overviews/sizedefinition-fivebuttons-large.png)

![image du modèle fivebuttons Medium sizedefinition.](images/overviews/sizedefinition-fivebuttons-medium.png)

![image du modèle fivebuttons Small sizedefinition.](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

Cinq contrôles de famille de boutons et un sixième bouton facultatif.<br/>

![image du modèle fiveorsixbuttons large sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![image du modèle fiveorsixbuttons Medium sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![image du modèle fiveorsixbuttons Small sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

Six contrôles de famille de boutons.<br/>

![image du modèle sixbuttons large sizedefinition.](images/overviews/sizedefinition-sixbuttons-large.png)

![image du modèle sixbuttons Medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-medium.png)

![image du modèle sixbuttons Small sizedefinition.](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Six contrôles de famille de boutons (autre présentation).<br/>

![image du modèle de grand sizedefinition sixbuttons-twocolumns.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![modèle sixbuttons-twocolumns Medium sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![image du modèle sixbuttons-twocolumns Small sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

Sept contrôles de la famille de boutons.<br/>

![image du modèle sevenbuttons large sizedefinition.](images/overviews/sizedefinition-sevenbuttons-large.png)

![image du modèle sevenbuttons mediumsizedefinition.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![image du modèle sevenbuttons Small sizedefinition.](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

Huit contrôles de la famille de boutons.<br/>

![image du modèle de grand sizedefinition eightbuttons-lastthreesmall.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![image du modèle eightbuttons-lastthreesmall Medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![image du modèle eightbuttons-lastthreesmall Small sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Huit contrôles de la famille de boutons (autre présentation).<br/>

> [!Note]  
> Tous les éléments de contrôle déclarés avec ce modèle doivent être contenus dans deux éléments [**ControlGroup**](windowsribbon-element-controlgroup.md) : un pour les cinq premiers éléments et un pour les trois derniers éléments.

<br/> L’exemple suivant illustre le balisage requis pour ce modèle.<br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![image du modèle eightbuttons large sizedefinition.](images/overviews/sizedefinition-eightbuttons-large.png)

![image du modèle eightbuttons Medium sizedefinition.](images/overviews/sizedefinition-eightbuttons-medium.png)

![image du modèle eightbuttons Small sizedefinition.](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

Neuf contrôles de la famille de boutons.

![image du modèle ninebuttons large sizedefinition.](images/overviews/sizedefinition-ninebuttons-large.png)

![image du modèle ninebuttons Medium sizedefinition.](images/overviews/sizedefinition-ninebuttons-medium.png)

![image du modèle ninebuttons Small sizedefinition.](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

Dix contrôles de la famille de boutons.

![image du modèle tenbuttons large sizedefinition.](images/overviews/sizedefinition-tenbuttons-large.png)

![image du modèle tenbuttons Medium sizedefinition.](images/overviews/sizedefinition-tenbuttons-medium.png)

![image du modèle tenbuttons Small sizedefinition.](images/overviews/sizedefinition-tenbuttons-small.png)

ElevenButtons

Onze contrôles de la famille de boutons.

![image du modèle elevenbuttons large sizedefinition.](images/overviews/sizedefinition-elevenbuttons-large.png)

![image du modèle elevenbuttons Medium sizedefinition.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![image du modèle elevenbuttons Small sizedefinition.](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

Un [**FontControl**](windowsribbon-element-fontcontrol.md).

Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.

> [!IMPORTANT]
> L’inclusion d’un [**FontControl**](windowsribbon-element-fontcontrol.md) dans une définition de modèle personnalisé n’est pas prise en charge par l’infrastructure.

 

![image du modèle onefontcontrol large sizedefinition.](images/overviews/sizedefinition-onefontcontrol-large.png)

![image du modèle onefontcontrol Medium sizedefinition.](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

Un contrôle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .

Seules les tailles de groupe de grande et de petite taille sont prises en charge.

![image du modèle oneinribbongallery large sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![image du modèle oneinribbongallery Small sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

Un contrôle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) et un contrôle de famille de boutons.

Seules les tailles de groupe de grande et de petite taille sont prises en charge.

![image du modèle inribbongalleryandbigbutton large sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![image du modèle inribbongalleryandbigbutton Small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Un contrôle [de galerie dans le ruban](windowsribbon-controls-inribbongallery.md) et deux ou trois contrôles de la famille de boutons.

La Galerie est réduite à une représentation contextuelle dans des tailles de groupes de taille moyenne et petite.

![image du modèle de grand sizedefinition inribbongalleryandbuttons-galleryscalesfirst.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![image du modèle inribbongalleryandbuttons-galleryscalesfirst Medium sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![image du modèle inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

Disposition complexe des contrôles de famille de boutons 32 (la plupart sont facultatifs).

> [!Note]  
> À part le bouton en pleine taille facultatif du modèle ButtonGroups de grande taille, tous les éléments de contrôle déclarés avec ce modèle doivent être contenus dans les éléments [**ControlGroup**](windowsribbon-element-controlgroup.md) .

 

L’exemple suivant illustre le balisage requis pour afficher tous les éléments de contrôle 32 (obligatoires et facultatifs) avec ce modèle.


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![image du modèle ButtonGroups large sizedefinition.](images/overviews/sizedefinition-buttongroups-large.png)

![image du modèle ButtonGroups Medium sizedefinition.](images/overviews/sizedefinition-buttongroups-medium.png)

![image du modèle ButtonGroups Small sizedefinition.](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

Deux contrôles de la famille d’entrée (le second est facultatif) suivis d’une disposition complexe de 29 contrôles de famille de boutons (la plupart sont facultatifs).

Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.

> [!Note]  
> Tous les éléments de contrôle déclarés avec ce modèle doivent être contenus dans les éléments [**ControlGroup**](windowsribbon-element-controlgroup.md) .

 

L’exemple suivant illustre le balisage requis pour afficher tous les éléments de contrôle (obligatoires et facultatifs) avec ce modèle.


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![image du modèle buttongroupsandinputs large sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![image du modèle buttongroupsandinputs Medium sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

Deux contrôles de famille de boutons (à la fois facultatifs) suivis de deux ou trois contrôles Button ou Family.

Seules les tailles de groupe de taille moyenne et moyenne sont prises en charge.

![image du modèle bigbuttonsandsmallbuttonsorinputs large sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![image du modèle bigbuttonsandsmallbuttonsorinputs Medium sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Exemple de SizeDefinition de base

L’exemple de code suivant fournit une démonstration de base sur la façon de déclarer un modèle [**SizeDefinition**](windowsribbon-element-sizedefinition.md) dans le balisage du ruban.

L' *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) est utilisé pour cet exemple particulier, mais tous les modèles d’infrastructure sont spécifiés de manière similaire.


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Exemple de SizeDefinition complexe avec des stratégies de mise à l’échelle

Le comportement de réduction des modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) peut être contrôlé à l’aide de stratégies de mise à l’échelle dans le balisage du ruban.

L’élément [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contient un manifeste de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) et des déclarations de mise à l' [**échelle**](windowsribbon-element-scale.md) qui spécifient des préférences de disposition adaptative pour un ou plusieurs éléments de [**groupe**](windowsribbon-element-group.md) lorsque le ruban est redimensionné.

> [!Note]  
> Il est fortement recommandé de spécifier des détails de stratégie de mise à l’échelle adéquats de sorte que la plupart des éléments de [**groupe**](windowsribbon-element-group.md) soient associés à un élément d' [**échelle**](windowsribbon-element-scale.md) où l’attribut de *taille* est égal à `Popup` . Cela permet à l’infrastructure d’afficher le ruban à la plus petite taille possible et de prendre en charge la plus large gamme de périphériques d’affichage, avant d’introduire automatiquement un mécanisme de défilement.

 

L’exemple de code suivant montre un manifeste [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) qui spécifie une préférence [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pour chacun des quatre groupes de contrôles sur un onglet de **démarrage** . En outre, les éléments de mise à l' [**échelle**](windowsribbon-element-scale.md) sont spécifiés pour influencer le comportement de réduction, dans l’ordre de la taille décroissant, de chaque groupe.


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a>Modèles personnalisés

Si les comportements de disposition par défaut et les modèles [**SizeDefinition**](windowsribbon-element-sizedefinition.md) prédéfinis n’offrent pas la flexibilité ou la prise en charge d’un scénario de disposition particulier, les modèles personnalisés sont pris en charge par l’infrastructure du ruban via l’élément [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .

Les modèles personnalisés peuvent être déclarés de deux façons : une méthode autonome à l’aide de l’élément [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) pour la déclaration de modèles réutilisables, nommés ou une méthode Inline spécifique à un [**groupe**](windowsribbon-element-group.md).

### <a name="standalone-template"></a>Modèle autonome

L’exemple de code suivant illustre un modèle personnalisé de base, réutilisable.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a>Modèle Inline

Les exemples de code suivants illustrent un modèle personnalisé inline de base pour un groupe de quatre boutons.

Cette section de code montre les déclarations de commande pour un groupe de boutons. Les grandes et les petites ressources d’images sont également spécifiées ici.


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



Cette section de code montre comment définir des modèles [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) volumineux, moyens et petits pour afficher les quatre boutons à différentes tailles et dispositions. La Déclaration [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) pour l’onglet définit le modèle utilisé pour un groupe de contrôles en fonction de la taille du ruban et de l’espace requis par l’onglet actif.


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



Les images suivantes montrent comment les modèles de l’exemple précédent sont appliqués à l’interface ruban pour s’adapter à une diminution de la taille du ruban.



|  Type  |      Image                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| Large  | ![image d’un modèle personnalisé de grande taille en ligne.](images/overviews/sizedefinition-custom-large.png)   |
| Moyenne | ![image d’un modèle personnalisé de moyenne en ligne.](images/overviews/sizedefinition-custom-medium.png) |
| Small  | ![image d’un petit modèle personnalisé en ligne.](images/overviews/sizedefinition-custom-small.png)   |
| Fenêtre contextuelle  | ![image d’un modèle personnalisé contextuelle en ligne.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Mise à l’échelle**](windowsribbon-element-scale.md)
</dt> <dt>

[**Groupe**](windowsribbon-element-group.md)
</dt> </dl>

 

 





