---
description: La \_ classe WMI de l’Association ClientApplicationSetting Win32 associe un fichier exécutable et une application COM (Component Object Model) qui contient les options de configuration com pour le fichier exécutable.
ms.assetid: c43d80ee-0f29-4452-b51f-f18543bc1d35
ms.tgt_platform: multiple
title: Classe Win32_ClientApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClientApplicationSetting
- Win32_ClientApplicationSetting.Application
- Win32_ClientApplicationSetting.Client
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fda1f1305904fa919bb2080fe5de02f0e5850a8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950767"
---
# <a name="win32_clientapplicationsetting-class"></a><span data-ttu-id="8b990-103">\_Classe ClientApplicationSetting Win32</span><span class="sxs-lookup"><span data-stu-id="8b990-103">Win32\_ClientApplicationSetting class</span></span>

<span data-ttu-id="8b990-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de l’Association **\_ ClientApplicationSetting Win32** associe un fichier exécutable et une application COM (Component Object Model) qui contient les options de configuration com pour le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="8b990-104">The **Win32\_ClientApplicationSetting** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an executable file and a Component Object Model (COM) application that contains the COM configuration options for the executable file.</span></span>

<span data-ttu-id="8b990-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8b990-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8b990-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8b990-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b990-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b990-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{0F73ED5E-8ED9-11d2-B340-00105A1F8569}"), AMENDMENT]
class Win32_ClientApplicationSetting
{
  Win32_DCOMApplication REF Application;
  CIM_DataFile          REF Client;
};
```

## <a name="members"></a><span data-ttu-id="8b990-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8b990-108">Members</span></span>

<span data-ttu-id="8b990-109">La classe **Win32 \_ ClientApplicationSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b990-109">The **Win32\_ClientApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8b990-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b990-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8b990-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8b990-111">Properties</span></span>

<span data-ttu-id="8b990-112">La classe **Win32 \_ ClientApplicationSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8b990-112">The **Win32\_ClientApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8b990-113">**Application**</span><span class="sxs-lookup"><span data-stu-id="8b990-113">**Application**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b990-114">Type de données : **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="8b990-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="8b990-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b990-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b990-116">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="8b990-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="8b990-117">Référence à l’instance de qui représente l’application COM qui contient les options de configuration du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="8b990-117">Reference to the instance that represents the COM application that contains configuration options of the executable file.</span></span>

</dd> <dt>

<span data-ttu-id="8b990-118">**Client**</span><span class="sxs-lookup"><span data-stu-id="8b990-118">**Client**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8b990-119">Type de données **: \_ fichier** de données CIM</span><span class="sxs-lookup"><span data-stu-id="8b990-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="8b990-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8b990-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8b990-121">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("fichier de fichier CIM CIM \| \_ ")</span><span class="sxs-lookup"><span data-stu-id="8b990-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="8b990-122">Référence à l’instance qui représente le fichier exécutable qui utilise les paramètres COM.</span><span class="sxs-lookup"><span data-stu-id="8b990-122">Reference to the instance that represents the executable file that uses COM settings.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b990-123">Notes</span><span class="sxs-lookup"><span data-stu-id="8b990-123">Remarks</span></span>

<span data-ttu-id="8b990-124">**Win32 \_ ClientApplicationSetting** ne prend pas en charge l’énumération.</span><span class="sxs-lookup"><span data-stu-id="8b990-124">**Win32\_ClientApplicationSetting** does not support enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b990-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b990-125">Requirements</span></span>



| <span data-ttu-id="8b990-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b990-126">Requirement</span></span> | <span data-ttu-id="8b990-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b990-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b990-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b990-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8b990-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b990-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b990-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b990-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8b990-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b990-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b990-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b990-132">Namespace</span></span><br/>                | <span data-ttu-id="8b990-133">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8b990-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8b990-134">MOF</span><span class="sxs-lookup"><span data-stu-id="8b990-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b990-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b990-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b990-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8b990-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b990-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b990-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b990-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b990-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="8b990-139">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b990-139">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

