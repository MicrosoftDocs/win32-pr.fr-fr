---
description: La \_ classe LogonSessionMappedDisk Win32 représente une association entre une ouverture de session et les disques logiques mappés définis dans la session.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Classe Win32_LogonSessionMappedDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524268"
---
# <a name="win32_logonsessionmappeddisk-class"></a><span data-ttu-id="b50e9-103">\_Classe LogonSessionMappedDisk Win32</span><span class="sxs-lookup"><span data-stu-id="b50e9-103">Win32\_LogonSessionMappedDisk class</span></span>

<span data-ttu-id="b50e9-104">La \_ classe LogonSessionMappedDisk Win32 représente une association entre une ouverture de session et les disques logiques mappés définis dans la session.</span><span class="sxs-lookup"><span data-stu-id="b50e9-104">The Win32\_LogonSessionMappedDisk class represents an association between a logon session and the mapped logical disks defined within the session.</span></span>

<span data-ttu-id="b50e9-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b50e9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50e9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b50e9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b50e9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b50e9-107">Members</span></span>

<span data-ttu-id="b50e9-108">La classe **Win32 \_ LogonSessionMappedDisk** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b50e9-108">The **Win32\_LogonSessionMappedDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="b50e9-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b50e9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b50e9-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b50e9-110">Properties</span></span>

<span data-ttu-id="b50e9-111">La classe **Win32 \_ LogonSessionMappedDisk** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b50e9-111">The **Win32\_LogonSessionMappedDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b50e9-112">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="b50e9-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b50e9-113">Type de données : **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="b50e9-113">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="b50e9-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b50e9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b50e9-115">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b50e9-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b50e9-116">La propriété Antecedent fait référence à une ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="b50e9-116">The Antecedent property references a logon session.</span></span>

</dd> <dt>

<span data-ttu-id="b50e9-117">**Charge**</span><span class="sxs-lookup"><span data-stu-id="b50e9-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b50e9-118">Type de données : **Win32 \_ MappedLogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="b50e9-118">Data type: **Win32\_MappedLogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="b50e9-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b50e9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b50e9-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (« Dependent »), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b50e9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b50e9-121">La propriété dépendante fait référence à un disque logique mappé défini dans la session référencée par la propriété Antecedent.</span><span class="sxs-lookup"><span data-stu-id="b50e9-121">The Dependent property references a mapped logical disk defined within the session referenced by the Antecedent property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b50e9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b50e9-122">Requirements</span></span>



| <span data-ttu-id="b50e9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b50e9-123">Requirement</span></span> | <span data-ttu-id="b50e9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b50e9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b50e9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b50e9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b50e9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b50e9-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b50e9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b50e9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b50e9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b50e9-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b50e9-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b50e9-129">Namespace</span></span><br/>                | <span data-ttu-id="b50e9-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b50e9-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b50e9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b50e9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b50e9-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b50e9-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b50e9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b50e9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b50e9-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b50e9-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b50e9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b50e9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50e9-136">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="b50e9-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

