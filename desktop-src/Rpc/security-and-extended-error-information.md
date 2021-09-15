---
title: Sécurité et informations d’erreur étendues
description: Les informations d’erreur étendues offrent des données très utiles lors de la résolution d’un problème RPC, mais ces données sont souvent considérées comme confidentielles par les organisations soucieuses de la sécurité.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413556"
---
# <a name="security-and-extended-error-information"></a>Sécurité et informations d’erreur étendues

Les informations d’erreur étendues offrent des données très utiles lors de la résolution d’un problème RPC, mais ces données sont souvent considérées comme confidentielles par les organisations soucieuses de la sécurité. En considération de tels problèmes de sécurité, les informations d’erreur étendues sont désactivées par défaut.

Les informations d’erreur étendues sont toujours générées lorsque les informations d’erreur étendues sont désactivées, mais les informations ne sont jamais transmises au-delà des limites des processus ou des ordinateurs. Cette approche permet d’utiliser les informations d’erreur par les outils qui ont accès à l’espace d’adressage du processus, tels que les débogueurs. Lorsqu’elles sont activées, les informations d’erreur étendues sont générées et peuvent être envoyées entre les limites du processus et de l’ordinateur. Actuellement, les informations d’erreur étendues sont utilisées pour les séquences de protocole orientées connexion et les appels RPC locaux (LRPC). Elle est partiellement implémentée pour les datagrammes.

 

 




