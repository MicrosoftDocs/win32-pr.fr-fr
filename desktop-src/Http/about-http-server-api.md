---
title: À propos de l’API du serveur HTTP
description: L’API du serveur HTTP fournit aux développeurs une interface de bas niveau pour le côté serveur de la fonctionnalité HTTP, comme défini dans la norme RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API serveur HTTP, vue d’ensemble
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55883fa75b366a2f5c5ef434f1eef3a95651440738735b025cfe5ef1b0534106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015007"
---
# <a name="about-http-server-api"></a>À propos de l’API du serveur HTTP

L’API du serveur HTTP fournit aux développeurs une interface de bas niveau pour le côté serveur de la fonctionnalité HTTP, comme défini dans la [norme RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). L’API permet à une application de recevoir des requêtes HTTP dirigées vers des URL et d’envoyer des réponses HTTP. pour l’envoi de réponses dynamiques, les interfaces ISAPI ou ASP.NET sont recommandées.

L’API du serveur HTTP permet à plusieurs applications de coexister sur un système, en partageant le même port TCP (par exemple, le port 80 pour HTTP ou le port 443 pour HTTPs) et en desservant différentes parties de l’espace de noms d’URL.

l’api du serveur HTTP nécessite une connaissance du langage de programmation C et une connaissance de la programmation de l’api Windows. les Applications qui n’ont pas besoin d’un accès de bas niveau à HTTP doivent utiliser les classes ISAPI IIS ou .NET Framework pour les solutions basées sur http.

 

 




