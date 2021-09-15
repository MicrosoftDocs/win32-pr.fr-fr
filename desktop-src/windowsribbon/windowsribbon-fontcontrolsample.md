---
title: Exemple FontControl
description: cet exemple de code illustre le balisage et le code requis pour implémenter un FontControl dans une application de ruban Windows.
ms.assetid: 8fb84bd1-5e63-447c-b7a0-b3d7cb8c3be7
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 52a81a1a1950305437a7bbc68aab95876b3a6374
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411161"
---
# <a name="fontcontrol-sample"></a>Exemple FontControl

cet exemple de code illustre le balisage et le code requis pour implémenter un FontControl dans une application de ruban Windows.

- [Utilisation](#usage)
  - [Génération de l'exemple](#building-the-sample)
  - [Exécution de l’exemple](#running-the-sample)
- [Support](#support)
- [Configuration minimale requise](#minimum-requirements)
- [Rubriques connexes](#related-topics)

## <a name="usage"></a>Utilisation

les exemples d’infrastructure du ruban Windows peuvent être téléchargés en tant que projets Microsoft Visual Studio autonomes à partir du [centre de téléchargement Microsoft](https://www.microsoft.com/download/details.aspx?id=9620) ou installés dans le cadre du [kit de développement logiciel (SDK) Windows](https://developer.microsoft.com/windows/downloads/sdk-archive/).

- Windows kit de développement logiciel (sdk) (chemin d’installation standard) :% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ numéro de version \] \\ exemples \\ winui \\ WindowsRibbon \\ FontControl

### <a name="building-the-sample"></a>Génération de l'exemple

Téléchargez l’exemple.

installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération. Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.

Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple. À l'invite de commandes, tapez MSBUILD.

Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.

### <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers .exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.

Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.

## <a name="support"></a>Support

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

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> </dl>

 

 





