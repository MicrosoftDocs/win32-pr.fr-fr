---
description: Vous pouvez obtenir ou modifier les données du Registre à l’aide de la classe WMI StdRegProv et de ses méthodes.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Obtention de données de Registre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515193"
---
# <a name="obtaining-registry-data"></a><span data-ttu-id="b430d-103">Obtention de données de Registre</span><span class="sxs-lookup"><span data-stu-id="b430d-103">Obtaining Registry Data</span></span>

<span data-ttu-id="b430d-104">Vous pouvez obtenir ou modifier les données du Registre à l’aide de la classe WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) et de ses méthodes.</span><span class="sxs-lookup"><span data-stu-id="b430d-104">You can obtain or modify registry data by using the WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and its methods.</span></span> <span data-ttu-id="b430d-105">Si vous utilisez l’utilitaire regedit pour afficher et modifier les valeurs de Registre sur l’ordinateur local, **StdRegProv** vous permet d’utiliser un script ou une application pour automatiser ces activités sur l’ordinateur local et les ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="b430d-105">While use the Regedit utility to view and change registry values on the local computer, **StdRegProv** allows you to use a script or application to automate such activities on the local computer and remote computers.</span></span>

<span data-ttu-id="b430d-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contient des méthodes pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b430d-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contains methods to do the following:</span></span>

-   <span data-ttu-id="b430d-107">Vérifier les autorisations d’accès pour un utilisateur</span><span class="sxs-lookup"><span data-stu-id="b430d-107">Verify the access permissions for a user</span></span>
-   <span data-ttu-id="b430d-108">Créer, énumérer et supprimer des clés de Registre</span><span class="sxs-lookup"><span data-stu-id="b430d-108">Create, enumerate, and delete registry keys</span></span>
-   <span data-ttu-id="b430d-109">Créer, énumérer et supprimer des sous-clés ou des valeurs nommées</span><span class="sxs-lookup"><span data-stu-id="b430d-109">Create, enumerate, and delete subkeys or named values</span></span>
-   <span data-ttu-id="b430d-110">Lire, écrire et supprimer des valeurs de données</span><span class="sxs-lookup"><span data-stu-id="b430d-110">Read, write, and delete data values</span></span>

<span data-ttu-id="b430d-111">Les données du Registre sont organisées par sous-arborescences, clés et sous-clés imbriquées sous une clé de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="b430d-111">Registry data is organized by subtrees, keys, and subkeys nested under a top level key.</span></span> <span data-ttu-id="b430d-112">Les valeurs de données réelles sont appelées entrées ou valeurs nommées.</span><span class="sxs-lookup"><span data-stu-id="b430d-112">The actual data values are called entries or named values.</span></span>

<span data-ttu-id="b430d-113">Les sous-arborescences sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="b430d-113">The subtrees include the following:</span></span>

-   <span data-ttu-id="b430d-114">**HKEY \_ CLASSES \_ racine** (abrégées en **HKCR**)</span><span class="sxs-lookup"><span data-stu-id="b430d-114">**HKEY\_CLASSES\_ROOT** (abbreviated as **HKCR**)</span></span>
-   <span data-ttu-id="b430d-115">**HKEY \_ \_utilisateur actuel** (**HKCU**)</span><span class="sxs-lookup"><span data-stu-id="b430d-115">**HKEY\_CURRENT\_USER** (**HKCU**)</span></span>
-   <span data-ttu-id="b430d-116">**HKEY \_ \_ordinateur local** (**HKLM**)</span><span class="sxs-lookup"><span data-stu-id="b430d-116">**HKEY\_LOCAL\_MACHINE** (**HKLM**)</span></span>
-   <span data-ttu-id="b430d-117">**HKEY, \_ utilisateurs**</span><span class="sxs-lookup"><span data-stu-id="b430d-117">**HKEY\_USERS**</span></span>
-   <span data-ttu-id="b430d-118">**configuration de HKEY \_ Current \_**</span><span class="sxs-lookup"><span data-stu-id="b430d-118">**HKEY\_CURRENT\_CONFIG**</span></span>

