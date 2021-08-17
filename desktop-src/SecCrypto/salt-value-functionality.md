---
description: Le fournisseur de base crée des clés symétriques 40 bits créées avec onze octets de sel de valeur zéro, onze octets de sel différent de zéro si CRYPT \_ Create \_ Salt est spécifié, ou aucune valeur salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Fonctionnalité de valeur Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f911815152861921f1ffe12090c88ad4795ba042346aee875138acf591d14671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900369"
---
# <a name="salt-value-functionality"></a>Fonctionnalité de valeur Salt

Le fournisseur de base crée des [*clés symétriques*](../secgloss/s-gly.md) 40 bits créées avec onze octets de [*sel*](../secgloss/s-gly.md)de valeur zéro, onze octets de sel différent de zéro si crypt \_ Create \_ Salt est spécifié, ou aucune valeur salt. Toutefois, une clé symétrique 40 bits avec un Salt de valeur zéro n’est pas équivalente à une clé symétrique de 40 bits sans Salt. Pour l’interopérabilité, les clés doivent être créées sans Salt. Ce problème résulte d’une condition par défaut qui se produit uniquement avec les clés de 40 bits exactement. Toutes les autres [*longueurs de clé*](../secgloss/k-gly.md) n’ont pas de Salt alloué par défaut.

Les fournisseurs de base et le fournisseur étendu peuvent utiliser l' \_ indicateur de chiffrement non \_ Salt pour spécifier qu’aucune valeur Salt n’est allouée pour une clé symétrique 40 bits. Les fonctions qui acceptent cet indicateur sont [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)et [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). Par défaut, ces fonctions fournissent une compatibilité descendante pour le cas de clé symétrique 40 bits en continuant à utiliser le Salt de valeur zéro de onze octets.

 

 
