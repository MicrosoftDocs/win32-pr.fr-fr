---
description: Lorsqu’un objet TrustedDomain est créé, une protection standard lui est affectée.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Protection des objets TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515628"
---
# <a name="trusteddomain-object-protection"></a>Protection des objets TrustedDomain

Lorsqu’un objet [**trustedDomain**](trusteddomain-object.md) est créé, une protection standard lui est assignée comme suit :

-   L’accès en exécution générique est accordé au groupe WORLD local \_ .
-   Le groupe local d’administration local reçoit un \_ \_ accès en suppression, en lecture générique, en \_ écriture générique et en \_ Exécution générique.
-   Le \_ groupe local administrateur local est affecté en tant que propriétaire et groupe principal de l’objet.

 

 



