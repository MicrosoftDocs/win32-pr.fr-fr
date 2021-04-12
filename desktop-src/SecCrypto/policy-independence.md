---
description: Les certificats sont accordés conformément aux stratégies qui définissent les critères que les demandeurs doivent remplir pour recevoir un certificat.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Indépendance de la stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319590"
---
# <a name="policy-independence"></a>Indépendance de la stratégie

Les certificats sont accordés conformément aux stratégies qui définissent les critères que les demandeurs doivent remplir pour recevoir un certificat. Par exemple, une stratégie peut être d’accorder des certificats commerciaux uniquement si les candidats présentent leur identification en personne. Une autre stratégie peut accorder des [*informations d’identification*](../secgloss/c-gly.md) en fonction des demandes par courrier électronique. Une agence qui émet des cartes de crédit peut choisir de consulter une base de données et de faire des demandes de téléphone avant d’émettre une carte.

Les stratégies sont implémentées dans des modules de stratégie écrits en C++, C ou Visual Basic. Les fonctions des services de certificats sont isolées des modifications apportées à la stratégie qu’une Agence peut implémenter. Les modifications apportées à la stratégie peuvent être entièrement implémentées dans le code du module de stratégie serveur. Une [*autorité de certification*](../secgloss/c-gly.md) d’entreprise (ca) doit utiliser uniquement le module de stratégie d’entreprise fourni par Microsoft.

 

 
