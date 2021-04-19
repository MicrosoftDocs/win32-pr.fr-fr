---
description: Contient les droits de sécurité de l’espace de noms sous la forme d’un descripteur de sécurité.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: classe __thisNAMESPACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524392"
---
# <a name="__thisnamespace-class"></a><span data-ttu-id="5ddd3-103">\_\_thisNAMESPACE, classe</span><span class="sxs-lookup"><span data-stu-id="5ddd3-103">\_\_thisNAMESPACE class</span></span>

<span data-ttu-id="5ddd3-104">La classe système **\_ \_ thisNAMESPACE** contient les droits de sécurité pour l’espace de noms sous la forme d’un descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-104">The **\_\_thisNAMESPACE** system class holds the security rights for the namespace in the form of a security descriptor.</span></span> <span data-ttu-id="5ddd3-105">Cette classe et une instance unique se trouvent dans tous les espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-105">This class and a single instance is found in all namespaces.</span></span>

<span data-ttu-id="5ddd3-106">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5ddd3-107">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ddd3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ddd3-108">Syntax</span></span>

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a><span data-ttu-id="5ddd3-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5ddd3-109">Members</span></span>

<span data-ttu-id="5ddd3-110">La classe **\_ \_ thisNAMESPACE** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5ddd3-110">The **\_\_thisNAMESPACE** class has these types of members:</span></span>

-   [<span data-ttu-id="5ddd3-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5ddd3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ddd3-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5ddd3-112">Properties</span></span>

<span data-ttu-id="5ddd3-113">La classe **\_ \_ thisNAMESPACE** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-113">The **\_\_thisNAMESPACE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ddd3-114">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="5ddd3-114">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ddd3-115">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="5ddd3-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5ddd3-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5ddd3-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ddd3-117">Descripteur de sécurité décrivant qui peut accéder à l’espace de noms et qui peut lire ou écrire dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-117">Security descriptor describing who can access the namespace and who can read from or write to the namespace.</span></span> <span data-ttu-id="5ddd3-118">Cette propriété est héritée de l' [**\_ \_ événement**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="5ddd3-118">This property is inherited from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="5ddd3-119">Pour plus d’informations sur le format des descripteurs de sécurité, voir [descripteurs de sécurité](/windows/desktop/SecAuthZ/security-descriptors) dans la section sécurité de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-119">For more information about the format of security descriptors, see [Security Descriptors](/windows/desktop/SecAuthZ/security-descriptors) in the Security section of the Windows SDK.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ddd3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="5ddd3-120">Remarks</span></span>

<span data-ttu-id="5ddd3-121">L’instance singleton de **\_ \_ thisNAMESPACE** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5ddd3-121">The singleton instance of **\_\_thisNAMESPACE** is read-only.</span></span> <span data-ttu-id="5ddd3-122">Pour modifier les paramètres de la propriété descripteur de sécurité, utilisez les méthodes de la classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="5ddd3-122">To change the settings of the security descriptor property, use the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span> <span data-ttu-id="5ddd3-123">La classe **\_ \_ thisNAMESPACE** dérive de [**\_ \_ SystemClass**](--systemclass.md).</span><span class="sxs-lookup"><span data-stu-id="5ddd3-123">The **\_\_thisNAMESPACE** class derives from [**\_\_SystemClass**](--systemclass.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ddd3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ddd3-124">Requirements</span></span>



| <span data-ttu-id="5ddd3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ddd3-125">Requirement</span></span> | <span data-ttu-id="5ddd3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ddd3-126">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5ddd3-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ddd3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5ddd3-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ddd3-128">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5ddd3-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ddd3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5ddd3-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ddd3-130">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5ddd3-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5ddd3-131">Namespace</span></span><br/>                | <span data-ttu-id="5ddd3-132">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="5ddd3-132">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5ddd3-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ddd3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddd3-134">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="5ddd3-134">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="5ddd3-135">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="5ddd3-135">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

