---
description: Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder un fichier image et Direct2D pour afficher l’image à l’écran.
ms.assetid: 4f989ff6-b513-4354-a1bb-8d9521f693a2
title: Visionneuse d’images WIC avec l’exemple Direct2D
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: a18bf17e7f43d3c4ad935bae9f8ed42e7b48db01
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106532697"
---
# <a name="wic-image-viewer-using-direct2d-sample"></a>Visionneuse d’images WIC avec l’exemple Direct2D

Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder un fichier image et Direct2D pour afficher l’image à l’écran.

## <a name="requirements"></a>Configuration requise

Cet exemple présente les exigences suivantes.

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Windows Vista |
| SDK Windows minimal | [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour Windows 7 |

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans la [visionneuse WIC D2D](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewerd2d).

## <a name="building-the-sample"></a>Génération de l’exemple

### <a name="using-visual-studio-preferred-method"></a>Utilisation de Visual Studio (méthode recommandée)

1. Ouvrez l’Explorateur Windows et accédez au répertoire.
2. Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le fichier dans Visual Studio.
3. Dans le menu **Générer**, sélectionnez **Générer la solution**. L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .

### <a name="using-the-command-prompt"></a>À l’aide de l’invite de commandes

Pour générer l’exemple à l’aide d’une invite de commandes :

1. Ouvrez une fenêtre d’invite de commandes et accédez au répertoire de l’exemple.
2. Saisissez `msbuild WICViewerD2D.sln`

## <a name="running-the-sample"></a>Exécution de l’exemple

Après avoir démarré l’application, chargez un fichier image à l’aide de la commande **ouvrir** du menu **fichier** .

## <a name="see-also"></a>Voir aussi

[Codec d’image Microsoft Windows](-wic-lh.md)

[Guide de programmation](-wic-programming-guide.md)

[Référence](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Exemples et exemples de code](-wic-samples.md)
