---
title: Développement du client
description: Le développement d’un programme client RPC est semblable au développement du programme serveur. Pour plus d’informations sur le développement d’un programme serveur RPC, consultez développement du serveur.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- Appel de procédure distante RPC, tâches, développement du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ceddedc4ccfd1d068e3452b64ed8c6b54a621d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941271"
---
# <a name="developing-the-client"></a>Développement du client

Le développement d’un programme client RPC est semblable au développement du programme serveur. Pour plus d’informations sur le développement d’un programme serveur RPC, consultez [développement du serveur](developing-the-server.md).

Comme dans le développement de serveur, votre programme client doit inclure le fichier d’en-tête que le compilateur MIDL génère à partir de votre fichier. idl. Le compilateur MIDL génère également un fichier source C contenant le stub client. Vous devez compiler ce fichier source C et le lier à votre programme client. (En outre, le compilateur MIDL génère un fichier source C contenant le stub du serveur, mais cela ne s’applique pas à cette discussion.)

Outre la compilation et la liaison du stub client avec vos fichiers programme, vous devez lier la bibliothèque d’importation (et toutes les autres bibliothèques dont votre programme client a besoin) à votre programme client. Le processus de création d’un programme client RPC est illustré dans le diagramme suivant.

![processus de création d’un programme client pour une application distribuée](images/clntdev.png)

L’exemple de l’illustration précédente illustre la création d’un programme client RPC appelé MyClnt.exe. La première étape consiste à définir l’interface dans le fichier MyApp. idl. Le compilateur MIDL utilise MyApp. idl pour générer le fichier MyApp \_ c. c, qui contient le stub client. Il génère également le fichier MyApp. h, que le programme client doit inclure. Le programme client doit également inclure les fichiers RPC. h et RPCNDR. h.

Le programme client lui-même est créé dans le fichier MyClnt. c. Dans un projet réel, le programme client se compose généralement de plusieurs fichiers sources C. Tous doivent être compilés et liés ensemble. Toutefois, cet exemple utilise un seul fichier pour des raisons de simplicité.

Les fichiers MyClnt. c et MyApp \_ c. c sont compilés et liés avec la bibliothèque Runtime RPC et toutes les autres bibliothèques dont le programme client a besoin. Le résultat est un programme client exécutable nommé MyClnt.exe.

Si vous ne compilez pas votre fichier IDL en mode de compatibilité OSF ([**/OSF**](/windows/desktop/Midl/-osf)), votre programme client doit fournir une fonction pour allouer de la mémoire et une fonction pour le libérer. Pour Windows 2000 et versions ultérieures, le mode recommandé est [**/Oicf**](/windows/desktop/Midl/-oi). Pour plus d’informations, consultez [Comment la mémoire est allouée et désallouée](how-memory-is-allocated-and-deallocated.md), ainsi que les [pointeurs et l’allocation de mémoire](pointers-and-memory-allocation.md).

 

 