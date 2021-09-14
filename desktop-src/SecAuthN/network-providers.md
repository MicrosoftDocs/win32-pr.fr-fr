---
description: Un fournisseur de réseau est une DLL qui prend en charge un protocole réseau spécifique.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Fournisseurs de réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e3cc231f461d48e7ce71d908cb92f6cd06eabd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123370"
---
# <a name="network-providers"></a>Fournisseurs de réseau

Un fournisseur de réseau est une DLL qui prend en charge un protocole réseau spécifique. Il implémente également l' [API du fournisseur réseau](network-provider-api.md). cela lui permet d’interagir avec le système d’exploitation Windows pour recevoir des demandes réseau standard, telles que des demandes de connexion ou de déconnexion. Pour gérer ces requêtes, le fournisseur réseau appelle ensuite l’API spécifique au réseau qui est appropriée au protocole réseau pris en charge par le fournisseur réseau. En d’autres termes, le fournisseur réseau encapsule les fonctionnalités spécifiques au réseau dans une DLL, qui expose une interface standard pour Windows.

à l’aide de fournisseurs de réseau, Windows peut prendre en charge de nombreux types de protocoles réseau sans avoir à connaître les détails spécifiques au réseau de chaque réseau. Cela est essentiel, car les nouveaux protocoles réseau sont en cours de développement en permanence. Avec les fournisseurs de réseau, la prise en charge d’un nouveau protocole nécessite simplement la création et l’installation d’un nouveau fournisseur réseau.

Pour plus d’informations sur les structures et les fonctions des fournisseurs de réseau, consultez les rubriques suivantes :

-   [Fonctions du fournisseur de réseau](authentication-functions.md)
-   [Structures de fournisseur réseau](authentication-structures.md)

 

 



