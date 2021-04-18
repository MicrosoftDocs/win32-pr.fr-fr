---
description: Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder une image encodée avec des niveaux progressifs.
ms.assetid: 14018dce-26f0-4e1e-9d19-c5b42dd2cdab
title: Exemple de décodage progressif WIC
ms.topic: article
ms.date: 03/19/2021
ms.custom: project-verbatim
ms.openlocfilehash: 2e4b1fc560af0ee8c817208fec628ddb068676bb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106543156"
---
# <a name="wic-progressive-decoding-sample"></a>Exemple de décodage progressif WIC

Cet exemple illustre l’utilisation de WIC (Windows Imaging Component) pour décoder une image encodée avec des niveaux progressifs. Cet exemple utilise Direct2D pour restituer les différents niveaux progressifs à l’écran.

## <a name="requirements"></a>Configuration requise

Cet exemple présente les exigences suivantes.

| Condition requise | Valeur |
|-|
| Client minimal pris en charge | Windows 7 |
| SDK Windows minimal | [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) pour Windows 7 |

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible dans l' [encodage progressif WIC](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/progressivedecoding).

## <a name="building-the-sample"></a>Génération de l’exemple

### <a name="using-visual-studio-preferred-method"></a>Utilisation de Visual Studio (méthode recommandée)

1. Ouvrez l’Explorateur Windows et accédez au répertoire.
2. Double-cliquez sur l’icône du fichier. sln (solution) pour ouvrir le fichier dans Visual Studio.
3. Dans le menu Générer, sélectionnez Générer la solution. L’application sera générée dans le répertoire de \\ débogage ou de libération par défaut \\ .

### <a name="using-the-command-prompt"></a>À l’aide de l’invite de commandes

Pour générer l’exemple à l’aide de l’invite de commandes.

1. Ouvrez l’invite de commandes et accédez au répertoire de l’exemple.
2. Saisissez `msbuild WICProgressiveDecoding.sln`

## <a name="running-the-sample"></a>Exécution de l’exemple

Une fois l’application lancée, chargez un fichier image dans le menu fichier ouvrir. Lors du chargement, le niveau de progressif par défaut est défini sur 0. Vous pouvez accéder à différents niveaux progressifs via le menu ou la touche haut/PG. Le texte de niveau progressif actuel est affiché dans la barre d’état de la fenêtre principale. Le redimensionnement de fenêtre est pris en charge.

> [!NOTE]
> Le décodage progressif est disponible uniquement pour les images qui ont été encodées progressivement. L’image fournie avec cet exemple a été encodée progressivement.

## <a name="see-also"></a>Voir aussi

[Codec d’image Microsoft Windows](-wic-lh.md)

[Guide de programmation](-wic-programming-guide.md)

[Référence](-wic-codec-reference.md)

[Direct2D](../direct2d/direct2d-portal.md)

[Exemples et exemples de code](-wic-samples.md)

[Vue d’ensemble du décodage progressif](-wic-progressive-decoding.md)
