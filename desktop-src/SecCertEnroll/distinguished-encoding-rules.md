---
description: Le préfixe ASN. 1 (Abstract Syntax Notation One) définit les ensembles de règles suivants qui régissent la façon dont les structures de données envoyées entre les ordinateurs sont encodées et décodées.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527003"
---
# <a name="distinguished-encoding-rules"></a><span data-ttu-id="7c788-103">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="7c788-103">Distinguished Encoding Rules</span></span>

<span data-ttu-id="7c788-104">Le préfixe ASN. 1 (Abstract Syntax Notation One) définit les ensembles de règles suivants qui régissent la façon dont les structures de données envoyées entre les ordinateurs sont encodées et décodées.</span><span class="sxs-lookup"><span data-stu-id="7c788-104">Abstract Syntax Notation One (ASN.1) defines the following rule sets that govern how data structures that are being sent between computers are encoded and decoded.</span></span>

-   <span data-ttu-id="7c788-105">Règles de codage de base (BER)</span><span class="sxs-lookup"><span data-stu-id="7c788-105">Basic Encoding Rules (BER)</span></span>
-   <span data-ttu-id="7c788-106">Règles d’encodage canoniques (CER)</span><span class="sxs-lookup"><span data-stu-id="7c788-106">Canonical Encoding Rules (CER)</span></span>
-   <span data-ttu-id="7c788-107">Distinguished Encoding Rules (DER)</span><span class="sxs-lookup"><span data-stu-id="7c788-107">Distinguished Encoding Rules (DER)</span></span>
-   <span data-ttu-id="7c788-108">Règles d’encodage compressées (PER)</span><span class="sxs-lookup"><span data-stu-id="7c788-108">Packed Encoding Rules (PER)</span></span>

<span data-ttu-id="7c788-109">L’ensemble de règles d’origine a été défini par la spécification BER.</span><span class="sxs-lookup"><span data-stu-id="7c788-109">The original rule set was defined by the BER specification.</span></span> <span data-ttu-id="7c788-110">CER et DER ont été développés plus tard en tant que sous-ensembles spécialisés de BER.</span><span class="sxs-lookup"><span data-stu-id="7c788-110">CER and DER were developed later as specialized subsets of BER.</span></span> <span data-ttu-id="7c788-111">PAR a été développé en réponse à formulées sur la quantité de bande passante requise pour transmettre des données à l’aide de BER ou de ses variantes.</span><span class="sxs-lookup"><span data-stu-id="7c788-111">PER was developed in response to criticisms about the amount of bandwidth required to transmit data using BER or its variants.</span></span> <span data-ttu-id="7c788-112">PER fournit des économies substantielles.</span><span class="sxs-lookup"><span data-stu-id="7c788-112">PER provides a significant savings.</span></span>

<span data-ttu-id="7c788-113">DER a été créé pour répondre aux exigences de la spécification X. 509 pour un transfert de données sécurisé.</span><span class="sxs-lookup"><span data-stu-id="7c788-113">DER was created to satisfy the requirements of the X.509 specification for secure data transfer.</span></span> <span data-ttu-id="7c788-114">L’API d’inscription de certificats utilise DER exclusivement.</span><span class="sxs-lookup"><span data-stu-id="7c788-114">The Certificate Enrollment API uses DER exclusively.</span></span> <span data-ttu-id="7c788-115">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7c788-115">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="7c788-116">Syntaxe de transfert DER</span><span class="sxs-lookup"><span data-stu-id="7c788-116">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
-   [<span data-ttu-id="7c788-117">Codage DER des types ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7c788-117">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a><span data-ttu-id="7c788-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c788-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c788-119">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7c788-119">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="7c788-120">Encodage de demande de certificat</span><span class="sxs-lookup"><span data-stu-id="7c788-120">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="7c788-121">Présentation de la syntaxe et de l’encodage ASN. 1</span><span class="sxs-lookup"><span data-stu-id="7c788-121">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



