---
description: L’avenir du chiffrement et des communications sécurisées ne peut pas être prédit facilement.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Extension de la fonctionnalité CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952948"
---
# <a name="extending-cryptoapi-functionality"></a><span data-ttu-id="bd59d-103">Extension de la fonctionnalité CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="bd59d-103">Extending CryptoAPI Functionality</span></span>

<span data-ttu-id="bd59d-104">L’avenir du [*chiffrement*](../secgloss/c-gly.md) et des communications sécurisées ne peut pas être prédit facilement.</span><span class="sxs-lookup"><span data-stu-id="bd59d-104">The future of [*cryptography*](../secgloss/c-gly.md) and secure communications cannot easily be predicted.</span></span> <span data-ttu-id="bd59d-105">De nouveaux types de certificats peuvent émerger, de nombreuses extensions de certificat peuvent trouver une utilisation courante et de nouveaux types de messages peuvent être introduits.</span><span class="sxs-lookup"><span data-stu-id="bd59d-105">New certificate types might emerge, various certificate extensions might find common usage, and new message types might be introduced.</span></span> <span data-ttu-id="bd59d-106">Pour cette raison, l’extensibilité fait partie de la conception des fonctions [*CryptoAPI*](../secgloss/c-gly.md) de clé.</span><span class="sxs-lookup"><span data-stu-id="bd59d-106">Because of this, extensibility is part of the design of key [*CryptoAPI*](../secgloss/c-gly.md) functions.</span></span>

<span data-ttu-id="bd59d-107">Les sections suivantes présentent des vues d’ensemble de l’utilisation des OID pour étendre les fonctions CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="bd59d-107">The following sections present overviews on the use of OIDs for extending CryptoAPI functions.</span></span>



| <span data-ttu-id="bd59d-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="bd59d-108">Topic</span></span>                                                                              | <span data-ttu-id="bd59d-109">Contenu</span><span class="sxs-lookup"><span data-stu-id="bd59d-109">Contents</span></span>                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd59d-110">Vue d’ensemble des OID</span><span class="sxs-lookup"><span data-stu-id="bd59d-110">OID Overview</span></span>](oid-overview.md)                                                   | <span data-ttu-id="bd59d-111">Concepts fondamentaux de l’OID.</span><span class="sxs-lookup"><span data-stu-id="bd59d-111">OID fundamental concepts.</span></span>                                                                                                           |
| [<span data-ttu-id="bd59d-112">Création de la nouvelle fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="bd59d-112">Creating the New Functionality</span></span>](creating-the-new-functionality.md)               | <span data-ttu-id="bd59d-113">Création d’OID et de fonctions pour étendre l’utilisation des API existantes.</span><span class="sxs-lookup"><span data-stu-id="bd59d-113">Creating OIDs and functions to extend the use of existing APIs.</span></span>                                                                     |
| [<span data-ttu-id="bd59d-114">Inscription des nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="bd59d-114">Registering the New Functionality</span></span>](registering-the-new-functionality.md)         | <span data-ttu-id="bd59d-115">Configuration de nouvelles fonctions liées à OID.</span><span class="sxs-lookup"><span data-stu-id="bd59d-115">Setting up new OID-related functions.</span></span>                                                                                               |
| [<span data-ttu-id="bd59d-116">Installation des nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="bd59d-116">Installing the New Functionality</span></span>](installing-the-new-functionality.md)           | <span data-ttu-id="bd59d-117">Installation des fonctions OID dans la mémoire pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="bd59d-117">Installing OID functions to memory to improve performance.</span></span>                                                                          |
| [<span data-ttu-id="bd59d-118">Extension de la fonctionnalité CertOpenStore</span><span class="sxs-lookup"><span data-stu-id="bd59d-118">Extending CertOpenStore Functionality</span></span>](extending-certopenstore-functionality.md) | <span data-ttu-id="bd59d-119">Extension de la fonctionnalité [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) à l’aide d’une fonction de fournisseur de magasin de certificats installable ou enregistrée.</span><span class="sxs-lookup"><span data-stu-id="bd59d-119">Extending [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) functionality using installable or registered certificate-store-provider function.</span></span> |



 

 

 
