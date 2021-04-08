---
description: La \_ classe WMI de l’Association ShareToDirectory Win32 associe une ressource partagée sur le système de l’ordinateur et le répertoire auquel elle est mappée.
ms.assetid: f8562539-2cb4-4661-8ef9-8b665e76a292
ms.tgt_platform: multiple
title: Classe Win32_ShareToDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShareToDirectory
- Win32_ShareToDirectory.Share
- Win32_ShareToDirectory.SharedElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f02e5e1ce125a2c8495327a08c14c94ac9f48567
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747821"
---
# <a name="win32_sharetodirectory-class"></a><span data-ttu-id="ad8a6-103">\_Classe ShareToDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="ad8a6-103">Win32\_ShareToDirectory class</span></span>

<span data-ttu-id="ad8a6-104">La [classe WMI](../wmisdk/retrieving-a-class.md) de l’Association **\_ ShareToDirectory Win32** associe une ressource partagée sur le système de l’ordinateur et le répertoire auquel elle est mappée.</span><span class="sxs-lookup"><span data-stu-id="ad8a6-104">The **Win32\_ShareToDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a shared resource on the computer system and the directory to which it is mapped.</span></span>

<span data-ttu-id="ad8a6-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ad8a6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ad8a6-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="ad8a6-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad8a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad8a6-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{8502C511-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ShareToDirectory
{
  Win32_Share   REF Share;
  CIM_Directory REF SharedElement;
};
```

## <a name="members"></a><span data-ttu-id="ad8a6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ad8a6-108">Members</span></span>

<span data-ttu-id="ad8a6-109">La classe **Win32 \_ ShareToDirectory** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ad8a6-109">The **Win32\_ShareToDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="ad8a6-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad8a6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad8a6-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ad8a6-111">Properties</span></span>

<span data-ttu-id="ad8a6-112">La classe **Win32 \_ ShareToDirectory** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ad8a6-112">The **Win32\_ShareToDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad8a6-113">**Partager**</span><span class="sxs-lookup"><span data-stu-id="ad8a6-113">**Share**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad8a6-114">Type de données **: \_ partage Win32**</span><span class="sxs-lookup"><span data-stu-id="ad8a6-114">Data type: **Win32\_Share**</span></span>
</dt> <dt>

<span data-ttu-id="ad8a6-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad8a6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad8a6-116">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« \| partage WMI Win32 \_ »)</span><span class="sxs-lookup"><span data-stu-id="ad8a6-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Share")</span></span>
</dt> </dl>

<span data-ttu-id="ad8a6-117">Référence à l’instance de qui représente les propriétés d’une ressource partagée disponible par le biais du répertoire.</span><span class="sxs-lookup"><span data-stu-id="ad8a6-117">Reference to the instance representing the properties of a shared resource available through the directory.</span></span>

</dd> <dt>

<span data-ttu-id="ad8a6-118">**SharedElement**</span><span class="sxs-lookup"><span data-stu-id="ad8a6-118">**SharedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad8a6-119">Type de données **: \_ répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="ad8a6-119">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="ad8a6-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad8a6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad8a6-121">Qualificateurs : [**clé**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« répertoire CIM CIM \| \_ »)</span><span class="sxs-lookup"><span data-stu-id="ad8a6-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="ad8a6-122">Référence à l’instance représentant les propriétés du répertoire qui a été mappé à une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="ad8a6-122">Reference to the instance representing the properties of the directory that has been mapped to a shared resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad8a6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad8a6-123">Requirements</span></span>



| <span data-ttu-id="ad8a6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad8a6-124">Requirement</span></span> | <span data-ttu-id="ad8a6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad8a6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad8a6-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad8a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ad8a6-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad8a6-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad8a6-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad8a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ad8a6-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad8a6-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad8a6-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad8a6-130">Namespace</span></span><br/>                | <span data-ttu-id="ad8a6-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ad8a6-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad8a6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ad8a6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad8a6-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad8a6-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad8a6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ad8a6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad8a6-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad8a6-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad8a6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad8a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad8a6-137">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="ad8a6-137">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
