---
title: Blocage des commandes
description: Pour préserver l’intégrité des opérations, certaines commandes du module de plateforme sécurisée ne sont pas autorisées à être exécutées par les logiciels sur la plateforme.
ms.assetid: 47402a4a-5f8d-4648-b3ea-06c95b2a1fc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b9a302f12e7838240ee8bfeac1ea78a3884a1
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104381738"
---
# <a name="command-blocking"></a><span data-ttu-id="2ad7e-103">Blocage des commandes</span><span class="sxs-lookup"><span data-stu-id="2ad7e-103">Command Blocking</span></span>

<span data-ttu-id="2ad7e-104">Pour préserver l’intégrité des opérations, certaines commandes du module de plateforme sécurisée ne sont pas autorisées à être exécutées par les logiciels sur la plateforme.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-104">To preserve integrity of operations, certain TPM commands are not allowed to be executed by software on the platform.</span></span> <span data-ttu-id="2ad7e-105">Par exemple, certaines commandes sont exécutées uniquement par le logiciel système.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-105">For example, some commands are only executed by system software.</span></span> <span data-ttu-id="2ad7e-106">Lorsque le TBS bloque une commande, une erreur est renvoyée, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-106">When the TBS blocks a command, an error is returned as appropriate.</span></span> <span data-ttu-id="2ad7e-107">Par défaut, le TBS bloque les commandes qui peuvent avoir un impact sur la confidentialité, la sécurité et la stabilité du système.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-107">By default, the TBS blocks commands that could impact system privacy, security, and stability.</span></span> <span data-ttu-id="2ad7e-108">Le TBS suppose également que d’autres parties de la pile de logiciels peuvent limiter l’accès à certaines commandes aux entités autorisées.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-108">The TBS also assumes that other parts of the software stack may restrict access to certain commands to authorized entities.</span></span>

<span data-ttu-id="2ad7e-109">Pour les commandes de la version 1,2 du module de plateforme sécurisée, il existe trois listes de commandes bloquées : une liste contrôlée par la stratégie de groupe, une liste contrôlée par les administrateurs locaux et une liste par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-109">For TPM version 1.2 commands, there are three lists of blocked commands: a list controlled by group policy, a list controlled by local administrators, and a default list.</span></span> <span data-ttu-id="2ad7e-110">Une commande TPM est bloquée si elle figure sur une liste.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-110">A TPM command is blocked if it is on any of the lists.</span></span> <span data-ttu-id="2ad7e-111">Toutefois, il existe des indicateurs de stratégie de groupe pour permettre au TBS d’ignorer la liste locale et la liste par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-111">However, there are group policy flags to allow the TBS to ignore the local list and the default list.</span></span> <span data-ttu-id="2ad7e-112">Les indicateurs de stratégie de groupe peuvent être modifiés directement ou accessibles par le biais de l’éditeur d’objets stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-112">The group policy flags can be edited directly or accessed through the Group Policy Object Editor.</span></span>

> [!Note]  
> <span data-ttu-id="2ad7e-113">La liste des commandes bloquées localement n’est pas conservée après une mise à niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-113">The list of locally blocked commands is not preserved after an upgrade to the operating system.</span></span> <span data-ttu-id="2ad7e-114">Les commandes qui sont bloquées dans la liste stratégie de groupe sont conservées.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-114">Commands that are blocked on the Group Policy list are preserved.</span></span>

 

<span data-ttu-id="2ad7e-115">Pour les commandes de la version 2,0 du module de plateforme sécurisée, la logique de blocage est inversée. elle utilise une liste de commandes autorisées.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-115">For TPM version 2.0 commands, the logic for blocking is inverted; it uses a list of allowed commands.</span></span> <span data-ttu-id="2ad7e-116">Cette logique bloquera automatiquement les commandes qui n’étaient pas connues lors de la première création de la liste.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-116">This logic will automatically block commands that were not known when the list was first made.</span></span> <span data-ttu-id="2ad7e-117">Lorsque des commandes sont ajoutées à la spécification du module de plateforme sécurisée après la livraison d’une version de Windows, ces nouvelles commandes sont automatiquement bloquées.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-117">When commands are added to the TPM specification after a version of Windows has shipped, these new commands are automatically blocked.</span></span> <span data-ttu-id="2ad7e-118">Seule une mise à jour du Registre ajoute ces nouvelles commandes à la liste des commandes autorisées.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-118">Only an update of the registry will add these new commands to the list of allowed commands.</span></span>

