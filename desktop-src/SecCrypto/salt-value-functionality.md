---
description: Le fournisseur de base crée des clés symétriques 40 bits créées avec onze octets de sel de valeur zéro, onze octets de sel différent de zéro si CRYPT \_ Create \_ Salt est spécifié, ou aucune valeur salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Fonctionnalité de valeur Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318714"
---
# <a name="salt-value-functionality"></a><span data-ttu-id="4959d-103">Fonctionnalité de valeur Salt</span><span class="sxs-lookup"><span data-stu-id="4959d-103">Salt Value Functionality</span></span>

<span data-ttu-id="4959d-104">Le fournisseur de base crée des [*clés symétriques*](../secgloss/s-gly.md) 40 bits créées avec onze octets de [*sel*](../secgloss/s-gly.md)de valeur zéro, onze octets de sel différent de zéro si crypt \_ Create \_ Salt est spécifié, ou aucune valeur salt.</span><span class="sxs-lookup"><span data-stu-id="4959d-104">The Base Provider creates 40-bit [*symmetric keys*](../secgloss/s-gly.md) created with eleven bytes of zero-value [*salt*](../secgloss/s-gly.md), eleven bytes of nonzero salt if CRYPT\_CREATE\_SALT is specified, or no salt value.</span></span> <span data-ttu-id="4959d-105">Toutefois, une clé symétrique 40 bits avec un Salt de valeur zéro n’est pas équivalente à une clé symétrique de 40 bits sans Salt.</span><span class="sxs-lookup"><span data-stu-id="4959d-105">A 40-bit symmetric key with zero-value salt, however, is not equivalent to a 40-bit symmetric key without salt.</span></span> <span data-ttu-id="4959d-106">Pour l’interopérabilité, les clés doivent être créées sans Salt.</span><span class="sxs-lookup"><span data-stu-id="4959d-106">For interoperability, keys must be created without salt.</span></span> <span data-ttu-id="4959d-107">Ce problème résulte d’une condition par défaut qui se produit uniquement avec les clés de 40 bits exactement.</span><span class="sxs-lookup"><span data-stu-id="4959d-107">This problem results from a default condition that occurs only with keys of exactly 40 bits.</span></span> <span data-ttu-id="4959d-108">Toutes les autres [*longueurs de clé*](../secgloss/k-gly.md) n’ont pas de Salt alloué par défaut.</span><span class="sxs-lookup"><span data-stu-id="4959d-108">All other [*key lengths*](../secgloss/k-gly.md) do not have salt allocated by default.</span></span>

<span data-ttu-id="4959d-109">Les fournisseurs de base et le fournisseur étendu peuvent utiliser l' \_ indicateur de chiffrement non \_ Salt pour spécifier qu’aucune valeur Salt n’est allouée pour une clé symétrique 40 bits.</span><span class="sxs-lookup"><span data-stu-id="4959d-109">Both the Base Providers and the Extended Provider can use the CRYPT\_NO\_SALT flag to specify that no salt value is allocated for a 40-bit symmetric key.</span></span> <span data-ttu-id="4959d-110">Les fonctions qui acceptent cet indicateur sont [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)et [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="4959d-110">The functions that accept this flag are [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey), and [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span> <span data-ttu-id="4959d-111">Par défaut, ces fonctions fournissent une compatibilité descendante pour le cas de clé symétrique 40 bits en continuant à utiliser le Salt de valeur zéro de onze octets.</span><span class="sxs-lookup"><span data-stu-id="4959d-111">By default, these functions provide backward compatibility for the 40-bit symmetric key case by continuing the use of the eleven-byte-long zero-value salt.</span></span>

 

 
