---
title: Classe MDM_RemoteWipe
description: La \_ classe MDM RemoteWipe permet la réinitialisation à distance d’un appareil.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- Classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, Description
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032393"
---
# <a name="mdm_remotewipe-class"></a><span data-ttu-id="0f87b-105">\_Classe REMOTEWIPE MDM</span><span class="sxs-lookup"><span data-stu-id="0f87b-105">MDM\_RemoteWipe class</span></span>

<span data-ttu-id="0f87b-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="0f87b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0f87b-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="0f87b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0f87b-108">La classe **MDM \_ RemoteWipe** permet la réinitialisation à distance d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="0f87b-108">The **MDM\_RemoteWipe** class allows a remote wipe of a device.</span></span>

<span data-ttu-id="0f87b-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0f87b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f87b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f87b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a><span data-ttu-id="0f87b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="0f87b-111">Members</span></span>

<span data-ttu-id="0f87b-112">La **classe \_ RemoteWipe MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0f87b-112">The **MDM\_RemoteWipe** class has these types of members:</span></span>

-   [<span data-ttu-id="0f87b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0f87b-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f87b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0f87b-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0f87b-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0f87b-115">Methods</span></span>

<span data-ttu-id="0f87b-116">La classe **MDM \_ RemoteWipe** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0f87b-116">The **MDM\_RemoteWipe** class has these methods.</span></span>



| <span data-ttu-id="0f87b-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="0f87b-117">Method</span></span>                                              | <span data-ttu-id="0f87b-118">Description</span><span class="sxs-lookup"><span data-stu-id="0f87b-118">Description</span></span>                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="0f87b-119">**doWipeMethod**</span><span class="sxs-lookup"><span data-stu-id="0f87b-119">**doWipeMethod**</span></span>](mdm-remotewipe-dowipemethod.md) | <span data-ttu-id="0f87b-120">Déclenche le démarrage de la réinitialisation à distance par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0f87b-120">Triggers the device to start the remote wipe.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0f87b-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0f87b-121">Properties</span></span>

<span data-ttu-id="0f87b-122">La **classe \_ RemoteWipe MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0f87b-122">The **MDM\_RemoteWipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f87b-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0f87b-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f87b-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0f87b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f87b-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0f87b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f87b-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0f87b-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0f87b-127">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="0f87b-127">Identifies the name of the parent node.</span></span> <span data-ttu-id="0f87b-128">Pour cette classe, la chaîne est « RemoteWipe ».</span><span class="sxs-lookup"><span data-stu-id="0f87b-128">For this class, the string is "RemoteWipe".</span></span>

</dd> <dt>

<span data-ttu-id="0f87b-129">**ID**</span><span class="sxs-lookup"><span data-stu-id="0f87b-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f87b-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0f87b-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f87b-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0f87b-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f87b-132">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0f87b-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0f87b-133">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="0f87b-133">Describes the full path to the parent node.</span></span> <span data-ttu-id="0f87b-134">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="0f87b-134">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="0f87b-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="0f87b-135">Example</span></span>

<span data-ttu-id="0f87b-136">L’exemple suivant montre comment utiliser RemoteWipe et appeler doWipeMethod.</span><span class="sxs-lookup"><span data-stu-id="0f87b-136">The following example demonstrates how to use the RemoteWipe and invoke the doWipeMethod.</span></span>

> [!Note]  
> <span data-ttu-id="0f87b-137">Cet exemple doit être exécuté sous utilisateur du système local.</span><span class="sxs-lookup"><span data-stu-id="0f87b-137">This example must be executed under local system user.</span></span> <span data-ttu-id="0f87b-138">Pour ce faire, téléchargez l’outil PsExec depuis <https://technet.microsoft.com/sysinternals/bb897553.aspx> et exécutez `psexec.exe -i -s cmd.exe` à partir d’une invite de commandes d’administrateur élevé.</span><span class="sxs-lookup"><span data-stu-id="0f87b-138">To do that, download the psexec tool from <https://technet.microsoft.com/sysinternals/bb897553.aspx> and run `psexec.exe -i -s cmd.exe` from an elevated admin command prompt.</span></span>

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a><span data-ttu-id="0f87b-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f87b-139">Requirements</span></span>



| <span data-ttu-id="0f87b-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f87b-140">Requirement</span></span> | <span data-ttu-id="0f87b-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f87b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f87b-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f87b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0f87b-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f87b-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f87b-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f87b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0f87b-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f87b-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0f87b-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0f87b-146">Namespace</span></span><br/>                | <span data-ttu-id="0f87b-147">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="0f87b-147">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="0f87b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="0f87b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f87b-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f87b-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f87b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0f87b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f87b-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f87b-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f87b-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f87b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f87b-153">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="0f87b-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

