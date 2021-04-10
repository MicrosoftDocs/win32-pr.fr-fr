---
title: Contrôle de l’accès aux objets et à leurs propriétés
description: Pour contrôler l’accès aux objets d’application, utilisez le descripteur de sécurité de l’objet, et plus précisément, avec la liste de contrôle d’accès discrétionnaire (DACL) et sa liste d’entrées de contrôle d’accès (ACE).
ms.assetid: cfcb0998-4400-45cd-bbee-415d43b96a99
ms.tgt_platform: multiple
keywords:
- objet AD, contrôle de l’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4534f383fa3747e0a53b402098f5a8338812c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190709"
---
# <a name="controlling-access-to-objects-and-their-properties"></a>Contrôle de l’accès aux objets et à leurs propriétés

Pour contrôler l’accès aux objets d’application, utilisez le descripteur de sécurité de l’objet, et plus précisément, avec la liste de contrôle d’accès discrétionnaire (DACL) et sa liste d’entrées de contrôle d’accès (ACE).

Lorsqu’un objet est créé, il reçoit un descripteur de sécurité. Pour plus d’informations et pour obtenir une description des règles que le système utilise pour créer la liste DACL pour un nouvel objet, voir [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](how-security-descriptors-are-set-on-new-directory-objects.md). Ces règles révèlent que vous pouvez :

-   Créez un nouveau descripteur de sécurité et attachez-le à l’objet au moment de la création. Pour plus d’informations, consultez [création d’un descripteur de sécurité pour un nouvel objet d’annuaire](creating-a-security-descriptor-for-a-new-directory-object.md).
-   Appliquez une entrée du contrôle d’accès héritable, à tout moment dans la hiérarchie de répertoires, de telle sorte qu’une entrée du contrôle d’accès est héritée par les objets de l’arborescence. Un objet peut hériter d’une entrée du contrôle d’accès de son conteneur parent. Pour plus d’informations, consultez [héritage et délégation de l’administration](inheritance-and-delegation-of-administration.md).
-   Spécifiez une entrée du contrôle d’accès dans la liste DACL par défaut dans le schéma, si vous disposez des droits d’accès nécessaires. Chaque définition de classe d’objet dans le schéma comprend un descripteur de sécurité par défaut qui peut avoir une liste DACL par défaut. Pour plus d’informations, consultez [descripteur de sécurité par défaut](default-security-descriptor.md).

En outre, la liste DACL d’un objet existant peut être modifiée. Vous pouvez :

-   Remplacez la liste DACL par une nouvelle.
-   Lisez la liste DACL existante, modifiez-la et appliquez la liste DACL modifiée. Pour plus d’informations, consultez [définition des droits d’accès sur un objet](setting-access-rights-on-an-object.md).

La liste suivante décrit la fonction la plus importante d’une entrée du contrôle d’accès dans Active Directory Domain Services. Avec une entrée de contrôle d’accès, vous pouvez :

-   Contrôler qui peut effectuer des opérations spécifiques sur un objet.
-   Contrôler qui a accès à une propriété spécifique, ou à un ensemble de propriétés, d’un objet.
-   Contrôler qui peut créer des objets enfants dans un conteneur, y compris qui peut créer un type spécifique d’objet enfant.
-   Définir des droits d’accès au contrôle privé pour un type d’objet et contrôler qui peut effectuer les opérations protégées par les droits privés.
-   Appliquez une entrée du contrôle d’accès à un objet conteneur à la racine d’une sous-arborescence de répertoires, de façon à ce que les protections puissent être héritées automatiquement par tous les objets enfants dans l’arborescence.
-   Applique une entrée du contrôle d’accès qui est héritée automatiquement par un type spécifique d’objet enfant dans une sous-arborescence.
-   Créer une entrée du contrôle d’accès qui accorde des droits à un groupe de sécurité plutôt qu’à un seul utilisateur.
-   Appliquez une entrée du contrôle d’accès pour stratégie de groupe objets afin de contrôler les comptes et les ordinateurs affectés par la stratégie.

 

 




