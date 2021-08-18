---
description: Lorsqu’un objet TrustedDomain est créé, une protection standard lui est affectée.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Protection des objets TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e34eac9b9e3a021db7580803cec6c99f6489d01c9499b28251cb262b721fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004797"
---
# <a name="trusteddomain-object-protection"></a>Protection des objets TrustedDomain

Lorsqu’un objet [**trustedDomain**](trusteddomain-object.md) est créé, une protection standard lui est assignée comme suit :

-   L’accès en exécution générique est accordé au groupe WORLD local \_ .
-   Le groupe local d’administration local reçoit un \_ \_ accès en suppression, en lecture générique, en \_ écriture générique et en \_ Exécution générique.
-   Le \_ groupe local administrateur local est affecté en tant que propriétaire et groupe principal de l’objet.

 

 



