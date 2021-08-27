---
description: Explique comment créer un package de sécurité personnalisé.
ms.assetid: af8b9796-77e7-43c1-8f8e-acee01a62bf9
title: Création de packages de sécurité personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88093ba7faed1ac2287c2a54391015984e83d4ad3878a60453978a9924706f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008847"
---
# <a name="creating-custom-security-packages"></a>Création de packages de sécurité personnalisés

## <a name="ssp-security-packages"></a>Packages de sécurité SSP

Si un package de sécurité SSP (Security Support Provider) personnalisé est utilisé exclusivement pour la prise en charge de la sécurité client/serveur, il peut implémenter l' [interface du fournisseur de support de sécurité](sspi.md)Microsoft.

L’exemple SampSSP fourni avec le kit de développement logiciel (SDK) de plateforme contient un exemple d’implémentation de package de sécurité SSP.

## <a name="sspap-security-packages"></a>Packages de sécurité SSP/AP

Les [](/windows/desktop/SecGloss/s-gly) / [*packages d’authentification*](/windows/desktop/SecGloss/a-gly) du fournisseur de support de sécurité personnalisés (SSP/APS) contiennent des packages de sécurité qui fonctionnent comme des packages d’authentification (APS) et des fournisseurs de support de sécurité (SSP). Ces packages implémentent des API distinctes pour prendre en charge chaque rôle.

Étant donné qu’il fonctionne comme un point d’accès, un [*package de sécurité*](/windows/desktop/SecGloss/s-gly) SSP/AP personnalisé doit fournir des implémentations pour toutes les [fonctions implémentées par les packages d’authentification](authentication-functions.md).

Pour assurer la prise en charge de la sécurité intégrée, un package de sécurité SSP/AP personnalisé doit fournir des implémentations pour les [fonctions implémentées par le fournisseur SSP/APS](authentication-functions.md). Les [fonctions LSA appelées par SSP/APS](authentication-functions.md) décrivent les fonctions de prise en charge disponibles pour les développeurs SSP/AP qui souhaitent interagir avec l’autorité LSA.

Les packages de sécurité SSP/AP, afin d’être exécutés à la fois comme un point d’accès et un SSP, peuvent s’exécuter dans le cadre du système d’exploitation et dans le cadre d’une application utilisateur. Ces deux modes d’exécution sont appelés le mode LSA et le mode utilisateur, respectivement. Pour plus d’informations sur les packages de sécurité personnalisés en mode LSA, consultez [initialisation du mode LSA](lsa-mode-initialization.md). Pour plus d’informations sur le mode utilisateur, consultez [initialisation du mode utilisateur](user-mode-initialization.md).

Si un package de sécurité SSP/AP personnalisé offre des services pour les applications client/serveur, il doit fournir des implémentations pour les fonctions décrites dans [fonctions implémentées par SSP/APS en mode utilisateur](authentication-functions.md). Les [fonctions LSA appelées par SSP/APS en mode utilisateur](authentication-functions.md) décrivent les fonctions de prise en charge disponibles pour l’exécution d’un fournisseur SSP/AP dans un processus client ou serveur.

Pour plus d’informations sur l’inscription d’une DLL SSP/AP, consultez [inscription de dll SSP/AP](registering-ssp-ap-dlls.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Restrictions concernant l’inscription et l’installation d’un package de sécurité](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
