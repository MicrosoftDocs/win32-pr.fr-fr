---
description: Association entre un objet et un autre objet qui lui a été appliqué.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Classe CIM_LastAppliedSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536457"
---
# <a name="cim_lastappliedsettingdata-class"></a><span data-ttu-id="f5617-103">\_Classe CIM LastAppliedSettingData</span><span class="sxs-lookup"><span data-stu-id="f5617-103">CIM\_LastAppliedSettingData class</span></span>

<span data-ttu-id="f5617-104">Association entre un objet et un autre objet qui lui a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="f5617-104">An association between an object and another object which has been applied to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5617-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="f5617-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5617-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5617-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5617-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f5617-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5617-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5617-108">Syntax</span></span>

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a><span data-ttu-id="f5617-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f5617-109">Members</span></span>

<span data-ttu-id="f5617-110">La classe **CIM \_ LastAppliedSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f5617-110">The **CIM\_LastAppliedSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="f5617-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5617-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5617-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f5617-112">Properties</span></span>

<span data-ttu-id="f5617-113">La classe **CIM \_ LastAppliedSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f5617-113">The **CIM\_LastAppliedSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5617-114">**AppliedObject**</span><span class="sxs-lookup"><span data-stu-id="f5617-114">**AppliedObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5617-115">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="f5617-115">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f5617-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5617-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5617-117">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f5617-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f5617-118">Objet qui a été appliqué à l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="f5617-118">The object that was applied to the target object.</span></span>

</dd> <dt>

<span data-ttu-id="f5617-119">**Cible**</span><span class="sxs-lookup"><span data-stu-id="f5617-119">**Target**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5617-120">Type de données : **CIM \_ propriété ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="f5617-120">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f5617-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f5617-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5617-122">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="f5617-122">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f5617-123">Objet qui était la cible de l’application de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f5617-123">The object that was the target of the object's application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5617-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5617-124">Requirements</span></span>



| <span data-ttu-id="f5617-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5617-125">Requirement</span></span> | <span data-ttu-id="f5617-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5617-126">Value</span></span> |
|----------------------|------------------------|
| <span data-ttu-id="f5617-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f5617-127">Namespace</span></span><br/> | <span data-ttu-id="f5617-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="f5617-128">Root\\CIMV2</span></span><br/> |



 

 




