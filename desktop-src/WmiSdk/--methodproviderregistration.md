---
description: Inscrit les fournisseurs de méthode avec WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: Classe __MethodProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534092"
---
# <a name="__methodproviderregistration-class"></a><span data-ttu-id="c04f0-103">\_\_MethodProviderRegistration, classe</span><span class="sxs-lookup"><span data-stu-id="c04f0-103">\_\_MethodProviderRegistration class</span></span>

<span data-ttu-id="c04f0-104">La classe système **\_ \_ MethodProviderRegistration** inscrit des fournisseurs de méthode avec WMI.</span><span class="sxs-lookup"><span data-stu-id="c04f0-104">The **\_\_MethodProviderRegistration** system class registers method providers with WMI.</span></span>

<span data-ttu-id="c04f0-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c04f0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c04f0-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="c04f0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c04f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c04f0-107">Syntax</span></span>

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="c04f0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c04f0-108">Members</span></span>

<span data-ttu-id="c04f0-109">La classe **\_ \_ MethodProviderRegistration** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c04f0-109">The **\_\_MethodProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="c04f0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c04f0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c04f0-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c04f0-111">Properties</span></span>

<span data-ttu-id="c04f0-112">La classe **\_ \_ MethodProviderRegistration** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="c04f0-112">The **\_\_MethodProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c04f0-113">**moteur**</span><span class="sxs-lookup"><span data-stu-id="c04f0-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c04f0-114">Type de données : **\_ \_ fournisseur**</span><span class="sxs-lookup"><span data-stu-id="c04f0-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="c04f0-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c04f0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c04f0-116">Référence à une instance du [**\_ \_ fournisseur**](--provider.md) qui représente le chemin d’accès de l’objet du fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="c04f0-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the method provider.</span></span> <span data-ttu-id="c04f0-117">Cette propriété est héritée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="c04f0-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c04f0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c04f0-118">Remarks</span></span>

<span data-ttu-id="c04f0-119">La classe **\_ \_ MethodProviderRegistration** est dérivée de [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="c04f0-119">The **\_\_MethodProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="c04f0-120">Seuls les administrateurs peuvent inscrire ou supprimer un fournisseur de méthode en créant une instance de [**\_ \_ Win32Provider**](--win32provider.md) et **\_ \_ MethodProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="c04f0-120">Only administrators can register or delete a method provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_MethodProviderRegistration**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c04f0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c04f0-121">Requirements</span></span>



| <span data-ttu-id="c04f0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c04f0-122">Requirement</span></span> | <span data-ttu-id="c04f0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c04f0-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c04f0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c04f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c04f0-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c04f0-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c04f0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c04f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c04f0-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c04f0-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c04f0-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c04f0-128">Namespace</span></span><br/>                | <span data-ttu-id="c04f0-129">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="c04f0-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c04f0-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c04f0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c04f0-131">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="c04f0-131">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="c04f0-132">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="c04f0-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c04f0-133">Inscription d’un fournisseur de méthode</span><span class="sxs-lookup"><span data-stu-id="c04f0-133">Registering a Method Provider</span></span>](registering-a-method-provider.md)
</dt> </dl>

 