<span data-ttu-id="2ad7e-119">À compter de Windows 10 1809 (Windows Server 2019), les commandes TPM 2,0 autorisées ne peuvent plus être manipulées via les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-119">Starting with Windows 10 1809 (Windows Server 2019), allowed TPM 2.0 commands can no longer be manipulated through registry settings.</span></span> <span data-ttu-id="2ad7e-120">Pour ces versions de Windows 10, les commandes TPM 2,0 autorisées sont fixes dans le pilote du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-120">For these Windows 10 versions, the allowed TPM 2.0 commands are fixed in the TPM driver.</span></span> <span data-ttu-id="2ad7e-121">Les commandes TPM 1,2 peuvent toujours être bloquées et débloquées par le biais de modifications du Registre.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-121">TPM 1.2 commands can still be blocked and unblocked through registry changes.</span></span> 

## <a name="direct-registry-access"></a><span data-ttu-id="2ad7e-122">Accès direct au registre</span><span class="sxs-lookup"><span data-stu-id="2ad7e-122">Direct Registry Access</span></span>

<span data-ttu-id="2ad7e-123">Les indicateurs de stratégie de groupe se trouvent sous la clé de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **TPM** \\ **BlockedCommands**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-123">The Group Policy flags are under registry key **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Tpm**\\**BlockedCommands**.</span></span>

<span data-ttu-id="2ad7e-124">Pour déterminer les listes à utiliser pour bloquer les commandes TPM, deux valeurs **DWORD** sont utilisées comme indicateurs booléens :</span><span class="sxs-lookup"><span data-stu-id="2ad7e-124">To determine which lists should be used to block TPM commands, there are two **DWORD** values that are used as Boolean flags:</span></span>

-   <span data-ttu-id="2ad7e-125">"IgnoreDefaultList"</span><span class="sxs-lookup"><span data-stu-id="2ad7e-125">"IgnoreDefaultList"</span></span>

    <span data-ttu-id="2ad7e-126">Si SET (la valeur existe et est différent de zéro), le TBS ignore la liste par défaut des commandes bloquées.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-126">If set (value exists and is nonzero), the TBS ignores the default blocked-commands list.</span></span>

-   <span data-ttu-id="2ad7e-127">"IgnoreLocalList"</span><span class="sxs-lookup"><span data-stu-id="2ad7e-127">"IgnoreLocalList"</span></span>

    <span data-ttu-id="2ad7e-128">Si SET (la valeur existe et est différent de zéro), le TBS ignore la liste locale des commandes bloquées.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-128">If set (value exists and is nonzero), the TBS ignores the local blocked-commands list.</span></span>

## <a name="group-policy-object-editor"></a><span data-ttu-id="2ad7e-129">Éditeur d'objets de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2ad7e-129">Group Policy Object Editor</span></span>

<span data-ttu-id="2ad7e-130">**Pour accéder à l’éditeur d’objets stratégie de groupe**</span><span class="sxs-lookup"><span data-stu-id="2ad7e-130">**To access the Group Policy object editor**</span></span>

1.  <span data-ttu-id="2ad7e-131">Cliquez sur **Start**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-131">Click **Start**.</span></span>
2.  <span data-ttu-id="2ad7e-132">Cliquez sur **Exécuter**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-132">Click **Run**.</span></span>
3.  <span data-ttu-id="2ad7e-133">Dans la zone **Ouvrir** , tapez **gpedit.msc**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-133">In the **Open** box, type **gpedit.msc**.</span></span> <span data-ttu-id="2ad7e-134">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-134">Click **OK**.</span></span> <span data-ttu-id="2ad7e-135">L’éditeur d’objets de stratégie de groupe s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-135">The Group Policy object editor opens.</span></span>
4.  <span data-ttu-id="2ad7e-136">Développez Configuration de l' **ordinateur**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-136">Expand **Computer Configuration**.</span></span>
5.  <span data-ttu-id="2ad7e-137">Développez **modèles d’administration**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-137">Expand **Administrative Templates**.</span></span>
6.  <span data-ttu-id="2ad7e-138">Développez **système**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-138">Expand **System**.</span></span>
7.  <span data-ttu-id="2ad7e-139">Développez **Services module de plateforme sécurisée (TPM)**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-139">Expand **Trusted Platform Module Services**.</span></span>

<span data-ttu-id="2ad7e-140">Les listes de commandes TPM 1.2 bloquées spécifiques peuvent être modifiées directement aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-140">The lists of specific blocked TPM1.2 commands can be edited directly in the following locations.</span></span>

-   <span data-ttu-id="2ad7e-141">Liste des stratégies de groupe :</span><span class="sxs-lookup"><span data-stu-id="2ad7e-141">Group policy list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Policies
             Microsoft
                Tpm
                   BlockedCommands
                      List
    ```

-   <span data-ttu-id="2ad7e-142">Liste locale :</span><span class="sxs-lookup"><span data-stu-id="2ad7e-142">Local list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                SharedAccess
                   Parameters
                      Tpm
                         BlockedCommands
                            List
    ```

