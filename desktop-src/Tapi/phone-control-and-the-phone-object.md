---
description: TAPI 3,1 introduit les contrôles de téléphone COM. La connaissance du modèle d’objet TAPI 3 est supposée vous familiariser avec COM, OLE Automation et les scripts. La connaissance des fonctions de contrôle de téléphone TAPI 2 est également utile.
ms.assetid: e56aef54-e358-429b-9f0f-c8776507d95f
title: Contrôle de téléphone et objet de téléphone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e9344d54a63efcf1692af361a5f8e88121981e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527842"
---
# <a name="phone-control-and-the-phone-object"></a>Contrôle de téléphone et objet de téléphone

TAPI 3,1 introduit les contrôles de téléphone COM. La connaissance du modèle d’objet TAPI 3 est supposée vous familiariser avec COM, OLE Automation et les scripts. La connaissance des fonctions de contrôle de téléphone TAPI 2 est également utile.

Le contrôle téléphonique est implémenté à trois niveaux de fonctionnalités, chacun d’entre eux s’appuyant sur le précédent :

-   Objet Phone. Le premier niveau définit la manière dont les appareils téléphoniques TAPI 2. x (API, constantes et messages commençant par « Phone ») sont exposés dans le modèle objet TAPI 3,1. Cela implique un nouvel objet téléphone exposé par TAPI 3,1, avec [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) comme interface par défaut sur le nouvel objet. L’interface **ITPhone** , ainsi que les constantes, les types énumérés et les événements qui lui sont associés, exposent généralement le même niveau de détail et de fonctionnalité que les fonctions, les constantes, les structures et les messages TAPI 2. x qui commencent par le mot « Phone ». Ce niveau implique également de nouvelles interfaces sur plusieurs objets TAPI 3. x existants pour faciliter la création d’objets téléphoniques et l’Association d’objets Phone avec d’autres objets auxquels ils sont associés.
-   Gestion automatique des appels et du contrôle par téléphone. Le deuxième niveau se compose d’une interface supplémentaire appelée [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) et des constantes, des types énumérés et des événements associés. Il s’agit d’une interface secondaire sur l’objet Phone. Si l’appareil téléphonique a été ouvert avec un privilège de propriétaire, utilisez la méthode **QueryInterface** sur l’interface [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) pour obtenir un pointeur d’interface **ITAutomatedPhoneControl** .
-   Numéroteur téléphonique Windows 2000. Le troisième niveau est constitué de modifications apportées à l’application de Numéroteur téléphonique Windows 2000 pour implémenter des interactions utilisateur spécifiques.

Microsoft ou des développeurs tiers peuvent utiliser le modèle d’objet TAPI 3,1 pour implémenter des applications ou des services plus avancés impliquant des téléphones, y compris un service qui active des combinés USB (Universal Serial Bus), par exemple, à utiliser pour les appels téléphoniques, même si aucun utilisateur n’est connecté et qu’aucune autre application TAPI n’a été démarrée explicitement.

Dans TAPI 3,0, un MSP de téléphone a tenté d’améliorer les appareils téléphoniques associés aux lignes utilisées pour les appels TAPI 3,0. Ce développement est destiné à la prise en charge de modems avec des mains libres commutables logicielles. Les applications TAPI 3,1 qui utilisent ce type de modem doivent utiliser les objets téléphoniques TAPI 3,1 pour manipuler l’état du modem hookswitch.

Pour plus d’informations et pour obtenir la liste de toutes les interfaces associées à l’objet Phone, consultez [Phone Object interfaces](phone-object-interfaces.md). Les interfaces de contrôle téléphonique exposent des méthodes qui permettent de contrôler les ensembles de téléphones à l’aide de COM.

 

 



