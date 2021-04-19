---
description: La \_ classe propriété MANAGEDELEMENT CIM est une classe abstraite qui fournit une superclasse commune (ou supérieure de l’arborescence d’héritage) pour les classes non-association dans le schéma CIM.
ms.assetid: 6655a480-37bd-403c-9673-4eaa3d381201
title: Classe CIM_ManagedElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedElement
- CIM_ManagedElement.InstanceID
- CIM_ManagedElement.Caption
- CIM_ManagedElement.Description
- CIM_ManagedElement.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5d98c6e594103932b180fcb63a2eebaf2c328c4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515597"
---
# <a name="cim_managedelement-class"></a><span data-ttu-id="a9177-103">\_Classe CIM propriété ManagedElement</span><span class="sxs-lookup"><span data-stu-id="a9177-103">CIM\_ManagedElement class</span></span>

<span data-ttu-id="a9177-104">La **classe \_ propriété ManagedElement CIM** est une classe abstraite qui fournit une superclasse commune (ou supérieure de l’arborescence d’héritage) pour les classes non-association dans le schéma CIM.</span><span class="sxs-lookup"><span data-stu-id="a9177-104">The **CIM\_ManagedElement** class is an abstract class that provides a common superclass (or top of the inheritance tree) for the non-association classes in the CIM Schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9177-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9177-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="a9177-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a9177-106">Members</span></span>

<span data-ttu-id="a9177-107">La classe **CIM \_ propriété ManagedElement** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a9177-107">The **CIM\_ManagedElement** class has these types of members:</span></span>

-   [<span data-ttu-id="a9177-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9177-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9177-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a9177-109">Properties</span></span>

<span data-ttu-id="a9177-110">La classe **CIM \_ propriété ManagedElement** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9177-110">The **CIM\_ManagedElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9177-111">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a9177-111">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9177-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9177-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9177-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9177-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9177-114">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a9177-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a9177-115">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9177-115">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a9177-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="a9177-116">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9177-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9177-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9177-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9177-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9177-119">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9177-119">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a9177-120">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a9177-120">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9177-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9177-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9177-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9177-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9177-123">Nom convivial de l’objet.</span><span class="sxs-lookup"><span data-stu-id="a9177-123">A user-friendly name for the object.</span></span> <span data-ttu-id="a9177-124">Cette propriété permet à chaque instance de définir un nom convivial en plus de ses propriétés de clé, données d’identité et informations de description.</span><span class="sxs-lookup"><span data-stu-id="a9177-124">This property allows each instance to define a user-friendly name in addition to its key properties, identity data, and description information.</span></span>

</dd> <dt>

<span data-ttu-id="a9177-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a9177-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9177-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a9177-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9177-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a9177-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9177-128">Identifie de façon unique et opaque une instance de cette classe dans la portée de l’espace de noms conteneur.</span><span class="sxs-lookup"><span data-stu-id="a9177-128">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="a9177-129">Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="a9177-129">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="a9177-130">*Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou d’autre nom unique qui est détenu par l’entité métier qui définit l' **InstanceID**, ou être un ID inscrit qui est affecté par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="a9177-130">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="a9177-131">Ce modèle est similaire à la structure des noms de classes de schéma.</span><span class="sxs-lookup"><span data-stu-id="a9177-131">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="a9177-132">En outre, pour garantir l’unicité, les premiers deux-points dans **InstanceID** doivent être compris entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="a9177-132">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="a9177-133">Par conséquent, le *identifiant OrgID* ne doit pas contenir de signe deux-points («  : »).</span><span class="sxs-lookup"><span data-stu-id="a9177-133">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="a9177-134">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.</span><span class="sxs-lookup"><span data-stu-id="a9177-134">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="a9177-135">Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="a9177-135">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="a9177-136">Pour les instances définies pour Distributed Management Task Force (DMTF), le modèle doit être utilisé avec le *identifiant OrgID* défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="a9177-136">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9177-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9177-137">Requirements</span></span>



| <span data-ttu-id="a9177-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9177-138">Requirement</span></span> | <span data-ttu-id="a9177-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9177-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9177-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9177-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a9177-141">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a9177-141">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a9177-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9177-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a9177-143">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9177-143">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a9177-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a9177-144">Namespace</span></span><br/>                | <span data-ttu-id="a9177-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a9177-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a9177-146">MOF</span><span class="sxs-lookup"><span data-stu-id="a9177-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9177-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9177-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9177-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a9177-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9177-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a9177-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

