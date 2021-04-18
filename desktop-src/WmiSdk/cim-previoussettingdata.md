---
description: Association entre un système virtuel et les données de paramètre de l’instantané qui est le parent du système virtuel.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: Classe CIM_PreviousSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533027"
---
# <a name="cim_previoussettingdata-class"></a><span data-ttu-id="3bee9-103">\_Classe CIM PreviousSettingData</span><span class="sxs-lookup"><span data-stu-id="3bee9-103">CIM\_PreviousSettingData class</span></span>

<span data-ttu-id="3bee9-104">Association entre un système virtuel et les données de paramètre de l’instantané qui est le parent du système virtuel.</span><span class="sxs-lookup"><span data-stu-id="3bee9-104">An association between a virtual system and the setting data of the snapshot which is the parent to the virtual system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bee9-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="3bee9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3bee9-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3bee9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3bee9-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3bee9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bee9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bee9-108">Syntax</span></span>

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a><span data-ttu-id="3bee9-109">Membres</span><span class="sxs-lookup"><span data-stu-id="3bee9-109">Members</span></span>

<span data-ttu-id="3bee9-110">La classe **CIM \_ PreviousSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3bee9-110">The **CIM\_PreviousSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3bee9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3bee9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bee9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3bee9-112">Properties</span></span>

<span data-ttu-id="3bee9-113">La classe **CIM \_ PreviousSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3bee9-113">The **CIM\_PreviousSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3bee9-114">**PreviousObject**</span><span class="sxs-lookup"><span data-stu-id="3bee9-114">**PreviousObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bee9-115">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="3bee9-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="3bee9-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bee9-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bee9-117">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="3bee9-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3bee9-118">Données du paramètre d’instantané qui est le parent de ce système informatique.</span><span class="sxs-lookup"><span data-stu-id="3bee9-118">The snapshot setting data that is the parent of this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="3bee9-119">**Cible**</span><span class="sxs-lookup"><span data-stu-id="3bee9-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bee9-120">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="3bee9-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="3bee9-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3bee9-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bee9-122">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="3bee9-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3bee9-123">Système informatique qui était la cible de l’application.</span><span class="sxs-lookup"><span data-stu-id="3bee9-123">The computer system that was the target of the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bee9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3bee9-124">Requirements</span></span>



| <span data-ttu-id="3bee9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bee9-125">Requirement</span></span> | <span data-ttu-id="3bee9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bee9-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="3bee9-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3bee9-127">Namespace</span></span><br/> | <span data-ttu-id="3bee9-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="3bee9-128">Root\\CIMV2</span></span><br/> |



 

 




