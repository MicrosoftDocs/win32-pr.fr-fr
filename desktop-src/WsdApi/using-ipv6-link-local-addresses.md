---
description: L’adressage local de la liaison IPv6 dans les messages SOAP fournit un défi unique, car les adresses IPv6 à liaison locale nécessitent un ID d’étendue explicite, mais l’ID d’étendue n’a que la signification de l’ordinateur local.
ms.assetid: 63495335-e447-4564-b669-0896c7aac63f
title: Utilisation d’adresses lien-local IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c1719e4e6d374e7afd859b80cd1bc14c4c841cb7dceee149f14d0acb777f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897159"
---
# <a name="using-ipv6-link-local-addresses"></a>Utilisation d’adresses lien-local IPv6

L’adressage local de la liaison IPv6 dans les messages SOAP fournit un défi unique, car les adresses IPv6 à liaison locale nécessitent un ID d’étendue explicite, mais l’ID d’étendue n’a que la signification de l’ordinateur local. Toutes les implémentations de clients et d’appareils doivent supprimer l’ID d’étendue avant d’envoyer une adresse lien-local IPv6 dans un message SOAP. En outre, lorsqu’une adresse de lien local IPv6 est reçue dans un message, l’interface sur laquelle le message a été reçu doit être connue afin que l’adresse locale de lien complète avec l’ID d’étendue puisse être reconstruite.

 

 



