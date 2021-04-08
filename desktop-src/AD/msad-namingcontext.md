---
title: Classe MSAD_NamingContext
description: Représente un contexte d’appellation (NC) particulier sur le contrôleur de domaine.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- MSAD_NamingContext de la classe Active Directory
- MSAD_NamingContext de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68f70c6e40e823df0a6827e1114f40dae7937be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741588"
---
# <a name="msad_namingcontext-class"></a><span data-ttu-id="be8b2-105">MSAD \_ du DN, classe</span><span class="sxs-lookup"><span data-stu-id="be8b2-105">MSAD\_NamingContext class</span></span>

<span data-ttu-id="be8b2-106">Représente un contexte d’appellation (NC) particulier sur le contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="be8b2-106">Represents a particular naming context (NC) on the domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8b2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be8b2-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="be8b2-108">Membres</span><span class="sxs-lookup"><span data-stu-id="be8b2-108">Members</span></span>

<span data-ttu-id="be8b2-109">La classe **MSAD \_ du DN** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="be8b2-109">The **MSAD\_NamingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="be8b2-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be8b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be8b2-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be8b2-111">Properties</span></span>

<span data-ttu-id="be8b2-112">La classe **MSAD \_ du DN** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="be8b2-112">The **MSAD\_NamingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be8b2-113">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="be8b2-113">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8b2-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="be8b2-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="be8b2-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be8b2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be8b2-116">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="be8b2-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="be8b2-117">Obtient le chemin d’accès X. 500 du contexte de nommage.</span><span class="sxs-lookup"><span data-stu-id="be8b2-117">Gets the X.500 path of the NC.</span></span>

</dd> <dt>

<span data-ttu-id="be8b2-118">**IsFullReplica**</span><span class="sxs-lookup"><span data-stu-id="be8b2-118">**IsFullReplica**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be8b2-119">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="be8b2-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="be8b2-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="be8b2-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be8b2-121">Obtient la valeur qui indique si le contexte de nommage est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="be8b2-121">Gets the value that indicates whether the NC is read/write.</span></span> <span data-ttu-id="be8b2-122">**True** si le contexte de nommage est en lecture/écriture ; **False** si le contexte de nommage est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="be8b2-122">**TRUE** if the NC is read/write; **FALSE** if the NC is read-only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be8b2-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be8b2-123">Requirements</span></span>



| <span data-ttu-id="be8b2-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be8b2-124">Requirement</span></span> | <span data-ttu-id="be8b2-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="be8b2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be8b2-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be8b2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be8b2-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="be8b2-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="be8b2-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be8b2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be8b2-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be8b2-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be8b2-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be8b2-130">Namespace</span></span><br/>                | <span data-ttu-id="be8b2-131">\\MicrosoftActiveDirectory racine</span><span class="sxs-lookup"><span data-stu-id="be8b2-131">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="be8b2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="be8b2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be8b2-133"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be8b2-133"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="be8b2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="be8b2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be8b2-135"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be8b2-135"><dt>Replprov.dll</dt></span></span> </dl> |



 

