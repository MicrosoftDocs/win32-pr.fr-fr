---
title: Exemple de Galerie
description: cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de galerie inclus dans l’infrastructure de ruban Windows.
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: ef776a8a1a8eadf9ee41cf9964066cc612a9f9a1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691748"
---
# <a name="gallery-sample"></a>Exemple de Galerie

cet exemple de code illustre le balisage et le code requis pour utiliser les différents types de contrôles de galerie inclus dans l’infrastructure de ruban Windows. L’exemple comprend du code qui peut être utilisé pour remplir dynamiquement des éléments dans les galeries et gérer des événements de prévisualisation de Galerie spéciaux qui prennent en charge l’interface utilisateur orientée résultats.

- [Utilisation](#usage)
  - [Génération de l'exemple](#building-the-sample)
  - [Exécution de l’exemple](#running-the-sample)
- [Support technique](#support)
- [Configuration minimale requise](#minimum-requirements)
- [Rubriques connexes](#related-topics)

## <a name="usage"></a>Usage

les exemples d’infrastructure du ruban Windows peuvent être téléchargés en tant que projets Microsoft Visual Studio autonomes à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou installés dans le cadre du [kit de développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).

- Windows kit de développement logiciel (sdk) (chemin d’installation standard) :% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ numéro de version \] \\ exemples \\ winui \\ WindowsRibbon \\ Gallery

### <a name="building-the-sample"></a>Génération de l'exemple

Téléchargez l’exemple.

installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération. Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.

Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple. À l'invite de commandes, tapez MSBUILD.

Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.

### <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers .exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.

Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.

## <a name="support"></a>Assistance

le [Forum de développement Windows ruban](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.

## <a name="minimum-requirements"></a>Configuration minimale requise



| Condition requise | Valeur |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 7<br/> Windows vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Serveur minimal pris en charge | Windows Server 2008 R2<br/> Windows serveur 2008 avec SP2 et [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de développement logiciel (SDK) Windows              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Fichiers d’en-tête et IDL     | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) est un ensemble de bibliothèques runtime qui permettent aux développeurs de cibler Windows applications du ruban à la fois Windows Vista et Windows Server 2008. les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 par le biais de Windows Update. les applications tierces qui requièrent la [mise à jour de la plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des galeries](ribbon-controls-galleries.md)
</dt> <dt>

[Zone de liste déroulante](windowsribbon-controls-combobox.md)
</dt> <dt>

[Galerie déroulante](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[Galerie dans le ruban](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Propriétés de la collection](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





