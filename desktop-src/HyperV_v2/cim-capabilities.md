---
description: Classe abstraite pour les sous-classes qui décrit les capacités d’un élément géré associé et le potentiel des capacités.
ms.assetid: f0ffddf5-99d4-49be-ac0a-c2cfd4a92d96
title: Classe CIM_Capabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Capabilities
- CIM_Capabilities.InstanceID
- CIM_Capabilities.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e08fcef34c8c2e932851fb428fd32533eee4877e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541834"
---
# <a name="cim_capabilities-class"></a><span data-ttu-id="f7b2a-103">\_Classe des fonctionnalités CIM</span><span class="sxs-lookup"><span data-stu-id="f7b2a-103">CIM\_Capabilities class</span></span>

<span data-ttu-id="f7b2a-104">Classe abstraite pour les sous-classes qui décrit les capacités d’un élément géré associé et le potentiel des capacités.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-104">An abstract class for subclasses that describes the abilities of an associated managed element, and the potential of the abilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b2a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7b2a-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Capabilities"), AMENDMENT]
class CIM_Capabilities : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="f7b2a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f7b2a-106">Members</span></span>

<span data-ttu-id="f7b2a-107">La classe des **\_ fonctionnalités CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f7b2a-107">The **CIM\_Capabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="f7b2a-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7b2a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7b2a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f7b2a-109">Properties</span></span>

<span data-ttu-id="f7b2a-110">La classe des **\_ fonctionnalités CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-110">The **CIM\_Capabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7b2a-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f7b2a-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7b2a-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7b2a-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7b2a-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7b2a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7b2a-114">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="f7b2a-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="f7b2a-115">Nom convivial de cette instance de classe.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-115">The user friendly name for this class instance.</span></span> <span data-ttu-id="f7b2a-116">En outre, le nom convivial de l’utilisateur peut être utilisé comme propriété d’index pour une requête.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-116">In addition, the user friendly name can be used as a index property for a query.</span></span> <span data-ttu-id="f7b2a-117">Cette valeur ne doit pas nécessairement être unique dans son espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-117">This value does not have to be unique within its namespace.</span></span>

</dd> <dt>

<span data-ttu-id="f7b2a-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f7b2a-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7b2a-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f7b2a-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7b2a-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f7b2a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7b2a-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="f7b2a-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="f7b2a-122">Identifie de façon unique et opaque une instance de cette classe dans la portée de l’espace de noms conteneur.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-122">Uniquely and opaquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f7b2a-123">Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="f7b2a-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="f7b2a-124">*Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou d’autre nom unique qui est détenu par l’entité métier qui définit l' **InstanceID**, ou être un ID inscrit qui est affecté par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="f7b2a-125">Ce modèle est similaire à la structure des noms de classes de schéma.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-125">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="f7b2a-126">En outre, pour garantir l’unicité, les premiers deux-points dans **InstanceID** doivent être compris entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-126">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="f7b2a-127">Par conséquent, le *identifiant OrgID* ne doit pas contenir de signe deux-points («  : »).</span><span class="sxs-lookup"><span data-stu-id="f7b2a-127">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="f7b2a-128">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-128">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="f7b2a-129">Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-129">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="f7b2a-130">Pour les instances définies pour Distributed Management Task Force (DMTF), le modèle doit être utilisé avec le *identifiant OrgID* défini sur CIM.</span><span class="sxs-lookup"><span data-stu-id="f7b2a-130">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7b2a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7b2a-131">Requirements</span></span>



| <span data-ttu-id="f7b2a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7b2a-132">Requirement</span></span> | <span data-ttu-id="f7b2a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7b2a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b2a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b2a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b2a-135">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f7b2a-135">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f7b2a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7b2a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b2a-137">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f7b2a-137">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f7b2a-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7b2a-138">Namespace</span></span><br/>                | <span data-ttu-id="f7b2a-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f7b2a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f7b2a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f7b2a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7b2a-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7b2a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7b2a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b2a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b2a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7b2a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7b2a-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7b2a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b2a-145">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f7b2a-145">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

