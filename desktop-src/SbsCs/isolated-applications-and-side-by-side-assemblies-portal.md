---
description: Gérer le partage d’assemblys et le contrôle de version des DLL dans le magasin d’assemblys côte à côte des systèmes à partir de programmes. Écrivez des manifestes d’assembly et des applications auto-descriptives pour le partage d’assembly et la redirection des dll.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Applications isolées et assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237965"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Applications isolées et assemblys côte à côte

## <a name="purpose"></a>Objectif

les applications isolées et les assemblys côte à côte sont une solution Microsoft Windows qui réduit les conflits de contrôle de version dans les Applications clientes Windows. avec Windows, les développeurs d’applications peuvent créer des applications isolées qui sont entièrement explicites et non affectées par des modifications apportées au registre, à d’autres applications ou à d’autres versions d’assemblys s’exécutant sur le système. Les créateurs d’applications et les administrateurs peuvent utiliser des manifestes pour gérer le partage d’assemblys côte à côte après le déploiement, au niveau global ou par application. Les clients bénéficient d’applications isolées qui sont plus stables et mises à jour de manière plus fiable.

## <a name="where-applicable"></a>Le cas échéant

Les applications isolées et le partage d’assembly côte à côte peuvent être utilisés pour développer des applications qui partagent en toute sécurité des assemblys de système d’exploitation. Les développeurs peuvent utiliser cette technologie pour corriger les conflits de contrôle de version des DLL causés par une version incompatible d’un assembly partagé.

Si votre application doit toujours obtenir la version d’un composant que vous avez testé, il est possible d’isoler votre application afin qu’elle s’exécute toujours avec la version testée du composant sur l’ordinateur de l’utilisateur.

Les applications isolées et les assemblys côte à côte sont destinés au développement d’applications de style bureau.

## <a name="developer-audience"></a>Développeurs concernés

Cette documentation est destinée principalement aux développeurs de logiciels, aux développeurs d’applications et aux administrateurs réseau :

-   Les développeurs de logiciels qui souhaitent créer des applications isolées qui utiliseront les assemblys côte à côte mis à disposition par Microsoft et d’autres éditeurs d’assembly côte à côte.
-   Les développeurs d’applications qui souhaitent créer leurs propres assemblys côte à côte pour isoler leurs applications.
-   Administrateurs réseau qui souhaitent obtenir des informations supplémentaires sur les applications isolées.

En tant que référence principale pour le partage d’assembly côte à côte et les applications isolées, cette documentation fournit des informations générales sur la création de manifestes et d’assemblys côte à côte, l’installation d’applications isolées et d’assemblys côte à côte, et l’utilisation de l’API de contexte d’activation.

## <a name="run-time-requirements"></a>Conditions d’exécution

Windows le serveur 2003 et versions ultérieures ou Windows XP et versions ultérieures sont requis pour utiliser des manifestes et des assemblys côte à côte afin d’isoler les applications et d’utiliser l’API de contexte d’Activation.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                         | Description                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Référence](side-by-side-assemblies-reference.md)<br/> | Documentation des applications isolées et des assemblys côte à côte.<br/> |



 

 

 




