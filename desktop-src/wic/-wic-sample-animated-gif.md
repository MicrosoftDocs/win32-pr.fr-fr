---
description: Cet exemple illustre le décodage de différents frames dans un fichier GIF, la lecture des métadonnées appropriées pour chaque frame, la composition des frames et le rendu de l’animation avec Direct2D.
ms.assetid: d71c66b5-d37c-4c8a-bfd7-b97c69c3b8e9
title: Exemple de Gif animé WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 925beb45b58bdecb7d12505a9d2067cbcb9e6fbf1867786286f18333fea986e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709599"
---
# <a name="wic-animated-gif-sample"></a>Exemple de GIF animé WIC

Cet exemple illustre le décodage de différents frames dans un fichier GIF, la lecture des métadonnées appropriées pour chaque frame, la composition des frames et le rendu de l’animation avec Direct2D.

## <a name="requirements"></a>Configuration requise

Cet exemple présente les exigences suivantes.

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Windows 7 |
| SDK Windows minimal | [kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour Windows 7 |

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans le fichier [gif animé WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicanimatedgif).

## <a name="building-the-sample"></a>Génération de l’exemple

### <a name="using-visual-studio-preferred-method"></a>utilisation de Visual Studio (méthode recommandée)

1. Ouvrez l’Explorateur Windows et accédez au répertoire.
2. Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le fichier dans Visual Studio.
3. Dans le menu **Générer**, sélectionnez **Générer la solution**. L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .

### <a name="using-the-command-prompt"></a>À l’aide de l’invite de commandes

Pour générer l’exemple à l’aide d’une invite de commandes.

1. Ouvrez l’invite de commandes et accédez au répertoire de l’exemple.
2. Saisissez `msbuild WICAnimatedGif.sln`

## <a name="running-the-sample"></a>Exécution de l’exemple

Une fois l’application lancée, chargez un fichier image à l’aide de la commande **ouvrir** du menu **fichier** . Le redimensionnement de fenêtre est pris en charge.

## <a name="see-also"></a>Voir aussi

[Codec Microsoft Windows Imaging](-wic-lh.md)

[Guide de programmation](-wic-programming-guide.md)

[Référence](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Exemples et exemples de code](-wic-samples.md)
