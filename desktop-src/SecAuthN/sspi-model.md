---
description: L’interface SSPI (Security Support Provider Interface) permet à une application d’utiliser différents modèles de sécurité disponibles sur un ordinateur ou un réseau sans modifier l’interface du système de sécurité.
ms.assetid: 86ffc8c0-727d-437f-ac36-10df6563b0be
title: Modèle SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cf79185693f40694d1bc6de319376b037fb853
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096366"
---
# <a name="sspi-model"></a>Modèle SSPI

L’interface SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) permet à une application d’utiliser différents modèles de sécurité disponibles sur un ordinateur ou un réseau sans modifier l’interface du système de sécurité. SSPI n’établit pas les [*informations d’identification*](../secgloss/c-gly.md) de connexion, car il s’agit généralement d’une opération privilégiée gérée par le système d’exploitation.

Un [*fournisseur SSP (Security Support Provider*](../secgloss/s-gly.md) ) est contenu dans une [*bibliothèque de liens dynamiques*](../secgloss/d-gly.md) (dll) qui implémente l’interface SSPI en mettant un ou plusieurs [*packages de sécurité*](../secgloss/s-gly.md) à la disposition des applications. Chaque package de sécurité fournit des mappages entre les appels de fonction SSPI d’une application et les fonctions d’un modèle de sécurité réel. Les packages de sécurité prennent en charge des [*protocoles de sécurité*](../secgloss/s-gly.md) tels que l’authentification [*Kerberos*](../secgloss/k-gly.md) et le gestionnaire LAN.

L’interface SSPI est disponible en mode noyau et en mode utilisateur. pour utiliser la fonctionnalité SSPI en mode noyau, vous devez installer le Windows DDK du système de fichiers installable. Le modèle appelant reste le même, mais les considérations en mode noyau sont indiquées sur les pages de référence de fonction. Pour plus d’informations, consultez [fonctions SSPI](authentication-functions.md).

 

 
