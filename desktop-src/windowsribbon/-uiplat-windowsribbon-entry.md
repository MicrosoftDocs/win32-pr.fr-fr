---
title: Windows Infrastructure du ruban
description: lisez une présentation de l’infrastructure du ruban Windows, qui est une alternative moderne aux menus en couches, aux barres d’outils et aux volets des tâches des applications Windows traditionnelles.
ms.assetid: c6108c38-17ef-4d8a-ab32-171bc496d44c
keywords:
- Windows Dernier
- Ruban
- Windows Documentation ruban
- Documentation ruban
- Windows API du ruban
- API du ruban
- Windows Ruban, infrastructure
- Ruban, infrastructure
- Windows Ruban, à propos de
- Ruban, à propos de
- Windows Ruban, composants
- Ruban, composants
- Windows Ruban, vues
- Ruban, vues
- Windows Ruban, architecture
- Ruban, architecture
- Windows Ruban, API
- Ruban, API
- Windows Ruban, sécurité
- Ruban, sécurité
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 98f7dbf42d604f93c76bb9897aa25918d45d126f
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691648"
---
# <a name="windows-ribbon-framework"></a>Windows Infrastructure du ruban

l’infrastructure du ruban Windows est un système de présentation de commande riche qui offre une alternative moderne aux menus en couches, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles. comme dans les fonctionnalités et l’apparence de l’interface utilisateur Microsoft Office 2007 Fluent, l’infrastructure du ruban est composée d’une barre de commandes de ruban qui expose les principales fonctionnalités d’une application via une série d’onglets en haut d’une fenêtre d’application, et un système de menu contextuel.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                           | Description                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vues d’ensemble de Framework de ruban](windowsribbon-overviews-entry.md)<br/>      | Les rubriques contenues dans cette section explorent les notions de base de l’infrastructure du ruban. <br/>                                                                                                                   |
| [Guides du développeur de Framework de ruban](windowsribbon-guides-entry.md)<br/>  | les rubriques contenues dans cette section décrivent des aspects spécifiques de l’infrastructure du ruban Windows. <br/>                                                                                                          |
| [Bibliothèque de contrôles de Framework du ruban](windowsribbon-controls-entry.md)<br/> | Les rubriques contenues dans cette section décrivent l’ensemble des contrôles inclus avec l’infrastructure du ruban. Les contrôles répertoriés ici sont les objets d’interface utilisateur d’un ruban qui exposent les fonctionnalités de commande.<br/> |
| [Informations de référence sur l’infrastructure du ruban](windowsribbon-reference-entry.md)<br/>      | Les rubriques contenues dans cette section fournissent les spécifications de référence pour l’infrastructure du ruban.<br/>                                                                                                       |
| [Exemples d’infrastructure de ruban](windowsribbon-samples-entry.md)<br/>          | les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la Windows documentation de l’infrastructure du ruban. <br/>                                                                     |
| [Glossaire du Framework du ruban](windowsribbon-glossary.md)<br/>              |                                                                                                                                                                                                                      |



 

## <a name="developer-audience"></a>Public de développeurs

l’infrastructure du ruban Windows est conçue pour être utilisée par les développeurs C/C++ et les concepteurs d’interface utilisateur.

Compétences recommandées :

- Programmation COM
- Windows Programmation d’API
- Programmation XML/XAML

Connaissances de base recommandées :

- Concepts de programmation de l’interface utilisateur
- Concepts généraux de l’interface utilisateur

## <a name="minimum-requirements"></a>Configuration minimale requise



| Condition requise | Valeur |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge               | Windows 7<br/> Windows vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Serveur minimal pris en charge               | Windows Server 2008 R2<br/> Windows serveur 2008 avec SP2 et [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de développement logiciel Windows | 7.0                                                                                                                                                                      |
| Fichiers d’en-tête et IDL                   | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) est un ensemble de bibliothèques runtime qui permettent aux développeurs de cibler Windows applications du ruban à la fois Windows Vista et Windows Server 2008. les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update. les applications tierces qui requièrent la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

 

## <a name="see-also"></a>Voir aussi

[COM (Component Object Model)](../com/component-object-model--com--portal.md)


[API Windows](/previous-versions//cc433218(v=vs.85))


[XAML](/dotnet/framework/wpf/advanced/xaml-in-wpf)


 

