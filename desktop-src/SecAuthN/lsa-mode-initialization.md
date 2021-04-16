---
description: Lorsque le système informatique est démarré, l’autorité de sécurité locale (LSA) charge automatiquement toutes les dll du package d’authentification/fournisseur de services de sécurité (SSP/AP) inscrit dans son espace de processus. Les illustrations suivantes illustrent le processus d’initialisation.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: Initialisation du mode LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529740"
---
# <a name="lsa-mode-initialization"></a><span data-ttu-id="542a9-104">Initialisation du mode LSA</span><span class="sxs-lookup"><span data-stu-id="542a9-104">LSA Mode Initialization</span></span>

<span data-ttu-id="542a9-105">Lorsque le système informatique est démarré, l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) charge automatiquement toutes les dll du [](../secgloss/s-gly.md) / [*package d’authentification*](../secgloss/a-gly.md) du fournisseur de support de sécurité (SSP/AP) inscrit dans son espace de processus.</span><span class="sxs-lookup"><span data-stu-id="542a9-105">When the computer system is started, the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) automatically loads all registered [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) DLLs into its process space.</span></span> <span data-ttu-id="542a9-106">Les illustrations suivantes illustrent le processus d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="542a9-106">The following illustrations show the initialization process.</span></span>

> [!Note]  
> <span data-ttu-id="542a9-107">« Kerberos » représente le SSP/AP Microsoft [*Kerberos*](../secgloss/k-gly.md) , et « mon SSP/AP » représente un SSP/AP personnalisé qui contient deux packages de sécurité personnalisés.</span><span class="sxs-lookup"><span data-stu-id="542a9-107">"Kerberos" represents the Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, and "My SSP/AP" represents a custom SSP/AP that contains two custom security packages.</span></span>

 

![initialisation du mode LSA](images/lsamode1.png)

<span data-ttu-id="542a9-109">Au démarrage, l’autorité LSA appelle la fonction [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) dans chaque fournisseur de services partagés/AP pour obtenir des pointeurs vers les fonctions implémentées par chaque [*package de sécurité*](../secgloss/s-gly.md) dans la dll.</span><span class="sxs-lookup"><span data-stu-id="542a9-109">At startup, the LSA calls the [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) function in each SSP/AP to obtain pointers to the functions implemented by each [*security package*](../secgloss/s-gly.md) in the DLL.</span></span> <span data-ttu-id="542a9-110">Les pointeurs de fonction sont passés à l’autorité LSA dans un tableau de structures de [**\_ \_ table de fonctions SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) .</span><span class="sxs-lookup"><span data-stu-id="542a9-110">The function pointers are passed to the LSA in an array of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures.</span></span>

![l’autorité LSA appelle splsamodeinitialize pour recevoir des pointeurs de fonction](images/lsamode2.png)

<span data-ttu-id="542a9-112">Après avoir reçu l’ensemble de structures de [**\_ \_ table de fonctions SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) , l’autorité LSA appelle la fonction de [**réinitialisation**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) de chaque package de sécurité.</span><span class="sxs-lookup"><span data-stu-id="542a9-112">After receiving the set of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures, the LSA calls each security package's [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) function.</span></span> <span data-ttu-id="542a9-113">Le LSA utilise cet appel de fonction pour passer chaque package de sécurité à une structure de [**\_ table de \_ fonctions \_ LSA SECPKG**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) , qui contient des pointeurs vers les fonctions de prise en charge LSA disponibles pour les packages de sécurité.</span><span class="sxs-lookup"><span data-stu-id="542a9-113">The LSA uses this function call to pass each security package an [**LSA\_SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) structure, which contains pointers to the LSA support functions available to security packages.</span></span> <span data-ttu-id="542a9-114">En plus de stocker les pointeurs dans les fonctions de prise en charge LSA, les packages de sécurité personnalisés doivent utiliser leur implémentation de la fonction de **réinitialisation** pour effectuer tout traitement relatif à l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="542a9-114">In addition to storing the pointers to the LSA support functions, custom security packages should use their implementation of the **SpInitialize** function to perform any initialization-related processing.</span></span>

<span data-ttu-id="542a9-115">Pour obtenir la liste des fonctions de prise en charge LSA disponibles pour les packages de sécurité en mode LSA, voir [LSA Functions called by SSP/APS](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="542a9-115">For a list of the LSA support functions available to LSA-mode security packages, see [LSA Functions Called by SSP/APs](authentication-functions.md).</span></span>

<span data-ttu-id="542a9-116">Pour plus d’informations sur l’inscription d’une DLL SSP/AP, consultez [inscription de dll SSP/AP](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="542a9-116">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

 

 
