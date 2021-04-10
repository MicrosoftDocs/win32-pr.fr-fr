---
title: Développement du serveur
description: Lorsque vous créez un programme serveur pour une application distribuée, vous devez utiliser le fichier d’en-tête et le stub de serveur générés par le compilateur MIDL.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- Appel de procédure distante RPC, tâches, développement du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc3405c52c48f531572ab159ad083bad93f95e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316074"
---
# <a name="developing-the-server"></a>Développement du serveur

Lorsque vous créez un programme serveur pour une application distribuée, vous devez utiliser le fichier d’en-tête et le stub de serveur générés par le compilateur MIDL. Pour plus d’informations, consultez [développement de l’interface](developing-the-interface.md). Incluez le fichier d’en-tête dans le fichier programme du serveur C. Compilez le stub serveur avec les fichiers sources C qui composent votre application. Liez les fichiers objets résultants à la bibliothèque d’importation. Ce processus est illustré dans le diagramme suivant.

![processus de création d’un programme serveur pour une application distribuée](images/srvrdev.png)

Comme vous pouvez le voir dans l’exemple de l’illustration, un fichier MIDL appelé MyApp. idl a été utilisé pour définir l’interface. Le compilateur MIDL a utilisé MyApp. idl pour produire MyApp \_ s. c et MyApp. h. Il produit également un fichier source C pour le stub client, mais cela ne s’applique pas à cette discussion particulière. Le fichier source C pour le programme serveur (dans le cas présent, Mysrvr. C) doit inclure le fichier MyApp. h. Il doit également inclure les fichiers RPC. h et Rpcndr. h.

L’application serveur a été développée dans deux fichiers, Mysrvr. c et Rprocs. c. Le fichier Mysrvr. c contient les fonctions nécessaires à la mise en service du programme serveur. Les procédures distantes proposées par le programme serveur sont contenues dans le fichier Rprocs. c.

Les fichiers Mysrvr. c et Rprocs. c ont été compilés avec MyApp \_ s. c pour produire des fichiers objets. Les fichiers objets étaient ensuite liés à la bibliothèque Runtime RPC et à toutes les autres bibliothèques dont ils peuvent avoir besoin. Le résultat est un programme serveur exécutable nommé Mysrvr.exe.

Si vous ne compilez pas votre fichier IDL en mode de compatibilité OSF (Open Software Foundation) ([**/OSF**](/windows/desktop/Midl/-osf)), votre programme serveur doit fournir une fonction pour allouer de la mémoire et une fonction pour la libérer. Pour Windows 2000 et les versions ultérieures de Windows, le mode recommandé est [**/Oicf**](/windows/desktop/Midl/-oi). Pour plus d’informations, consultez [Comment la mémoire est allouée et désallouée](how-memory-is-allocated-and-deallocated.md), ainsi que les [pointeurs et l’allocation de mémoire](pointers-and-memory-allocation.md).

 

 