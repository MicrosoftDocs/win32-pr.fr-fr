---
description: CNG est une API de chiffrement que vous pouvez utiliser pour créer un logiciel de sécurité de chiffrement pour la gestion des clés de chiffrement, le chiffrement et la sécurité des données, ainsi que la cryptographie et la sécurité réseau.
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 'API de chiffrement : nouvelle génération'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861874"
---
# <a name="cryptography-api-next-generation"></a><span data-ttu-id="d16a6-103">API de chiffrement : nouvelle génération</span><span class="sxs-lookup"><span data-stu-id="d16a6-103">Cryptography API: Next Generation</span></span>

## <a name="purpose"></a><span data-ttu-id="d16a6-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="d16a6-104">Purpose</span></span>

<span data-ttu-id="d16a6-105">API de chiffrement : Next Generation (CNG) est le remplacement à long terme de l’interface [*CryptoAPI*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d16a6-105">Cryptography API: Next Generation (CNG) is the long-term replacement for the [*CryptoAPI*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d16a6-106">CNG est conçu pour être extensible à de nombreux niveaux et un chiffrement indépendant dans le comportement.</span><span class="sxs-lookup"><span data-stu-id="d16a6-106">CNG is designed to be extensible at many levels and cryptography agnostic in behavior.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d16a6-107">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="d16a6-107">Developer audience</span></span>

<span data-ttu-id="d16a6-108">CNG est destiné aux développeurs d’applications qui permettent aux utilisateurs de créer et d’échanger des documents et d’autres données dans un environnement sécurisé, en particulier sur des médias non sécurisés tels qu’Internet.</span><span class="sxs-lookup"><span data-stu-id="d16a6-108">CNG is intended for use by developers of applications that will enable users to create and exchange documents and other data in a secure environment, especially over nonsecure media such as the Internet.</span></span> <span data-ttu-id="d16a6-109">Les développeurs doivent être familiarisés avec les langages de programmation C et C++ et dans l’environnement de programmation Windows.</span><span class="sxs-lookup"><span data-stu-id="d16a6-109">Developers should be familiar with the C and C++ programming languages and the Windows-based programming environment.</span></span> <span data-ttu-id="d16a6-110">Bien que cela ne soit pas obligatoire, il est recommandé de bien comprendre le chiffrement ou les sujets liés à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="d16a6-110">Although not required, an understanding of cryptography or security-related subjects is advised.</span></span>

<span data-ttu-id="d16a6-111">Si vous développez un fournisseur d’algorithme de chiffrement CNG ou un fournisseur de stockage de clés, vous devez télécharger le [Kit de développement du fournisseur de services de chiffrement](https://www.microsoft.com/download/details.aspx?id=30688) auprès de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d16a6-111">If you are developing a CNG cryptographic algorithm provider or key storage provider, you must download the [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) from Microsoft.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d16a6-112">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="d16a6-112">Run-time requirements</span></span>

<span data-ttu-id="d16a6-113">CNG est pris en charge à partir de Windows Server 2008 et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d16a6-113">CNG is supported beginning with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="d16a6-114">Pour plus d’informations sur les exigences d’exécution d’un élément de programmation particulier, consultez la section Configuration requise de la page de référence de cet élément.</span><span class="sxs-lookup"><span data-stu-id="d16a6-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d16a6-115">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d16a6-115">In this section</span></span>



| <span data-ttu-id="d16a6-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d16a6-116">Topic</span></span>                                         | <span data-ttu-id="d16a6-117">Description</span><span class="sxs-lookup"><span data-stu-id="d16a6-117">Description</span></span>                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d16a6-118">À propos de CNG</span><span class="sxs-lookup"><span data-stu-id="d16a6-118">About CNG</span></span>](about-cng.md)<br/>         | <span data-ttu-id="d16a6-119">Décrit les fonctionnalités CNG, les primitives de chiffrement, le stockage de clés, la récupération, l’importation et l’exportation.</span><span class="sxs-lookup"><span data-stu-id="d16a6-119">Describes CNG features, cryptographic primitives, and key storage, retrieval, import, and export.</span></span><br/>                                   |
| [<span data-ttu-id="d16a6-120">Utilisation de CNG</span><span class="sxs-lookup"><span data-stu-id="d16a6-120">Using CNG</span></span>](using-cng.md)<br/>         | <span data-ttu-id="d16a6-121">Explique comment utiliser les fonctionnalités de configuration de chiffrement CNG et la programmation CNG classique.</span><span class="sxs-lookup"><span data-stu-id="d16a6-121">Explains how to use the cryptography configuration features of CNG and typical CNG programming.</span></span><br/>                                     |
| [<span data-ttu-id="d16a6-122">Référence CNG</span><span class="sxs-lookup"><span data-stu-id="d16a6-122">CNG Reference</span></span>](cng-reference.md)<br/> | <span data-ttu-id="d16a6-123">Description détaillée des éléments de programmation CNG.</span><span class="sxs-lookup"><span data-stu-id="d16a6-123">Detailed descriptions of the CNG programming elements.</span></span> <span data-ttu-id="d16a6-124">Ces pages incluent des descriptions de référence de l’API pour l’utilisation de CNG.</span><span class="sxs-lookup"><span data-stu-id="d16a6-124">These pages include reference descriptions of the API for working with CNG.</span></span> <br/> |



 

 

