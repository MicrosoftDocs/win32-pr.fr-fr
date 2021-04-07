---
title: Protection des objets et des attributs
description: Une liste de contrôle d’accès (ACL) protège tous les objets de Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protection des objets et des attributs
- sécurité AD, objet et attribut protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671262"
---
# <a name="object-and-attribute-protection"></a>Protection des objets et des attributs

Une liste de contrôle d’accès (ACL) protège tous les objets de Active Directory Domain Services. Les listes de contrôle d’accès déterminent qui peut afficher l’objet, les attributs qu’ils peuvent lire et les actions que chaque utilisateur peut effectuer sur l’objet. L’existence d’un objet ou d’un attribut n’est jamais révélée à un utilisateur non autorisé.

Une liste ACL est une liste d’entrées de contrôle d’accès (ACE) stockées avec l’objet qu’elle protège. Dans Windows NT et Windows 2000, une liste de contrôle d’accès est stockée sous forme de valeur binaire, appelée descripteur de sécurité. Chaque ACE contient un identificateur de sécurité (SID), qui identifie le principal (utilisateur ou groupe) auquel l’entrée du contrôle d’accès s’applique, ainsi que les données sur le type d’accès accordé ou refusé par l’ACE.

Les listes de contrôle d’accès pour les objets d’annuaire contiennent des entrées de contrôle d’accès qui s’appliquent à l’objet dans son ensemble et aux ACE qui s’appliquent aux attributs individuels de l’objet. Cela permet à un administrateur de contrôler non seulement quels utilisateurs peuvent voir un objet, mais également quelles propriétés ils peuvent afficher. Par exemple, tous les utilisateurs peuvent se voir accorder l’accès en lecture aux attributs de messagerie et de numéro de téléphone de tous les autres utilisateurs, mais les propriétés de sécurité des utilisateurs peuvent être refusées à tous les membres du groupe administrateurs de sécurité spéciaux. Les utilisateurs individuels peuvent bénéficier d’un accès en écriture à des attributs personnels, tels que les adresses de téléphone et de publipostage sur leurs propres objets utilisateur.

 

 




