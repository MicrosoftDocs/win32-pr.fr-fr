---
title: Inscription d’un serveur exécutable en cours d’exécution
description: Inscription d’un serveur exécutable en cours d’exécution
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363555"
---
# <a name="registering-a-running-exe-server"></a>Inscription d’un serveur exécutable en cours d’exécution

Lorsqu’un serveur exécutable (EXE) est lancé, il doit appeler [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), qui inscrit le CLSID du serveur dans ce que l’on appelle la table de classe (une table différente de la table d’objets en cours d’exécution). Lorsqu’un serveur est inscrit dans la table de classe, il permet au gestionnaire de contrôle des services (SCM) de déterminer qu’il n’est pas nécessaire de lancer à nouveau la classe, car le serveur est déjà en cours d’exécution. Si le serveur n’est pas listé dans la table de classe, le SCM recherche les valeurs appropriées dans le registre et lance le serveur associé au CLSID donné.

Vous transmettez [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) au CLSID pour la classe et un pointeur vers son interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Les clients qui appellent par la suite [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) avec ce CLSID récupèrent un pointeur vers l’interface demandée, tant que la sécurité ne l’interdit pas. (Consultez [fonctions d’assistance](instance-creation-helper-functions.md) pour la création d’instance pour obtenir une description de plusieurs fonctions de création et d’activation d’une instance.)

Le serveur d’un objet de classe doit appeler [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) pour révoquer l’objet de classe (supprimer son inscription) lorsque toutes les conditions suivantes sont remplies :

-   Il n’existe aucune instance existante de la définition de l’objet.
-   Il n’y a aucun verrou sur l’objet de classe.
-   L’application qui fournit des services à l’objet de classe n’est pas sous le contrôle utilisateur (non visible par l’utilisateur sur l’affichage).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Installation d’une application en tant que service](installing-as-a-service-application.md)
</dt> <dt>

[Inscription d’une classe lors de l’installation](registering-a-class-at-installation.md)
</dt> <dt>

[Inscription d’objets dans le ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Inscription automatique](self-registration.md)
</dt> </dl>

 

 




