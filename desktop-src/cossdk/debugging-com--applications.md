---
description: Les techniques de débogage pour les applications COM+ dépendent du langage dans lequel vous choisissez d’écrire votre composant.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Débogage des applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748868"
---
# <a name="debugging-com-applications"></a>Débogage des applications COM+

Les techniques de débogage pour les applications COM+ dépendent du langage dans lequel vous choisissez d’écrire votre composant.

Si vous codez dans Microsoft Visual C++, vous pouvez lancer le débogueur en C++ ou, avec un client distant, vous pouvez procéder au débogage à l’aide du contrôle de procédure à distance (RPC) OLE et du débogage juste-à-temps (JIT). Vous pouvez toujours utiliser l’outil d’administration Services de composants pour déboguer votre composant à l’aide du paramètre **lancement com+ dans le débogueur** sous l’onglet **avancé** de la boîte de dialogue **Propriétés** de l’application com+. Pour plus d’informations sur le débogage des composants codés en C++, consultez [débogage de composants écrits en Visual C++](debugging-components-written-in-visual-c--.md).

À moins que vous ne déboguez actuellement le multithreading, le suivi des composants, les appels distants ou l’isolation des processus, vous pouvez utiliser l’environnement Microsoft Visual Basic à des fins de débogage. Les [composants de débogage écrits en Visual Basic](debugging-components-written-in-visual-basic.md) décrivent le processus de débogage dans un environnement Visual Basic.

La rubrique [débogage dans l’IDE Visual Basic](debugging-in-the-visual-basic-ide.md) fournit une vue d’ensemble générale avec des indications, des conseils et une procédure de débogage dans l’environnement de développement intégré (IDE).

Pour plus d’informations sur le débogage des processus avancés, consultez [débogage de composants Visual Basic compilés](debugging-compiled-visual-basic-components.md).

> [!Note]  
> Plusieurs limitations associées à l’utilisation de l’environnement de Visual Basic pour déboguer des composants avec MTS ont été résolues pour COM+. Pour plus d’informations, consultez [prise en charge du débogage des Visual Basic com+ et différences avec MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM+](handling-errors-in-com-.md)
</dt> </dl>

 

 



