---
description: Utilisez des technologies de chiffrement pour le chiffrement à clé publique, les algorithmes de chiffrement, le chiffrement RSA et les certificats numériques.
ms.assetid: c53af815-ee3f-417a-8e62-3a3689715bc6
title: Chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852b7c2b38ca5b7d330a70e91a5b7a9dd5bb6557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517472"
---
# <a name="cryptography"></a><span data-ttu-id="24221-103">Chiffrement</span><span class="sxs-lookup"><span data-stu-id="24221-103">Cryptography</span></span>

## <a name="purpose"></a><span data-ttu-id="24221-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="24221-104">Purpose</span></span>

<span data-ttu-id="24221-105">Le chiffrement consiste à utiliser des codes pour convertir des données afin que seul un destinataire spécifique puisse les lire à l’aide d’une clé.</span><span class="sxs-lookup"><span data-stu-id="24221-105">Cryptography is the use of codes to convert data so that only a specific recipient will be able to read it, using a key.</span></span>

<span data-ttu-id="24221-106">Les technologies de chiffrement Microsoft incluent CryptoAPI, les fournisseurs de services de chiffrement (CSP), les outils CryptoAPI, CAPICOM, WinTrust, émettant et gérant les certificats et le développement d’infrastructures de clé publique personnalisables.</span><span class="sxs-lookup"><span data-stu-id="24221-106">Microsoft cryptographic technologies include CryptoAPI, Cryptographic Service Providers (CSP), CryptoAPI Tools, CAPICOM, WinTrust, issuing and managing certificates, and developing customizable public key infrastructures.</span></span> <span data-ttu-id="24221-107">L’inscription des certificats et des cartes à puce, la gestion des certificats et le développement de modules personnalisés sont également décrits.</span><span class="sxs-lookup"><span data-stu-id="24221-107">Certificate and smart card enrollment, certificate management, and custom module development are also described.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="24221-108">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="24221-108">Developer audience</span></span>

<span data-ttu-id="24221-109">CryptoAPI est destiné aux développeurs d’applications Windows qui permettent aux utilisateurs de créer et d’échanger des documents et d’autres données dans un environnement sécurisé, en particulier sur des médias non sécurisés tels qu’Internet.</span><span class="sxs-lookup"><span data-stu-id="24221-109">CryptoAPI is intended for use by developers of Windows-based applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="24221-110">Les développeurs doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation Windows.</span><span class="sxs-lookup"><span data-stu-id="24221-110">Developers should be familiar with the C and C++ programming languages and the Windows programming environment.</span></span> <span data-ttu-id="24221-111">Bien que cela ne soit pas obligatoire, il est recommandé de bien comprendre le chiffrement ou les sujets liés à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="24221-111">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="24221-112">CAPICOM est un composant de 32 bits uniquement destiné aux développeurs qui créent des applications à l’aide du langage de programmation Visual Basic Scripting Edition (VBScript) ou du langage de programmation C++.</span><span class="sxs-lookup"><span data-stu-id="24221-112">CAPICOM is a 32-bit only component that is intended for use by developers who are creating applications using Visual Basic Scripting Edition (VBScript) programming language or the C++ programming language.</span></span> <span data-ttu-id="24221-113">CAPICOM peut être utilisé dans les systèmes d’exploitation spécifiés dans Run-Time exigences.</span><span class="sxs-lookup"><span data-stu-id="24221-113">CAPICOM is available for use in the operating systems specified in Run-Time Requirements.</span></span> <span data-ttu-id="24221-114">Pour un développement futur, nous vous recommandons d’utiliser le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="24221-114">For future development, we recommend that you use the .NET Framework to implement security features.</span></span> <span data-ttu-id="24221-115">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="24221-115">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="24221-116">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="24221-116">Run-time requirements</span></span>

<span data-ttu-id="24221-117">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="24221-117">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="24221-118">CAPICOM 2.1.0.2 est pris en charge sur les versions et systèmes d’exploitation suivants :</span><span class="sxs-lookup"><span data-stu-id="24221-118">CAPICOM 2.1.0.2 is supported on the following operating systems and versions:</span></span>

-   <span data-ttu-id="24221-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="24221-119">Windows Server 2003</span></span>
-   <span data-ttu-id="24221-120">Windows XP</span><span class="sxs-lookup"><span data-stu-id="24221-120">Windows XP</span></span>

<span data-ttu-id="24221-121">CAPICOM est disponible sous la forme d’un fichier redistribuable qui peut être téléchargé à partir de [Platform SDK Redistributable : CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span><span class="sxs-lookup"><span data-stu-id="24221-121">CAPICOM is available as a redistributable file that can be downloaded from [Platform SDK Redistributable: CAPICOM](https://www.microsoft.com/download/details.aspx?id=25281).</span></span>

<span data-ttu-id="24221-122">Les services de certificats requièrent les versions suivantes de ces systèmes d’exploitation :</span><span class="sxs-lookup"><span data-stu-id="24221-122">Certificate Services requires the following versions of these operating systems:</span></span>

-   <span data-ttu-id="24221-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24221-123">Windows Server 2008 R2</span></span>
-   <span data-ttu-id="24221-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24221-124">Windows Server 2008</span></span>
-   <span data-ttu-id="24221-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="24221-125">Windows Server 2003</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24221-126">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="24221-126">In this section</span></span>



| <span data-ttu-id="24221-127">Rubrique</span><span class="sxs-lookup"><span data-stu-id="24221-127">Topic</span></span>                                                           | <span data-ttu-id="24221-128">Description</span><span class="sxs-lookup"><span data-stu-id="24221-128">Description</span></span>                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24221-129">À propos du chiffrement</span><span class="sxs-lookup"><span data-stu-id="24221-129">About Cryptography</span></span>](about-cryptography.md)<br/>         | <span data-ttu-id="24221-130">Principaux concepts de chiffrement et une vue de haut niveau des technologies de chiffrement de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="24221-130">Key cryptography concepts and a high-level view of Microsoft cryptography technologies.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="24221-131">Utilisation du chiffrement</span><span class="sxs-lookup"><span data-stu-id="24221-131">Using Cryptography</span></span>](using-cryptography.md)<br/>         | <span data-ttu-id="24221-132">Processus de chiffrement, procédures et exemples étendus de programmes C et Visual Basic à l’aide des fonctions CryptoAPI et des objets CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="24221-132">Cryptography processes, procedures, and extended samples of C and Visual Basic programs using CryptoAPI functions and CAPICOM objects.</span></span><br/>                                                                            |
| [<span data-ttu-id="24221-133">Référence de chiffrement</span><span class="sxs-lookup"><span data-stu-id="24221-133">Cryptography Reference</span></span>](cryptography-reference.md)<br/> | <span data-ttu-id="24221-134">Description détaillée des fonctions, interfaces, objets, structures et autres éléments de programmation de Microsoft Cryptography.</span><span class="sxs-lookup"><span data-stu-id="24221-134">Detailed descriptions of the Microsoft cryptography functions, interfaces, objects, structures, and other programming elements.</span></span> <span data-ttu-id="24221-135">Contient des descriptions de référence de l’API pour l’utilisation de certificats numériques.</span><span class="sxs-lookup"><span data-stu-id="24221-135">Includes reference descriptions of the API for working with digital certificates.</span></span><br/> |



 

 

 




