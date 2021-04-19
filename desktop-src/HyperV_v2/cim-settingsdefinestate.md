---
description: Associe des données de paramètres à un élément managé.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: Classe CIM_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1931b365108bb7b3df4269ae6acbb78292a0401d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528226"
---
# <a name="cim_settingsdefinestate-class"></a><span data-ttu-id="a070d-103">\_Classe CIM SettingsDefineState</span><span class="sxs-lookup"><span data-stu-id="a070d-103">CIM\_SettingsDefineState class</span></span>

<span data-ttu-id="a070d-104">Associe des données de paramètres à un élément managé.</span><span class="sxs-lookup"><span data-stu-id="a070d-104">Associates settings data with a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="a070d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a070d-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="a070d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a070d-106">Members</span></span>

<span data-ttu-id="a070d-107">La classe **CIM \_ SettingsDefineState** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a070d-107">The **CIM\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="a070d-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a070d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a070d-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a070d-109">Properties</span></span>

<span data-ttu-id="a070d-110">La classe **CIM \_ SettingsDefineState** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a070d-110">The **CIM\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a070d-111">**Propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a070d-111">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a070d-112">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="a070d-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="a070d-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a070d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a070d-114">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a070d-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a070d-115">Élément managé dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="a070d-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="a070d-116">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="a070d-116">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a070d-117">Type de données **: \_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="a070d-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="a070d-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a070d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a070d-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a070d-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a070d-120">Données de paramètres dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="a070d-120">The settings data in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a070d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a070d-121">Requirements</span></span>



| <span data-ttu-id="a070d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a070d-122">Requirement</span></span> | <span data-ttu-id="a070d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a070d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a070d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a070d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a070d-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a070d-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a070d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a070d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a070d-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a070d-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a070d-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a070d-128">Namespace</span></span><br/>                | <span data-ttu-id="a070d-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a070d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a070d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a070d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a070d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a070d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a070d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a070d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a070d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a070d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

