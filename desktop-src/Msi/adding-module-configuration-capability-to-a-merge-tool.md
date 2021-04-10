---
description: Windows Installer les développeurs peuvent créer des outils qui permettent aux utilisateurs finaux d’utiliser des modules de fusion configurables.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Ajout de la fonctionnalité de configuration de module à un outil de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756255"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a>Ajout de la fonctionnalité de configuration de module à un outil de fusion

Pour permettre aux utilisateurs finaux d’utiliser des modules de fusion configurables, vous pouvez créer des outils de fusion et de configuration pour effectuer les opérations suivantes :

-   Les outils de fusion doivent appeler les fonctions de Mergemod.dll version 2,0 pour fusionner le module. Les versions antérieures de Mergemod.dll ne peuvent pas être utilisées pour configurer des modules de fusion.
-   Les applications de configuration clientes doivent interagir avec l’utilisateur du module de fusion pour collecter les sélections d’éléments configurables par l’utilisateur.
-   Les outils de fusion doivent exposer les informations de configuration créées dans le module de fusion à l’application cliente afin que le client puisse utiliser ces informations pour interroger l’utilisateur.
-   Lorsqu’un outil de fusion rencontre un élément configurable pendant une fusion, il doit appeler l’outil de configuration du client pour les informations de personnalisation obtenues auprès de l’utilisateur. L’outil de fusion doit effectuer les modifications spécifiées dans le module de fusion.
-   Les applications de configuration doivent permettre à l’utilisateur de fournir des choix pour les éléments configurables, mais il n’est pas nécessaire que tous les choix soient révélés à l’utilisateur. L’outil de fusion peut utiliser des valeurs par défaut pour les éléments configurables que l’utilisateur ne sélectionne pas.
-   Si un utilisateur ne fournit pas d’informations de personnalisation, les outils de fusion doivent utiliser les valeurs de configuration par défaut spécifiées dans le module de fusion.
-   Une fois qu’un utilisateur a effectué les sélections spécifiques à l’outil de configuration, l’outil de fusion appelle Mergemod.dll pour effectuer la fusion.

 

 



