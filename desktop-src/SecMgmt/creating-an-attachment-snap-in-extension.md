---
description: Une extension de composant logiciel enfichable d’une pièce jointe fournit une interface que les utilisateurs peuvent utiliser pour modifier les paramètres de configuration spécifiques aux services.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Création d’une extension de composant logiciel enfichable pièce jointe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009022"
---
# <a name="creating-an-attachment-snap-in-extension"></a>Création d’une extension de composant logiciel enfichable pièce jointe

Une extension de composant logiciel enfichable d’une pièce jointe fournit une interface que les utilisateurs peuvent utiliser pour modifier les paramètres de configuration spécifiques aux services. L’extension du composant logiciel enfichable d’attachement doit respecter les exigences de la console MMC pour être une extension de composant logiciel enfichable valide. Pour plus d’informations sur ces conditions requises, consultez la documentation de la console MMC ( [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) ).

Outre les interfaces requises par MMC, une extension de composant logiciel enfichable d’attachement doit implémenter l’interface COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Les composants logiciels enfichables de configuration de la sécurité appellent les méthodes de cette interface pour déterminer si les données de configuration ont été modifiées et, le cas échéant, pour mettre à jour la base de données de sécurité. Le composant logiciel enfichable pièce jointe doit stocker les modifications de configuration jusqu’à ce que les composants logiciels enfichables de configuration de sécurité récupèrent ces données.

Une extension de composant logiciel enfichable d’une pièce jointe doit fournir les fonctionnalités suivantes :

-   [Afficher les informations de configuration et d’analyse](displaying-configuration-and-analysis-information.md)
-   [Modifier les informations de configuration dans l’interface utilisateur](modifying-configuration-information-in-the-user-interface.md)
-   [Modifier les informations de configuration dans la base de données de sécurité](modifying-configuration-information-in-the-database.md)

Pour aider votre extension de composant logiciel enfichable à effectuer ces tâches, les composants logiciels enfichables de configuration de sécurité implémentent une interface COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), qui fournit des méthodes que votre extension de composant logiciel enfichable peut appeler afin de s’initialiser et de demander des informations à partir de la base de données de sécurité.

Une fois que vous avez créé votre extension de composant logiciel enfichable d’attachement, vous devez l’inscrire auprès des composants logiciels enfichables de configuration de sécurité, comme décrit dans [inscription d’une extension de composant logiciel enfichable d’attachement](registering-an-attachment-snap-in-extension.md).

 

 
