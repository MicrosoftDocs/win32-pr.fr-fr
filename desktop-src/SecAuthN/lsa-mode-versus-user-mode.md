---
description: Lorsqu’un package de sécurité SSP/AP fonctionne comme un package d’authentification, il est chargé dans l’espace de processus de l’autorité de sécurité locale (LSA) et est dit en mode LSA.
ms.assetid: ff4e61be-dbaa-4cfa-8c72-43e99fe1c3cb
title: Mode LSA et mode utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa965cd66f43548243c1e62329e6d9d337a2a0123344a8cb9f10915846a765f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922078"
---
# <a name="lsa-mode-vs-user-mode"></a>Mode LSA et mode utilisateur

Lorsqu’un [*package de sécurité*](../secgloss/s-gly.md) SSP/AP fonctionne comme un [*package d’authentification*](../secgloss/a-gly.md), il est chargé dans l’espace de processus de l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) et est dit en mode LSA. Les applications de connexion accèdent à la fonctionnalité de package d’authentification à l’aide des [fonctions de connexion LSA](authentication-functions.md). Les développeurs peuvent utiliser les fonctions de prise en charge LSA disponibles uniquement pour les packages de sécurité en mode LSA afin d’implémenter des packages d’authentification plus sophistiqués que ceux précédemment pris en charge.

Lorsqu’un [*package de sécurité*](../secgloss/s-gly.md) fournit des services de sécurité à une application client/serveur, il est chargé dans les processus client et serveur et est dit en mode utilisateur. Les applications client/serveur accèdent aux services de support de sécurité du package de sécurité à l’aide de l’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) de Microsoft.

La prise en charge LSA pour le fournisseur de services partagés/APs comprend des fonctions que les instances du mode LSA et du mode utilisateur d’un package de sécurité peuvent utiliser pour communiquer. En outre, l’instance de mode utilisateur d’un package de sécurité peut déléguer des demandes d’informations sélectionnées à l’instance du package en mode LSA.

Pour plus d’informations sur la façon dont les packages de sécurité sont initialisés pour chaque mode, consultez [initialisation du mode LSA](lsa-mode-initialization.md) et [initialisation du mode utilisateur](user-mode-initialization.md).

 

 
