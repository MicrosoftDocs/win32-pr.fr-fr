---
title: Infrastructure de ruban Windows
description: L’infrastructure de ruban Windows est un système de présentation de commande riche qui offre une alternative moderne aux menus en couches, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Ruban Windows
- Ruban
- Documentation sur le ruban Windows
- Documentation ruban
- API de ruban Windows
- API du ruban
- Ruban Windows, infrastructure
- Ruban, infrastructure
- Ruban Windows, à propos de
- Ruban, à propos de
- Ruban Windows, composants
- Ruban, composants
- Ruban Windows, vues
- Ruban, vues
- Ruban Windows, architecture
- Ruban, architecture
- Ruban Windows, API
- Ruban, API
- Ruban Windows, sécurité
- Ruban, sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6906401573cb244ddc4386faf8c283d7938a0ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941975"
---
# <a name="windows-ribbon-framework"></a>Infrastructure de ruban Windows

L’infrastructure de ruban Windows est un système de présentation de commande riche qui offre une alternative moderne aux menus en couches, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles. Comme dans les fonctionnalités et l’apparence de l’interface utilisateur Fluent Microsoft Office 2007, l’infrastructure du ruban est composée d’une barre de commandes du ruban qui expose les principales fonctionnalités d’une application via une série d’onglets en haut d’une fenêtre d’application, et un système de menu contextuel.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                           | Description                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vues d’ensemble de Framework de ruban](windowsribbon-overviews-entry.md)<br/>      | Les rubriques contenues dans cette section explorent les notions de base de l’infrastructure du ruban. <br/>                                                                                                                   |
| [Guides du développeur de Framework de ruban](windowsribbon-guides-entry.md)<br/>  | Les rubriques contenues dans cette section décrivent des aspects spécifiques de l’infrastructure du ruban Windows. <br/>                                                                                                          |
| [Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)<br/> | Les rubriques contenues dans cette section décrivent l’ensemble des contrôles inclus avec l’infrastructure du ruban. Les contrôles répertoriés ici sont les objets d’interface utilisateur d’un ruban qui exposent les fonctionnalités de commande.<br/> |
| [Informations de référence sur l’infrastructure du ruban](windowsribbon-reference-entry.md)<br/>      | Les rubriques contenues dans cette section fournissent les spécifications de référence pour l’infrastructure du ruban.<br/>                                                                                                       |
| [Exemples d’infrastructure de ruban](windowsribbon-samples-entry.md)<br/>          | Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation de l’infrastructure du ruban Windows. <br/>                                                                     |
| [Glossaire du Framework du ruban](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Public de développeurs

L’infrastructure de ruban Windows est conçue pour être utilisée par les développeurs C/C++ et les concepteurs d’interface utilisateur.

Compétences recommandées :

-   Programmation COM
-   Programmation d’API Windows
-   Programmation XML/XAML

Connaissances de base recommandées :

-   Concepts de programmation de l’interface utilisateur
-   Concepts généraux de l’interface utilisateur

## <a name="minimum-requirements"></a>Configuration minimale requise



| Condition requise | Valeur |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge               | Windows 7<br/> Windows Vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Serveur minimal pris en charge               | Windows Server 2008 R2<br/> Windows Server 2008 avec SP2 et la [mise à jour de la plateforme pour Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de développement logiciel Windows | 7.0                                                                                                                                                                      |
| Fichiers d’en-tête et IDL                   | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> La [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sont des ensembles de bibliothèques Runtime qui permettent aux développeurs de cibler des applications de ruban Windows vers Windows Vista et Windows Server 2008. Les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update. Les applications tierces qui requièrent une [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou une [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

 

## <a name="see-also"></a>Voir aussi

[COM (Component Object Model)](../com/component-object-model--com--portal.md)


[API Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

