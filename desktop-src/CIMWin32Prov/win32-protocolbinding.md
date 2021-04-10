---
description: La \_ classe WMI de l’Association ProtocolBinding Win32 associe un pilote au niveau du système, un protocole réseau et une carte réseau.
ms.assetid: 09b84bb2-9999-4e80-a330-88ed6b2bd5e9
ms.tgt_platform: multiple
title: Classe Win32_ProtocolBinding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProtocolBinding
- Win32_ProtocolBinding.Antecedent
- Win32_ProtocolBinding.Dependent
- Win32_ProtocolBinding.Device
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91e735a599a1dda2536fe26bcd654dcdf4b119dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860693"
---
# <a name="win32_protocolbinding-class"></a><span data-ttu-id="b2d61-103">\_Classe ProtocolBinding Win32</span><span class="sxs-lookup"><span data-stu-id="b2d61-103">Win32\_ProtocolBinding class</span></span>

<span data-ttu-id="b2d61-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ ProtocolBinding Win32** associe un pilote au niveau du système, un protocole réseau et une carte réseau.</span><span class="sxs-lookup"><span data-stu-id="b2d61-104">The **Win32\_ProtocolBinding** association [WMI class](../wmisdk/retrieving-a-class.md) relates a system-level driver, network protocol, and network adapter.</span></span>

<span data-ttu-id="b2d61-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b2d61-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b2d61-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b2d61-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2d61-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2d61-107">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("CIMWin32"), UUID("{8502C509-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProtocolBinding
{
  Win32_NetworkProtocol REF Antecedent;
  Win32_SystemDriver    REF Dependent;
  Win32_NetworkAdapter  REF Device;
};
```

## <a name="members"></a><span data-ttu-id="b2d61-108">Membres</span><span class="sxs-lookup"><span data-stu-id="b2d61-108">Members</span></span>

<span data-ttu-id="b2d61-109">La classe **Win32 \_ ProtocolBinding** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b2d61-109">The **Win32\_ProtocolBinding** class has these types of members:</span></span>

-   [<span data-ttu-id="b2d61-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2d61-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2d61-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2d61-111">Properties</span></span>

<span data-ttu-id="b2d61-112">La classe **Win32 \_ ProtocolBinding** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b2d61-112">The **Win32\_ProtocolBinding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2d61-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b2d61-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d61-114">Type de données : **Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="b2d61-114">Data type: **Win32\_NetworkProtocol**</span></span>
</dt> <dt>

<span data-ttu-id="b2d61-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2d61-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2d61-116">Qualificateurs : [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkProtocol")</span><span class="sxs-lookup"><span data-stu-id="b2d61-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="b2d61-117">Référence à l’instance de qui représente le protocole utilisé avec le pilote système et sur la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="b2d61-117">Reference to the instance representing the protocol that is used with the system driver and on the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="b2d61-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b2d61-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d61-119">Type de données : **Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="b2d61-119">Data type: **Win32\_SystemDriver**</span></span>
</dt> <dt>

<span data-ttu-id="b2d61-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2d61-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2d61-121">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")</span><span class="sxs-lookup"><span data-stu-id="b2d61-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SystemDriver")</span></span>
</dt> </dl>

<span data-ttu-id="b2d61-122">Référence à l’instance de qui représente le pilote système qui utilise la carte réseau via le protocole réseau de cette classe.</span><span class="sxs-lookup"><span data-stu-id="b2d61-122">Reference to the instance representing the system driver that uses the network adapter through the network protocol of this class.</span></span>

</dd> <dt>

<span data-ttu-id="b2d61-123">**Appareil**</span><span class="sxs-lookup"><span data-stu-id="b2d61-123">**Device**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2d61-124">Type de données : carte réseau **Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="b2d61-124">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="b2d61-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b2d61-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2d61-126">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« WMI \| Win32 \_ NetworkAdapter »)</span><span class="sxs-lookup"><span data-stu-id="b2d61-126">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="b2d61-127">Propriétés de la carte réseau utilisée sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="b2d61-127">Properties of the network adapter being used on the computer system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2d61-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2d61-128">Requirements</span></span>



| <span data-ttu-id="b2d61-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2d61-129">Requirement</span></span> | <span data-ttu-id="b2d61-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2d61-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d61-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2d61-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d61-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2d61-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2d61-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2d61-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d61-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2d61-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2d61-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b2d61-135">Namespace</span></span><br/>                | <span data-ttu-id="b2d61-136">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b2d61-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b2d61-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b2d61-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2d61-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2d61-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2d61-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b2d61-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2d61-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2d61-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2d61-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2d61-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2d61-142">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b2d61-142">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
