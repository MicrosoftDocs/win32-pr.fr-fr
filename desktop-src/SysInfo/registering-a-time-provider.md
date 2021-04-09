---
description: Le système charge un fournisseur de temps en fonction de ses informations de configuration stockées dans le registre.
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: Inscription d’un fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865706"
---
# <a name="registering-a-time-provider"></a><span data-ttu-id="dc789-103">Inscription d’un fournisseur de temps</span><span class="sxs-lookup"><span data-stu-id="dc789-103">Registering a Time Provider</span></span>

<span data-ttu-id="dc789-104">Le système charge un fournisseur de temps en fonction de ses informations de configuration stockées dans le registre.</span><span class="sxs-lookup"><span data-stu-id="dc789-104">The system loads a time provider based on its configuration information stored in the registry.</span></span> <span data-ttu-id="dc789-105">Chaque fournisseur de temps doit créer la clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="dc789-105">Each time provider should create the following registry key:</span></span>

<span data-ttu-id="dc789-106">**HKEY \_ \_ \\ Système d’ordinateur local** services de \\ **CurrentControlSet** \\  \\  \\ **TimeProviders** \\ *providerName*</span><span class="sxs-lookup"><span data-stu-id="dc789-106">**HKEY\_LOCAL\_MACHINE\\System**\\**CurrentControlSet**\\**Services**\\**W32Time**\\**TimeProviders**\\*ProviderName*</span></span>

<span data-ttu-id="dc789-107">Le tableau suivant décrit les valeurs qui doivent exister dans la clé de chaque fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dc789-107">The following table describes the values that must exist in each provider's key.</span></span>



| <span data-ttu-id="dc789-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc789-108">Value</span></span>             | <span data-ttu-id="dc789-109">Description</span><span class="sxs-lookup"><span data-stu-id="dc789-109">Description</span></span>                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc789-110">**DllName**</span><span class="sxs-lookup"><span data-stu-id="dc789-110">**DllName**</span></span>       | <span data-ttu-id="dc789-111">Nom de la DLL qui contient le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="dc789-111">The name of the DLL that contains the provider.</span></span> <span data-ttu-id="dc789-112">Cette valeur est du type **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="dc789-112">This value has the type **REG\_SZ**.</span></span>                                                                                                                                     |
| <span data-ttu-id="dc789-113">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="dc789-113">**Enabled**</span></span>       | <span data-ttu-id="dc789-114">Indique si le fournisseur doit être démarré.</span><span class="sxs-lookup"><span data-stu-id="dc789-114">Indicates whether the provider should be started.</span></span> <span data-ttu-id="dc789-115">Si la valeur est 1, le fournisseur est démarré.</span><span class="sxs-lookup"><span data-stu-id="dc789-115">If this value is 1, the provider is started.</span></span> <span data-ttu-id="dc789-116">Dans le cas contraire, le fournisseur n’est pas démarré.</span><span class="sxs-lookup"><span data-stu-id="dc789-116">Otherwise, the provider is not started.</span></span> <span data-ttu-id="dc789-117">Cette valeur est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="dc789-117">This value has the type **REG\_DWORD**.</span></span>                                           |
| <span data-ttu-id="dc789-118">**InputProvider**</span><span class="sxs-lookup"><span data-stu-id="dc789-118">**InputProvider**</span></span> | <span data-ttu-id="dc789-119">Indique si le fournisseur est un fournisseur d’entrée ou un fournisseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="dc789-119">Indicates whether the provider is an input provider or an output provider.</span></span> <span data-ttu-id="dc789-120">Si la valeur est 1, le fournisseur est un fournisseur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="dc789-120">If this value is 1, the provider is an input provider.</span></span> <span data-ttu-id="dc789-121">Dans le cas contraire, le fournisseur est un fournisseur de sortie.</span><span class="sxs-lookup"><span data-stu-id="dc789-121">Otherwise, the provider is an output provider.</span></span> <span data-ttu-id="dc789-122">Cette valeur est de type **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="dc789-122">This value has the type **REG\_DWORD**.</span></span> |



 

<span data-ttu-id="dc789-123">Le gestionnaire de fournisseurs de temps énumère les clés sous la clé **TimeProviders** et démarre chaque fournisseur activé.</span><span class="sxs-lookup"><span data-stu-id="dc789-123">The time provider manager enumerates the keys under the **TimeProviders** key and starts each enabled provider.</span></span> <span data-ttu-id="dc789-124">Les fournisseurs sont démarrés au démarrage du système et chaque fois qu’il y a des modifications de paramètres.</span><span class="sxs-lookup"><span data-stu-id="dc789-124">Providers are started at system startup and whenever there are parameter changes.</span></span>

<span data-ttu-id="dc789-125">Chaque fournisseur de temps peut également stocker des informations de configuration spécifiques à l’application dans le registre.</span><span class="sxs-lookup"><span data-stu-id="dc789-125">Each time provider can also store application-specific configuration information in the registry.</span></span>

 

 



