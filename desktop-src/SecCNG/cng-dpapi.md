---
description: Microsoft a introduit l’interface de programmation d’applications de protection des données (DPAPI) dans Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515973"
---
# <a name="cng-dpapi"></a><span data-ttu-id="8f7bd-103">DPAPI CNG</span><span class="sxs-lookup"><span data-stu-id="8f7bd-103">CNG DPAPI</span></span>

<span data-ttu-id="8f7bd-104">Microsoft a introduit l’interface de programmation d’applications de protection des données (DPAPI) dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-104">Microsoft introduced the data protection application programming interface (DPAPI) in Windows 2000.</span></span> <span data-ttu-id="8f7bd-105">L’API se compose de deux fonctions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="8f7bd-105">The API consists of two functions, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span> <span data-ttu-id="8f7bd-106">DPAPI fait partie de CryptoAPI et était destiné aux développeurs qui savent très peu utiliser le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-106">DPAPI is part of CryptoAPI and was intended for developers who knew very little about using cryptography.</span></span> <span data-ttu-id="8f7bd-107">Les deux fonctions peuvent être utilisées pour chiffrer et déchiffrer des données statiques sur un seul ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-107">The two functions could be used to encrypt and decrypt static data on a single computer.</span></span>

<span data-ttu-id="8f7bd-108">Toutefois, le Cloud Computing requiert souvent que le contenu chiffré sur un ordinateur soit déchiffré sur un autre.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-108">Cloud computing, however, often requires that content encrypted on one computer be decrypted on another.</span></span> <span data-ttu-id="8f7bd-109">Par conséquent, à partir de Windows 8, Microsoft a étendu l’idée d’utiliser une API relativement simple pour englober les scénarios de Cloud.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-109">Therefore, beginning with Windows 8, Microsoft extended the idea of using a relatively straightforward API to encompass cloud scenarios.</span></span> <span data-ttu-id="8f7bd-110">Cette nouvelle API, appelée DPAPI-GN, vous permet de partager en toute sécurité des secrets (clés, mots de passe, matériel de clé) et des messages en les protégeant sur un ensemble de principaux qui peuvent être utilisés pour les déprotéger sur des ordinateurs différents après une authentification et une autorisation appropriées.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-110">This new API, called DPAPI-NG, enables you to securely share secrets (keys, passwords, key material) and messages by protecting them to a set of principals that can be used to unprotect them on different computers after proper authentication and authorization.</span></span> <span data-ttu-id="8f7bd-111">Les principaux suivants sont actuellement pris en charge :</span><span class="sxs-lookup"><span data-stu-id="8f7bd-111">The following principals are currently supported:</span></span>

-   <span data-ttu-id="8f7bd-112">Groupe dans une forêt Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-112">A group in an Active Directory forest.</span></span>
-   <span data-ttu-id="8f7bd-113">Informations d’identification Web.</span><span class="sxs-lookup"><span data-stu-id="8f7bd-113">Web credentials.</span></span>

<span data-ttu-id="8f7bd-114">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f7bd-114">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8f7bd-115">Fournisseurs de protection</span><span class="sxs-lookup"><span data-stu-id="8f7bd-115">Protection Providers</span></span>](protection-providers.md)
-   [<span data-ttu-id="8f7bd-116">Descripteurs de protection</span><span class="sxs-lookup"><span data-stu-id="8f7bd-116">Protection Descriptors</span></span>](protection-descriptors.md)
-   [<span data-ttu-id="8f7bd-117">Format de données protégées</span><span class="sxs-lookup"><span data-stu-id="8f7bd-117">Protected Data Format</span></span>](protected-data-format.md)

<span data-ttu-id="8f7bd-118">DPAPI-GN est basé sur le CNG (Cryptography Next Generation) et comprend les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="8f7bd-118">DPAPI-NG is built on top of Cryptography Next Generation (CNG) and includes the following functions:</span></span>

-   [<span data-ttu-id="8f7bd-119">**NCryptCreateProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-119">**NCryptCreateProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [<span data-ttu-id="8f7bd-120">**NCryptCloseProtectionDescriptor**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-120">**NCryptCloseProtectionDescriptor**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [<span data-ttu-id="8f7bd-121">**NCryptProtectSecret**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-121">**NCryptProtectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [<span data-ttu-id="8f7bd-122">**NCryptQueryProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-122">**NCryptQueryProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [<span data-ttu-id="8f7bd-123">**NCryptRegisterProtectionDescriptorName**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-123">**NCryptRegisterProtectionDescriptorName**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [<span data-ttu-id="8f7bd-124">**NCryptStreamClose**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-124">**NCryptStreamClose**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [<span data-ttu-id="8f7bd-125">**NCryptStreamOpenToProtect**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-125">**NCryptStreamOpenToProtect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [<span data-ttu-id="8f7bd-126">**NCryptStreamOpenToUnprotect**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-126">**NCryptStreamOpenToUnprotect**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [<span data-ttu-id="8f7bd-127">**NCryptStreamUpdate**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-127">**NCryptStreamUpdate**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [<span data-ttu-id="8f7bd-128">**NCryptUnprotectSecret**</span><span class="sxs-lookup"><span data-stu-id="8f7bd-128">**NCryptUnprotectSecret**</span></span>](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
