---
description: les systèmes basés sur Windows peuvent avoir plusieurs instances du type d’objet TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Type d’objet TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab860f9192e48433242251578a20a45bf294164c0bffff8b6f00562a1442e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004837"
---
# <a name="the-trusteddomain-object-type"></a>Type d’objet TrustedDomain

les systèmes basés sur Windows peuvent avoir plusieurs instances du type d’objet [**TrustedDomain**](trusteddomain-object.md) . Les objets **trustedDomain** ont deux champs qui doivent être uniques parmi tous les objets **trustedDomain** :

-   Nom du [ **trustedDomain**](trusteddomain-object.md)
-   [*Identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du [**trustedDomain**](trusteddomain-object.md).

Une tentative de création d’un nouvel objet **trustedDomain** avec un nom ou un SID qui est déjà utilisé par un autre objet **trustedDomain** est rejetée.

 

 
