---
description: Les certificats sont associés à des propriétés, telles qu’un nom d’affichage, une description et des utilisations autorisées, qui peuvent être affichées et modifiées.
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: Création, affichage et gestion des certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514599"
---
# <a name="creating-viewing-and-managing-certificates"></a><span data-ttu-id="85cd6-103">Création, affichage et gestion des certificats</span><span class="sxs-lookup"><span data-stu-id="85cd6-103">Creating, Viewing, and Managing Certificates</span></span>

<span data-ttu-id="85cd6-104">Les [*certificats*](../secgloss/c-gly.md) sont des structures en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85cd6-104">[*Certificates*](../secgloss/c-gly.md) are read-only structures.</span></span> <span data-ttu-id="85cd6-105">Le contenu d’un certificat peut être affiché, mais ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="85cd6-105">The contents of a certificate can be viewed but cannot be modified.</span></span> <span data-ttu-id="85cd6-106">Les informations contenues dans le certificat lui-même incluent les dates de validité, l’émetteur, l’objet et la clé publique du certificat.</span><span class="sxs-lookup"><span data-stu-id="85cd6-106">Information in the certificate itself includes the certificate's validity dates, issuer, subject, and the public key.</span></span> <span data-ttu-id="85cd6-107">Toutefois, les certificats sont associés à des propriétés, telles qu’un nom d’affichage, une description et des utilisations autorisées, qui peuvent être affichées et modifiées.</span><span class="sxs-lookup"><span data-stu-id="85cd6-107">However, certificates have associated properties, such as a display name, description, and allowed uses, that can be viewed and edited.</span></span>

<span data-ttu-id="85cd6-108">Cette section explique comment créer des certificats de test, afficher des certificats et gérer des certificats et d’autres objets de sécurité.</span><span class="sxs-lookup"><span data-stu-id="85cd6-108">This section demonstrates creating test certificates, viewing certificates, and managing certificates and other security objects.</span></span> <span data-ttu-id="85cd6-109">Les certificats et les certificats de l' [*éditeur de logiciels*](../secgloss/s-gly.md) (SPCS) qui peuvent être créés avec Makecert sont strictement à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="85cd6-109">The certificates and [*Software Publisher Certificates*](../secgloss/s-gly.md) (SPCs) that can be created with MakeCert are strictly for test purposes.</span></span> <span data-ttu-id="85cd6-110">Un [*certificat racine*](../secgloss/r-gly.md) de test et une [*clé privée*](../secgloss/p-gly.md) de racine de test sont fournis à des fins de test uniquement.</span><span class="sxs-lookup"><span data-stu-id="85cd6-110">A test [*root certificate*](../secgloss/r-gly.md) and a test root [*private key*](../secgloss/p-gly.md) are provided for testing purposes only.</span></span> <span data-ttu-id="85cd6-111">Les éditeurs de logiciels indépendants doivent obtenir un certificat auprès de GTE, VeriSign, Inc., ou une autre [*autorité de certification*](../secgloss/c-gly.md) pour signer le code qui sera distribué au public.</span><span class="sxs-lookup"><span data-stu-id="85cd6-111">Independent software vendors must obtain a certificate from GTE, VeriSign, Inc., or other [*certification authority*](../secgloss/c-gly.md) (CA) to sign code that will be distributed to the public.</span></span>

<span data-ttu-id="85cd6-112">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="85cd6-112">This section includes the following topics:</span></span>

-   [<span data-ttu-id="85cd6-113">Utilisation de MakeCert</span><span class="sxs-lookup"><span data-stu-id="85cd6-113">Using MakeCert</span></span>](using-makecert.md)
-   [<span data-ttu-id="85cd6-114">Utilisation de Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="85cd6-114">Using Cert2SPC</span></span>](using-cert2spc.md)
-   [<span data-ttu-id="85cd6-115">Utilisation de CertMgr</span><span class="sxs-lookup"><span data-stu-id="85cd6-115">Using CertMgr</span></span>](using-certmgr.md)

 

 
