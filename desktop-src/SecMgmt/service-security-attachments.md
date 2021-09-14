---
description: L’ensemble d’outils de configuration de sécurité Microsoft est un ensemble d’outils MMC (Microsoft Management Console) qui simplifient la configuration et l’analyse de la sécurité du système.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Pièces jointes de sécurité de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228894"
---
# <a name="service-security-attachments"></a>Pièces jointes de sécurité de service

L’ensemble d’outils de configuration de sécurité Microsoft est un ensemble d’outils MMC (Microsoft Management Console) qui simplifient la configuration et l’analyse de la sécurité du système. Certains services, toutefois, ont des besoins de configuration spécialisés qui vont au-delà des paramètres de sécurité fournis par le jeu d’outils standard. Pour gérer ces besoins, vous pouvez étendre les fonctionnalités de l’ensemble d’outils en écrivant une pièce jointe qui gère les tâches de sécurité spécifiques au service.

Par exemple, le spouleur est un service Windows NT qui définit des objets privés, qui doivent être sécurisés, par exemple des imprimantes. Cette fonctionnalité n’est pas gérée par le jeu d’outils standard et nécessite donc une pièce jointe pour gérer la configuration et l’analyse des objets d’imprimante. La configuration des paramètres de sécurité généraux, tels que la stratégie d’appel de service, est toujours gérée par le jeu d’outils de configuration de la sécurité.

Les pièces jointes du service de sécurité étendent les fonctionnalités de l’outil de configuration de la sécurité défini pour prendre en charge les configurations spécifiques au service.

Une pièce jointe comporte deux composants :

-   Extension de composant logiciel enfichable MMC qui implémente l’interface utilisateur de la pièce jointe.
-   Moteur d’attachement qui traite les tâches d’analyse et de configuration de la sécurité spécifiques au service.

L’extension du composant logiciel enfichable pièce jointe est hébergée par les composants logiciels enfichables de configuration de sécurité. Il s’agit de composants logiciels enfichables MMC qui fournissent à l’utilisateur des interfaces permettant de configurer et d’analyser les paramètres de sécurité généraux d’un service. Les paramètres spécifiques au service sont configurés à l’aide de l’extension du composant logiciel enfichable pièce jointe.

Lorsque l’utilisateur modifie un paramètre de configuration, les composants logiciels enfichables de configuration de la sécurité stockent les nouvelles informations et transmettent la demande au moteur de configuration de sécurité. Le moteur traite la demande et définit le service sur la nouvelle configuration. Si la requête affecte un paramètre de sécurité standard, elle est gérée par le moteur. Si la demande est spécifique au service, le moteur appelle le moteur d’attachement approprié pour gérer la demande.

L’illustration suivante montre comment le moteur de pièce jointe et l’extension du composant logiciel enfichable fonctionnent dans le cadre du jeu d’outils de configuration de la sécurité.

![moteur de pièce jointe et composants logiciels enfichables](images/model1a.png)

Pour plus d’informations sur l’utilisation du jeu d’outils de configuration de sécurité Microsoft, recherchez Configuration de la sécurité à l’aide de votre moteur de recherche préféré.

 

 



