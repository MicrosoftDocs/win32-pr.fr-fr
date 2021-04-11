---
title: Exemple HTMLEditRibbon
description: Cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows.
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032573"
---
# <a name="htmleditribbon-sample"></a>Exemple HTMLEditRibbon

Cet exemple de code montre le balisage et le code requis pour migrer une application Microsoft Foundation Classes (MFC) existante afin d’utiliser le ruban Windows. Il a été créé en acceptant l’exemple d’application MFC HTMLEdit existante et en modifiant son code et ses ressources pour utiliser le ruban Windows.

-   [Remarques](#remarks)
-   [Utilisation](#usage)
    -   [Génération de l'exemple](#building-the-sample)
    -   [Exécution de l’exemple](#running-the-sample)
-   [Support](#support)
-   [Configuration minimale requise](#minimum-requirements)

## <a name="remarks"></a>Notes

Pour l’exemple MFC, consultez [HtmlEdit, exemple : encapsule le contrôle d’édition MSHTML d’Internet Explorer](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx).

## <a name="usage"></a>Utilisation

L’exemple HTMLEditRibbon peut être téléchargé en tant que projet Microsoft Visual Studio autonome à partir du [Centre de téléchargement Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) ou installé dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx).

-   Centre de téléchargement Microsoft : [exemples de ruban Windows](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)
-   Kit de développement logiciel (SDK) Windows (chemin d’installation standard) :% ProgramFiles% \\ Microsoft SDK \\ Windows \\ \[ numéro de version \] \\ exemples \\ WinUI \\ WindowsRibbon \\ HTMLEditRibbon

### <a name="building-the-sample"></a>Génération de l'exemple

Téléchargez l’exemple sur votre disque dur.

Installez les SDK Windows pour Windows 7 et ouvrez la fenêtre de commande de l’environnement de génération. Dans le menu Démarrer, pointez sur Tous les programmes et sur Microsoft Windows SDK, puis cliquez sur CMD Shell.

Pour générer l'exemple à partir de la fenêtre Commande de l'environnement de génération, accédez au répertoire source de l'exemple. À l'invite de commandes, tapez MSBUILD.

Pour générer l'exemple dans Microsoft Visual Studio, chargez l'exemple de solution ou de fichier projet, puis appuyez sur CTRL+MAJ+B.

### <a name="running-the-sample"></a>Exécution de l'exemple

Pour exécuter l’exemple à partir de la fenêtre de commande de l’environnement de génération, exécutez les fichiers. exe dans le \\ dossier bin debug ou bin \\ Release contenu dans le dossier source de l’exemple.

Pour exécuter l'exemple compilé avec le débogage dans Visual Studio, appuyez sur F5.

## <a name="support"></a>Support

Le [Forum de développement du ruban Windows](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications de ruban Windows.

## <a name="minimum-requirements"></a>Configuration minimale requise



| Condition requise | Valeur |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 7<br/> Windows Vista avec Service Pack 2 (SP2) et [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| Serveur minimal pris en charge | Windows Server 2008 R2<br/> Windows Server 2008 avec SP2 et la [mise à jour de la plateforme pour Windows server 2008](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Kit de développement logiciel (SDK) Windows              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| Fichiers d’en-tête et IDL     | UIRibbon. h, UIRibbon. idl                                                                                                                                                 |



 

> [!Note]  
> La [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) et la [mise à jour de la plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) sont des ensembles de bibliothèques Runtime qui permettent aux développeurs de cibler des applications de ruban Windows vers Windows Vista et Windows Server 2008. Les mises à jour de la plateforme seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update. Les applications tierces qui requièrent une [mise à jour de plateforme pour Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) ou une [mise à jour de plateforme pour Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.

 

 

 





