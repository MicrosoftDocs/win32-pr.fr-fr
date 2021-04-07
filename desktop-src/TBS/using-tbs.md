---
title: Utilisation de TBS
description: Chaque commande soumise au TBS est associée à une entité spécifique. Pour ce faire, vous devez créer un ou plusieurs contextes pour une entité, qui sont ensuite associés à chaque commande suivante soumise par cette entité.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TPM base services TBS, exemples
- Services de base du module de plateforme sécurisée (TPM), utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940013"
---
# <a name="using-tbs"></a><span data-ttu-id="d9a2e-106">Utilisation de TBS</span><span class="sxs-lookup"><span data-stu-id="d9a2e-106">Using TBS</span></span>

<span data-ttu-id="d9a2e-107">La fonctionnalité des services de base du module de plateforme sécurisée est divisée en quatre zones fonctionnelles :</span><span class="sxs-lookup"><span data-stu-id="d9a2e-107">The TPM Base Services feature is divided into four functional areas:</span></span>

-   [<span data-ttu-id="d9a2e-108">Virtualisation des ressources</span><span class="sxs-lookup"><span data-stu-id="d9a2e-108">Resource Virtualization</span></span>](resource-virtualization.md)
-   [<span data-ttu-id="d9a2e-109">Planification des commandes</span><span class="sxs-lookup"><span data-stu-id="d9a2e-109">Command Scheduling</span></span>](command-scheduling.md)
-   [<span data-ttu-id="d9a2e-110">Gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="d9a2e-110">Power Management</span></span>](power-management.md)
-   [<span data-ttu-id="d9a2e-111">Blocage des commandes</span><span class="sxs-lookup"><span data-stu-id="d9a2e-111">Command Blocking</span></span>](command-blocking.md)

<span data-ttu-id="d9a2e-112">Pour vous assurer que les différentes entités ne peuvent pas accéder aux ressources de l’autre, chaque commande soumise à la TBS est associée à une entité spécifique.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-112">To ensure that different entities cannot access each other's resources, each command submitted to the TBS is associated with a specific entity.</span></span> <span data-ttu-id="d9a2e-113">Pour ce faire, vous devez créer un ou plusieurs contextes pour une entité, qui sont ensuite associés à chaque commande suivante soumise par cette entité.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-113">This is accomplished by creating one or more contexts for an entity, which are then associated with each subsequent command submitted by that entity.</span></span> <span data-ttu-id="d9a2e-114">Chaque commande comprend un objet Context, qui permet au TBS d’exécuter des commandes TPM dans le contexte approprié.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-114">Each command includes a context object, which allows the TBS to execute TPM commands under the appropriate context.</span></span> <span data-ttu-id="d9a2e-115">Tous les objets créés par les commandes sont vidés du module de plateforme sécurisée (TPM) lorsque le contexte est fermé.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-115">All objects created by commands are flushed from the TPM when the context is closed.</span></span>

<span data-ttu-id="d9a2e-116">Une entité crée le contexte avant d’accéder au service TBS et de maintenir le contexte jusqu’à ce que l’exécution des accès TBS soit terminée.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-116">An entity creates the context before it first accesses the TBS and maintains the context until it is finished performing TBS accesses.</span></span> <span data-ttu-id="d9a2e-117">Par exemple, dans le cas d’un TSS, la fonctionnalité de services de base (TCS) du TSS crée un contexte TBS au démarrage, et conserve ce contexte actif jusqu’à ce qu’il s’arrête.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-117">For example, in the case of a TSS, the TCG core services (TCS) feature of the TSS would create a TBS context when it starts up, and it would keep that context active until it shuts down.</span></span>

