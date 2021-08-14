---
description: Winlogon, GINA et les fournisseurs de réseau sont les parties du modèle d’ouverture de session interactive.
ms.assetid: d049d83f-b962-4c47-a79a-da556831e319
title: Winlogon et GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cc39b905d6a49eb84ccab164f99481561133e6cdd9ea40cfd0b1067315569a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915068"
---
# <a name="winlogon-and-gina"></a>Winlogon et GINA

[*Winlogon*](../secgloss/w-gly.md), [*Gina*](../secgloss/g-gly.md)et les fournisseurs de réseau sont les parties du modèle d’ouverture de session interactive. La procédure d’ouverture de session interactive est normalement contrôlée par Winlogon, MSGina.dll et les fournisseurs de réseau. Pour modifier la procédure d’ouverture de session interactive, MSGina.dll peut être remplacé par une DLL GINA personnalisée.

pour travailler avec Winlogon, les fournisseurs GINA et les fournisseurs de réseau, vous devez avoir une connaissance ferme de l’architecture de sécurité Windows, en particulier en ce qui concerne les [*jetons*](../secgloss/a-gly.md), les [*packages d’authentification*](../secgloss/a-gly.md)et les aspects connexes.

> [!Note]  
> les dll GINA sont ignorées dans Windows Vista.

 

Pour plus d’informations sur des fonctions et des structures spécifiques, consultez [référence d’authentification](authentication-reference.md). Cette section de référence comprend des descriptions des fonctions qu’une DLL GINA doit implémenter, les fonctions de prise en charge de Winlogon que la DLL GINA peut appeler et les structures de données utilisées pour passer des informations entre Winlogon et GINA.

Vous trouverez un exemple de code GINA dans les exemples de sécurité du kit de développement logiciel (SDK) de la plateforme. Les exemples contiennent du code C pour implémenter un stub GINA et un hook GINA. Pour plus d’informations sur le développement de DLL GINA personnalisées, envoyez un message électronique à : ginareqs@microsoft.com .

pour plus d’informations sur le modèle d’authentification pris en charge par Windows et pour plus d’informations sur les services lsa ( [*Local Security Authority*](../secgloss/l-gly.md) ) et les interfaces de [*package d’authentification*](../secgloss/a-gly.md) , consultez la page [authentification lsa](lsa-authentication.md).

Pour plus d’informations sur les aspects de l’autorité de sécurité locale liés à l’administration de la stratégie de sécurité, qui comprend les relations d’approbation avec d’autres ordinateurs et domaines, l’attribution de privilèges, le contrôle de génération d’audit, l’accessibilité du système et d’autres rubriques similaires, consultez [LSA Policy](../secmgmt/lsa-policy.md).

Pour plus d’informations sur Winlogon et GINA, consultez les rubriques suivantes.



| Rubrique                                                                              | Description                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Winlogon](winlogon.md)                                                           | Winlogon fournit un ensemble de fonctions de prise en charge pour la DLL GINA.<br/>                                                                                                                                                                 |
| [GINA](gina.md)                                                                   | Une DLL GINA fournit une identification utilisateur personnalisable et des procédures d’authentification.<br/>                                                                                                                                            |
| [Fonctions GINA des services Terminal Server](terminal-services-gina-functions.md)           | Lorsque les services Terminal Server sont activés, GINA doit appeler les fonctions de prise en charge de Winlogon pour effectuer plusieurs tâches.<br/>                                                                                                                   |
| [Interaction avec les fournisseurs de réseau](interaction-with-network-providers.md)       | Vous pouvez configurer un système pour qu’il prenne en charge zéro, un ou plusieurs fournisseurs réseau.<br/>                                                                                                                                                          |
| [Responsabilités et fonctionnalités](responsibilities-and-features.md)                 | Chaque partie du processus d’ouverture de session interactive a un ensemble de responsabilités.<br/>                                                                                                                                                      |
| [Interaction entre Winlogon et GINA](interaction-between-winlogon-and-gina.md) | L’état de Winlogon détermine la fonction GINA qui est appelée pour traiter un événement de séquence de touches de [*sécurité*](../secgloss/s-gly.md) (SAS) donné.<br/> |
| [Packages de notification Winlogon](winlogon-notification-packages.md)               | Vous pouvez implémenter un package de notification pour surveiller les événements Winlogon et y répondre.<br/>                                                                                                                                            |



 

 

 
