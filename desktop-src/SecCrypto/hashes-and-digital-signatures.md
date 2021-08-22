---
description: Avec les fonctions de hachage et de signature numérique, un utilisateur peut signer numériquement des données afin que n’importe quel autre utilisateur puisse vérifier que les données n’ont pas été modifiées depuis qu’il a été signé. L’identité de l’utilisateur qui a signé les données peut également être vérifiée.
ms.assetid: dbe70506-f0d9-4239-a3af-8494fd6d4149
title: Hachages et signatures numériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd6367217343a067bbdd0d5a4ad5e9f4f47e9b744ee9f159046259ec2e26185
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006487"
---
# <a name="hashes-and-digital-signatures"></a>Hachages et signatures numériques

Avec les [fonctions de hachage et de signature numérique](cryptography-functions.md), un utilisateur peut signer numériquement des données afin que n’importe quel autre utilisateur puisse vérifier que les données n’ont pas été modifiées depuis qu’il a été signé. L’identité de l’utilisateur qui a signé les données peut également être vérifiée.

Une [*signature numérique*](../secgloss/d-gly.md) est constituée d’une petite quantité de données binaires, en général moins de 256 octets. Cette signature peut être regroupée avec le message signé ou stockée séparément, en fonction de la façon dont une application particulière a été implémentée.

Le fournisseur de services de chiffrement fort Microsoft crée des signatures numériques conformes aux [*normes de chiffrement de clé publique*](../secgloss/p-gly.md) RSA (PKCS) \# 1.

 

 
