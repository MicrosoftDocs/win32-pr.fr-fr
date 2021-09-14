---
title: Reconfiguration du ruban avec les modes d’application
description: l’infrastructure du ruban Windows prend en charge la reconfiguration et l’exposition dynamiques des éléments principaux de l’interface ruban au moment de l’exécution, en fonction de l’état de l’application (également appelé contexte).
ms.assetid: 8e9d85c5-33e4-4212-b9e4-2fc3b492c273
keywords:
- Windows Ruban, reconfiguration avec les modes d’application
- Ruban, reconfiguration avec les modes d’application
- reconfiguration d’Windows ruban avec les modes d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d206c238e6fe7463562077daaa52a5522a79d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196096"
---
# <a name="reconfiguring-the-ribbon-with-application-modes"></a>Reconfiguration du ruban avec les modes d’application

l’infrastructure du ruban Windows prend en charge la reconfiguration et l’exposition dynamiques des éléments principaux de l’interface ruban au moment de l’exécution, en fonction de l’état de l’application (également appelé contexte). Déclarés et associés à des éléments spécifiques dans le balisage, les différents États pris en charge par une application sont appelés modes d’application.

-   [Introduction](#introduction)
-   [Interface utilisateur contextuelle](#contextual-user-interface)
    -   [Scénario simple en mode application](#a-simple-application-mode-scenario)
-   [Implémentation des modes d’application](#implementing-application-modes)
    -   [Identifier les modes](#identify-the-modes)
    -   [Assigner des contrôles aux modes d’application](#assign-controls-to-application-modes)
    -   [Basculer les modes au moment de l’exécution](#switch-modes-at-runtime)
-   [Remarques](#remarks)
-   [Rubriques connexes](#related-topics)

## <a name="introduction"></a>Introduction

Les modes d’application se composent de groupes logiques de contrôles qui exposent certaines fonctionnalités d’application principales dans l’interface ruban. Ces modes sont activés ou désactivés dynamiquement par l’application via un appel à la méthode Framework [**IUIFramework :: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes), qui active ou désactive la visibilité d’un ou plusieurs modes d’application.

## <a name="contextual-user-interface"></a>Interface utilisateur contextuelle

L’infrastructure du ruban offre une expérience utilisateur riche en incorporant des contrôles dynamiques qui répondent en toute transparence à l’interaction de l’utilisateur et au contexte de l’application. Cette interface utilisateur contextuelle riche est fournie grâce à une combinaison des mécanismes suivants :

-   Galeries-contrôles basés sur des collections qui prennent en charge la manipulation dynamique de leurs collections d’éléments.
-   Onglets contextuels : onglets du ruban dont la visibilité est déterminée par une modification du contexte de l’espace de travail, telle que la sélection d’une image dans un document.
-   Modes d’application-fonctionnalités d’application principales qui dépendent du contexte de l’application.

À certains égards, les modes d’application s’affichent de façon fonctionnelle, à l’instar des onglets contextuels. Toutefois, la distinction fondamentale réside dans l’objectif et l’étendue de chaque.

Les contrôles contextuels sont activés en réponse à un changement de contexte dans une application. par exemple, dans Microsoft Paint pour Windows 7, un onglet contextuel qui contient des groupes de commandes liées au texte s’affiche lorsqu’un utilisateur insère une zone de texte dans l’espace de travail. Cet onglet contextuel ne contient pas de commandes de base pour l’application et n’est exposé dans l’interface utilisateur que si le contexte *de* l’application a changé. Les fonctionnalités principales de l’application (commandes de modification d’image) sont toujours pertinentes et disponibles pour l’utilisateur, même si l’onglet contextuel est visible.

Les modes d’application diffèrent des contrôles contextuels dans le fait qu’ils reconfigurent les fonctionnalités en réponse à des modifications dans le contexte dans lequel l’application fonctionne. Les modes d’application se trouvent à un niveau supérieur d’abstraction. ils offrent un moyen de reconfigurer la fonctionnalité de base d’une application au lieu d’exposer temporairement des fonctionnalités qui ne sont pas un composant fondamental de l’interface utilisateur. par exemple, dans Microsoft Paint pour Windows 7, un commutateur en mode application se produit lorsque la commande **aperçu avant impression** est appelée. lorsque Microsoft Paint passe en **mode aperçu avant impression**, le contexte dans lequel l’application est en cours de modification passe de la modification à l’aperçu. Par conséquent, la fonctionnalité de base de l’application change jusqu’à ce que l' **Aperçu avant impression** soit annulé et que l’application entre à nouveau dans le contexte d’édition.

### <a name="a-simple-application-mode-scenario"></a>Scénario simple en mode application

Le scénario suivant montre comment les modes d’application sont utilisés, dans une application appelée RibbonApp, pour exposer des aspects discrets de la fonctionnalité de base.

Deux modes d’application sont définis dans RibbonApp :

-   Le mode **simple** expose les commandes de base dans l’ensemble de l’interface ruban. Ces commandes s’affichent à tout moment, quel que soit le mode d’application actif.
-   Le mode **avancé** expose des commandes complexes destinées aux utilisateurs expérimentés de l’application. Ces commandes avancées s’affichent dans l’interface ruban, en plus des commandes simples.

Par défaut, RibbonApp est défini pour s’ouvrir en mode **simple** , et les commandes requises par les utilisateurs débutants sont affichées dans le menu de l' **application** et dans l’onglet dossier de **démarrage** . Les captures d’écran suivantes montrent le menu de l' **application** RibbonApp et l’onglet **Accueil** en mode **simple** , en mettant en surbrillance les contrôles modaux.

![capture d’écran montrant un onglet pour le mode d’application simple.](images/overviews/appmode-hometab.png)![capture d’écran montrant le menu de l’application pour le mode d’application simple.](images/overviews/appmode-simpleappmenu.png)

Bien que ces commandes soient suffisantes pour les utilisateurs débutants, RibbonApp prend également en charge les utilisateurs experts via un mode **avancé** qui, lorsqu’ils sont activés en cliquant sur le bouton **basculer en mode avancé** dans le **menu application**, affiche des fonctionnalités de base supplémentaires.

Ce scénario est facilement implémenté par la liaison de différents éléments dans le balisage à des modes d’application discrets qui peuvent être activés et désactivés selon les besoins. Les captures d’écran suivantes montrent le menu de l' **application** RibbonApp et l’onglet **Accueil** en mode **avancé** , en mettant en surbrillance les contrôles modaux.

![capture d’écran montrant un onglet pour le mode d’application avancé.](images/overviews/appmode-advancedtab.png)![capture d’écran montrant le menu de l’application pour le mode d’application avancé.](images/overviews/appmode-advancedappmenu.png)

## <a name="implementing-application-modes"></a>Implémentation des modes d’application

Cette section décrit les trois étapes généralement requises pour l’implémentation des modes d’application de l’infrastructure du ruban. RibbonApp est utilisé pour fournir un exemple pour chaque étape.

### <a name="identify-the-modes"></a>Identifier les modes

Chaque mode dans une application doit représenter un ensemble logique de fonctionnalités qui dépendent du contexte dans lequel une application peut fonctionner. Par exemple, si une application affiche des contrôles qui ne sont pertinents que lorsqu’une connexion réseau est détectée, ces contrôles opèrent dans un contexte réseau qui peut justifier la création d’un mode **réseau** .

RibbonApp a deux contextes qui peuvent être actifs à un moment donné : **simple** et **avancé**. Par conséquent, RibbonApp requiert deux modes : **simple** et **avancé**.

### <a name="assign-controls-to-application-modes"></a>Assigner des contrôles aux modes d’application

Une fois les modes d’application identifiés, assignez chaque contrôle de ruban à un mode en déclarant un attribut *ApplicationModes* dans le balisage pour les éléments de contrôle qui prennent en charge les modes d’application.

La vue du ruban permet de spécifier des modes sur les éléments de contrôle suivants :

-   Éléments de l' [**onglet**](windowsribbon-element-tab.md) principal.
-   [**Regroupez**](windowsribbon-element-group.md) les éléments enfants d’un élément d' [**onglet**](windowsribbon-element-tab.md) principal.
-   Éléments [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)et [**DropDownButton**](windowsribbon-element-dropdownbutton.md) affectés à un [**MenuGroup**](windowsribbon-element-menugroup.md) dans le menu de l' [application](windowsribbon-controls-applicationmenu.md).
    > [!Note]  
    > Les éléments [**Button**](windowsribbon-element-button.md), [**SplitButton**](windowsribbon-element-splitbutton.md)et [**DropDownButton**](windowsribbon-element-dropdownbutton.md) ne peuvent pas être assignés à un mode, sauf s’ils sont hébergés dans le menu de l' [application](windowsribbon-controls-applicationmenu.md).

     

Dans l’infrastructure du ruban, ces éléments de contrôle sont appelés contrôles modaux. Elles s’affichent uniquement si un mode auquel elles sont liées est actif dans l’interface utilisateur.

Les éléments de contrôle contenus dans un contrôle modal héritent du comportement du mode d’application. Par exemple, si un contrôle modal de [**groupe**](windowsribbon-element-group.md) est affecté à un mode **avancé** et que le mode **avancé** n’est pas actif, alors ce **groupe** et les contrôles qu’il contient, modaux ou non, ne sont pas visibles dans l’interface utilisateur du ruban.

Avec l’utilisation de l’attribut *ApplicationModes* , les modes sont assignés aux contrôles modaux dans une relation 1 : N (un-à-plusieurs), où un seul contrôle modal peut être associé à plusieurs modes.

L’infrastructure du ruban fait référence aux modes numériques, de 0 à 31, le mode 0 étant considéré comme le mode par défaut qui est activé automatiquement au démarrage d’une application de ruban. Tout contrôle modal qui ne spécifie pas d’attribut *ApplicationModes* est considéré comme un membre du mode par défaut.

Dans RibbonApp, **simple** est le mode par défaut, avec les fonctionnalités du mode **avancé** affichées uniquement lorsqu’il est lancé par l’utilisateur.

L’exemple suivant illustre le balisage requis pour RibbonApp.


```C++
<Application.Views>
  <Ribbon>

    <!--Application Menu-->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName='cmdAppMenu'>                    
        <MenuGroup>
          <Button CommandName='cmdSave'/>                        
          <Button CommandName='cmdExportMetadata' ApplicationModes='1'/>                   
        </MenuGroup>              
        <MenuGroup>
          <Button CommandName='cmdSwitchModes' ApplicationModes ='0,1'/>
          <Button CommandName='cmdExit'/>
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
            
    <!--Tabs-->
    <Ribbon.Tabs>
      <!--Home Tab-->
      <Tab CommandName='cmdHomeTab'>
                    
        <!--Scaling Policy for Home tab-->
        <Tab.ScalingPolicy>
          <ScalingPolicy>
            <ScalingPolicy.IdealSizes>
              <Scale Group='cmdSimpleControlsGroup' Size='Medium'/>                                
            </ScalingPolicy.IdealSizes>                     
          </ScalingPolicy>
        </Tab.ScalingPolicy>     
                    
        <!--Simple Controls Group-->
        <Group CommandName='cmdSimpleControlsGroup' SizeDefinition='ThreeButtons-OneBigAndTwoSmall'>                        
          <Button CommandName="cmdPaste" />
          <Button CommandName='cmdCut'/>                        
          <Button CommandName='cmdCopy'/>                        
        </Group>
      </Tab>
                
      <!--Advanced Tab-->
      <Tab CommandName='cmdAdvancedTab' ApplicationModes='1'>
        <!--Advanced Controls Group-->
        <Group CommandName='cmdMetadataGroup' ApplicationModes='1' SizeDefinition='TwoButtons'>
          <Button CommandName='cmdEditMetadata' />
          <Button CommandName='cmdCheckErrors' />
        </Group>
      </Tab>
    </Ribbon.Tabs>                   
                             
  </Ribbon>         
</Application.Views>
```



Cet exemple illustre les éléments suivants :

-   Le mode par défaut 0 n’a pas besoin d’être explicitement déclaré. Étant donné que les contrôles modaux qui ne spécifient pas l’attribut *ApplicationModes* sont automatiquement liés au mode 0 (mode **simple** dans l’exemple RibbonApp), il n’est pas nécessaire de déclarer explicitement l’attribut pour les contrôles modaux par défaut.
-   Les contrôles peuvent être liés à plusieurs modes. Pour RibbonApp, le seul besoin de l’attribut *ApplicationModes* dans un contrôle en mode **simple** est le `cmdSwitchModes` bouton, car il fait partie des modes **simple** et **avancé** . Si l’un des deux modes est actif, ce contrôle s’affiche dans le menu de l' [application](windowsribbon-controls-applicationmenu.md).
-   Les contrôles modaux n’héritent pas de leurs parents. L’onglet **avancé** de RibbonApp contient un groupe de **métadonnées** ; ces deux contrôles modaux sont assignés au mode 1 (mode **avancé** ). L’affectation de l’onglet **avancé** au mode 1 n’affecte pas automatiquement les contrôles enfants, tels que le groupe de **métadonnées** , au mode 1. Cela permet à n’importe quel groupe d’un onglet d’être activé ou désactivé indépendamment au moment de l’exécution.
-   Les contrôles non modaux peuvent toujours reposer sur des commutateurs de mode. Les boutons **modifier les métadonnées** et **vérifier les erreurs** de RibbonApp sont destinés aux utilisateurs avancés et sont disponibles uniquement lorsque l’utilisateur bascule en mode **avancé** . Les contrôles bouton qui ne sont pas hébergés dans le menu de l' [application](windowsribbon-controls-applicationmenu.md) ne sont pas modaux ; Toutefois, étant donné que ces boutons sont hébergés à l’intérieur d’un contrôle modal (le groupe de **métadonnées** ), ils sont visibles lorsque le groupe est visible. Par conséquent, ces boutons apparaissent lorsque le mode avancé est activé et que le groupe de **métadonnées** est exposé dans l’interface ruban.

### <a name="switch-modes-at-runtime"></a>Basculer les modes au moment de l’exécution

Une fois les modes définis dans le balisage, ils peuvent être facilement activés ou désactivés en réponse à des événements contextuels. Comme mentionné précédemment, les applications de ruban démarrent toujours en mode par défaut 0. Une fois que l’application a été initialisée et que le mode 0 est actif, l’ensemble de modes actifs peut être modifié en appelant la fonction [**IUIFramework :: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) . Cette fonction accepte un entier 32 bits comme représentation au niveau du bit des modes qui doivent être actifs ; le bit de poids faible représente le mode 0 et le bit le plus significatif représente le mode 31. Si un bit est défini sur zéro, le mode n’est pas actif dans l’interface ruban.

Dans RibbonApp, quand un utilisateur active le mode **avancé** , les commandes avancées s’affichent en même temps que les commandes simples. Le gestionnaire de commandes pour le bouton **basculer vers le mode avancé** appelle [**IUIFramework :: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) pour définir les modes 0 (**simple**) et 1 (**avancé**) comme étant actifs dans l’interface utilisateur. L’exemple suivant est le code RibbonApp pour cet appel de fonction :


```C++
const int SIMPLE_MODE = 0;
const int ADVANCED_MODE = 1;
pFramework->SetModes( UI_MAKEAPPMODE(SIMPLE_MODE) | UI_MAKEAPPMODE(ADVANCED_MODE) );
```



> [!Note]  
> La macro MAKEAPPMODE de l’interface utilisateur de l’infrastructure du ruban \_ simplifie la définition de ces bits correctement en préparation de l’appel à [**IUIFramework :: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes).

 

Cet exemple illustre les éléments suivants :

-   Utilisez la \_ macro MAKEAPPMODE de l’interface utilisateur pour générer un jeu de modes.
-   Les modes sont définis explicitement et atomiquement. La valeur entière transmise à [**IUIFramework :: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) représente les modes qui seront actifs après le retour de la fonction. Bien que le mode **simple** soit précédemment actif, **IUIFramework :: SetModes** doit indiquer que le mode **simple** reste actif lorsque le mode **avancé** est activé.
-   Le mode par défaut peut être supprimé. Même si, dans RibbonApp, le mode par défaut (mode 0) n’est jamais supprimé, il peut être supprimé à l’aide de l’appel suivant : `g_pFramework->SetModes(UI_MAKEAPPMODE(ADVANCED_MODE))` , en exposant uniquement les commandes avancées dans l’interface utilisateur.

> [!Note]  
> Lorsque les modes d’une application sont reconfigurés, le ruban tente de conserver l’onglet précédemment sélectionné dans l’interface utilisateur. Si le nouvel ensemble de modes ne contient plus l’onglet sélectionné avant l’appel, le ruban sélectionne l’onglet dans sa disposition qui est le plus proche du menu de l' [application](windowsribbon-controls-applicationmenu.md). Cet onglet est destiné à contenir les commandes les plus pertinentes pour l’utilisateur. Pour plus d’informations, consultez [instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx).

 

## <a name="remarks"></a>Notes

Le ruban doit avoir au moins un mode actif à tout moment. Si une application tente de désactiver tous les modes en appelant [**IUIFramework :: SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes) avec une valeur de mode de 0, E \_ Fail est retourné et le mode actif reste inchangé.

L’infrastructure requiert à tout moment qu’au moins un onglet existe dans l’interface ruban. Par conséquent, il doit y avoir au moins un onglet exposé par le mode par défaut (mode 0) et après chaque commutateur de mode.

Toutes les zones de l’interface utilisateur du ruban ne sont pas affectées par les modes d’application. Par exemple, si la désactivation d’un mode provoque la disparition des boutons du ruban qui ont été précédemment ajoutés à la [barre d’outils accès rapide](windowsribbon-controls-quickaccesstoolbar.md), ces boutons restent dans la barre d’outils accès rapide, ce qui permet aux utilisateurs d’exécuter les commandes liées aux boutons. En règle générale, si une commande appartient à un ou plusieurs modes inactifs, elle doit également être désactivée en affectant à la propriété de l' [interface utilisateur \_ \_ activée](windowsribbon-reference-properties-uipkey-enabled.md) la valeur 0 (variante \_ false).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Affichage des onglets contextuels](ribbon-contextualtabs.md)
</dt> </dl>

 

 