---
description: L’avenir du chiffrement et des communications sécurisées ne peut pas être prédit facilement.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Extension de la fonctionnalité CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120978"
---
# <a name="extending-cryptoapi-functionality"></a>Extension de la fonctionnalité CryptoAPI

L’avenir du [*chiffrement*](../secgloss/c-gly.md) et des communications sécurisées ne peut pas être prédit facilement. De nouveaux types de certificats peuvent émerger, de nombreuses extensions de certificat peuvent trouver une utilisation courante et de nouveaux types de messages peuvent être introduits. Pour cette raison, l’extensibilité fait partie de la conception des fonctions [*CryptoAPI*](../secgloss/c-gly.md) de clé.

Les sections suivantes présentent des vues d’ensemble de l’utilisation des OID pour étendre les fonctions CryptoAPI.



| Rubrique                                                                              | Contenu                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d’ensemble des OID](oid-overview.md)                                                   | Concepts fondamentaux de l’OID.                                                                                                           |
| [Création de la nouvelle fonctionnalité](creating-the-new-functionality.md)               | Création d’OID et de fonctions pour étendre l’utilisation des API existantes.                                                                     |
| [Inscription des nouvelles fonctionnalités](registering-the-new-functionality.md)         | Configuration de nouvelles fonctions liées à OID.                                                                                               |
| [Installation des nouvelles fonctionnalités](installing-the-new-functionality.md)           | Installation des fonctions OID dans la mémoire pour améliorer les performances.                                                                          |
| [Extension de la fonctionnalité CertOpenStore](extending-certopenstore-functionality.md) | Extension de la fonctionnalité [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) à l’aide d’une fonction de fournisseur de magasin de certificats installable ou enregistrée. |



 

 

 
