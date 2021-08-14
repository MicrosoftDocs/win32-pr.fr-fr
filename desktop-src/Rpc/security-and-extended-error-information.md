---
title: Sécurité et informations d’erreur étendues
description: Les informations d’erreur étendues offrent des données très utiles lors de la résolution d’un problème RPC, mais ces données sont souvent considérées comme confidentielles par les organisations soucieuses de la sécurité.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f246e86dee31ea5e755c45211e3bd949657cdf95c37bf6ab4de3706be09fdec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925686"
---
# <a name="security-and-extended-error-information"></a>Sécurité et informations d’erreur étendues

Les informations d’erreur étendues offrent des données très utiles lors de la résolution d’un problème RPC, mais ces données sont souvent considérées comme confidentielles par les organisations soucieuses de la sécurité. En considération de tels problèmes de sécurité, les informations d’erreur étendues sont désactivées par défaut.

Les informations d’erreur étendues sont toujours générées lorsque les informations d’erreur étendues sont désactivées, mais les informations ne sont jamais transmises au-delà des limites des processus ou des ordinateurs. Cette approche permet d’utiliser les informations d’erreur par les outils qui ont accès à l’espace d’adressage du processus, tels que les débogueurs. Lorsqu’elles sont activées, les informations d’erreur étendues sont générées et peuvent être envoyées entre les limites du processus et de l’ordinateur. Actuellement, les informations d’erreur étendues sont utilisées pour les séquences de protocole orientées connexion et les appels RPC locaux (LRPC). Elle est partiellement implémentée pour les datagrammes.

 

 




