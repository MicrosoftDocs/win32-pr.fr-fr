---
description: l’utilisation de l’environnement de développement intégré (IDE) de Microsoft Visual Basic pour le débogage offre aux développeurs Visual Basic accès à des outils familiers et à une facilité d’utilisation.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: débogage dans l’IDE Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295730"
---
# <a name="debugging-in-the-visual-basic-ide"></a>débogage dans l’IDE Visual Basic

l’utilisation de l’environnement de développement intégré (IDE) de Microsoft Visual Basic pour le débogage offre aux développeurs Visual Basic accès à des outils familiers et à une facilité d’utilisation. si de nombreux composants finiront par être plus complètement débogués à l’aide de l’environnement Microsoft Visual C++, une stratégie peut consister à déboguer autant de fonctionnalités que possible avec Visual Basic. par exemple, vous pouvez utiliser l’IDE Visual Basic pour le débogage dans COM+ lorsque vous n’êtes pas encore en train de déboguer le multithreading, le suivi des composants, les appels distants ou l’isolation des processus.

en général, lors de l’utilisation de l’environnement de Visual Basic pour le débogage, vous devez d’abord compiler le projet et ajouter la DLL à une application COM+. Vous définissez ensuite la compatibilité binaire pour le projet, en référençant la DLL que vous avez créée et démarrez le projet pour commencer le débogage.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>instructions générales pour le débogage dans l’environnement de Visual Basic

-   lors du débogage à l’aide de Visual Basic, COM+ traite les composants Visual Basic comme s’ils appartenaient à une application de bibliothèque, même si les composants sont inscrits comme appartenant à une application serveur. Étant donné qu’il s’exécute en tant qu’application de bibliothèque, les icônes de composant dans l’outil d’administration Services de composants ne s’exécutent pas lorsque les composants sont débogués.
-   si vous modifiez les attributs de transaction sur un composant pendant le débogage ou que vous modifiez le code source qui requiert Visual Basic pour générer un nouveau CLSID ou ProgID, veillez à supprimer et réinstaller l’application COM+ contenant le composant. Si vous avez défini la compatibilité binaire pour le composant, vous êtes averti que des modifications ont été apportées.

## <a name="notes-on-debugging-within-a-com-application"></a>Remarques sur le débogage dans une application COM+

-   si vous apportez des modifications dans l’IDE Visual Basic dans les interfaces de votre composant, les noms de classe, les noms de projet, la prise en charge transactionnelle ou d’autres paramètres, il peut y avoir des incompatibilités entre les données de configuration dans l’explorateur de Services de composants et la configuration réelle en cours d’exécution dans le débogueur Visual Basic.
-   N’exportez pas une application COM+ pendant que vous déboguez un composant dans l’application. COM+ traitera l’environnement de développement Visual Basic en tant que composant.
-   Si vous exécutez un composant en dehors du débogueur et décidez ensuite de commencer le débogage, une instance du composant peut toujours s’exécuter dans COM+ lorsque vous le démarrez dans le débogueur. COM+ détecte cette condition et tente d’arrêter silencieusement l’instance qu’il contrôle. Pour éviter ce problème, supprimez le composant de l’outil d’administration Services de composants avant de commencer le débogage.

**pour déboguer à l’aide de l’environnement Visual Basic**

1.  Ouvrez le projet de composant dans Visual Basic.

2.  Compilez votre composant, puis définissez la compatibilité binaire de votre projet sur le composant compilé.

3.  Affectez à la propriété MTSTransactionMode une valeur différente de 0-NotAnMTSObject. quand vous démarrez le projet, ce paramètre invite Visual Basic à activer votre composant dans COM+.

4.  dans le menu **Project** , cliquez sur **propriétés**, puis entrez le programme démarrer sous l’onglet **débogage** . Le programme de démarrage est l’exécutable client qui appelle ce composant.

    > [!Note]  
    > Le programme de démarrage doit être local pour le composant que vous déboguez.

     

5.  Appuyez sur la touche F5 pour commencer le débogage du composant.

une fois que vous avez appuyé sur F5, Visual Basic lance l’application cliente et exécute le composant en mode débogage. Vous pouvez placer des points d’arrêt dans le code du composant et définir des espions sur des variables.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[prise en charge du débogage des Visual Basic COM+ avec MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[débogage de composants Visual Basic compilés](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



