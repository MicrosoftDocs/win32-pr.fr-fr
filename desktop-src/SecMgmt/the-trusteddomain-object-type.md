---
description: Les systèmes Windows peuvent avoir plusieurs instances du type d’objet TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Type d’objet TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750860"
---
# <a name="the-trusteddomain-object-type"></a>Type d’objet TrustedDomain

Les systèmes Windows peuvent avoir plusieurs instances du type d’objet [**trustedDomain**](trusteddomain-object.md) . Les objets **trustedDomain** ont deux champs qui doivent être uniques parmi tous les objets **trustedDomain** :

-   Nom du [ **trustedDomain**](trusteddomain-object.md)
-   [*Identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du [**trustedDomain**](trusteddomain-object.md).

Une tentative de création d’un nouvel objet **trustedDomain** avec un nom ou un SID qui est déjà utilisé par un autre objet **trustedDomain** est rejetée.

 

 
