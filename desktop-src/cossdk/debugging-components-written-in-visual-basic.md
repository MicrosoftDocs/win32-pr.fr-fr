---
description: Débogage de composants écrits en Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Débogage de composants écrits en Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295734"
---
# <a name="debugging-components-written-in-visual-basic"></a>Débogage de composants écrits en Visual Basic

vous pouvez utiliser l’environnement de développement Microsoft Visual Basic 6,0 pour le débogage dans certains scénarios. l’utilisation de Visual Basic pour le débogage permet d’accéder à des outils familiers aux programmeurs Visual Basic. en revanche, comme lors du débogage Visual Basic composants s’exécutent dans le processus de l’environnement Visual Basic, il peut être nécessaire de déboguer votre composant après qu’il a été compilé à l’aide de l’environnement de développement Microsoft Visual C++.

pour plus d’informations sur le débogage dans l’environnement de développement intégré (ide) Visual Basic, consultez [débogage dans l’ide Visual Basic](debugging-in-the-visual-basic-ide.md). pour plus d’informations sur le débogage des composants de Visual Basic une fois qu’ils sont compilés à l’aide de l’environnement de développement Visual C++, consultez [débogage de composants Visual Basic compilés](debugging-compiled-visual-basic-components.md).

en outre, plusieurs limitations associées à l’utilisation de l’environnement de Visual Basic pour déboguer des composants avec MTS ont été résolues pour COM+. pour plus d’informations, consultez [prise en charge du débogage des Visual Basic COM+ et différences avec MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> si vous avez déjà utilisé Visual Basic sur le même ordinateur que COM+, vous avez peut-être remarqué que le complément Services de composants est disponible dans l’environnement Visual Basic. À l’origine dans MTS, cette fonctionnalité a été conçue pour mettre à jour le registre chaque fois que vous recompilez un composant dans une application COM+. toutefois, étant donné la nature de l’interaction du registre de Windows Microsoft et de la base de données d’inscription COM+, certains paramètres peuvent ne pas être entièrement mis à jour. Par conséquent, au lieu d’utiliser les commandes disponibles avec ce complément, vous devez supprimer et réinstaller vos composants pour mettre à jour les paramètres après la recompilation.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Débogage de composants écrits en Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



