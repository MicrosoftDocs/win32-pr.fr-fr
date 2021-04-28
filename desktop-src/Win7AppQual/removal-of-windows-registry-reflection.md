---
description: Suppression de la réflexion du Registre Windows
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Suppression de la réflexion du Registre Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeab0109cbbac988c89d6add91fa899cea9169ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116257"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="7ed1b-103">Suppression de la réflexion du Registre Windows</span><span class="sxs-lookup"><span data-stu-id="7ed1b-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="7ed1b-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="7ed1b-104">Platform</span></span>

<span data-ttu-id="7ed1b-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ed1b-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="7ed1b-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ed1b-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="7ed1b-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="7ed1b-107">Feature Impact</span></span>

 <span data-ttu-id="7ed1b-108">**Gravité** -faible</span><span class="sxs-lookup"><span data-stu-id="7ed1b-108">**Severity** - Low</span></span>  
<span data-ttu-id="7ed1b-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="7ed1b-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="7ed1b-110">Description</span><span class="sxs-lookup"><span data-stu-id="7ed1b-110">Description</span></span>

<span data-ttu-id="7ed1b-111">Le processus de réflexion du Registre copie les clés de Registre et les valeurs entre deux vues du Registre pour les maintenir synchronisées. Dans les précédentes installations 64 bits de Windows, le processus reflétait un sous-ensemble des clés de Registre redirigées entre les vues 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="7ed1b-112">Toutefois, l’implémentation de cela provoquait des incohérences dans l’état du Registre.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="7ed1b-113">(Pour plus d’informations sur la réflexion du Registre, consultez l’article MSDN correspondant dans la section *liens vers d’autres ressources* ci-dessous.)</span><span class="sxs-lookup"><span data-stu-id="7ed1b-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="7ed1b-114">À compter de Windows 7, nous avons supprimé complètement la réflexion du Registre et fusionné les clés qui ont utilisé pour être reflétées :</span><span class="sxs-lookup"><span data-stu-id="7ed1b-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="7ed1b-115">HKEY \_ local \_ machine \\ classes de logiciels \\</span><span class="sxs-lookup"><span data-stu-id="7ed1b-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="7ed1b-116">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="7ed1b-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="7ed1b-117">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="7ed1b-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="7ed1b-118">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ OLE</span><span class="sxs-lookup"><span data-stu-id="7ed1b-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="7ed1b-119">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ RPC</span><span class="sxs-lookup"><span data-stu-id="7ed1b-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="7ed1b-120">\_Classes de \\ \* \\ logiciels \\ de HKEY Users</span><span class="sxs-lookup"><span data-stu-id="7ed1b-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="7ed1b-121">\_Classes HKEY Users \\ \* \_</span><span class="sxs-lookup"><span data-stu-id="7ed1b-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="7ed1b-122">En fait, cela fournit le même comportement de réflexion, car les modifications apportées immédiatement à ces clés sont disponibles pour les applications 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="7ed1b-123">Les clés qui ont été représentées de manière conditionnelle restent fractionnées :</span><span class="sxs-lookup"><span data-stu-id="7ed1b-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="7ed1b-124">HKEY \_ local \_ machine \\ classes de logiciels \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="7ed1b-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="7ed1b-125">HKEY \_ local \_ machine \\ classes logicielles ( \\ \\ interface)</span><span class="sxs-lookup"><span data-stu-id="7ed1b-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="7ed1b-126">\_CLSID des \\ \* \\ classes de logiciels \\ \\ de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="7ed1b-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="7ed1b-127">HKEY \_ Users, \\ \* \\ classes de logiciels ( \\ \\ interface)</span><span class="sxs-lookup"><span data-stu-id="7ed1b-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="7ed1b-128">\_CLSID des \\ \* \_ classes \\ de l’utilisateur HKEY</span><span class="sxs-lookup"><span data-stu-id="7ed1b-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="7ed1b-129">\_ \\ \* \_ Interface classes de HKEY Users \\</span><span class="sxs-lookup"><span data-stu-id="7ed1b-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="7ed1b-130">Ils sont utilisés pour conserver les données qui ne doivent pas être partagées entre les applications 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7ed1b-131">Manifestation</span><span class="sxs-lookup"><span data-stu-id="7ed1b-131">Manifestation</span></span>

<span data-ttu-id="7ed1b-132">Les clés CLSID et interface de la liste ci-dessus ne sont plus reflétées alors qu’elles sont toujours redirigées.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="7ed1b-133">Bien qu’il s’agit du comportement souhaité dans la plupart des cas, il est possible que les applications prennent une dépendance sur leur comportement réfléchi dans Vista.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="7ed1b-134">Les fonctions permettant aux applications de contrôler la réflexion (RegDisableReflectionKey et RegEnableReflectionKey) ne sont pas des opérations dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="7ed1b-135">Atténuation de l’impact</span><span class="sxs-lookup"><span data-stu-id="7ed1b-135">Mitigation of Impact</span></span>

<span data-ttu-id="7ed1b-136">COM est le principal consommateur de la réflexion du Registre.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="7ed1b-137">COM et les autres consommateurs ont été mis à jour pour prendre en compte cette modification.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="7ed1b-138">Cette modification n’affecte pas les applications qui utilisent des API COM standard.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="7ed1b-139">Solution</span><span class="sxs-lookup"><span data-stu-id="7ed1b-139">Solution</span></span>

<span data-ttu-id="7ed1b-140">Appliquez l’une des options suivantes si vous vous fiez à la réflexion du Registre pour synchroniser les vues 32 bits et 64 bits :</span><span class="sxs-lookup"><span data-stu-id="7ed1b-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="7ed1b-141">Créer des clés dans les deux vues explicitement lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="7ed1b-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="7ed1b-142">Déplacer les clés en dehors de l’étendue des clés réfléchies</span><span class="sxs-lookup"><span data-stu-id="7ed1b-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="7ed1b-143">Vérifier les deux vues du registre lors de l’interrogation d’une clé réfléchie</span><span class="sxs-lookup"><span data-stu-id="7ed1b-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="7ed1b-144">**Remarque :** \_ \_ Les indicateurs Key WOW64 32KEY et Key \_ WOW64 \_ 64KEY ne peuvent pas être combinés</span><span class="sxs-lookup"><span data-stu-id="7ed1b-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="7ed1b-145">Appliquez l’une des options suivantes si vous vous fiez aux fonctions RegDisableReflectionKey pour désactiver la réflexion du Registre :</span><span class="sxs-lookup"><span data-stu-id="7ed1b-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="7ed1b-146">Créer des clés dans les deux vues explicitement lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="7ed1b-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="7ed1b-147">Déplacer les clés en dehors de l’étendue des clés réfléchies</span><span class="sxs-lookup"><span data-stu-id="7ed1b-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="7ed1b-148">Utiliser des sous-clés spécifiques à la plateforme (telles que x86, amd64 et ia64) pour séparer les données de bits spécifiques</span><span class="sxs-lookup"><span data-stu-id="7ed1b-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="7ed1b-149">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="7ed1b-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="7ed1b-150">Article sur la réflexion du Registre</span><span class="sxs-lookup"><span data-stu-id="7ed1b-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="7ed1b-151">Liste des clés redirigées dans l’article redirecteur du Registre</span><span class="sxs-lookup"><span data-stu-id="7ed1b-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="7ed1b-152">Meilleures pratiques pour WOW64</span><span class="sxs-lookup"><span data-stu-id="7ed1b-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="7ed1b-153">Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.</span><span class="sxs-lookup"><span data-stu-id="7ed1b-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
