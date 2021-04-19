---
description: La \_ classe WMI d’association SessionProcess Win32 représente une association entre une ouverture de session et les processus associés à cette session.
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Classe Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516562"
---
# <a name="win32_sessionprocess-class"></a><span data-ttu-id="0b15b-103">\_Classe SessionProcess Win32</span><span class="sxs-lookup"><span data-stu-id="0b15b-103">Win32\_SessionProcess class</span></span>

<span data-ttu-id="0b15b-104">La [classe WMI](../wmisdk/retrieving-a-class.md) d’association **\_ SessionProcess Win32** représente une association entre une ouverture de session et les processus associés à cette session.</span><span class="sxs-lookup"><span data-stu-id="0b15b-104">The **Win32\_SessionProcess** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between a logon session and the processes associated with that session.</span></span>

<span data-ttu-id="0b15b-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0b15b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0b15b-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="0b15b-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b15b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b15b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0b15b-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0b15b-108">Members</span></span>

<span data-ttu-id="0b15b-109">La classe **Win32 \_ SessionProcess** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0b15b-109">The **Win32\_SessionProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="0b15b-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0b15b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b15b-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0b15b-111">Properties</span></span>

<span data-ttu-id="0b15b-112">La classe **Win32 \_ SessionProcess** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0b15b-112">The **Win32\_SessionProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b15b-113">**Antécédent**</span><span class="sxs-lookup"><span data-stu-id="0b15b-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b15b-114">Type de données : **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="0b15b-114">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="0b15b-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0b15b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b15b-116">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**clé**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0b15b-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="0b15b-117">[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) qui représente la session associée au processus.</span><span class="sxs-lookup"><span data-stu-id="0b15b-117">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that represents the session which is related to the process.</span></span>

</dd> <dt>

<span data-ttu-id="0b15b-118">**Charge**</span><span class="sxs-lookup"><span data-stu-id="0b15b-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b15b-119">Type de données **: \_ processus Win32**</span><span class="sxs-lookup"><span data-stu-id="0b15b-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="0b15b-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0b15b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b15b-121">Qualificateurs : [**override**](../wmisdk/standard-qualifiers.md) (« Dependent »), [**Key**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0b15b-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="0b15b-122">[**\_ Processus Win32**](win32-processor.md) qui représente le processus associé à la session.</span><span class="sxs-lookup"><span data-stu-id="0b15b-122">A [**Win32\_Process**](win32-processor.md) that represents the process associated with the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b15b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="0b15b-123">Remarks</span></span>

<span data-ttu-id="0b15b-124">**Win32 \_ SessionProcess** retourne l’ensemble de la session de l’administrateur lorsqu’il est connecté avec élévation de privilèges ou lorsqu’il est exécuté à distance.</span><span class="sxs-lookup"><span data-stu-id="0b15b-124">**Win32\_SessionProcess** returns all session for the administrator when logged in elevated or when run remotely.</span></span> <span data-ttu-id="0b15b-125">Il s’agit d’une extension du comportement de la classe.</span><span class="sxs-lookup"><span data-stu-id="0b15b-125">This is an extension to the behavior of the class.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b15b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b15b-126">Requirements</span></span>



| <span data-ttu-id="0b15b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b15b-127">Requirement</span></span> | <span data-ttu-id="0b15b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b15b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b15b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b15b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0b15b-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b15b-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b15b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b15b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0b15b-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b15b-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b15b-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0b15b-133">Namespace</span></span><br/>                | <span data-ttu-id="0b15b-134">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0b15b-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b15b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="0b15b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b15b-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b15b-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b15b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0b15b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b15b-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b15b-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b15b-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b15b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b15b-140">**\_SessionResource Win32**</span><span class="sxs-lookup"><span data-stu-id="0b15b-140">**Win32\_SessionResource**</span></span>](win32-sessionresource.md)
</dt> <dt>

[<span data-ttu-id="0b15b-141">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="0b15b-141">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
