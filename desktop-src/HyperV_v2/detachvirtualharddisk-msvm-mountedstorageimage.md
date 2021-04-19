---
description: Détache l’image de stockage montée associée à cette classe.
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Méthode DetachVirtualHardDisk de la classe Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0d411134d85fe70163b2e08eebed0ff0d4b88e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530656"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a><span data-ttu-id="bf344-103">Méthode DetachVirtualHardDisk de la \_ classe MountedStorageImage MSVM</span><span class="sxs-lookup"><span data-stu-id="bf344-103">DetachVirtualHardDisk method of the Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="bf344-104">Détache l’image de stockage montée associée à cette classe.</span><span class="sxs-lookup"><span data-stu-id="bf344-104">Detaches the mounted storage image that is associated with this class.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf344-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf344-105">Syntax</span></span>


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a><span data-ttu-id="bf344-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf344-106">Parameters</span></span>

<span data-ttu-id="bf344-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bf344-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf344-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf344-108">Return value</span></span>

<span data-ttu-id="bf344-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf344-109">Type: **uint32**</span></span>

<span data-ttu-id="bf344-110">Cette méthode peut retourner l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf344-110">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bf344-111">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="bf344-111">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf344-112">**Échec** (1)</span><span class="sxs-lookup"><span data-stu-id="bf344-112">**Failed** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bf344-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bf344-113">Remarks</span></span>

<span data-ttu-id="bf344-114">L’accès à la classe [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="bf344-114">Access to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bf344-115">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bf344-115">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="bf344-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="bf344-116">Examples</span></span>

<span data-ttu-id="bf344-117">L’exemple C# suivant montre comment détacher un fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="bf344-117">The following C# example shows how to detach a virtual hard disk file.</span></span> <span data-ttu-id="bf344-118">Les utilitaires référencés se trouvent dans [les utilitaires courants pour les exemples de virtualisation (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="bf344-118">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="bf344-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf344-119">Requirements</span></span>



| <span data-ttu-id="bf344-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf344-120">Requirement</span></span> | <span data-ttu-id="bf344-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf344-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf344-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf344-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bf344-123">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf344-123">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bf344-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf344-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bf344-125">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf344-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf344-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf344-126">Namespace</span></span><br/>                | <span data-ttu-id="bf344-127">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="bf344-127">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bf344-128">MOF</span><span class="sxs-lookup"><span data-stu-id="bf344-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf344-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf344-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf344-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bf344-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf344-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf344-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf344-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf344-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf344-133">**MSVM \_ MountedStorageImage**</span><span class="sxs-lookup"><span data-stu-id="bf344-133">**Msvm\_MountedStorageImage**</span></span>](msvm-mountedstorageimage.md)
</dt> </dl>

 

