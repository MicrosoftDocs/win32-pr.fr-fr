---
title: Vue d'ensemble d'UI Automation
description: Microsoft UI Automation est une infrastructure d’accessibilité pour Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- UI Automation, à propos de
- UI Automation, accessibilité
- UI Automation, composants
- UI Automation, API du fournisseur
- UI Automation, API client
- UI Automation, fichiers d’en-tête
- UI Automation, modèle
- components
- accessibilité
- API du fournisseur
- API client
- fichiers d'en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3664866280d570f9fa5f07acc6245ca2b4c1bff7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292467"
---
# <a name="ui-automation-overview"></a>Vue d'ensemble d'UI Automation

Microsoft UI Automation est une infrastructure d’accessibilité pour Windows. Il fournit un accès par programme à la plupart des éléments d’interface utilisateur sur le bureau. Il permet aux produits de technologie d’assistance, tels que les lecteurs d’écran, de fournir des informations sur l’interface utilisateur aux utilisateurs finaux et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard. UI Automation permet également aux scripts de test automatisés d’interagir avec l’interface utilisateur.

UI Automation était d’abord disponible dans Windows XP dans le cadre de la .NET Framework Microsoft. Bien qu’une API C++ non managée ait également été publiée à ce moment-là, l’utilité des fonctions clientes était limitée en raison de problèmes d’interopérabilité. pour Windows 7, l’API a été réécrite dans le modèle COM (component Object Model).

> [!Note]  
> Bien que les fonctions de bibliothèque introduites dans la version antérieure d’UI Automation soient toujours documentées, elles ne doivent pas être utilisées dans les nouvelles applications.

 

les applications clientes UI Automation peuvent être écrites avec l’assurance qu’elles fonctionneront sur plusieurs infrastructures de contrôle Microsoft Windows. Le noyau UI Automation masque les différences dans les infrastructures qui sous-tendent les différents éléments de l’interface utilisateur. par exemple, la propriété de **contenu** d’un bouton Windows Presentation Foundation (WPF), la propriété **Caption** d’un bouton Microsoft Win32 et la propriété **ALT** d’une image HTML sont toutes mappées à une seule propriété, **Name**, dans la vue UI Automation.

UI Automation offre des fonctionnalités complètes dans Windows XP, Windows Server 2003 et les systèmes d’exploitation ultérieurs.

Les fournisseurs UI Automation sont des composants qui implémentent la prise en charge d’UI Automation sur les contrôles et offrent une certaine prise en charge pour les applications clientes Microsoft Active Accessibility, par le biais d’un service de pontage intégré.

> [!Note]  
> UI Automation n’active pas la communication entre les processus démarrés par différents utilisateurs via la commande **exécuter en tant que** .

 

Cette rubrique contient les sections suivantes.

