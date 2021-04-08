---
title: Exemples de l’infrastructure de ruban Windows
description: Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation de l’infrastructure du ruban Windows.
ms.assetid: 79d092c9-347b-4b8f-8ba4-a8f696ce6a85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cdb69bf7da6dde6676969e7da2f1fb3a96d3736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741700"
---
# <a name="windows-ribbon-framework-samples"></a>Exemples de l’infrastructure de ruban Windows

Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation de l’infrastructure du ruban Windows.

## <a name="download-information"></a>Informations sur le téléchargement

Les exemples de l’infrastructure du ruban Windows peuvent être téléchargés en tant que projets autonomes Microsoft Visual Studio à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou installés dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx).

## <a name="samples"></a>Exemples



| Exemple                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Exemple SimpleRibbon](windowsribbon-sample1.md)<br/>                          | Cet exemple de code montre comment implémenter une application de ruban Windows simple.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Exemple ContextPopup](windowsribbon-contextpopupsample.md)<br/>               | Cet exemple de code illustre le balisage et le code requis pour implémenter une application de ruban Windows avec ContextPopups. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Exemple DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)<br/> | Cet exemple de code illustre le balisage et le code requis pour utiliser un contrôle DropDownColorPicker du ruban Windows. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Exemple de Galerie](windowsribbon-gallerysample.md)<br/>                         | Cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de Galerie inclus dans l’infrastructure du ruban. L’exemple comprend du code qui peut être utilisé pour remplir dynamiquement des éléments dans les galeries et gérer des événements de prévisualisation de Galerie spéciaux qui prennent en charge l’interface utilisateur orientée résultats. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Exemple HTMLEditRibbon](windowsribbon-htmleditribbonsample.md)<br/>           | Cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows. Il a été créé en acceptant l’exemple d’application MFC HTMLEdit existante et en modifiant son code et ses ressources pour utiliser le ruban Windows. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Exemple FontControl](windowsribbon-fontcontrolsample.md)<br/>                 | Cet exemple de code illustre le balisage et le code requis pour implémenter un FontControl dans une application de ruban Windows. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
## <a name="support"></a>Support

Le [Forum de développement du ruban Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.

## <a name="minimum-requirements"></a>Configuration minimale requise



| Condition requise | Valeur |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge               | Windows 7<br/> Windows Vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Serveur minimal pris en charge               | Windows Server 2008 R2<br/> Windows Server 2008 avec SP2 et la [mise à jour de la plateforme pour Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de développement logiciel Windows | 7.0                                                                                                                                                                      |
| Fichiers d’en-tête et IDL                   | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> La [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sont des ensembles de bibliothèques Runtime qui permettent aux développeurs de cibler des applications de ruban Windows vers Windows Vista et Windows Server 2008. Les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update. Les applications tierces qui requièrent une [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou une [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

 

 

 





