---
title: Exigences de sécurité pour la fonction de gestion de réseau
description: L’appel de certaines fonctions de gestion de réseau ne nécessite pas d’appartenance de groupe spéciale.
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508081"
---
# <a name="network-management-function-security-requirements"></a>Exigences de sécurité pour la fonction de gestion de réseau

L’appel de certaines fonctions de gestion de réseau ne nécessite pas d’appartenance de groupe spéciale. D’autres fonctions requièrent que les utilisateurs disposent d’un niveau de privilège spécifique pour s’exécuter avec succès. Le cas échéant, la section Notes sur la page de référence d’une fonction indique le niveau de privilège qu’un utilisateur doit avoir pour exécuter la fonction particulière.

Les exigences de sécurité qui s’appliquent à Active Directory contrôleurs de domaine peuvent différer de celles qui s’appliquent aux serveurs et aux stations de travail.

Pour plus d’informations et pour obtenir la liste des fonctions affectées, consultez les rubriques suivantes :

-   [Configuration requise pour les fonctions de gestion de réseau sur les contrôleurs de domaine Active Directory](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [Configuration requise pour les fonctions de gestion de réseau sur les serveurs et les stations de travail](requirements-for-network-management-functions-on-servers-and-workstations.md)

Pour plus d’informations sur le contrôle de l’accès aux objets sécurisables, consultez [Access Control](/windows/desktop/SecAuthZ/access-control), [privilèges](/windows/desktop/SecAuthZ/privileges)et [objets sécurisables](/windows/desktop/SecAuthZ/securable-objects).

Pour plus d’informations sur les descripteurs de sécurité spécifiques utilisés pendant les contrôles d’accès, consultez la page de référence des fonctions individuelles. Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

 

 