---
description: Windows Installer les développeurs peuvent créer des outils qui permettent aux utilisateurs finaux d’utiliser des modules de fusion configurables.
ms.assetid: 5857b788-f1dd-41d0-b0ee-0872494e3c2c
title: Ajout de la fonctionnalité de configuration de module à un outil de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba04d297ad93cffc553670c648577f650cd21407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756255"
---
# <a name="adding-module-configuration-capability-to-a-merge-tool"></a><span data-ttu-id="b3777-103">Ajout de la fonctionnalité de configuration de module à un outil de fusion</span><span class="sxs-lookup"><span data-stu-id="b3777-103">Adding Module Configuration Capability to a Merge Tool</span></span>

<span data-ttu-id="b3777-104">Pour permettre aux utilisateurs finaux d’utiliser des modules de fusion configurables, vous pouvez créer des outils de fusion et de configuration pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3777-104">To enable end users to use configurable merge modules, you can author merge and configuration tools to do the following:</span></span>

-   <span data-ttu-id="b3777-105">Les outils de fusion doivent appeler les fonctions de Mergemod.dll version 2,0 pour fusionner le module.</span><span class="sxs-lookup"><span data-stu-id="b3777-105">Merge tools should call the functions in Mergemod.dll version 2.0 to merge the module.</span></span> <span data-ttu-id="b3777-106">Les versions antérieures de Mergemod.dll ne peuvent pas être utilisées pour configurer des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="b3777-106">Earlier versions of Mergemod.dll cannot be used to configure merge modules.</span></span>
-   <span data-ttu-id="b3777-107">Les applications de configuration clientes doivent interagir avec l’utilisateur du module de fusion pour collecter les sélections d’éléments configurables par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3777-107">Client configuration applications should interact with the merge module user to collect the user selections for configurable items.</span></span>
-   <span data-ttu-id="b3777-108">Les outils de fusion doivent exposer les informations de configuration créées dans le module de fusion à l’application cliente afin que le client puisse utiliser ces informations pour interroger l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3777-108">Merge tools should expose configuration information authored into the merge module to the client application so that the client can use this information to query the user.</span></span>
-   <span data-ttu-id="b3777-109">Lorsqu’un outil de fusion rencontre un élément configurable pendant une fusion, il doit appeler l’outil de configuration du client pour les informations de personnalisation obtenues auprès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3777-109">When a merge tool encounters a configurable item during a merge, it should call the client configuration tool for customization information obtained from the user.</span></span> <span data-ttu-id="b3777-110">L’outil de fusion doit effectuer les modifications spécifiées dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="b3777-110">The merge tool should make the specified changes to the merge module.</span></span>
-   <span data-ttu-id="b3777-111">Les applications de configuration doivent permettre à l’utilisateur de fournir des choix pour les éléments configurables, mais il n’est pas nécessaire que tous les choix soient révélés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b3777-111">Configuration applications should enable the user to provide choices for configurable items, but all the possible choices do not need to be revealed to the user.</span></span> <span data-ttu-id="b3777-112">L’outil de fusion peut utiliser des valeurs par défaut pour les éléments configurables que l’utilisateur ne sélectionne pas.</span><span class="sxs-lookup"><span data-stu-id="b3777-112">The merge tool can use default values for configurable items that the user does not select.</span></span>
-   <span data-ttu-id="b3777-113">Si un utilisateur ne fournit pas d’informations de personnalisation, les outils de fusion doivent utiliser les valeurs de configuration par défaut spécifiées dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="b3777-113">If a user does not provide customization information, merge tools should use the default configuration values that are specified in the merge module.</span></span>
-   <span data-ttu-id="b3777-114">Une fois qu’un utilisateur a effectué les sélections spécifiques à l’outil de configuration, l’outil de fusion appelle Mergemod.dll pour effectuer la fusion.</span><span class="sxs-lookup"><span data-stu-id="b3777-114">After a user gives the configuration tool specific selections, the merge tool calls Mergemod.dll to perform the merge.</span></span>

 

 



