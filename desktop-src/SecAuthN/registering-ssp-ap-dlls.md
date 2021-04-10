---
description: Après avoir développé un fournisseur de support de sécurité/une bibliothèque de liens dynamiques (DLL) de package d’authentification contenant un ou plusieurs packages de sécurité personnalisés, vous devez l’inscrire.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Inscription des dll SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756424"
---
# <a name="registering-sspap-dlls"></a><span data-ttu-id="ce78d-103">Inscription des dll SSP/AP</span><span class="sxs-lookup"><span data-stu-id="ce78d-103">Registering SSP/AP DLLs</span></span>

<span data-ttu-id="ce78d-104">Après avoir développé [](../secgloss/s-gly.md)une / bibliothèque de liens dynamiques (dll) de [*package d’authentification*](../secgloss/a-gly.md) du fournisseur de support de sécurité (SSP/AP) contenant un ou plusieurs [*packages de sécurité*](../secgloss/s-gly.md)personnalisés, vous devez l’inscrire.</span><span class="sxs-lookup"><span data-stu-id="ce78d-104">After developing a [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) dynamic-link library (SSP/AP DLL) containing one or more custom [*security packages*](../secgloss/s-gly.md), you must register it.</span></span> <span data-ttu-id="ce78d-105">Pour ce faire, ajoutez le nom de votre DLL SSP/AP personnalisée aux données de la valeur de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="ce78d-105">To do so, add the name of your custom SSP/AP DLL to the data of the following registry value:</span></span>

<span data-ttu-id="ce78d-106">**HKEY \_ \_** Packages de \\  \\  \\  \\  \\ **sécurité** LSA de contrôle de système d’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="ce78d-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Security Packages**</span></span>

<span data-ttu-id="ce78d-107">Les données de cette valeur de Registre sont une liste des noms des dll SSP/AP, sans l’extension « . dll ».</span><span class="sxs-lookup"><span data-stu-id="ce78d-107">The data for this registry value is a list of the names of SSP/AP DLLs, without the ".dll" extension.</span></span> <span data-ttu-id="ce78d-108">Le type de données de cette liste **est \_ reg \_ multisz** , ce qui signifie qu’il doit y avoir un caractère null (« \\ 0 ») entre chaque nom de dll dans la liste.</span><span class="sxs-lookup"><span data-stu-id="ce78d-108">The data type for this list is **REG\_MULTI\_SZ** so there must be a null character ('\\0') between each DLL name in the list.</span></span>

<span data-ttu-id="ce78d-109">En règle générale, les dll SSP/AP sont stockées dans le répertoire% SystemRoot%/system32</span><span class="sxs-lookup"><span data-stu-id="ce78d-109">Typically, SSP/AP DLLs are stored in the %systemroot%/system32 directory.</span></span> <span data-ttu-id="ce78d-110">S’il s’agit du chemin d’accès à votre DLL SSP/AP personnalisée, n’incluez pas le chemin d’accès en tant que partie du nom de la DLL.</span><span class="sxs-lookup"><span data-stu-id="ce78d-110">If this is the path to your custom SSP/AP DLL then do not include the path as part of the DLL name.</span></span> <span data-ttu-id="ce78d-111">Toutefois, si la DLL se trouve dans un chemin d’accès différent, incluez le chemin d’accès complet à la DLL dans le nom.</span><span class="sxs-lookup"><span data-stu-id="ce78d-111">If, however, the DLL is in a different path, include the complete path to the DLL in the name.</span></span>

<span data-ttu-id="ce78d-112">Chaque fois que le système démarre, le LSA charge les dll SSP/AP dans cette liste et exécute la séquence d’initialisation décrite dans l' [initialisation du mode LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="ce78d-112">Each time the system starts, the LSA loads the SSP/AP DLLs in this list and performs the initialization sequence described in [LSA-Mode Initialization](lsa-mode-initialization.md).</span></span>

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a><span data-ttu-id="ce78d-113">Inscription d’un package de sécurité personnalisé en tant que SSP TLS par défaut</span><span class="sxs-lookup"><span data-stu-id="ce78d-113">Registering a custom security package as the default TLS SSP</span></span>

<span data-ttu-id="ce78d-114">Après avoir développé un fournisseur de support de sécurité TLS personnalisé et l’avoir inscrit comme décrit ci-dessus, vous devez également l’inscrire en tant que « SSP TLS par défaut ».</span><span class="sxs-lookup"><span data-stu-id="ce78d-114">After developing a custom TLS security support provider and registering it as described above, you must also register it as the “default TLS SSP.”</span></span> <span data-ttu-id="ce78d-115">Pour ce faire, renseignez le nom du package de votre SSP personnalisé sur les données de la valeur de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="ce78d-115">To do so, populate the package name of your custom SSP to the data of the following registry value:</span></span>

<span data-ttu-id="ce78d-116">**HKEY \_ Système d' \_ ordinateur local** \\ **système** de \\ **CurrentControlSet** \\ **contrôle** de l' \\ **autorité de certification** \\ **SSP TLS par défaut**</span><span class="sxs-lookup"><span data-stu-id="ce78d-116">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Default TLS SSP**</span></span>

<span data-ttu-id="ce78d-117">Les données de cette valeur de Registre sont le nom du package SSP, et non le nom de la dll.</span><span class="sxs-lookup"><span data-stu-id="ce78d-117">The data for this registry value is the package name of SSP, not the dll name.</span></span> <span data-ttu-id="ce78d-118">Le type de données est **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="ce78d-118">The data type for this is **REG\_SZ**.</span></span>

<span data-ttu-id="ce78d-119">Les applications en mode utilisateur qui utilisent « TLS TLS par défaut » utilisent la valeur par défaut inscrite ici.</span><span class="sxs-lookup"><span data-stu-id="ce78d-119">User mode applications which use “default TLS SSP” will use the default registered here.</span></span> <span data-ttu-id="ce78d-120">Les applications en mode noyau ou les applications en mode utilisateur qui utilisent le « fournisseur de protocole de sécurité unifié Microsoft » ou d’autres noms de SSP TLS spécifiques ne seront pas affectés par cette modification.</span><span class="sxs-lookup"><span data-stu-id="ce78d-120">Kernel mode applications or user mode applications which use “Microsoft Unified Security Protocol Provider” or other specific TLS SSP names will not be impacted by this change.</span></span>

> [!Note]  
> <span data-ttu-id="ce78d-121">Ces informations de Registre se rapportent uniquement aux DLL SSP/AP.</span><span class="sxs-lookup"><span data-stu-id="ce78d-121">This registry information pertains to SSP/AP DLL's only.</span></span> <span data-ttu-id="ce78d-122">Pour plus d’informations sur l’inscription des fournisseurs de support de sécurité (SSP), consultez [écriture et installation d’un fournisseur de support de sécurité](writing-and-installing-a-security-support-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ce78d-122">For information about registering security support providers (SSPs), see [Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md).</span></span> <span data-ttu-id="ce78d-123">Pour plus d’informations sur les différences entre les dll SSP/AP et SSP, consultez [SSP/APS](ssp-aps-versus-ssps.md)et ssp.</span><span class="sxs-lookup"><span data-stu-id="ce78d-123">For information about the differences between SSP/AP and SSP DLLs, see [SSP/APs vs. SSPs](ssp-aps-versus-ssps.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ce78d-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ce78d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce78d-125">Restrictions concernant l’inscription et l’installation d’un package de sécurité</span><span class="sxs-lookup"><span data-stu-id="ce78d-125">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