<span data-ttu-id="b430d-119">Par exemple, dans l’entrée de Registre **HKEY** \\ **Software** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**, la sous-arborescence HKEY est **Software**; les sous-clés sont **Microsoft** et **DirectX**; et l’entrée de valeur nommée est **InstalledVersion**.</span><span class="sxs-lookup"><span data-stu-id="b430d-119">For example, in the registry entry **HKEY**\\**SOFTWARE**\\**Microsoft**\\**DirectX**\\**InstalledVersion**, the HKEY subtree is **SOFTWARE**; the subkeys are **Microsoft** and **DirectX**; and the named value entry is **InstalledVersion**.</span></span>

<span data-ttu-id="b430d-120">Un [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) se produit lorsqu’une modification apportée à une clé spécifique se produit, mais que l’entrée n’identifie pas la manière dont les valeurs sont modifiées et que cet événement est déclenché par des modifications sous la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b430d-120">A [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) occurs when a change to a specific key occurs, but the entry does not identify how the values change nor will this event be triggered by changes below the specified key.</span></span> <span data-ttu-id="b430d-121">Pour identifier les modifications n’importe où dans une structure de clé hiérarchique, utilisez [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), qui ne retourne pas de valeurs spécifiques ou de modifications de clé qui se produisent.</span><span class="sxs-lookup"><span data-stu-id="b430d-121">To identify changes anywhere in a hierarchical key structure, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), which does not return specific values or key changes that occur.</span></span> <span data-ttu-id="b430d-122">Pour obtenir une modification de valeur d’entrée spécifique, utilisez [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), puis lisez l’entrée pour obtenir une valeur de ligne de base.</span><span class="sxs-lookup"><span data-stu-id="b430d-122">To obtain a specific entry value change, use the [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), and then read the entry to obtain a baseline value.</span></span>

<span data-ttu-id="b430d-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) possède uniquement des méthodes qui peuvent être appelées à partir de C++ ou d’un script, ce qui diffère de la structure de la classe Win32.</span><span class="sxs-lookup"><span data-stu-id="b430d-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) only has methods that can be called from C++ or script, which is different from the Win32 class structure.</span></span>

<span data-ttu-id="b430d-124">L’exemple de code suivant montre comment utiliser la méthode [**StdRegProv. enumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) pour répertorier toutes les sous-clés logicielles Microsoft sous la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="b430d-124">The following code example shows how to use the [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) method to list all of the Microsoft software subkeys under the registry key.</span></span>

<span data-ttu-id="b430d-125">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="b430d-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





<span data-ttu-id="b430d-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) a des méthodes différentes pour lire les différents types de données de valeur d’entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="b430d-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) has different methods for reading the various registry entry value data types.</span></span> <span data-ttu-id="b430d-127">Si l’entrée contient des valeurs inconnues, vous pouvez appeler [**StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) pour les répertorier.</span><span class="sxs-lookup"><span data-stu-id="b430d-127">If the entry has unknown values, then you can call [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) to list them.</span></span> <span data-ttu-id="b430d-128">Le tableau suivant répertorie la correspondance entre les méthodes **StdRegProv** et les types de données.</span><span class="sxs-lookup"><span data-stu-id="b430d-128">The following table lists the correspondence between **StdRegProv** methods and the data types.</span></span>



| <span data-ttu-id="b430d-129">Méthode</span><span class="sxs-lookup"><span data-stu-id="b430d-129">Method</span></span>                                                                                  | <span data-ttu-id="b430d-130">Type de données</span><span class="sxs-lookup"><span data-stu-id="b430d-130">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="b430d-131">**GetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-131">**GetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="b430d-132">**\_fichier binaire reg**</span><span class="sxs-lookup"><span data-stu-id="b430d-132">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="b430d-133">**GetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-133">**GetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="b430d-134">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="b430d-134">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="b430d-135">**GetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-135">**GetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="b430d-136">**REG \_ développer \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b430d-136">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="b430d-137">**GetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-137">**GetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="b430d-138">**REG \_ multiple \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b430d-138">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="b430d-139">**GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-139">**GetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="b430d-140">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="b430d-140">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="b430d-141">Le tableau suivant répertorie les méthodes correspondantes pour la création de clés ou de valeurs, ou la modification de clés existantes.</span><span class="sxs-lookup"><span data-stu-id="b430d-141">The following table lists the corresponding methods for creating new keys or values, or changing existing ones.</span></span>



