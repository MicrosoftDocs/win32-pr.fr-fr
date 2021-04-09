---
description: L’objet gestionnaire de capteurs fournit l’accès aux capteurs disponibles pour votre utilisation.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Objet du gestionnaire de capteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112623"
---
# <a name="the-sensor-manager-object"></a>Objet du gestionnaire de capteurs

L’objet gestionnaire de capteurs fournit l’accès aux capteurs disponibles pour votre utilisation.

Pour utiliser l’API de capteur, vous devez d’abord appeler la méthode COM **CoCreateInstance** pour créer une instance de l’objet de gestionnaire de capteurs et récupérer un pointeur vers son interface, nommée [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager). Le gestionnaire de capteurs gère la liste des capteurs disponibles. Vous pouvez utiliser **ISensorManager** pour appeler des méthodes qui récupèrent des groupes de capteurs par catégorie ou par type, ou vous pouvez appeler une méthode pour récupérer un capteur particulier à l’aide de son ID unique. Le gestionnaire de capteurs vous permet également de vous inscrire pour recevoir un événement qui vous avertit lorsqu’un nouveau capteur a été connecté à la plateforme.

Parfois, le gestionnaire de capteurs fournit un pointeur vers un capteur, mais l’utilisateur n’a pas activé le capteur. Par exemple, vous pouvez souvent récupérer des valeurs pour les propriétés d’un capteur non privé, telles que le modèle ou le fabricant du capteur, avant que l’utilisateur active le capteur. Ces informations peuvent vous aider à décider s’il faut demander à l’utilisateur l’autorisation d’utiliser le capteur. Vous pouvez appeler [**ISensorManager :: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) pour inviter l’utilisateur à activer un capteur ou une collection de capteurs particuliers.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des autorisations utilisateur](managing-user-permissions.md)
</dt> <dt>

[Demande d’autorisations utilisateur](requesting-user-permissions.md)
</dt> </dl>

 

 
