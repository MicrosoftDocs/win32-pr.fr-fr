---
description: Contient les paramètres utilisés pendant les opérations de maintenance.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Classe Msvm_ServicingSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485272"
---
# <a name="msvm_servicingsettings-class"></a><span data-ttu-id="00ef0-103">MSVM \_ ServicingSettings, classe</span><span class="sxs-lookup"><span data-stu-id="00ef0-103">Msvm\_ServicingSettings class</span></span>

<span data-ttu-id="00ef0-104">Contient les paramètres utilisés pendant les opérations de maintenance.</span><span class="sxs-lookup"><span data-stu-id="00ef0-104">Contains settings used during servicing operations.</span></span>

<span data-ttu-id="00ef0-105">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="00ef0-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="00ef0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00ef0-106">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="00ef0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="00ef0-107">Members</span></span>

<span data-ttu-id="00ef0-108">La classe **MSVM \_ ServicingSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="00ef0-108">The **Msvm\_ServicingSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="00ef0-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00ef0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00ef0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="00ef0-110">Properties</span></span>

<span data-ttu-id="00ef0-111">La classe **MSVM \_ ServicingSettings** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="00ef0-111">The **Msvm\_ServicingSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00ef0-112">**Version**</span><span class="sxs-lookup"><span data-stu-id="00ef0-112">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00ef0-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="00ef0-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="00ef0-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="00ef0-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="00ef0-115">Contient la version de la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="00ef0-115">Contains the class definition's version.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00ef0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00ef0-116">Requirements</span></span>



| <span data-ttu-id="00ef0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00ef0-117">Requirement</span></span> | <span data-ttu-id="00ef0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="00ef0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00ef0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00ef0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="00ef0-120">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00ef0-120">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="00ef0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00ef0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="00ef0-122">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00ef0-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00ef0-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="00ef0-123">Namespace</span></span><br/>                | <span data-ttu-id="00ef0-124">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="00ef0-124">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="00ef0-125">MOF</span><span class="sxs-lookup"><span data-stu-id="00ef0-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00ef0-126"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00ef0-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="00ef0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="00ef0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00ef0-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00ef0-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




