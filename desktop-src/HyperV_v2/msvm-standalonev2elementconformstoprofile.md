---
description: Définit les profils enregistrés conformes au système autonome référencé.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Classe Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c492ad5bdd0e50bbbe86fd220000099269501ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951524"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a><span data-ttu-id="0b3d9-103">MSVM \_ StandaloneV2ElementConformsToProfile, classe</span><span class="sxs-lookup"><span data-stu-id="0b3d9-103">Msvm\_StandaloneV2ElementConformsToProfile class</span></span>

<span data-ttu-id="0b3d9-104">Définit les profils enregistrés conformes au système autonome référencé.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-104">Defines the registered profiles to which the referenced standalone system conforms.</span></span>

<span data-ttu-id="0b3d9-105">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b3d9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b3d9-106">Syntax</span></span>

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a><span data-ttu-id="0b3d9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0b3d9-107">Members</span></span>

<span data-ttu-id="0b3d9-108">La classe **MSVM \_ StandaloneV2ElementConformsToProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0b3d9-108">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="0b3d9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0b3d9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b3d9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0b3d9-110">Properties</span></span>

<span data-ttu-id="0b3d9-111">La classe **MSVM \_ StandaloneV2ElementConformsToProfile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-111">The **Msvm\_StandaloneV2ElementConformsToProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b3d9-112">**ConformantStandard**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-112">**ConformantStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b3d9-113">Type de données : **MSVM \_ RegisteredProfile**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-113">Data type: **Msvm\_RegisteredProfile**</span></span>
</dt> <dt>

<span data-ttu-id="0b3d9-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0b3d9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b3d9-115">Qualificateurs : [ **override**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0b3d9-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0b3d9-116">Profil inscrit auquel le système autonome est conforme.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-116">The registered profile to which the standalone system conforms.</span></span>

</dd> <dt>

<span data-ttu-id="0b3d9-117">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-117">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b3d9-118">Type de données : **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="0b3d9-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0b3d9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b3d9-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers), **targetNamespace, \_ targetNamespace** ("root \\ \\ Virtualization \\ \\ V2")</span><span class="sxs-lookup"><span data-stu-id="0b3d9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT\_TargetNamespace** ("root\\\\virtualization\\\\v2")</span></span>
</dt> </dl>

<span data-ttu-id="0b3d9-121">Système autonome conforme au profil enregistré.</span><span class="sxs-lookup"><span data-stu-id="0b3d9-121">The standalone system that conforms to the registered profile.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b3d9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b3d9-122">Requirements</span></span>



| <span data-ttu-id="0b3d9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b3d9-123">Requirement</span></span> | <span data-ttu-id="0b3d9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b3d9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b3d9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b3d9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b3d9-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b3d9-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0b3d9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b3d9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b3d9-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0b3d9-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0b3d9-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0b3d9-129">Namespace</span></span><br/>                | <span data-ttu-id="0b3d9-130">\\Interop racine</span><span class="sxs-lookup"><span data-stu-id="0b3d9-130">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="0b3d9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0b3d9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b3d9-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b3d9-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b3d9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0b3d9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b3d9-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b3d9-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b3d9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b3d9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b3d9-136">**MSVM \_ ElementConformsToProfile**</span><span class="sxs-lookup"><span data-stu-id="0b3d9-136">**Msvm\_ElementConformsToProfile**</span></span>](msvm-elementconformstoprofile.md)
</dt> </dl>

 