<span data-ttu-id="d9a2e-118">Pour Windows Server 2008 et Windows Vista, le service TBS restreint l’accès à l’API TBS aux comptes administrateurs, NT autorité \\ LocalService et autorité NT \\ NetworkService.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-118">For Windows Server 2008 and Windows Vista, the TBS restricts access to the TBS API to the Administrators, NT AUTHORITY\\LocalService, and NT AUTHORITY\\NetworkService accounts.</span></span> <span data-ttu-id="d9a2e-119">Par défaut, ces comptes sont les seuls à pouvoir se connecter à TBS et à créer des contextes.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-119">By default, these accounts are the only ones that can connect to TBS and create contexts.</span></span> <span data-ttu-id="d9a2e-120">Les restrictions d’accès peuvent être modifiées en créant un **accès** à la clé de Registre avec un nom de valeur de Registre String (**reg \_ SZ**) **SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d9a2e-120">Access restrictions can be modified by creating a registry key **Access** with a string (**REG\_SZ**) registry value name **SecurityDescriptor**</span></span> <dl> <dt>

<span data-ttu-id="d9a2e-121">Type de données</span><span class="sxs-lookup"><span data-stu-id="d9a2e-121">Data type</span></span>
</dt> <dd><span data-ttu-id="d9a2e-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d9a2e-122">REG_SZ</span></span></dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

<span data-ttu-id="d9a2e-123">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d9a2e-123">Example:</span></span>

<span data-ttu-id="d9a2e-124">**O :BAG : BAD : (A ;; 0 x00000001;;; BA) (A ;; 0 x00000001;;; NS) (A ;; 0 x00000001;;; LS**</span><span class="sxs-lookup"><span data-stu-id="d9a2e-124">**O:BAG:BAD:(A;;0x00000001;;;BA)(A;;0x00000001;;;NS)(A;;0x00000001;;;LS)**</span></span>

<span data-ttu-id="d9a2e-125">Par défaut, le nombre maximal de contextes pris en charge par le TBS est de 25.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-125">By default, the maximum number of contexts supported by the TBS is 25.</span></span> <span data-ttu-id="d9a2e-126">Ce nombre peut être modifié en créant ou en modifiant une valeur de Registre **DWORD** nommée **MaxContexts** sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **TPM**.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-126">This number can be altered by creating or modifying a **DWORD** registry value named **MaxContexts** under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Tpm**.</span></span> <span data-ttu-id="d9a2e-127">L’utilisation du contexte TBS en temps réel peut être observée à l’aide de l’outil Analyseur de performances pour suivre le nombre de contextes TBS.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-127">Real-time TBS context usage can be observed by using the performance monitor tool to track the number of TBS contexts.</span></span>

<span data-ttu-id="d9a2e-128">Pour Windows 8, Windows Server 2012 et versions ultérieures, le TBS autorise l’accès aux utilisateurs et aux administrateurs standard.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-128">For Windows 8, Windows Server 2012 and later, the TBS allows access to standard users and administrators.</span></span> <span data-ttu-id="d9a2e-129">Les clés de Registre **SecurityDescriptor** et **MaxContexts** sont devenues obsolètes.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-129">The **SecurityDescriptor** and **MaxContexts** registry keys became obsolete.</span></span> <span data-ttu-id="d9a2e-130">Pour Windows 8, Windows Server 2012 et versions ultérieures, le TBS restreint l’accès à certaines commandes à l’aide du blocage de commande.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-130">For Windows 8, Windows Server 2012 and later, the TBS restricts access to certain commands using Command Blocking.</span></span>

<span data-ttu-id="d9a2e-131">Pour Windows 10, la version 1607, le TBS autorise l’accès à partir des applications AppContainer.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-131">For Windows 10, version 1607, the TBS allows access from AppContainer applications.</span></span> <span data-ttu-id="d9a2e-132">Pour chaque version de module de plateforme sécurisée, les clés **BlockedAppContainerCommands** et **AllowedW8AppContainerCommands** ont été ajoutées avec les listes de correspondance des commandes TPM bloquées et autorisées, respectivement.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-132">For each TPM version, the keys **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands** have been added with the matching lists of blocked and allowed TPM commands, respectively.</span></span>

<span data-ttu-id="d9a2e-133">Pour Windows 10, version 1803, les clés de Registre sous **AllowedW8AppContainerCommands** ne sont plus prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d9a2e-133">For Windows 10, version 1803, the registry keys under **AllowedW8AppContainerCommands** are no longer supported.</span></span>

 

 