| <span data-ttu-id="b430d-142">Méthode</span><span class="sxs-lookup"><span data-stu-id="b430d-142">Method</span></span>                                                                                  | <span data-ttu-id="b430d-143">Type de données</span><span class="sxs-lookup"><span data-stu-id="b430d-143">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="b430d-144">**SetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-144">**SetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="b430d-145">**\_fichier binaire reg**</span><span class="sxs-lookup"><span data-stu-id="b430d-145">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="b430d-146">**SetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-146">**SetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="b430d-147">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="b430d-147">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="b430d-148">**SetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-148">**SetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="b430d-149">**REG \_ développer \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b430d-149">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="b430d-150">**SetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-150">**SetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="b430d-151">**REG \_ multiple \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="b430d-151">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="b430d-152">**SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="b430d-152">**SetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="b430d-153">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="b430d-153">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="b430d-154">L’exemple suivant montre comment lire la liste des sources du journal des événements système à partir de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="b430d-154">The following example shows how to read the list of sources for the system event log from the registry key.</span></span>

<span data-ttu-id="b430d-155">**HKEY \_ Système d' \_ ordinateur local** système de \\  \\ contrôle des services du **jeu de contrôle actuel** \\  \\  \\ </span><span class="sxs-lookup"><span data-stu-id="b430d-155">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Services**\\**Eventlog**\\**System**</span></span>

<span data-ttu-id="b430d-156">Notez que les éléments de la valeur multichaîne sont traités comme une collection ou un tableau.</span><span class="sxs-lookup"><span data-stu-id="b430d-156">Note that the items in the multistring value are treated as a collection or array.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



<span data-ttu-id="b430d-157">Le fournisseur de Registre est hébergé dans LocalService, et non dans le LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="b430d-157">The registry provider is hosted in LocalService—not the LocalSystem.</span></span> <span data-ttu-id="b430d-158">Par conséquent, il n’est pas possible d’obtenir des informations à distance à partir de la sous-arborescence **HKEY \_ Current \_ User** .</span><span class="sxs-lookup"><span data-stu-id="b430d-158">Therefore, obtaining information remotely from the subtree **HKEY\_CURRENT\_USER** is not possible.</span></span> <span data-ttu-id="b430d-159">Toutefois, les scripts exécutés sur l’ordinateur local peuvent toujours accéder à **HKEY \_ Current \_ User**.</span><span class="sxs-lookup"><span data-stu-id="b430d-159">However, scripts run on the local computer can still access **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="b430d-160">Vous pouvez définir le modèle d’hébergement sur LocalSystem sur un ordinateur distant, mais cela pose un problème de sécurité, car le registre sur l’ordinateur distant est vulnérable à un accès hostile.</span><span class="sxs-lookup"><span data-stu-id="b430d-160">You can set the hosting model to LocalSystem on a remote machine, but that is a security risk because the registry on the remote machine is vulnerable to hostile access.</span></span> <span data-ttu-id="b430d-161">Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="b430d-161">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b430d-162">Exemples</span><span class="sxs-lookup"><span data-stu-id="b430d-162">Examples</span></span>

<span data-ttu-id="b430d-163">L’exemple de code VBScript [lire une valeur de Registre binaire](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) dans la Galerie TechNet utilise WMI pour lire une valeur de Registre binaire.</span><span class="sxs-lookup"><span data-stu-id="b430d-163">The [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript code example on TechNet Gallery uses WMI to read a binary registry value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b430d-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b430d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b430d-165">Tâches WMI : Registre</span><span class="sxs-lookup"><span data-stu-id="b430d-165">WMI Tasks: Registry</span></span>](wmi-tasks--registry.md)
</dt> </dl>

 

 