-   [Composants UI Automation](#ui-automation-components)
-   [Fichiers d’en-tête UI Automation](#ui-automation-header-files)
-   [Modèle UI Automation](#ui-automation-model)
-   [Rubriques connexes](#related-topics)

## <a name="ui-automation-components"></a>Composants UI Automation

UI Automation comporte quatre composants principaux, comme indiqué dans le tableau suivant.




| Composant | Description | 
|-----------|-------------|
| API du fournisseur | Ensemble d’interfaces COM qui sont implémentées par les fournisseurs UI Automation. Les fournisseurs UI Automation sont des objets qui fournissent des informations sur les éléments d’interface utilisateur et répondent aux entrées par programmation. | 
| API client | Ensemble d’interfaces COM qui permettent aux applications clientes d’obtenir des informations sur l’interface utilisateur et d’envoyer des entrées à des contrôles.<blockquote>[!Note]<br />Les fonctions décrites dans <a href="uiauto-entry-cpfunctions.md">fonctions de modèle de contrôle déconseillées</a> et <a href="uiauto-entry-uianodefunctions.md">fonctions de nœud déconseillées</a> sont déconseillées. Au lieu de cela, les applications clientes doivent utiliser les interfaces COM UI Automation décrites dans <a href="uiauto-entry-uiautoclientinterfaces.md">interfaces d’élément UI Automation pour les clients</a>.</blockquote><br /> | 
| UIAutomationCore.dll | La bibliothèque Runtime, parfois appelée noyau UI Automation, gère la communication entre les fournisseurs et les clients. | 
| Oleacc.dll | La bibliothèque Runtime pour Microsoft Active Accessibility et les objets proxy. La bibliothèque fournit également des objets proxy utilisés par Microsoft Microsoft Active Accessibility au proxy UI Automation pour prendre en charge les contrôles Win32. | 




 

Il existe deux façons d’utiliser UI Automation : pour créer la prise en charge des contrôles personnalisés à l’aide de l’API du fournisseur et pour créer des applications clientes qui utilisent le noyau UI Automation pour communiquer et récupérer des informations sur les éléments d’interface utilisateur. Selon votre objectif, reportez-vous à différentes parties de cette documentation. Si vous devez créer la prise en charge des contrôles personnalisés, consultez le [Guide du programmeur de fournisseur UI Automation](uiauto-providerportal.md). Si vous avez besoin de communiquer avec ou de récupérer des informations sur les éléments d’interface utilisateur, consultez le [Guide du programmeur du client UI Automation](uiauto-clientportal.md).

## <a name="ui-automation-header-files"></a>Fichiers d’en-tête UI Automation

l’API UI Automation est définie dans plusieurs fichiers d’en-tête C/C++ qui sont inclus avec le kit de développement logiciel (SDK) Windows. Les fichiers d’en-tête UI Automation sont décrits dans le tableau suivant :



| Fichier d’en-tête           | Description                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient. h  | Définit les interfaces et les éléments de programmation associés utilisés par les clients UI Automation.                                                                                                                                                                                           |
| UIAutomationCore. h    | Définit les interfaces et les éléments de programmation associés utilisés par les fournisseurs UI Automation.                                                                                                                                                                                         |
| UIAutomationCoreApi. h | Définit des constantes générales, des GUID, des types de données et des structures utilisés par des fournisseurs et des clients UI Automation. Elle contient également des définitions pour le nœud déconseillé et les fonctions de modèle de contrôle.                                                                                    |
| UIAutomation. h        | Comprend tous les autres fichiers d’en-tête UI Automation. Étant donné que la plupart des applications UI Automation requièrent des éléments de tous les fichiers d’en-tête UI Automation, il est préférable d’inclure UIAutomation. h dans vos projets d’application UI Automation au lieu d’inclure chaque fichier individuellement. |



 

Si vous développez une application qui utilise l’API UI Automation, vous devez inclure UIAutomation. h dans votre projet. Si votre application prend en charge Microsoft Active Accessibility, incluez le fichier d’en-tête oleacc. h. Les applications UI Automation qui utilisent des GUID requièrent également le fichier d’en-tête Initguid. h. Si nécessaire, Initguid. h doit être inclus avant UIAutomation. h.

## <a name="ui-automation-model"></a>Modèle UI Automation

UI Automation expose chaque élément de l’interface utilisateur aux applications clientes sous la forme d’un objet représenté par l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Les éléments sont contenus dans une arborescence, avec le bureau comme élément racine. Les clients peuvent filtrer l’affichage brut de l’arborescence sous la forme d’une vue de contrôle ou d’une vue de contenu. ces vues standard de la structure peuvent être consultées facilement à l’aide de l’application [Inspect](inspect-objects.md) qui est incluse dans le SDK Windows. Les applications peuvent également créer des vues personnalisées.

Un élément UI Automation expose les propriétés du contrôle ou de l’élément d’interface qu’il représente. L’une de ces propriétés est le type de contrôle, qui définit l’apparence et les fonctionnalités de base du contrôle ou de l’élément d’interface utilisateur sous la forme d’une entité reconnaissable unique, par exemple, un bouton ou une case à cocher. Pour plus d’informations sur les types de contrôle, consultez [UI Automation Control types Overview](uiauto-controltypesoverview.md).

En outre, un élément UI Automation expose un ou plusieurs modèles de contrôle. Un modèle de contrôle fournit un ensemble de propriétés spécifiques à un type de contrôle particulier. Un modèle de contrôle expose également des méthodes qui permettent aux applications clientes d’obtenir plus d’informations sur l’élément et de fournir une entrée à l’élément. Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Il n’existe pas de correspondance un-à-un entre les types de contrôle et les modèles de contrôle. Un modèle de contrôle peut être pris en charge par plusieurs types de contrôle, et un contrôle peut prendre en charge plusieurs modèles de contrôle, dont chacun expose différents aspects de son comportement. Par exemple, une zone de liste déroulante possède au moins deux modèles de contrôle : un qui représente sa capacité de développement et de réduction, et l’autre qui représente le mécanisme de sélection. Toutefois, un contrôle ne peut présenter qu’un seul type de contrôle.

 

UI Automation fournit des informations aux applications clientes via des événements. Contrairement à WinEvents, les événements UI Automation ne sont pas basés sur un mécanisme de diffusion. Les clients UI Automation s’inscrivent pour des notifications d’événements spécifiques et peuvent demander que des propriétés spécifiques et des informations de modèle de contrôle soient passées à leurs gestionnaires d’événements. En outre, un événement UI Automation contient une référence à l’élément qui l’a déclenché. Les fournisseurs peuvent améliorer les performances en déclenchant des événements de manière sélective, selon que des clients les écoutent ou non. Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Vue d'ensemble des types de contrôle UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d'ensemble des événements UI Automation](uiauto-eventsoverview.md)
</dt> </dl>

 

 





