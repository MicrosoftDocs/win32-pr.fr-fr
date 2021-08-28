---
description: Le fournisseur de services de chiffrement de base Microsoft est le fournisseur du fournisseur de services de chiffrement (CSP) initial et est distribué avec les versions 1,0 et 2,0 de CryptoAPI. Il s’agit d’un fournisseur à usage général qui prend en charge les signatures numériques et le chiffrement des données.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Fournisseur de services de chiffrement de base Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32082fc6cd7ec6d34bd994e3d3122e2b4c06eee290af8074cea0c183e5dd0116
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100699"
---
# <a name="microsoft-base-cryptographic-provider"></a>Fournisseur de services de chiffrement de base Microsoft

Le fournisseur de services de chiffrement de base Microsoft est le fournisseur du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP) initial et est distribué avec les versions 1,0 et 2,0 de [*CryptoAPI*](../secgloss/c-gly.md) . Il s’agit d’un fournisseur à usage général qui prend en charge les [*signatures numériques*](../secgloss/d-gly.md) et le chiffrement des données.

L’algorithme de clé publique RSA est utilisé pour toutes les opérations de clé publique.

Pour assurer la compatibilité descendante avec les versions antérieures, la nouvelle version du fournisseur conserve la désignation de version 1,0 du nom dans wincrypt. h. Toutefois, la version 2,0 de ce fournisseur est actuellement commercialisée. Pour déterminer la version réelle du fournisseur en cours d’utilisation, appelez [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) avec l’argument *DwParam* défini sur **pp \_ version**. Si 0x0200 est retourné dans *pbData*, vous avez la version 2,0.

|                   | Valeur            |
|-------------------|------------------|
| **Type de fournisseur** | PROUVER \_ RSA \_ Full  |
| **Nom du fournisseur** | MS \_ Def \_ Prov    |



 

 

 
