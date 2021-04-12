---
title: Héritage et délégation de l’administration
description: Décrit AD DS la prise en charge de l’héritage des autorisations dans l’arborescence d’objets, ainsi que l’héritage spécifique aux objets.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- héritage et délégation d’administration Active Directory
- Active Directory Active Directory, héritage des autorisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190758"
---
# <a name="inheritance-and-delegation-of-administration"></a>Héritage et délégation de l’administration

Active Directory Domain Services prend en charge l’héritage des autorisations dans l’arborescence des objets pour permettre l’exécution des tâches d’administration à des niveaux supérieurs de l’arborescence. Cela permet aux administrateurs de définir des autorisations pouvant être héritées sur des objets proches de la racine, tels que des unités de domaine et d’organisation, et de faire en sorte que ces autorisations soient distribuées à différents objets dans l’arborescence.

L’héritage peut être défini sur une base par ACE. Le tableau suivant répertorie les indicateurs qui peuvent être spécifiés dans le **AceFlags** pour contrôler l’héritage de l’entrée du contrôle d’accès.



| Indicateur                                                     | Description                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ACE ACEFLAG \_ hériter des publicités \_**<br/>                | Entraîne l’héritage de l’entrée du contrôle d’accès dans l’arborescence.<br/>                                                                                     |
| **AD \_ ACEFLAG \_ non \_ propager \_ hériter \_ ACE**<br/> | Fait en sorte que l’entrée du contrôle d’accès soit héritée d’un seul niveau dans l’arborescence.<br/>                                                                      |
| **\_ACEFLAG ADS \_ hériter \_ uniquement \_ ACE**<br/>          | Fait en sorte que l’entrée du contrôle d’accès soit ignorée sur l’objet sur lequel elle est spécifiée, elle ne peut être héritée et être effective où elle a été héritée.<br/> |



 

Outre la définition de l’héritage, Active Directory Domain Services prend en charge l’héritage spécifique aux objets. Cela permet aux ACE pouvant être héritées d’être héritées de l’arborescence, mais uniquement applicables à un type spécifique d’objet. Cela est extrêmement utile pour déléguer l’administration. Par exemple, il peut être utilisé pour définir une entrée de contrôle d’accès (ACE) héritable spécifique à un objet au niveau d’une unité d’organisation qui permet à un groupe d’avoir un contrôle total sur tous les objets utilisateur de l’unité d’organisation, mais rien d’autre. Ainsi, la gestion des utilisateurs dans cette unité d’organisation est déléguée aux utilisateurs de ce groupe.

### <a name="delegating-service-administration-with-security-groups"></a>Délégation de l’administration de service à des groupes de sécurité

Utilisez des groupes de sécurité pour définir et déléguer des rôles d’administration associés à votre serveur d’applications. Par exemple, votre service peut être associé à un groupe d’administrateurs MyService. Les utilisateurs identifiés comme administrateurs MyService seront ajoutés au groupe d’administrateurs MyService. Le programme d’installation de MyService peut définir des listes de contrôle d’accès sur l’annuaire pour permettre aux administrateurs MyService d’avoir des autorisations suffisantes pour lire/écrire des attributs liés à MyService ou créer des objets spécifiques au fichier MyService, par exemple.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Rôles dans des groupes de sécurité pour les ordinateurs qui exécutent votre service

Utilisez des groupes de sécurité pour définir l’ensemble des ordinateurs qui sont autorisés à accéder aux objets de votre service dans l’annuaire. Par exemple, votre service peut être associé à un groupe de serveurs MyService. Tous les ordinateurs qui exécutent le serveur MyService sont ajoutés au groupe de serveurs MyService et ce groupe peut ensuite accéder aux parties du répertoire où les serveurs MyService doivent lire/écrire des données. Le programme d’installation de MyService peut définir des listes de contrôle d’accès sur l’annuaire pour permettre aux serveurs MyService d’accéder à des autorisations suffisantes pour lire/écrire des attributs liés à MyService ou créer des objets spécifiques au fichier MyService, par exemple.

 

 





