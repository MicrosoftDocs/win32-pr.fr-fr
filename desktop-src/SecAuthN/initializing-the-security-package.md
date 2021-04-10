---
description: Répertorie et explique les étapes nécessaires à l’initialisation d’un package de sécurité.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Initialisation du package de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115066"
---
# <a name="initializing-the-security-package"></a><span data-ttu-id="bef3b-103">Initialisation du package de sécurité</span><span class="sxs-lookup"><span data-stu-id="bef3b-103">Initializing the Security Package</span></span>

<span data-ttu-id="bef3b-104">Ces étapes sont nécessaires avant d’utiliser SSPI :</span><span class="sxs-lookup"><span data-stu-id="bef3b-104">These steps are necessary before using SSPI:</span></span>

1.  <span data-ttu-id="bef3b-105">La fonction d’initialisation doit être appelée pour obtenir l’adresse de la table de fonctions de sécurité.</span><span class="sxs-lookup"><span data-stu-id="bef3b-105">The initialization function must be called to obtain the address of the security function table.</span></span>

    <span data-ttu-id="bef3b-106">Le client et le serveur appellent [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) pour un pointeur vers une table de dispatch [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) .</span><span class="sxs-lookup"><span data-stu-id="bef3b-106">The client and server call [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) for a pointer to a [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) dispatch table.</span></span> <span data-ttu-id="bef3b-107">Ce tableau contient des pointeurs vers des fonctions de rappel déclarées dans SSPI. h.</span><span class="sxs-lookup"><span data-stu-id="bef3b-107">This table contains pointers to callback functions declared in Sspi.h.</span></span> <span data-ttu-id="bef3b-108">Ces pointeurs fournissent un accès aux implémentations de la DLL des différentes fonctions SSPI.</span><span class="sxs-lookup"><span data-stu-id="bef3b-108">These pointers provide access to the DLL's implementations of the various SSPI functions.</span></span>

2.  <span data-ttu-id="bef3b-109">Les informations doivent être obtenues sur les packages de sécurité pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bef3b-109">Information must be obtained about the supported security packages.</span></span>

    <span data-ttu-id="bef3b-110">Alors que la plupart des applications utilisent des packages de sécurité qui prennent en charge les fonctionnalités par défaut ou courantes, les packages de sécurité peuvent avoir des fonctionnalités uniques qui présentent un intérêt pour l’application.</span><span class="sxs-lookup"><span data-stu-id="bef3b-110">While most applications use security packages that support default or common capabilities, security packages can have unique capabilities of interest to the application.</span></span> <span data-ttu-id="bef3b-111">Une application nécessitant des fonctionnalités spéciales peut utiliser un package qui offre ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="bef3b-111">An application needing special capabilities can use a package that offers those capabilities.</span></span> <span data-ttu-id="bef3b-112">Pour plus d’informations, consultez [obtention d’informations sur les packages de sécurité](getting-information-about-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="bef3b-112">For more information, see [Getting Information About Security Packages](getting-information-about-security-packages.md).</span></span>

<span data-ttu-id="bef3b-113">À ce stade, l’application a initialisé avec succès un SSP et a choisi un package de sécurité avec des fonctionnalités suffisantes.</span><span class="sxs-lookup"><span data-stu-id="bef3b-113">At this point, the application has successfully initialized an SSP and chosen a security package with sufficient capabilities.</span></span>

<span data-ttu-id="bef3b-114">Le package [*Negotiate*](../secgloss/n-gly.md) peut être utilisé lorsque l’accord entre le client et le serveur sur le [*package de sécurité*](../secgloss/s-gly.md) à utiliser est effectué en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="bef3b-114">The [*Negotiate*](../secgloss/n-gly.md) package can be used where agreement between client and server about which [*security package*](../secgloss/s-gly.md) to use is done behind the scenes.</span></span> <span data-ttu-id="bef3b-115">Si le package Negotiate n’est pas utilisé, le client et le serveur doivent s’accorder sur le package de sécurité spécifique à utiliser avant d’effectuer les étapes de configuration ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="bef3b-115">If the Negotiate package is not used, the client and server must agree on the specific security package to use before performing the setup steps above.</span></span>

 

 
