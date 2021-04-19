---
description: Représente une collection d’autres collections.
ms.assetid: 1f7f5517-55d9-44a3-b0ca-444a9d7d5941
title: Classe Msvm_ManagementCollection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ManagementCollection
- Msvm_ManagementCollection.CollectionID
- Msvm_ManagementCollection.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2d3499bb161495152b6de4b8aebd7c64d041d069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535599"
---
# <a name="msvm_managementcollection-class"></a><span data-ttu-id="4fc89-103">MSVM \_ ManagementCollection, classe</span><span class="sxs-lookup"><span data-stu-id="4fc89-103">Msvm\_ManagementCollection class</span></span>

<span data-ttu-id="4fc89-104">Représente une collection d’autres collections.</span><span class="sxs-lookup"><span data-stu-id="4fc89-104">Represents a collection of other collections.</span></span>

<span data-ttu-id="4fc89-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4fc89-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc89-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fc89-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ManagementCollection : CIM_CollectionOfMSEs
{
  string CollectionID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="4fc89-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4fc89-107">Members</span></span>

<span data-ttu-id="4fc89-108">La classe **MSVM \_ ManagementCollection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4fc89-108">The **Msvm\_ManagementCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="4fc89-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4fc89-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4fc89-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4fc89-110">Properties</span></span>

<span data-ttu-id="4fc89-111">La classe **MSVM \_ ManagementCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4fc89-111">The **Msvm\_ManagementCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fc89-112">**CollectionID**</span><span class="sxs-lookup"><span data-stu-id="4fc89-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc89-113">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fc89-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fc89-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4fc89-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fc89-115">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) (« porte »), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="4fc89-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4fc89-116">Identification unique de l’objet de collection.</span><span class="sxs-lookup"><span data-stu-id="4fc89-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="4fc89-117">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4fc89-117">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fc89-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fc89-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fc89-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4fc89-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fc89-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="4fc89-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="4fc89-121">Nom défini par l’utilisateur pour la collection.</span><span class="sxs-lookup"><span data-stu-id="4fc89-121">An user-defined name for the collection.</span></span> <span data-ttu-id="4fc89-122">Notez qu’il n’est pas garanti qu’il soit unique.</span><span class="sxs-lookup"><span data-stu-id="4fc89-122">Note this is not guaranteed to be unique.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fc89-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fc89-123">Requirements</span></span>



| <span data-ttu-id="4fc89-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fc89-124">Requirement</span></span> | <span data-ttu-id="4fc89-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fc89-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc89-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fc89-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4fc89-127">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fc89-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4fc89-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fc89-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4fc89-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4fc89-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4fc89-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4fc89-130">Namespace</span></span><br/>                | <span data-ttu-id="4fc89-131">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4fc89-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4fc89-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4fc89-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fc89-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fc89-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fc89-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4fc89-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fc89-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4fc89-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4fc89-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fc89-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc89-137">**\_COLLECTIONOFMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="4fc89-137">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> </dl>

 

