---
title: Informations d’inscription de la tâche
description: Les informations d’inscription permettent d’identifier une tâche de différentes façons. Par exemple, une tâche peut être identifiée par l’auteur, comment elle a été créée (appelée « source de tâche ») et la date d’inscription.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- informations d’inscription Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309194"
---
# <a name="task-registration-information"></a>Informations d’inscription de la tâche

Les informations d’inscription permettent d’identifier une tâche de différentes façons. Par exemple, une tâche peut être identifiée par l’auteur, comment elle a été créée (appelée « source de tâche ») et la date d’inscription.

## <a name="using-registration-information"></a>Utilisation des informations d’inscription

Les informations d’inscription sont généralement spécifiées lors de la création de la tâche, puis utilisées de la façon suivante :

-   Affiché par l’interface utilisateur Planificateur de tâches.
-   Obtient ou définit par les applications ou les scripts C++.
-   Dans un environnement d’entreprise, utilisé comme critère de recherche lors de l’énumération de toutes les tâches inscrites.

## <a name="types-of-registration-information"></a>Types d’informations d’inscription

Les informations d’inscription des tâches sont définies par les propriétés de l’objet [**RegistrationInfo**](registrationinfo.md) pour les applications de script, les propriétés de l’interface [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) pour les applications C++ et les éléments enfants de l' [**élément RegistrationInfo (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) pour la lecture ou l’écriture de code XML.

Ces propriétés autorisent l’accès aux types d’informations d’inscription suivants :

-   Auteur de la tâche

    Planificateur de tâches définit l’auteur de la tâche lors de sa création.

-   Date d’inscription de la tâche

    Planificateur de tâches définit cette date lorsque la tâche est inscrite.

-   Description de la tâche

    Description définie par l’utilisateur qui peut inclure les déclencheurs utilisés pour démarrer la tâche ou les actions effectuées par la tâche.

-   Documentation sur les tâches

    Documentation fournie par l’utilisateur et exigée par la tâche.

-   Descripteur de sécurité des tâches

    Descripteur de sécurité fourni par l’utilisateur.

-   Source de la tâche

    Informations fournies par l’utilisateur qui décrivent l’origine de la tâche. Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.

-   URI de tâche

    URI (Uniform Resource Identifier) de la tâche.

-   Version de la tâche

    Informations fournies par l’utilisateur qui sont utilisées lorsque plusieurs versions d’une tâche existent.

-   Texte XML

    Version au format XML des informations d’inscription. Notez que vous pouvez définir ou modifier les informations d’inscription directement par le biais de ce code XML, et que les propriétés de l’objet et de l’interface appropriées seront mises à jour en conséquence.

## <a name="registering-tasks"></a>Inscription de tâches

Une tâche peut être inscrite après la création des définitions de tâche, et les informations d’inscription et les valeurs de paramètres sont fournies par l’utilisateur. Une tâche est inscrite à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) pour les applications de script ou de la méthode [**ITaskFolder :: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) pour les applications C++. Si vous souhaitez inscrire une tâche à l’aide de XML pour définir la tâche, utilisez la méthode [**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour les applications de script et la méthode [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) pour les applications C++.

Dans les méthodes mentionnées ci-dessus, vous pouvez spécifier le contexte de sécurité pour l’exécution de la tâche. Vous devez être administrateur sur le système pour planifier l’exécution des tâches sous des contextes autres que les vôtres. Pour plus d’informations sur les contextes de sécurité pour exécuter des tâches, consultez [contextes de sécurité pour les tâches en cours d’exécution](security-contexts-for-running-tasks.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’Planificateur de tâches](about-the-task-scheduler.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 




