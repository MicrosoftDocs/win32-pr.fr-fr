---
description: Représente les paramètres de configuration et opérationnels pour les \_ instances CIM propriété ManagedElement.
ms.assetid: a9ee0eb6-dc48-43f2-bdb5-f84fe7bbc1f2
title: Classe CIM_SettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingData
- CIM_SettingData.InstanceID
- CIM_SettingData.ElementName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 934aaaf694a79537f5761717f91db398141c33d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203418"
---
# <a name="cim_settingdata-class"></a><span data-ttu-id="5c971-103">\_Classe SETTINGDATA CIM</span><span class="sxs-lookup"><span data-stu-id="5c971-103">CIM\_SettingData class</span></span>

<span data-ttu-id="5c971-104">Représente les paramètres de configuration et opérationnels pour les instances [**CIM \_ propriété ManagedElement**](cim-managedelement.md) .</span><span class="sxs-lookup"><span data-stu-id="5c971-104">Represents configuration and operational parameters for [**CIM\_ManagedElement**](cim-managedelement.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c971-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c971-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingData : CIM_ManagedElement
{
  string InstanceID;
  string ElementName;
};
```

## <a name="members"></a><span data-ttu-id="5c971-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5c971-106">Members</span></span>

<span data-ttu-id="5c971-107">La classe **CIM \_ SettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5c971-107">The **CIM\_SettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5c971-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5c971-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c971-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5c971-109">Properties</span></span>

<span data-ttu-id="5c971-110">La classe **CIM \_ SettingData** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5c971-110">The **CIM\_SettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c971-111">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5c971-111">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c971-112">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5c971-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c971-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5c971-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c971-114">Qualificateurs : [**obligatoire**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="5c971-114">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="5c971-115">Nom convivial d’une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="5c971-115">The user-friendly name for an instance of this class.</span></span> <span data-ttu-id="5c971-116">En outre, le nom convivial peut être utilisé comme index pour une recherche ou une requête.</span><span class="sxs-lookup"><span data-stu-id="5c971-116">In addition, the user-friendly name can be used as an index for a search or query.</span></span> <span data-ttu-id="5c971-117">Le nom ne doit pas nécessairement être unique au sein d’un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="5c971-117">The name does not have to be unique within a namespace.</span></span>

</dd> <dt>

<span data-ttu-id="5c971-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5c971-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c971-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5c971-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c971-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5c971-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c971-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="5c971-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="5c971-122">Identifie de façon unique une instance de cette classe dans la portée de l’espace de noms conteneur.</span><span class="sxs-lookup"><span data-stu-id="5c971-122">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="5c971-123">Pour garantir l’unicité au sein de l’espace de noms, la valeur de la propriété **InstanceID** doit être construite au format suivant : *identifiant OrgID*:*LocalID*</span><span class="sxs-lookup"><span data-stu-id="5c971-123">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> -   <span data-ttu-id="5c971-124">*Identifiant OrgID* doit inclure un nom de droits d’auteur, de marque déposée ou un nom unique qui est détenu par l’entité métier qui définit la propriété **InstanceID** , ou être un ID inscrit qui est attribué par une autorité globale reconnue.</span><span class="sxs-lookup"><span data-stu-id="5c971-124">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID** property, or be a registered ID that is assigned by a recognized global authority.</span></span>
> -   <span data-ttu-id="5c971-125">*Identifiant OrgID* ne doit pas contenir de signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="5c971-125">*OrgID* must not contain a colon.</span></span> <span data-ttu-id="5c971-126">Le premier signe deux-points dans **InstanceID** doit être compris entre *identifiant OrgID* et *LocalID*.</span><span class="sxs-lookup"><span data-stu-id="5c971-126">The first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span>
> -   <span data-ttu-id="5c971-127">*LocalID* est choisi par l’entité métier et ne doit pas être réutilisé pour identifier des éléments réels sous-jacents différents.</span><span class="sxs-lookup"><span data-stu-id="5c971-127">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
> -   <span data-ttu-id="5c971-128">Si le modèle ci-dessus n’est pas utilisé, l’entité de définition doit s’assurer que la valeur **InstanceID** obtenue n’est pas réutilisée dans les propriétés **InstanceID** produites par ce fournisseur ou d’autres fournisseurs pour cet espace de noms.</span><span class="sxs-lookup"><span data-stu-id="5c971-128">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
> -   <span data-ttu-id="5c971-129">Pour les instances DMTF définies, le modèle doit être utilisé avec le *identifiant OrgID* défini sur « CIM ».</span><span class="sxs-lookup"><span data-stu-id="5c971-129">For DMTF defined instances, the pattern must be used with the *OrgID* set to "CIM".</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c971-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c971-130">Requirements</span></span>



| <span data-ttu-id="5c971-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c971-131">Requirement</span></span> | <span data-ttu-id="5c971-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c971-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c971-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c971-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5c971-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5c971-134">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="5c971-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c971-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5c971-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c971-136">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="5c971-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5c971-137">Namespace</span></span><br/>                | <span data-ttu-id="5c971-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5c971-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5c971-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5c971-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c971-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c971-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c971-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5c971-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c971-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5c971-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5c971-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c971-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c971-144">**\_Propriété MANAGEDELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="5c971-144">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