-   <span data-ttu-id="2ad7e-143">Liste par défaut :</span><span class="sxs-lookup"><span data-stu-id="2ad7e-143">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                BlockedCommands
                   List
    ```

<span data-ttu-id="2ad7e-144">Sous chacune de ces clés de Registre figure une liste de valeurs de registre de type de Registre \_ sz.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-144">Under each of these registry keys, there is a list of registry values of REG\_SZ type.</span></span> <span data-ttu-id="2ad7e-145">Chaque valeur représente une commande TPM bloquée.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-145">Each value represents a blocked TPM command.</span></span> <span data-ttu-id="2ad7e-146">Chaque clé de registre a un champ « nom de la valeur » et un champ « données de valeur ».</span><span class="sxs-lookup"><span data-stu-id="2ad7e-146">Each registry key has a "Value name" field and a "Value data" field.</span></span> <span data-ttu-id="2ad7e-147">Les deux champs (« nom de la valeur » et « données de valeur ») doivent correspondre exactement à la valeur décimale du numéro de commande du module de plateforme sécurisée à bloquer.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-147">Both fields ("Value Name" and "Value data"), should exactly match the decimal value of the TPM command ordinal to be blocked.</span></span>

<span data-ttu-id="2ad7e-148">La liste des commandes TPM 2,0 spécifiques autorisées peut être modifiée directement à l’emplacement suivant.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-148">The list of specific allowed TPM 2.0 commands can be edited directly in the following location.</span></span> <span data-ttu-id="2ad7e-149">Sous la clé de Registre figure la liste des valeurs de Registre du type de Registre \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-149">Under the registry key, there is a list of registry values of REG\_DWORD type.</span></span> <span data-ttu-id="2ad7e-150">Chaque valeur représente une commande TPM 2,0 autorisée.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-150">Each value represents an allowed TPM 2.0 command.</span></span> <span data-ttu-id="2ad7e-151">Chaque valeur de registre a un **nom** et un champ de **valeur** .</span><span class="sxs-lookup"><span data-stu-id="2ad7e-151">Each registry value has a **name** and a **value** field.</span></span> <span data-ttu-id="2ad7e-152">Le **nom** correspond à l’ordinal de commande TPM 2,0 hexadécimal qui doit être autorisé.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-152">The **name** matches the hexadecimal TPM 2.0 command ordinal that should be allowed.</span></span> <span data-ttu-id="2ad7e-153">La **valeur est 1** si la commande est autorisée.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-153">The **value** has a value of 1 if the command is allowed.</span></span> <span data-ttu-id="2ad7e-154">Si l’ordinal d’une commande n’est pas présent ou a la valeur 0, la commande est bloquée.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-154">If a command ordinal is not present or has a value of 0, the command will be blocked.</span></span>

-   <span data-ttu-id="2ad7e-155">Liste par défaut :</span><span class="sxs-lookup"><span data-stu-id="2ad7e-155">Default list:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Tpm
                AllowedW8Commands
                   List
    ```

<span data-ttu-id="2ad7e-156">Pour Windows 8, Windows Server 2012 et versions ultérieures, les clés de Registre **BlockedCommands** et **AllowedW8Commands** déterminent respectivement les commandes TPM bloquées ou autorisées pour les comptes d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-156">For Windows 8, Windows Server 2012 and later, the **BlockedCommands** and **AllowedW8Commands** registry keys respectively determine the blocked or allowed TPM commands for administrator accounts.</span></span> <span data-ttu-id="2ad7e-157">Les comptes d’utilisateur disposent respectivement d’une liste de commandes TPM bloquées ou autorisées dans les clés de Registre **BlockedUserCommands** et **AllowedW8UserCommands** .</span><span class="sxs-lookup"><span data-stu-id="2ad7e-157">User accounts have a list of blocked or allowed TPM commands in the **BlockedUserCommands** and **AllowedW8UserCommands** registry keys respectively.</span></span> <span data-ttu-id="2ad7e-158">Dans Windows 10, version 1607, de nouvelles clés de Registre ont été introduites pour les applications AppContainer : **BlockedAppContainerCommands** et **AllowedW8AppContainerCommands**.</span><span class="sxs-lookup"><span data-stu-id="2ad7e-158">In Windows 10, version 1607, new registry keys have been introduces for AppContainer applications: **BlockedAppContainerCommands** and **AllowedW8AppContainerCommands**.</span></span>

 

 




