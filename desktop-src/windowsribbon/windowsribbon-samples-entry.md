---
title: Windows Exemples d’infrastructure de ruban
description: les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la Windows documentation de l’infrastructure du ruban.
ms.assetid: 79d092c9-347b-4b8f-8ba4-a8f696ce6a85
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 44fa4ae8a10956bdea34b0145b1af34156ff0db0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691638"
---
# <a name="windows-ribbon-framework-samples"></a>Windows Exemples d’infrastructure de ruban

les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la Windows documentation de l’infrastructure du ruban.

## <a name="download-information"></a>Informations sur le téléchargement

les exemples d’infrastructure du ruban Windows peuvent être téléchargés en tant que projets Microsoft Visual Studio autonomes à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou installés dans le cadre du [kit de développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).

## <a name="samples"></a>Exemples

| Exemple                                                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Exemple SimpleRibbon](windowsribbon-sample1.md)<br/>                          | cet exemple de code montre comment implémenter une application Windows ruban simple.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Exemple ContextPopup](windowsribbon-contextpopupsample.md)<br/>               | cet exemple de code illustre le balisage et le code requis pour implémenter une application Windows Ribbon avec ContextPopups. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [Exemple DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)<br/> | cet exemple de code illustre le balisage et le code requis pour utiliser un Windows contrôle DropDownColorPicker du ruban. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Exemple de Galerie](windowsribbon-gallerysample.md)<br/>                         | Cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de Galerie inclus dans l’infrastructure du ruban. L’exemple comprend du code qui peut être utilisé pour remplir dynamiquement des éléments dans les galeries et gérer des événements de prévisualisation de Galerie spéciaux qui prennent en charge l’interface utilisateur orientée résultats. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Exemple HTMLEditRibbon](windowsribbon-htmleditribbonsample.md)<br/>           | cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows. il a été créé en acceptant l’exemple d’application MFC HTMLEdit existante et en modifiant son code et ses ressources afin d’utiliser le ruban Windows. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Exemple FontControl](windowsribbon-fontcontrolsample.md)<br/>                 | cet exemple de code illustre le balisage et le code requis pour implémenter un FontControl dans une application de ruban Windows. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
## <a name="support"></a>Assistance

le [Forum de développement Windows ruban](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.

## <a name="minimum-requirements"></a>Configuration minimale requise



| Condition requise | Valeur |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge               | Windows 7<br/> Windows vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Serveur minimal pris en charge               | Windows Server 2008 R2<br/> Windows serveur 2008 avec SP2 et [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de développement logiciel Windows | 7.0                                                                                                                                                                      |
| Fichiers d’en-tête et IDL                   | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) est un ensemble de bibliothèques runtime qui permettent aux développeurs de cibler Windows applications du ruban à la fois Windows Vista et Windows Server 2008. les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update. les applications tierces qui requièrent la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

 

 

 





