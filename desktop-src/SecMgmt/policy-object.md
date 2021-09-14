---
description: L’objet de stratégie est utilisé pour contrôler l’accès à la base de données de l’autorité de sécurité locale (LSA) et contient des informations qui s’appliquent à l’ensemble du système ou qui établissent des valeurs par défaut pour le système.
ms.assetid: 4253c7fb-85f5-441d-90bf-492e802ad0f8
title: Objet de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcceec080d51f9c432ab2d63b8eeb26b3211cd28
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120773"
---
# <a name="policy-object"></a>Objet de stratégie

L’objet de **stratégie** est utilisé pour contrôler l’accès à la base de données de l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) et contient des informations qui s’appliquent à l’ensemble du système ou qui établissent des valeurs par défaut pour le système. Chaque système n’a qu’un seul objet de **stratégie** . Cet objet de **stratégie** est créé par l’autorité LSA au démarrage du système, et les applications ne peuvent pas la créer ou la détruire.

Les informations stockées dans un objet de **stratégie** incluent :

-   Quota de mémoire par défaut du système. Sauf indication contraire, chaque utilisateur ouvrant une session sur le système se verra attribuer ce quota de mémoire. Des quotas de mémoire spéciaux peuvent être attribués à des personnes ou à des membres de groupes ou groupes locaux par le biais d’un objet de [**compte**](account-object.md) .
-   Exigences d’audit de sécurité à l’ensemble du système.
-   Nom et SID du domaine du compte de ce système.
-   Informations sur le domaine principal de ce système. Ces informations incluent le nom et le SID du domaine principal, le nom du compte dans le domaine principal à utiliser pour les demandes d’authentification, le nom et les traductions de SID, et l’obtention des noms des contrôleurs de domaine au sein du domaine. Ces noms peuvent être obsolètes et ne doivent être pris en considération qu’en tant qu’indicateur. L’ordre de cette liste est supposé être significatif et sera conservé. Cela permet, par exemple, que le prénom de la liste représente le dernier contrôleur de domaine principal connu.
-   Informations indiquant si l’autorité de certification locale détient la copie principale des informations de stratégie ou un réplica. Seule une partie des informations de stratégie est répliquée ; le reste est établi en fonction du système.

Les champs **AccountDomain** et **PrimaryDomain** de l’objet de **stratégie** sont utilisés à des fins différentes selon le type de relations système et d’approbation :

-   Sur un système qui n’a pas de domaine principal, le champ **AccountDomain** contient le nom et le SID du domaine du compte local du système, qui est le même que le nom de l’ordinateur. Le champ **PrimaryDomain** contient le nom du groupe de travail dont cet ordinateur est membre. Les objets [**trustedDomain**](trusteddomain-object.md) sont ignorés à une exception près : il ne peut pas y avoir d’objet **trustedDomain** portant le même nom que le groupe de travail, car il s’affiche comme s’il s’agissait du domaine principal de l’ordinateur.
-   Sur un système qui a un domaine principal, le champ **AccountDomain** identifie le nom et le SID du domaine de compte local, comme précédemment. Toutefois, le champ **PrimaryDomain** contient le nom et le SID du domaine principal pour le système. En outre, il doit exister un objet [**trustedDomain**](trusteddomain-object.md) avec le nom et le SID identifiés dans le champ **PrimaryDomain** . Cet objet **trustedDomain** contient les informations relatives au compte et au serveur nécessaires pour établir un canal sécurisé vers un contrôleur de domaine dans le domaine principal. Tous les autres objets **trustedDomain** sont ignorés.
-   Sur les contrôleurs de domaine, le champ **AccountDomain** identifie le domaine de compte local pour le système. Toutefois, le nom du compte est attribué à l’utilisateur plutôt qu’à un nom connu. Étant donné que le domaine principal est le même que le domaine du compte, le champ **PrimaryDomain** doit contenir la même valeur que le champ **AccountDomain** . En outre, tous les objets [**trustedDomain**](trusteddomain-object.md) sont supposés être valides et représentent des relations d’approbation avec d’autres domaines. Si le système n’approuve aucun autre domaine, il ne doit pas y avoir d’objets **trustedDomain** .

 

 
