---
description: Important cette API est déconseillée.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Fournisseurs de services de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393508"
---
# <a name="cryptographic-service-providers"></a>Fournisseurs de services de chiffrement

> [!IMPORTANT]
> Cette API est déconseillée. Les logiciels nouveaux et existants doivent commencer à utiliser les [API de cryptographie nouvelle génération.](/windows/desktop/SecCNG/cng-portal) Microsoft peut supprimer cette API dans les versions ultérieures.

 

Un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) contient des implémentations de normes et d’algorithmes de chiffrement. Au minimum, un CSP se compose d’une [*bibliothèque de liens dynamiques*](../secgloss/d-gly.md) (dll) qui implémente les fonctions dans [*CryptoSPI*](../secgloss/c-gly.md) (une [*interface de programme système*](../secgloss/s-gly.md)). La plupart des fournisseurs de services de chiffrement contiennent l’implémentation de toutes leurs propres fonctions. Certains fournisseurs de services de chiffrement, toutefois, implémentent leurs fonctions principalement dans un programme de service Windows géré par le gestionnaire de contrôle des services Windows. D’autres implémentent des fonctions matérielles, telles qu’une [*carte à puce*](../secgloss/s-gly.md) ou un coprocesseur sécurisé. Si un fournisseur de services de chiffrement n’implémente pas ses propres fonctions, la DLL agit comme une couche directe, facilitant ainsi la communication entre le système d’exploitation et l’implémentation réelle du CSP.

Cette section comprend les rubriques suivantes.



| Rubrique                                                                                      | Contenu                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Types de fournisseur de chiffrement](cryptographic-provider-types.md)                           | Les types de fournisseur de chiffrement sont des familles de fournisseurs de services de chiffrement qui partagent des formats de données et des protocoles de chiffrement. Les formats de données incluent les schémas de [*remplissage*](../secgloss/p-gly.md) des algorithmes, les [*longueurs de clé*](../secgloss/k-gly.md)et les modes par défaut. |
| [Fournisseurs de services de chiffrement Microsoft](microsoft-cryptographic-service-providers.md) | Informations détaillées sur les fournisseurs de services de chiffrement actuellement disponibles auprès de Microsoft.                                                                                                                                                                                                                                                                                       |



 

 

 
