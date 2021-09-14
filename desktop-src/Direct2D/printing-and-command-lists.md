---
title: Impression et listes de commandes
description: Le contrôle d’impression Direct2D \ 32 ; est un nouveau composant du module Direct2D dans Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112585"
---
# <a name="printing-and-command-lists"></a>Impression et listes de commandes

Le [](./direct2d-portal.md) [**contrôle d’impression**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Direct2D est un nouveau composant du module Direct2D dans Windows 8. Ce composant permet aux applications Direct2D de réutiliser leurs appels de dessin Direct2D (en termes de modifications d’État et de primitives rendu) pour fournir des résultats d’impression similaires à ceux que vous voyez à l’écran.

L’interface [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) représente un travail d’impression virtuel : vous pouvez créer un contrôle d’impression [Direct2D](./direct2d-portal.md) pour lancer un nouveau travail d’impression, passer le contenu Direct2D pour chaque page que vous souhaitez imprimer, puis fermer le contrôle d’impression pour terminer un travail d’impression.

> [!Note]  
> Un contrôle d’impression est mappé à un et un seul travail d’impression, et vous ne pouvez pas le réutiliser.

Le contrôle d’impression [Direct2D](./direct2d-portal.md) convertit et optimise le contenu de Direct2D passé pour le sous-système d’impression, qui fonctionne avec les véritables imprimantes pour remettre l’impression réelle. Tous les détails spécifiques à l’impression sont masqués dans les applications Direct2D, ce qui signifie que les applications Direct2D peuvent imprimer sans savoir quels appareils ils dessinent, ou comment les dessins sont convertis en impression.

Pour imprimer avec [Direct2D](./direct2d-portal.md), vous devez préparer une liste de commandes Direct2D pour chaque page que vous souhaitez imprimer, puis passer cette liste de commandes au contrôle d’impression Direct2D. Pour préparer cette liste de commandes Direct2D, vous devez simplement créer et définir une liste de commandes comme cible de dessin du contexte de périphérique actuel, puis dessiner sur ce contexte de périphérique, exactement comme si vous dessiniez dans une cible bitmap pour l’affichage. Pour plus d’informations sur les appareils et les cibles, consultez [contextes de périphériques et](devices-and-device-contexts.md) de périphériques.

Le diagramme ici illustre l’interaction entre l’application, le contexte de périphérique, la cible bitmap, la cible de la liste de commandes et le contrôle d’impression.

> [!Note]  
> les Windows d’impression Sub-System et les composants d’imprimante sont en gris, car ils sont complètement masqués dans les applications [Direct2D](./direct2d-portal.md) .

![diagramme qui montre comment le commandlist et l’impression interagissent avec une application et Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Exemple

Le processus complet d’impression du contenu Direct2D comprend les étapes suivantes.

1.  Créez un contrôle d’impression pour lancer un travail d’impression.
2.  Ajoutez une page au contrôle d’impression en passant dans une liste de commandes.
3.  Répétez l’étape 2 pour chaque page du reste du document
4.  Fermez le contrôle d’impression pour terminer le travail d’impression.

Voici un exemple de code qui illustre le processus.

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a>Rubriques connexes

[**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[Amélioration des performances des applications Direct2D et de l’impression](improving-direct2d-performance.md)