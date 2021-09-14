---
description: Les modules de sortie reçoivent des notifications du moteur de serveur lorsque des opérations telles que l’émission d’un certificat se produisent.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Modules de sortie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc0668717c4a7a690cce8a03ff8c140333347b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123162"
---
# <a name="exit-modules"></a>Modules de sortie

Les modules de sortie reçoivent des notifications du moteur de serveur lorsque des opérations telles que l’émission d’un certificat se produisent. Un module de sortie est implémenté en tant que [*bibliothèque de liens dynamiques*](../secgloss/d-gly.md) (dll). Une opération courante pour un module de sortie consiste à publier un certificat terminé à un emplacement spécifié (le module de sortie de l’autorité de certification d’entreprise par défaut, par exemple, publie des certificats utilisateur et des [*listes de révocation de certificats*](../secgloss/c-gly.md) (CRL) sur le Active Directory). Un module de sortie peut utiliser l’interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) pour communiquer avec les services de certificats. Les services de certificats communiquent avec un module de sortie par le biais d’appels COM directs ou, si le module ne prend pas en charge les appels COM directs, par le biais de l’automatisation.

Un module de sortie peut afficher les propriétés et les extensions de certificat existantes, et il peut également afficher les propriétés et les attributs de la requête. Toutefois, un module de sortie ne peut pas modifier les propriétés.

Les services de certificats fournissent un module de sortie par défaut, mais vous pouvez également créer des modules de sortie personnalisés pour répondre à des besoins spécifiques. Toutefois, avant d’écrire un module de sortie personnalisé, envisagez d’utiliser le module de sortie par défaut. En outre, pour une autorité de certification d’entreprise, le module de sortie par défaut doit toujours être utilisé, même si vous pouvez ajouter des modules de sortie personnalisés supplémentaires. Pour plus d’informations, consultez [écriture de modules de sortie personnalisés](writing-custom-exit-modules.md).

 

 
