---
description: Sert de classe parente pour la \_ \_ classe système Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Classe __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518306"
---
# <a name="__provider-class"></a><span data-ttu-id="8e974-103">\_\_Classe de fournisseur</span><span class="sxs-lookup"><span data-stu-id="8e974-103">\_\_Provider class</span></span>

<span data-ttu-id="8e974-104">La classe de système **\_ \_ fournisseur** est une classe de base abstraite qui sert de classe parente pour la classe système [**\_ \_ Win32Provider**](--win32provider.md) .</span><span class="sxs-lookup"><span data-stu-id="8e974-104">The **\_\_Provider** system class is an abstract base class that serves as the parent class for the [**\_\_Win32Provider**](--win32provider.md) system class.</span></span>

<span data-ttu-id="8e974-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8e974-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8e974-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8e974-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e974-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e974-107">Syntax</span></span>

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="8e974-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8e974-108">Members</span></span>

<span data-ttu-id="8e974-109">La classe de **\_ \_ fournisseur** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8e974-109">The **\_\_Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="8e974-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e974-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e974-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8e974-111">Properties</span></span>

<span data-ttu-id="8e974-112">La classe de **\_ \_ fournisseur** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8e974-112">The **\_\_Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e974-113">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8e974-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e974-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8e974-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e974-115">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8e974-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="8e974-116">Qualificateurs : [ **clé**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="8e974-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="8e974-117">Chaîne indépendante du langage qui identifie le fournisseur de manière unique.</span><span class="sxs-lookup"><span data-stu-id="8e974-117">Language-neutral string that uniquely identifies the provider.</span></span> <span data-ttu-id="8e974-118">Le format suivant est suggéré pour empêcher les conflits de noms :</span><span class="sxs-lookup"><span data-stu-id="8e974-118">The following format is suggested to prevent naming conflicts:</span></span>

<span data-ttu-id="8e974-119">\|version du fournisseur fournisseur \|</span><span class="sxs-lookup"><span data-stu-id="8e974-119">vendor\|provider\|version</span></span>

<span data-ttu-id="8e974-120">Par exemple, le nom de ce fournisseur représente la version 1,0 de Microsoft TestProvider :</span><span class="sxs-lookup"><span data-stu-id="8e974-120">For example, this provider name represents version 1.0 of the Microsoft TestProvider:</span></span>

<span data-ttu-id="8e974-121">« Microsoft \| TestProvider \| v 1.0 »</span><span class="sxs-lookup"><span data-stu-id="8e974-121">"Microsoft\|TestProvider\|V1.0"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e974-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8e974-122">Remarks</span></span>

<span data-ttu-id="8e974-123">La classe de **\_ \_ fournisseur** est dérivée de [**\_ \_ SystemClass**](--systemclass.md), qui n’a pas de propriétés.</span><span class="sxs-lookup"><span data-stu-id="8e974-123">The **\_\_Provider** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="8e974-124">Les fournisseurs créent des instances [**\_ \_ Win32Provider**](--win32provider.md) pour spécifier des informations sur leur implémentation physique.</span><span class="sxs-lookup"><span data-stu-id="8e974-124">Providers create [**\_\_Win32Provider**](--win32provider.md) instances to specify information about their physical implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e974-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e974-125">Requirements</span></span>



| <span data-ttu-id="8e974-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e974-126">Requirement</span></span> | <span data-ttu-id="8e974-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e974-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8e974-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e974-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8e974-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e974-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8e974-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8e974-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8e974-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e974-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8e974-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8e974-132">Namespace</span></span><br/>                | <span data-ttu-id="8e974-133">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="8e974-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8e974-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e974-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e974-135">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="8e974-135">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="8e974-136">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="8e974-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8e974-137">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="8e974-137">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

