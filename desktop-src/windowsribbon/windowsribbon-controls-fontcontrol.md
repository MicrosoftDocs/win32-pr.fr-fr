---
title: Contrôle de police
description: pour simplifier l’intégration et la configuration de la prise en charge des polices dans les applications qui requièrent des fonctionnalités de traitement de texte et d’édition de texte, l’infrastructure du ruban Windows fournit un contrôle de police spécialisé qui expose une large gamme de propriétés de police, telles que le nom, le style, la taille des points et les effets.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106163c03c506e438ffcffa261ebd7e3a2115e2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226156"
---
# <a name="font-control"></a>Contrôle de police

pour simplifier l’intégration et la configuration de la prise en charge des polices dans les applications qui requièrent des fonctionnalités de traitement de texte et d’édition de texte, l’infrastructure du ruban Windows fournit un contrôle de police spécialisé qui expose une large gamme de propriétés de police, telles que le nom, le style, la taille des points et les effets.

-   [Introduction](#introduction)
-   [Une expérience cohérente](#a-consistent-experience)
-   [Intégration et configuration faciles](#easy-integration-and-configuration)
-   [Alignement avec les structures de texte GDI courantes](#alignment-with-common-gdi-text-structures)
-   [Ajouter un FontControl](#add-a-fontcontrol)
    -   [Déclaration d’un FontControl dans le balisage](#declaring-a-fontcontrol-in-markup)
    -   [Propriétés du contrôle de police](#font-control-properties)
-   [Définir un gestionnaire de commandes FontControl](#define-a-fontcontrol-command-handler)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Le contrôle de police est un contrôle composite qui se compose de boutons, de boutons bascule, de zones de liste déroulante et de zones de liste déroulante, qui sont toutes utilisées pour spécifier une propriété de police ou une option de mise en forme particulière.

la capture d’écran suivante montre le contrôle de police du ruban dans WordPad pour Windows 7.

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>Une expérience cohérente

En tant que contrôle de ruban intégré, le contrôle de police améliore la gestion globale des polices, la fonctionnalité de sélection et de mise en forme et offre une expérience utilisateur riche et cohérente pour toutes les applications de ruban.

Cette expérience cohérente comprend

-   Mise en forme standardisée et sélection des polices dans les applications du ruban.
-   Représentation de police standardisée dans les applications de ruban.
-   automatique, dans Windows 7, activation de la police basée sur le paramètre **afficher** ou **masquer** pour chaque police dans le panneau de configuration **polices** . Le contrôle de police affiche uniquement les polices qui sont définies pour s' **Afficher**.
    > [!Note]  
    > dans Windows Vista, le panneau de configuration des **polices** n’offre pas la fonctionnalité d' **affichage** ou de **masquage** , donc toutes les polices sont activées.

     

-   Gestion des polices qui est disponible directement à partir du contrôle.

    La capture d’écran suivante montre que le panneau de configuration des **polices** est accessible directement à partir du contrôle font.

    ![capture d’écran de la liste des familles de polices dans WordPad pour Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   Prise en charge de l’aperçu automatique.
-   Exposition des polices les plus pertinentes pour un utilisateur, telles que
    -   Listes de polices localisées pour les utilisateurs internationaux.
    -   Listes de polices basées sur le périphérique d’entrée.

    > [!Note]  
    > la prise en charge de cette fonctionnalité n’est pas disponible sur les plateformes antérieures à Windows 7.

     

## <a name="easy-integration-and-configuration"></a>Intégration et configuration faciles

En fournissant des fonctionnalités standard, réutilisables et faciles à utiliser, le contrôle de police du ruban facilite l’intégration de la prise en charge des polices dans une application.

Les détails de la sélection et de la mise en forme des polices sont encapsulés dans un élément logique autonome qui

-   Élimine la gestion complexe des interdépendances de contrôle typiques des implémentations de contrôle de police.
-   Requiert un gestionnaire de commandes unique pour toutes les fonctionnalités exposées par les sous-contrôles de contrôle de police.

Ce gestionnaire de commandes unique permet au contrôle de police de gérer les fonctionnalités de différents sous-contrôles en interne ; un sous-contrôle n’interagit jamais directement avec l’application, quelle que soit sa fonction.

Les autres fonctionnalités du contrôle de police incluent

-   La génération automatique, compatible DPI, d’une représentation de type WYSIWYG (ce que vous obtenez) de l’image bitmap pour chaque police du menu **famille de polices** .
-   intégration [de Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .
-   Bitmaps et info-bulles de la famille de polices localisées.
-   Énumération des polices, regroupement et métadonnées pour la gestion et la présentation des polices.
    > [!Note]  
    > la prise en charge de cette fonctionnalité n’est pas disponible sur les plateformes antérieures à Windows 7.

     

-   Sélecteurs de couleurs de la couleur de **texte** et de la couleur de **mise en surbrillance du texte** qui reflètent le comportement du sélecteur de couleurs de la [zone de liste déroulante](windowsribbon-controls-dropdowncolorpicker.md) du ruban.
-   Prise en charge de l’aperçu automatique par tous les sous-contrôles basés sur la Galerie de contrôles de police : **famille de polices**, **taille de police**, couleur de **texte** et **couleur de surbrillance du texte**.

## <a name="alignment-with-common-gdi-text-structures"></a>Alignement avec les structures de texte GDI courantes

les composants de la pile de texte [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) sont utilisés pour exposer les fonctionnalités de sélection et de mise en forme des polices par le biais du contrôle de police du ruban. Les différentes fonctionnalités de police prises en charge par la structure [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), la [structure CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)et la [structure CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) sont exposées par le biais des sous-contrôles inclus dans le contrôle font.

Les sous-contrôles affichés dans le contrôle font dépendent du modèle *FontType* déclaré dans le balisage du ruban. les modèles *FontType* (décrits plus en détail dans la section suivante) sont conçus pour s’aligner sur les structures de texte common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .

## <a name="add-a-fontcontrol"></a>Ajouter un FontControl

Cette section décrit les étapes de base pour ajouter un contrôle de police à une application de ruban.

### <a name="declaring-a-fontcontrol-in-markup"></a>Déclaration d’un FontControl dans le balisage

Comme les autres contrôles de ruban, le contrôle de police est déclaré dans le balisage avec un élément [**FontControl**](windowsribbon-element-fontcontrol.md) et associé à une déclaration de commande via un ID de commande. Lorsque l’application est compilée, l’ID de commande est utilisé pour lier la commande à un gestionnaire de commandes dans l’application hôte.

> [!Note]  
> Si aucun ID de commande n’est déclaré avec [**FontControl**](windowsribbon-element-fontcontrol.md) dans le balisage, alors l’un est généré par l’infrastructure.

 

Étant donné que les sous-contrôles du contrôle font ne sont pas exposés directement, la personnalisation du contrôle font est limitée à trois modèles de disposition *FontType* définis par l’infrastructure.

Une personnalisation plus poussée du contrôle de police peut être effectuée en combinant le modèle de disposition avec des attributs [**FontControl**](windowsribbon-element-fontcontrol.md) tels que *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* et *IsUnderlineButtonVisible*.

> [!Note]  
> Les fonctionnalités de police au-delà de celles exposées par les attributs et les modèles de contrôle de police standard nécessitent une implémentation de contrôle de police personnalisée qui n’est pas traitée dans cet article.

 

Le tableau suivant répertorie les modèles de contrôle de police et le type de contrôle d’édition avec lesquels chaque modèle est aligné.



| Modèle      | Prise en charge                                                                 |
|---------------|--------------------------------------------------------------------------|
| FontOnly      | [LOGFONT, structure](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| FontWithColor | [CHOOSEFONT, structure](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| RichFont      | [CHARFORMAT2, structure](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

Le tableau suivant répertorie les contrôles qui sont associés à chaque modèle et identifie les contrôles qui sont facultatifs pour un modèle associé.



Commandes

Modèles

**RichFont**

**FontWithColor**

**FontOnly**

Default

Facultatif

Default

Facultatif

Default

Facultatif

Zone de liste déroulante **taille de police**

Oui

Non

Oui

Non

Oui

Non

Zone de liste déroulante **famille de polices**

Oui

Non

Oui

Non

Oui

Non

Bouton **agrandir la police**

Oui

Oui

Oui

Oui

\-

\-

Bouton **réduire la police**

Oui

Oui

Oui

Oui

\-

\-

Bouton **gras**

Oui

Non

Oui

Non

Oui

Non

Bouton **italique**

Oui

Non

Oui

Non

Oui

Non

Bouton **souligné**

Oui

Non

Oui

Oui

Oui

Oui

Bouton **barré**

Oui

Non

Oui

Oui

Oui

Oui

Bouton d' **indice**

Oui

Non

\-

\-

\-

\-

Bouton **exposant**

Oui

Non

\-

\-

\-

\-

Bouton **couleur de surbrillance du texte**

Oui

Non

Oui

Oui

\-

\-

Bouton **couleur du texte**

Oui

Non

Oui

Non

\-

\-



 

Lorsque le comportement de disposition d’un contrôle de police est déclaré, l’infrastructure du ruban fournit un modèle de disposition *SizeDefinition* facultatif, `OneFontControl` , qui définit deux configurations de sous-contrôle en fonction de la taille du ruban et de l’espace disponible pour le contrôle de police. Pour plus d’informations, consultez [Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle](windowsribbon-templates.md).

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>Ajout d’un FontControl à un ruban

Les exemples de code suivants illustrent les exigences de balisage de base pour l’ajout d’un contrôle font à un ruban :

Cette section de code montre le balisage de déclaration de commande [**FontControl**](windowsribbon-element-fontcontrol.md) , y compris les commandes de [**tabulation**](windowsribbon-element-tab.md) et de [**groupe**](windowsribbon-element-group.md) requises pour afficher un contrôle dans le [**ruban**](windowsribbon-element-ribbon.md).


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



Cette section de code montre le balisage requis pour déclarer et associer un [**FontControl**](windowsribbon-element-fontcontrol.md) à une [**commande**](windowsribbon-element-command.md) via un ID de commande. Cet exemple particulier comprend les déclarations de [**tabulation**](windowsribbon-element-tab.md) et de [**groupe**](windowsribbon-element-group.md) , avec des préférences de mise à l’échelle.


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>Ajout d’un FontControl à un ContextPopup

L’ajout d’un contrôle de police à un menu contextuel de [contexte](windowsribbon-controls-contextpopup.md) requiert une procédure similaire à celle qui consiste à ajouter un contrôle de police au ruban. Toutefois, un contrôle de police dans un [**MiniToolbar**](windowsribbon-element-minitoolbar.md) est limité à l’ensemble de sous-contrôles par défaut qui sont communs à tous les modèles de contrôle de police : **famille de polices**, taille de **police**, **gras** et **italique**.

Les exemples de code suivants illustrent les exigences de balisage de base pour l’ajout d’un contrôle de police à une [fenêtre contextuelle](windowsribbon-controls-contextpopup.md):

Cette section de code montre le balisage de déclaration de commande [**FontControl**](windowsribbon-element-fontcontrol.md) nécessaire pour afficher un **FontControl** dans le [**ContextPopup**](windowsribbon-element-contextpopup.md).


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



Cette section de code montre le balisage requis pour déclarer et associer un [**FontControl**](windowsribbon-element-fontcontrol.md) à une commande via un ID de commande.


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a>Touches d’accès

Chaque sous-contrôle du contrôle de police du ruban est accessible par le biais d’un raccourci clavier ou d’une touche d’accès. Ce KeyTip est prédéfini et affecté à chaque sous-contrôle par l’infrastructure.

Si une valeur d’attribut *KeyTip* est assignée à l’élément [**FontControl**](windowsribbon-element-fontcontrol.md) dans le balisage, cette valeur est ajoutée en tant que préfixe à la touche d’appel définie par l’infrastructure.

> [!Note]  
> L’application doit appliquer une règle à un seul caractère pour ce préfixe.

 

Le tableau suivant répertorie les touches accélératrices définies par l’infrastructure. 


| Sous-contrôle | KeyTip | 
|-------------|--------|
| Famille de polices | F | 
| Style de police | T | 
| Taille de police | S | 
| Agrandir la police | G | 
| Réduire la police | K | 
| Gras | B | 
| Italique | I | 
| Souligner | U | 
| Barré | X | 
| Exposant | Y ou Z<blockquote>[!Note]<br />Si l’attribut <em>KeyTip</em> n’est pas déclaré dans le balisage, la touche d’option par défaut est Y ; dans le cas contraire, la touche d’option par défaut est <em>KeyTip</em> + Z.</blockquote><br /> | 
| Indice | Un | 
| Couleur de police | C | 
| Mise en surbrillance de police | H | 




 

le préfixe recommandé pour un ruban en-US interface utilisateur multilingue (MUI) est « F », comme le montre l’exemple suivant.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



La capture d’écran suivante illustre les info-bulles de contrôle de police telles qu’elles sont définies dans l’exemple précédent.

![capture d’écran des info-bulles fontcontrol dans WordPad pour Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>Fichier de ressources du ruban

Lorsque le fichier de balisage est compilé, un fichier de ressources qui contient toutes les références de ressources pour l’application ruban est généré.

Exemple de fichier de ressources simple :


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a>Propriétés du contrôle de police

L’infrastructure du ruban définit une collection de [clés de propriété](windowsribbon-reference-properties.md) pour le contrôle de police et ses sous-contrôles constitutifs.

En général, une propriété de contrôle de police est mise à jour dans l’interface utilisateur du ruban en invalidant la commande associée au contrôle via un appel à la méthode [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L’événement d’invalidation est géré, et les mises à jour de la propriété sont définies par la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

La méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) n’est pas exécutée et l’application a interrogé une valeur de propriété mise à jour, jusqu’à ce que la propriété soit requise par le Framework. Par exemple, lorsqu’un onglet est activé et qu’un contrôle est affiché dans l’interface ruban, ou lorsqu’une info-bulle est affichée.

> [!Note]  
> Dans certains cas, une propriété peut être récupérée par le biais de la méthode [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et définie avec la méthode [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Le tableau suivant répertorie les clés de propriété associées au contrôle font.



| Clé de propriété                                                                                                                  | Notes                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IU \_ \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | Expose, dans l’agrégat comme un objet [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) , toutes les propriétés de sous-contrôle de contrôle de police.<br/> L’infrastructure interroge cette propriété lorsque `UI_INVALIDATIONS_VALUE` est passé comme valeur des *indicateurs* dans l’appel à [**IUIFramework :: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).<br/> |
| [IU \_ \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | Expose, dans l’agrégat comme un objet [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , uniquement les propriétés de sous-contrôle de police qui ont changé.<br/>                                                                                                                                                                                                        |
| [KeyTip de l’interface utilisateur \_ \_](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | Peut uniquement être mis à jour par le biais d’une invalidation.                                                                                                                                                                                                                                                                                                                                                      |
| [IU-au-dessus \_ \_ activé](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | Prend en charge [**IUIFramework :: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) et [**IUIFramework :: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).                                                                                                                                                                  |



 

Outre les propriétés prises en charge par le contrôle de police lui-même, l’infrastructure du ruban définit également une [clé de propriété](windowsribbon-reference-properties.md) pour chaque sous-contrôle de contrôle de police. Ces clés de propriété et leurs valeurs sont exposées par l’infrastructure par le biais d’une implémentation d’interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) qui définit les méthodes de gestion d’une collection, également appelées « conteneurs de propriétés », de paires nom/valeur.

L’application convertit les structures de police en propriétés accessibles par le biais des méthodes de l’interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) . ce modèle met en évidence la distinction entre le contrôle de police et les composants de pile de texte Windows Graphics Device Interface (GDI) ([structure LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [structure CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)et [structure CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) qui sont pris en charge par l’infrastructure.

Le tableau suivant répertorie les contrôles individuels et leurs clés de propriété associées.



| Commandes                 | Clé de propriété                                                                                                                                                                                                                                                           | Notes                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Taille de la police**            | [\_Taille de \_ FontProperties de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Lorsqu’une exécution de texte de taille hétérogène est mise en surbrillance, l’infrastructure du ruban définit le contrôle de la **taille** de la police sur vide et la valeur de l' [interface utilisateur \_ \_ FontProperties \_ taille](windowsribbon-reference-properties-uipkey-fontproperties-size.md) sur 0. Lorsque l’utilisateur clique sur le bouton **agrandir la police** ou **réduire la police** , tout le texte mis en surbrillance est redimensionné, mais la différence relative dans les tailles de texte est conservée.                                                                                                                                                    |
| **Famille de polices**          | [\_Famille de \_ FontProperties de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | Les noms des familles de polices GDI varient selon les paramètres régionaux système. Par conséquent, si la valeur de [la \_ \_ \_ famille FontProperties de l’interface utilisateur](windowsribbon-reference-properties-uipkey-fontproperties-family.md) est conservée entre les sessions d’application, cette valeur doit être récupérée sur chaque nouvelle session.                                                                                                                                                                                                                                                                            |
| **Agrandir la police**            | [\_Taille de \_ FontProperties de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Consultez **taille de police**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Réduire la police**          | [\_Taille de \_ FontProperties de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Consultez **taille de police**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Gras**                 | [IU \_ \_ FontProperties \_ gras](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Italique**               | [IU \_ \_ FontProperties \_ italique](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Souligner**            | [IU \_ \_ FontProperties \_ souligné](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Barré**        | [IU \_ \_ FontProperties \_ barré](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Indice**            | [IU \_ \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Si le bouton d' **indice** est défini, l' **exposant** ne peut pas être défini.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Exposant**          | [IU \_ \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Si le bouton **exposant** est défini, l' **indice** ne peut pas être également défini.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Couleur de mise en surbrillance du texte** | [Interface utilisateur \_ \_FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [IU \_ \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | Fournit les mêmes fonctionnalités que le `HighlightColors` modèle de l’élément [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Nous vous recommandons vivement de définir uniquement une valeur de **couleur de mise en surbrillance du texte** initiale par l’application. La dernière valeur sélectionnée doit être conservée et non définie lorsque le curseur est repositionné dans un document. Cela permet d’accéder rapidement à la dernière sélection de l’utilisateur, et il n’est pas nécessaire de rouvrir le sélecteur de couleurs.<br/> Les échantillons de couleurs ne peuvent pas être personnalisés.<br/> |
| **Couleur du texte**           | [Interface utilisateur \_ \_FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [IU # \_ \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)           | Fournit les mêmes fonctionnalités que le `StandardColors` modèle de l’élément [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Nous vous recommandons vivement de définir uniquement une valeur de **couleur de texte** initiale par l’application. La dernière valeur sélectionnée doit être conservée et non définie lorsque le curseur est repositionné dans un document. Cela permet d’accéder rapidement à la dernière sélection de l’utilisateur, et il n’est pas nécessaire de rouvrir le sélecteur de couleurs.<br/> Les échantillons de couleurs ne peuvent pas être personnalisés.<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>Définir un gestionnaire de commandes FontControl

Cette section décrit les étapes nécessaires pour lier un contrôle de police à un gestionnaire de commandes.

> [!WARNING]
> Toute tentative de sélection d’un échantillon de couleur dans le sélecteur de couleurs d’un contrôle de police peut entraîner une violation d’accès si aucun gestionnaire de commandes n’est associé au contrôle.

 

L’exemple de code suivant montre comment lier des commandes qui sont déclarées dans le balisage à un gestionnaire de commandes.


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



L’exemple de code suivant montre comment implémenter la méthode [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) pour un contrôle font.


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



L’exemple de code suivant montre comment implémenter la méthode [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) pour un contrôle font.


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Windows Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)
</dt> <dt>

[**Élément FontControl**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Exemple FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

