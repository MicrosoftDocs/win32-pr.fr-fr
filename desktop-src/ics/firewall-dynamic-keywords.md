---
title: Mots clés dynamiques de pare-feu
description: Vous utilisez les API de mots clés dynamiques de pare-feu pour gérer les adresses de mots clés dynamiques dans le pare-feu Windows Defender.
keywords:
- Mots clés dynamiques de pare-feu
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: e60526d8a7889af3173913774790bdd209121040
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681167"
---
# <a name="firewall-dynamic-keywords"></a><span data-ttu-id="d83a3-104">Mots clés dynamiques de pare-feu</span><span class="sxs-lookup"><span data-stu-id="d83a3-104">Firewall dynamic keywords</span></span>

<span data-ttu-id="d83a3-105">Vous utilisez les API de mots clés dynamiques de pare-feu pour gérer les *adresses de mots clés dynamiques* dans le [pare-feu Windows Defender](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span><span class="sxs-lookup"><span data-stu-id="d83a3-105">You use the firewall dynamic keywords APIs to manage *dynamic keyword addresses* in [Windows Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="d83a3-106">Une adresse de mot clé dynamique est utilisée pour créer un ensemble d’adresses IP auxquelles une ou plusieurs règles de pare-feu peuvent faire référence.</span><span class="sxs-lookup"><span data-stu-id="d83a3-106">A dynamic keyword address is used to create a set of IP addresses to which one or more firewall rules can refer.</span></span> <span data-ttu-id="d83a3-107">Les adresses de mots clés dynamiques prennent en charge IPv4 et IPv6.</span><span class="sxs-lookup"><span data-stu-id="d83a3-107">Dynamic keyword addresses support both IPv4 and IPv6.</span></span>

> [!NOTE]
> <span data-ttu-id="d83a3-108">Pour obtenir des informations de référence sur les API des API présentées dans cette rubrique, consultez [référence des mots clés dynamiques de pare-feu](firewall-dynamic-keywords-reference.md).</span><span class="sxs-lookup"><span data-stu-id="d83a3-108">For API reference content for the APIs introduced in this topic, see [Firewall dynamic keywords reference](firewall-dynamic-keywords-reference.md).</span></span>

## <a name="operations-on-dynamic-keyword-addresses"></a><span data-ttu-id="d83a3-109">Opérations sur les adresses de mots clés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d83a3-109">Operations on dynamic keyword addresses</span></span>

<span data-ttu-id="d83a3-110">Avec les API de mots clés dynamiques de pare-feu, vous pouvez effectuer les opérations suivantes.</span><span class="sxs-lookup"><span data-stu-id="d83a3-110">With the Firewall dynamic keywords APIs, you can perform the following operations.</span></span>

* <span data-ttu-id="d83a3-111">Ajouter des adresses de mots clés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d83a3-111">Add dynamic keyword addresses</span></span>
* <span data-ttu-id="d83a3-112">Supprimer les adresses de mots clés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d83a3-112">Delete dynamic keyword addresses</span></span>
* <span data-ttu-id="d83a3-113">Énumérer les adresses de mots clés dynamiques par ID ou par type</span><span class="sxs-lookup"><span data-stu-id="d83a3-113">Enumerate dynamic keyword addresses by ID, or by type</span></span>
* <span data-ttu-id="d83a3-114">Mettre à jour les adresses de mots clés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d83a3-114">Update dynamic keyword addresses</span></span>
* <span data-ttu-id="d83a3-115">S’abonner aux notifications de modification des adresses de mots clés dynamiques et les gérer</span><span class="sxs-lookup"><span data-stu-id="d83a3-115">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="d83a3-116">Il existe des exemples de code pour toutes ces opérations plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d83a3-116">There are code examples for all of those operations later in this topic.</span></span>

<span data-ttu-id="d83a3-117">Une fois que vous avez ajouté une adresse de mot clé dynamique, elle persiste entre les redémarrages.</span><span class="sxs-lookup"><span data-stu-id="d83a3-117">Once you've added a dynamic keyword address, it persists across reboots.</span></span> <span data-ttu-id="d83a3-118">Vous devez supprimer une adresse de mot clé dynamique une fois que vous avez fini d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="d83a3-118">You must delete a dynamic keyword address once you're done with the object.</span></span>

<span data-ttu-id="d83a3-119">Il existe deux classes d’adresses de mots clés dynamiques, comme décrit dans les deux sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="d83a3-119">There are two classes of dynamic keyword addresses, as described in the next two sections.</span></span>

## <a name="autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="d83a3-120">Résoudre automatiquement les adresses de mots clés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d83a3-120">AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="d83a3-121">Le premier type est *autosolve*, où le champ de *mot clé* représente un nom pouvant être résolu, et les adresses IP ne sont pas définies lors de la création.</span><span class="sxs-lookup"><span data-stu-id="d83a3-121">The first type is *AutoResolve*, where the *keyword* field represents a resolvable name, and the IP addresses aren't defined upon creation.</span></span>

<span data-ttu-id="d83a3-122">Ces objets sont conçus pour que leurs adresses IP soient résolues automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d83a3-122">These objects are intended to have their IP addresses resolved automatically.</span></span> <span data-ttu-id="d83a3-123">Autrement dit, pas via un administrateur au moment de la création de l’objet ; ni via le système d’exploitation lui-même.</span><span class="sxs-lookup"><span data-stu-id="d83a3-123">That is, not through an admin at object creation time; nor through the operating system (OS) itself.</span></span> <span data-ttu-id="d83a3-124">Un composant en dehors du service de pare-feu doit effectuer la résolution d’adresse IP pour ces objets et les mettre à jour de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="d83a3-124">A component outside of the firewall service must do the IP address resolution for these objects, and update them appropriately.</span></span> <span data-ttu-id="d83a3-125">L’implémentation d’un tel composant n’est pas la portée de ce contenu.</span><span class="sxs-lookup"><span data-stu-id="d83a3-125">The implementation of such a component is outside the scope of this content.</span></span>

<span data-ttu-id="d83a3-126">Une adresse de mot clé dynamique est indiquée comme étant *autosolve* en définissant l’indicateur **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** dans l’objet lors de l’appel de la fonction [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-126">A dynamic keyword address is indicated as being *AutoResolve* by setting the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag in the object when calling the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span> <span data-ttu-id="d83a3-127">Le champ de *mot clé* doit être utilisé pour représenter la valeur résolue &mdash; , c’est-à-dire un nom de domaine complet (FQDN) ou un nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="d83a3-127">The *keyword* field should be used to represent the value being resolved&mdash;that is, a fully qualified domain name (FQDN) or hostname.</span></span> <span data-ttu-id="d83a3-128">Initialement, le champ d' *adresses* doit avoir la valeur null pour ces objets.</span><span class="sxs-lookup"><span data-stu-id="d83a3-128">The *addresses* field must initially be NULL for these objects.</span></span> <span data-ttu-id="d83a3-129">Ces objets n’auront pas leurs adresses IP conservées entre les cycles de démarrage et vous devrez réévaluer/remplir à nouveau leurs adresses au cours du prochain cycle de démarrage.</span><span class="sxs-lookup"><span data-stu-id="d83a3-129">These objects won't have their IP addresses persisted across boot cycles, and you should re-evaluate/re-populate their addresses during the next boot cycle.</span></span>

> [!NOTE]
> <span data-ttu-id="d83a3-130">Résoudre automatiquement les objets d’adresse de mot clé dynamique déclenchent des notifications sur [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) et [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), mais pas sur [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="d83a3-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="non-autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="d83a3-131">Adresses de mots clés dynamiques non résolues automatiquement</span><span class="sxs-lookup"><span data-stu-id="d83a3-131">Non-AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="d83a3-132">Le deuxième type est *non autosolve*, où le champ de *mot clé* est une chaîne, et les adresses sont définies au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="d83a3-132">The second type is *non-AutoResolve*, where the *keyword* field is any string, and the addresses are defined at creation time.</span></span>

<span data-ttu-id="d83a3-133">Ces objets sont utilisés pour stocker un ensemble d’adresses IP, de sous-réseaux ou de plages.</span><span class="sxs-lookup"><span data-stu-id="d83a3-133">These objects are used to store a set of IP address, subnets, or ranges.</span></span> <span data-ttu-id="d83a3-134">Le champ de *mot clé* ici est utilisé à des fins de gestion et peut être défini sur n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="d83a3-134">The *keyword* field here is used for management convenience, and it can be set to any string.</span></span> <span data-ttu-id="d83a3-135">Le champ *adresses* ne doit pas avoir la valeur null lors de la création.</span><span class="sxs-lookup"><span data-stu-id="d83a3-135">The *addresses* field must be non-NULL upon creation.</span></span> <span data-ttu-id="d83a3-136">Les adresses de ces objets sont conservées entre les redémarrages.</span><span class="sxs-lookup"><span data-stu-id="d83a3-136">Addresses for these objects are persisted across reboots.</span></span>

> [!NOTE]
> <span data-ttu-id="d83a3-137">Les objets d’adresse de mot clé dynamique non résolus automatiquement déclenchent des notifications sur [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)et [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="d83a3-137">Non-AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), and also [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="more-about-dynamic-keyword-addresses"></a><span data-ttu-id="d83a3-138">En savoir plus sur les adresses de mots clés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d83a3-138">More about dynamic keyword addresses</span></span> 

<span data-ttu-id="d83a3-139">Toutes les adresses de mots clés dynamiques doivent avoir un identificateur [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) unique pour les représenter.</span><span class="sxs-lookup"><span data-stu-id="d83a3-139">All dynamic keyword addresses must have a unique [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) identifier to represent them.</span></span>

<span data-ttu-id="d83a3-140">L’API [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) fournit des notifications à un client lorsque les adresses de mots clés dynamiques changent.</span><span class="sxs-lookup"><span data-stu-id="d83a3-140">The [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API delivers notifications to a client when dynamic keyword addresses change.</span></span> <span data-ttu-id="d83a3-141">Aucune charge utile n’est fournie au client pour décrire exactement ce qui a changé sur le système.</span><span class="sxs-lookup"><span data-stu-id="d83a3-141">There's no payload delivered to the client describing exactly what changed on the system.</span></span> <span data-ttu-id="d83a3-142">Si vous avez besoin de savoir quels objets ont changé, vous devez interroger l’état actuel des objets sur le système à l’aide des API [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) ou [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-142">If you need to know what objects changed, then you should query the current state of objects on the system using the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs.</span></span> <span data-ttu-id="d83a3-143">Vous pouvez utiliser les différents indicateurs pour demander des notifications uniquement pour un sous-ensemble d’objets.</span><span class="sxs-lookup"><span data-stu-id="d83a3-143">You can use the various flags to request notifications for only a subset of objects.</span></span> <span data-ttu-id="d83a3-144">Si vous n’utilisez aucun indicateur, les notifications de modification sont remises pour tous les objets.</span><span class="sxs-lookup"><span data-stu-id="d83a3-144">If you use no flags, then change notifications will be delivered for all objects.</span></span>

<span data-ttu-id="d83a3-145">Une règle de pare-feu peut utiliser des adresses de mots clés dynamiques au lieu de définir explicitement des adresses IP pour sa condition d’adresse distante.</span><span class="sxs-lookup"><span data-stu-id="d83a3-145">A firewall rule can use dynamic keyword addresses instead of explicitly defining IP addresses for its remote address condition.</span></span> <span data-ttu-id="d83a3-146">Une règle de pare-feu peut utiliser à la fois des adresses de mots clés dynamiques et des plages d’adresses distantes définies statiquement.</span><span class="sxs-lookup"><span data-stu-id="d83a3-146">A firewall rule can use both dynamic keyword addresses and statically defined remote address ranges.</span></span> <span data-ttu-id="d83a3-147">Un seul objet d’adresse de mot clé dynamique peut être réutilisé sur plusieurs règles de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="d83a3-147">A single dynamic keyword address object can be re-used across multiple firewall rules.</span></span> <span data-ttu-id="d83a3-148">Si une règle de pare-feu n’a aucune adresse distante configurée (c’est-à-dire configurée uniquement avec des objets qui n’ont pas encore été résolus), la règle n’est pas appliquée.</span><span class="sxs-lookup"><span data-stu-id="d83a3-148">If a firewall rule doesn't have any configured remote addresses (that is, configured with only AutoResolve objects which have not yet been resolved), then the rule won't be enforced.</span></span> <span data-ttu-id="d83a3-149">En outre, si une règle utilise plusieurs adresses de mots clés dynamiques, la règle est appliquée à toutes les adresses qui sont actuellement résolues, même s’il existe d’autres objets qui ne sont pas encore résolus.</span><span class="sxs-lookup"><span data-stu-id="d83a3-149">Furthermore, if a rule uses multiple dynamic keyword addresses, then the rule will be enforced for all addresses that are currently resolved, even if there are other objects that are not yet resolved.</span></span> <span data-ttu-id="d83a3-150">Lorsqu’une adresse de mot clé dynamique est mise à jour, les adresses distantes sont également mises à jour pour tous les objets de règle associés.</span><span class="sxs-lookup"><span data-stu-id="d83a3-150">When a dynamic keyword address is updated, all associated rule objects will have their remote addresses updated as well.</span></span>

<span data-ttu-id="d83a3-151">Le système d’exploitation lui-même n’impose aucune dépendance entre une règle et une adresse de mot clé dynamique.</span><span class="sxs-lookup"><span data-stu-id="d83a3-151">The operating system (OS) itself doesn't enforce any dependencies between a rule and a dynamic keyword address.</span></span> <span data-ttu-id="d83a3-152">Cela signifie que l’un ou l’autre objet peut être créé &mdash; en premier, la règle peut faire référence à des ID d’adresse de mot clé dynamique qui n’existent pas encore (dans ce cas, la règle ne sera pas appliquée).</span><span class="sxs-lookup"><span data-stu-id="d83a3-152">This means that either object can be created first&mdash;the rule can reference dynamic keyword address IDs that don't yet exist (in which case, the rule won't be enforced).</span></span> <span data-ttu-id="d83a3-153">En outre, vous pouvez supprimer une adresse de mot clé dynamique, même si elle est utilisée par une règle de pare-feu.</span><span class="sxs-lookup"><span data-stu-id="d83a3-153">Furthermore, you can delete a dynamic keyword address even if it's in use by a firewall rule.</span></span> <span data-ttu-id="d83a3-154">Cette rubrique décrit comment un administrateur peut configurer des règles pour utiliser l’adresse de mot clé dynamique.</span><span class="sxs-lookup"><span data-stu-id="d83a3-154">This topic outlines how an admin can configure rules to use dynamic keyword address.</span></span>

## <a name="code-examples"></a><span data-ttu-id="d83a3-155">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="d83a3-155">Code examples</span></span>

<span data-ttu-id="d83a3-156">Pour essayer chacun de ces exemples de code, commencez par lancer Visual Studio et créez un nouveau projet basé sur le modèle de projet d' **application console** .</span><span class="sxs-lookup"><span data-stu-id="d83a3-156">To try out each of these code examples, first launch Visual Studio and create a new project based on the **Console App** project template.</span></span> <span data-ttu-id="d83a3-157">Vous pouvez simplement remplacer le contenu de `main.cpp` par la liste de code.</span><span class="sxs-lookup"><span data-stu-id="d83a3-157">You can just replace the contents of `main.cpp` with the code listing.</span></span>

<span data-ttu-id="d83a3-158">La plupart des exemples de code utilisent les [bibliothèques d’implémentation Windows (Wil)](https://github.com/Microsoft/wil).</span><span class="sxs-lookup"><span data-stu-id="d83a3-158">Most of the code examples use the [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil).</span></span> <span data-ttu-id="d83a3-159">Un moyen pratique d’installer Wil consiste à accéder à Visual Studio, puis à cliquer sur **projet** \> **gérer les packages NuGet...** \> **Parcourir**, taper ou coller **Microsoft. Windows. ImplementationLibrary** dans la zone de recherche, sélectionner l’élément dans les résultats de la recherche, puis cliquer sur **installer** pour installer le package pour ce projet.</span><span class="sxs-lookup"><span data-stu-id="d83a3-159">A convenient way to install WIL is to go to Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.Windows.ImplementationLibrary** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="d83a3-160">Les types de pointeurs pour les fonctions Free NetFw sont publiés via `NetFw.h` , mais une bibliothèque de liens statiques n’est pas publiée.</span><span class="sxs-lookup"><span data-stu-id="d83a3-160">Pointer types for the NetFw free functions are published via `NetFw.h`, but a static-link library isn't published.</span></span> <span data-ttu-id="d83a3-161">Utilisez le modèle [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) / [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour appeler ces fonctions, comme indiqué dans ces exemples de code.</span><span class="sxs-lookup"><span data-stu-id="d83a3-161">Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling these functions, as shown in these code examples.</span></span>

### <a name="add-a-dynamic-keyword-address"></a><span data-ttu-id="d83a3-162">Ajouter une adresse de mot clé dynamique</span><span class="sxs-lookup"><span data-stu-id="d83a3-162">Add a dynamic keyword address</span></span>

<span data-ttu-id="d83a3-163">Cet exemple montre comment utiliser la fonction [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-163">This example shows how to use the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a><span data-ttu-id="d83a3-164">Supprimer une adresse de mot clé dynamique</span><span class="sxs-lookup"><span data-stu-id="d83a3-164">Delete a dynamic keyword address</span></span>

<span data-ttu-id="d83a3-165">Cet exemple montre comment utiliser la fonction [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-165">This example shows how to use the [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a><span data-ttu-id="d83a3-166">Énumérer et libérer des adresses de mots clés dynamiques par ID</span><span class="sxs-lookup"><span data-stu-id="d83a3-166">Enumerate and free dynamic keyword addresses by ID</span></span>

<span data-ttu-id="d83a3-167">Cet exemple montre comment utiliser les fonctions [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) et [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-167">This example shows how to use the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a><span data-ttu-id="d83a3-168">Énumérer et libérer des adresses de mots clés dynamiques par type</span><span class="sxs-lookup"><span data-stu-id="d83a3-168">Enumerate and free dynamic keyword addresses by type</span></span>

<span data-ttu-id="d83a3-169">Cet exemple montre comment utiliser les fonctions [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) et [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-169">This example shows how to use the [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a><span data-ttu-id="d83a3-170">Mettre à jour les adresses de mots clés dynamiques</span><span class="sxs-lookup"><span data-stu-id="d83a3-170">Update dynamic keyword addresses</span></span>

<span data-ttu-id="d83a3-171">Cet exemple montre comment utiliser la fonction [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-171">This example shows how to use the [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a><span data-ttu-id="d83a3-172">S’abonner aux notifications de modification des adresses de mots clés dynamiques et les gérer</span><span class="sxs-lookup"><span data-stu-id="d83a3-172">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="d83a3-173">Cet exemple montre comment utiliser les fonctions [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) et [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) , ainsi que le rappel [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) .</span><span class="sxs-lookup"><span data-stu-id="d83a3-173">This example shows how to use the [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) and [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) functions, and the [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) callback.</span></span>

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a><span data-ttu-id="d83a3-174">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d83a3-174">Related topics</span></span>

* [<span data-ttu-id="d83a3-175">Référence des mots clés dynamiques du pare-feu</span><span class="sxs-lookup"><span data-stu-id="d83a3-175">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
