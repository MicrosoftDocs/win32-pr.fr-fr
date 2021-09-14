---
title: Windows Gestionnaire d’animations
description: le gestionnaire d’animations Windows (animation Windows) permet une animation enrichie d’éléments d’interface utilisateur.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows animation Windows animation, portail
- Windows animation du gestionnaire d’animations Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008549"
---
# <a name="windows-animation-manager"></a>Windows Gestionnaire d’animations

## <a name="purpose"></a>Objectif

le gestionnaire d’animations Windows (animation Windows) permet une animation enrichie d’éléments d’interface utilisateur. Il est conçu pour simplifier le processus d’ajout d’animation à l’interface utilisateur d’une application et pour permettre aux développeurs d’implémenter des animations lisses, naturelles et interactives.

L’infrastructure d’animation gère la planification et l’exécution des animations. Il fournit une bibliothèque de fonctions mathématiques utiles pour spécifier le comportement d’un élément d’interface utilisateur au fil du temps, et permet également aux développeurs d’implémenter des fonctions personnalisées qui fournissent des comportements supplémentaires.

Windows L’animation n’effectue pas le rendu ; Il peut être utilisé avec n’importe quelle plateforme graphique, y compris Direct2D, Direct3D ou GDI+.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                   | Description                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Guide de développement d’animation](windows-animation-developer-guide.md)<br/> | le guide du développeur fournit une vue d’ensemble de Windows animation et fournit un exemple de code qui couvre les tâches de base de l’animation.<br/>          |
| [Windows Référence d’animation](windows-animation-reference.md)<br/>               | les rubriques contenues dans cette section fournissent les spécifications de référence pour le gestionnaire d’animations Windows.<br/>                           |
| [Windows Exemples d’animation](windows-animation-samples.md)<br/>                   | les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation du gestionnaire d’animations Windows. <br/> |
| [Windows Glossaire d’animation](-ui-animation-glossary.md)<br/>                     | ce glossaire contient des termes et des acronymes intéressants pour les développeurs qui utilisent le gestionnaire d’animations Windows.<br/>                               |



 

## <a name="developer-audience"></a>Développeurs concernés

Windows L’animation est conçue pour être utilisée par les développeurs C/C++ expérimentés qui connaissent COM, les concepts de programmation de l’interface utilisateur et les concepts d’animation généraux.

## <a name="run-time-requirements"></a>Conditions d’exécution

le gestionnaire d’animations Windows a été introduit dans Windows 7.

les Applications qui requièrent la prise en charge de Windows gestionnaire d’animations sur Windows vista peuvent utiliser la mise à jour de plateforme pour Windows vista. les Applications qui requièrent une mise à jour de plateforme pour Windows Vista peuvent avoir Windows Update vérifier qu’elles sont installées, ou les télécharger et les installer en arrière-plan dans le cas contraire. pour plus d’informations, consultez à [propos de la mise à jour de plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Ressources supplémentaires

-   [vue d’ensemble de l’Animation Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (vidéo)
-   [dans Windows 7 : présentation approfondie du gestionnaire d’animations et didacticiel](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (vidéo)
-   [Animation Windows-rubriques avancées](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vidéo)
-   [Windows Exemple de code du gestionnaire d’animations](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Rubriques connexes

[Vue d’ensemble de l’animation (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)