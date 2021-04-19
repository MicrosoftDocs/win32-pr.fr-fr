---
description: Utilisé pour associer un RegisteredProfile CIM d’instance \_ à une instance de \_ RegisteredProfile CIM d’un autre profil qui fait référence au profil dépendant en tant que profil associé.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: Classe CIM_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518843"
---
# <a name="cim_referencedprofile-class"></a><span data-ttu-id="ec1fb-103">\_Classe CIM ReferencedProfile</span><span class="sxs-lookup"><span data-stu-id="ec1fb-103">CIM\_ReferencedProfile class</span></span>

<span data-ttu-id="ec1fb-104">Utilisé pour associer un [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)) d’instance à une instance **de \_ RegisteredProfile CIM** d’un autre profil qui fait référence au profil dépendant en tant que profil associé.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-104">Used to associate an instance [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) with an instance of **CIM\_RegisteredProfile** of another profile that references the dependent profile as a related profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec1fb-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ec1fb-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ec1fb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ec1fb-107">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec1fb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec1fb-108">Syntax</span></span>

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ec1fb-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ec1fb-109">Members</span></span>

<span data-ttu-id="ec1fb-110">La classe **CIM \_ ReferencedProfile** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ec1fb-110">The **CIM\_ReferencedProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="ec1fb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ec1fb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec1fb-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ec1fb-112">Properties</span></span>

<span data-ttu-id="ec1fb-113">La classe **CIM \_ ReferencedProfile** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-113">The **CIM\_ReferencedProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec1fb-114">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="ec1fb-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec1fb-115">Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ec1fb-115">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="ec1fb-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ec1fb-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec1fb-117">Spécifie l’instance [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)) qui est référencée par le profil **dépendant** .</span><span class="sxs-lookup"><span data-stu-id="ec1fb-117">Specifies the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that is referenced by the **Dependent** profile.</span></span>

</dd> <dt>

<span data-ttu-id="ec1fb-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="ec1fb-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec1fb-119">Type de données : **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ec1fb-119">Data type: **[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="ec1fb-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ec1fb-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec1fb-121">Spécifie une instance [**\_ RegisteredProfile CIM**](/previous-versions//ee309375(v=vs.85)) qui référence d’autres profils.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-121">Specifies a [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) instance that references other profiles.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec1fb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="ec1fb-122">Remarks</span></span>

<span data-ttu-id="ec1fb-123">L’utilisation des propriétés **Dependent** et **Antecedent** dans l’Association **CIM \_ ReferencedProfile** est définie de telle sorte que le profil référencé est l’antécédent et que le profil faisant l’objet d’un référencement soit le dépendant.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-123">The use of the **Dependent** and **Antecedent** properties in the **CIM\_ReferencedProfile** association is defined such that the profile being referenced is the antecedent and the profile doing the referencing is the dependent.</span></span>

<span data-ttu-id="ec1fb-124">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-124">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ec1fb-125">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ec1fb-125">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec1fb-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec1fb-126">Requirements</span></span>



| <span data-ttu-id="ec1fb-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec1fb-127">Requirement</span></span> | <span data-ttu-id="ec1fb-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec1fb-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1fb-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec1fb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1fb-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ec1fb-130">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="ec1fb-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec1fb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1fb-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec1fb-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="ec1fb-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ec1fb-133">Namespace</span></span><br/>                | <span data-ttu-id="ec1fb-134">\\Interop racine</span><span class="sxs-lookup"><span data-stu-id="ec1fb-134">Root\\interop</span></span><br/>                                                               |
| <span data-ttu-id="ec1fb-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ec1fb-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec1fb-136"><dt>Interop. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec1fb-136"><dt>Interop.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec1fb-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec1fb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1fb-138">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="ec1fb-138">**CIM\_Dependency**</span></span>](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

