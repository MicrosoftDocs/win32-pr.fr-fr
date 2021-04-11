---
description: 'Les applications Direct3D peuvent s’exécuter dans l’un ou l’autre des deux modes : plein écran ou fenêtre.'
ms.assetid: 6ec30c6e-93d1-4b77-9638-86308bbf8f3c
title: Mode fenêtre/Full-Screen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf51c641446d3f54ceb37c9cc1ac629604f68400
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108734"
---
# <a name="windowed-vs-full-screen-mode-direct3d-9"></a>Mode fenêtre/Full-Screen (Direct3D 9)

Les applications Direct3D peuvent s’exécuter dans l’un ou l’autre des deux modes : plein écran ou fenêtre.

Le mode plein écran signifie que la fenêtre dans laquelle l’application s’exécute couvre l’ensemble du bureau, en masquant toutes les applications en cours d’exécution (y compris votre environnement de développement). Les jeux utilisent généralement le mode plein écran par défaut pour plonger entièrement l’utilisateur dans le jeu en masquant toutes les applications en cours d’exécution. Une application exécutée en mode fenêtre partage le bureau avec toutes les applications en cours d’exécution. Les différences de code entre le mode plein écran et le mode fenêtre sont très petites.

Étant donné qu’une application s’exécutant en mode plein écran prend le contrôle à l’écran, le débogage de l’application nécessite un moniteur distinct ou l’utilisation d’un débogueur distant. Utilisez l' [outil panneau de configuration DirectX](https://msdn.microsoft.com/library/Ee416791(v=VS.85).aspx) pour activer le débogage à plusieurs écrans. L’un des avantages d’une application en mode fenêtre est que vous pouvez effectuer un pas à pas détaillé dans le code d’un débogueur sans plusieurs analyses ou un débogueur distant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 



