---
description: Représente un périphérique logique qui permet à un utilisateur d’entrer, d’afficher ou d’entendre des données sur le système informatique.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: Classe CIM_UserDevice (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864110"
---
# <a name="cim_userdevice-class-hyper-v-management"></a><span data-ttu-id="2b0a9-103">Classe CIM_UserDevice (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="2b0a9-103">CIM_UserDevice class (Hyper-V management)</span></span>

<span data-ttu-id="2b0a9-104">Représente un périphérique logique qui permet à un utilisateur d’entrer, d’afficher ou d’entendre des données sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="2b0a9-104">Represents a logical device that allows a user to input, view or hear data on the computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b0a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b0a9-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a><span data-ttu-id="2b0a9-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2b0a9-106">Members</span></span>

<span data-ttu-id="2b0a9-107">La classe **CIM \_ UserDevice** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2b0a9-107">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2b0a9-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b0a9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b0a9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2b0a9-109">Properties</span></span>

<span data-ttu-id="2b0a9-110">La classe **CIM \_ UserDevice** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2b0a9-110">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b0a9-111">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="2b0a9-111">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b0a9-112">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="2b0a9-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b0a9-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2b0a9-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b0a9-114">**true** si l’appareil est verrouillé, empêchant l’entrée ou la sortie de l’utilisateur ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2b0a9-114">**true** if the device is locked, preventing user input or output; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b0a9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b0a9-115">Requirements</span></span>



| <span data-ttu-id="2b0a9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b0a9-116">Requirement</span></span> | <span data-ttu-id="2b0a9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b0a9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0a9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b0a9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0a9-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2b0a9-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2b0a9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b0a9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0a9-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2b0a9-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2b0a9-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2b0a9-122">Namespace</span></span><br/>                | <span data-ttu-id="2b0a9-123">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b0a9-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2b0a9-124">MOF</span><span class="sxs-lookup"><span data-stu-id="2b0a9-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b0a9-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a9-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b0a9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2b0a9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b0a9-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a9-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b0a9-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b0a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0a9-129">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2b0a9-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




