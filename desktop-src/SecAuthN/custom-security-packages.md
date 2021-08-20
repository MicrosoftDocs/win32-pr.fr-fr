---
description: Explique comment créer des packages de sécurité personnalisés à l’aide de l’API du package de sécurité personnalisé.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Packages de sécurité personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799edb3eb8e0551afe7d7f7bcdc54924228445d6ffb28cb4773af843b5c2d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008667"
---
# <a name="custom-security-packages"></a>Packages de sécurité personnalisés

pour implémenter de nouveaux protocoles de sécurité intégrés aux systèmes d’exploitation Windows Server et Windows, utilisez l’API du package de sécurité personnalisé et les fonctions de l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA).

L’API du package de sécurité personnalisé prend en charge le développement combiné des fournisseurs SSP ( [*Security Support Provider*](/windows/desktop/SecGloss/s-gly) ) personnalisés, qui fournissent des services [d’authentification non interactifs](noninteractive-authentication.md) et des échanges de messages sécurisés aux applications client/serveur, avec le développement de [*packages d’authentification*](/windows/desktop/SecGloss/a-gly)personnalisés, qui fournissent des services pour les applications qui effectuent une [authentification interactive](interactive-authentication.md). Lorsqu’ils sont combinés dans un package unique, ces services sont appelés fournisseur de support de sécurité/package d’authentification (SSP/AP).

Comme pour les packages de sécurité fournis par Microsoft, les utilisateurs du package de sécurité personnalisé accèdent aux services d’authentification interactive à l’aide des [fonctions de connexion LSA](authentication-functions.md). L’authentification non interactive et les services de protection des messages sont accessibles directement à l’aide de SSPI ( [Security Support Provider Interface](sspi.md) ).

Les packages de sécurité déployés dans SSP/APs sont entièrement intégrés à l’autorité LSA. À l’aide des fonctions de prise en charge LSA disponibles pour les packages de sécurité personnalisés, les développeurs peuvent implémenter des fonctionnalités de sécurité avancées telles que la création de jetons, la prise en charge des [*informations d’identification supplémentaires*](/windows/desktop/SecGloss/s-gly) et l’authentification directe. Pour obtenir la liste de ces fonctions de prise en charge, consultez [LSA, fonctions appelées par les packages d’authentification](authentication-functions.md). Pour plus d’informations sur la façon d’implémenter des packages de sécurité personnalisés, consultez [création de packages de sécurité personnalisés](creating-custom-security-packages.md).

Pour plus d’informations sur les packages de sécurité personnalisés, consultez les rubriques suivantes.



| Rubrique                                                                                                                                                 | Description                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/APs et SSP](ssp-aps-versus-ssps.md)<br/>                                                                                                | Informations sur la façon de déterminer si un package de sécurité doit être dans un SSP/AP ou un SSP.<br/> |
| [Mode LSA et mode utilisateur](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Détails sur la façon dont le mode LSA et le mode utilisateur sont différents.<br/>                                      |
| [Restrictions concernant l’inscription et l’installation d’un package de sécurité](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Actions par des packages de sécurité qui ne sont pas pris en charge dans Windows.<br/>                              |



 

 

