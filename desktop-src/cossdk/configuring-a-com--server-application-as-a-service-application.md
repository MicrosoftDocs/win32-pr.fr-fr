---
description: Une application serveur COM+ peut être créée en tant que service pour démarrer automatiquement au démarrage du système ou manuellement par des activations.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configuration d’une application serveur COM+ en tant qu’application de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095445"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a>Configuration d’une application serveur COM+ en tant qu’application de service

Une application serveur COM+ peut être créée en tant que service pour démarrer automatiquement au démarrage du système ou manuellement par des activations. Si le service ne démarre pas, l’option de gestion des erreurs spécifie la gravité de l’erreur et détermine l’action à entreprendre. L’option permettant de configurer un service pour qu’il s’exécute en tant que compte système local est également disponible, ainsi que l’option permettant d’affecter un compte d’utilisateur spécifique pour lequel l’application serveur COM+ s’exécutera. Vous pouvez également sélectionner des dépendances dans une liste de services inscrits sur l’ordinateur à l’aide des services de composants. Cela permet de déterminer les services qui doivent être exécutés avant le démarrage de ce service.

**Pour configurer une application COM+ pour qu’elle s’exécute en tant que service**

1.  Dans l’arborescence de la console de l’outil d’administration Services de composants, localisez l’application serveur COM+ que vous souhaitez exécuter en tant que service.

2.  Cliquez avec le bouton droit sur l’application serveur COM+, puis cliquez sur **Propriétés**.

3.  Dans la boîte de dialogue **Propriétés** , cliquez sur l’onglet **activation** .

4.  Dans la zone **type d’activation** , activez la case à cocher exécuter l' **application en tant que service NT** .

    > [!Note]  
    > La case à cocher **exécuter l’application en tant que service NT** est activée uniquement pour les applications serveur et est désactivée pour les applications de bibliothèque.

     

5.  Cliquez sur le bouton **configurer un nouveau service** .

6.  Dans la zone **type de démarrage** de la boîte de dialogue nom du **service** , sélectionnez **automatique** ou **Manuel**.

7.  Facultatif Pour spécifier l’action à entreprendre pour une erreur particulière, sélectionnez **Ignorer**, **normal**, **grave** ou **critique** dans la zone **gestion des erreurs** . Le comportement associé à chaque option est le suivant :

    1.  **Ignorer**. Le programme de démarrage consigne l’erreur, mais poursuit l’opération de démarrage.
    2.  **Normal**. L’erreur est consignée, une boîte de message s’affiche et le programme de démarrage continue l’opération de démarrage.
    3.  **Grave**. L’erreur est journalisée et le système est redémarré avec la dernière bonne configuration connue. S’il s’agit de la dernière configuration correcte connue qui est démarrée lorsque l’erreur est journalisée, l’opération de démarrage se poursuit.
    4.  **Critique**. L’erreur est journalisée et le système est redémarré avec la dernière bonne configuration connue. S’il s’agit de la dernière configuration correcte connue qui est démarrée lorsque l’erreur est journalisée, l’opération de démarrage échoue.

8.  Facultatif Pour définir d’autres services comme dépendants, sélectionnez les services dépendants dans la liste de la zone **dépendances** .

9.  Facultatif Pour indiquer que le service doit être autorisé à interagir avec le bureau, activez la case à cocher **autoriser le service à interagir avec le bureau** .

10. Cliquez sur **Créer**.

11. Facultatif Pour affecter le service à un compte d’utilisateur :

    1.  Sous l’onglet **identité** , sélectionnez **cet utilisateur**.
    2.  Pour sélectionner l’utilisateur, entrez le nom d’utilisateur dans la zone **utilisateur** ou cliquez sur le bouton **Parcourir** .
    3.  Entrez le mot de passe du compte d’utilisateur dans la zone **mot de passe** .
    4.  Entrez le même mot de passe dans la zone **confirmer le mot de passe** .

 

 



