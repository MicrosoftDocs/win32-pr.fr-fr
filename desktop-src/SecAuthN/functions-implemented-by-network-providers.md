---
description: Les fonctions suivantes sont implémentées par une DLL de fournisseur réseau pour communiquer avec le routeur de fournisseur multiple (MPR).
ms.assetid: ebdaec3d-6335-4bdf-b150-91e538068f2b
title: Fonctions implémentées par les fournisseurs de réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8122d8e06e92f66958f597c8fbe26f8e1c7abdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952796"
---
# <a name="functions-implemented-by-network-providers"></a><span data-ttu-id="aa4bb-103">Fonctions implémentées par les fournisseurs de réseau</span><span class="sxs-lookup"><span data-stu-id="aa4bb-103">Functions Implemented by Network Providers</span></span>

<span data-ttu-id="aa4bb-104">Les fonctions suivantes sont implémentées par une DLL de fournisseur réseau pour communiquer avec le [*routeur de fournisseur multiple*](/windows/desktop/SecGloss/m-gly) (MPR).</span><span class="sxs-lookup"><span data-stu-id="aa4bb-104">The following functions are implemented by a network provider DLL to communicate with the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR).</span></span> <span data-ttu-id="aa4bb-105">Notez que seules les [fonctions de fonctionnalités](capabilities-functions.md) doivent être implémentées par un fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-105">Note that only the [Capabilities Functions](capabilities-functions.md) must be implemented by a network provider.</span></span> <span data-ttu-id="aa4bb-106">L’implémentation des autres types de fonctions est facultative et dépend des exigences du fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-106">Implementation of the other types of functions is optional and depends on the requirements of the network provider.</span></span>



| <span data-ttu-id="aa4bb-107">Ensemble de fonctions</span><span class="sxs-lookup"><span data-stu-id="aa4bb-107">Function set</span></span>                                                                                    | <span data-ttu-id="aa4bb-108">Description</span><span class="sxs-lookup"><span data-stu-id="aa4bb-108">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa4bb-109">Fonctions fonctions</span><span class="sxs-lookup"><span data-stu-id="aa4bb-109">Capabilities Functions</span></span>](capabilities-functions.md)<br/>                                 | <span data-ttu-id="aa4bb-110">Permet à l’appelant de déterminer les fonctionnalités du fournisseur réseau.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-110">Allows the caller to determine the capabilities of the network provider.</span></span><br/>                                                                |
| [<span data-ttu-id="aa4bb-111">Fonctions de nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="aa4bb-111">User Name Functions</span></span>](user-name-functions.md)<br/>                                       | <span data-ttu-id="aa4bb-112">Demande au fournisseur réseau le nom d’utilisateur associé à une connexion.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-112">Prompts the network provider for the user name associated with a connection.</span></span><br/>                                                            |
| [<span data-ttu-id="aa4bb-113">Fonctions de redirection de l’appareil</span><span class="sxs-lookup"><span data-stu-id="aa4bb-113">Device-Redirecting Functions</span></span>](device-redirecting-functions.md)<br/>                     | <span data-ttu-id="aa4bb-114">Permet à un fournisseur réseau de rediriger des appareils, des lettres de lecteur et des ports LPT standard sur le système d’exploitation Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-114">Allows a network provider to redirect devices, drive letters, and LPT ports that are standard on the Microsoft MS-DOS operating system.</span></span><br/> |
| [<span data-ttu-id="aa4bb-115">Fonctions de boîte de dialogue spécifiques au fournisseur</span><span class="sxs-lookup"><span data-stu-id="aa4bb-115">Provider-Specific Dialog Box Functions</span></span>](provider-specific-dialog-box-functions.md)<br/> | <span data-ttu-id="aa4bb-116">Permet à un fournisseur de réseau d’afficher ou d’agir sur des informations spécifiques au réseau.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-116">Allows a network provider to display or act on network-specific information.</span></span><br/>                                                            |
| [<span data-ttu-id="aa4bb-117">Fonctions d’administration</span><span class="sxs-lookup"><span data-stu-id="aa4bb-117">Administrative Functions</span></span>](administrative-functions.md)<br/>                             | <span data-ttu-id="aa4bb-118">Permet à un fournisseur de réseau d’afficher ou d’agir sur des répertoires réseau spéciaux.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-118">Allows a network provider to display or act on special network directories.</span></span><br/>                                                             |
| [<span data-ttu-id="aa4bb-119">Fonctions d’énumération</span><span class="sxs-lookup"><span data-stu-id="aa4bb-119">Enumeration Functions</span></span>](enumeration-functions.md)<br/>                                   | <span data-ttu-id="aa4bb-120">Permet à l’utilisateur de parcourir les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="aa4bb-120">Allows the user to browse network resources.</span></span><br/>                                                                                            |



 

<span data-ttu-id="aa4bb-121">Pour plus d’informations sur la création et l’inscription d’un fournisseur de réseau, consultez [implémentation d’un fournisseur de réseau](implementing-a-network-provider.md) et [inscription des fournisseurs de réseau et des gestionnaires d’informations d’identification](registering-network-providers-and-credential-managers.md).</span><span class="sxs-lookup"><span data-stu-id="aa4bb-121">For more information about how to create and register a network provider, see [Implementing a Network Provider](implementing-a-network-provider.md) and [Registering Network Providers and Credential Managers](registering-network-providers-and-credential-managers.md).</span></span>

 

