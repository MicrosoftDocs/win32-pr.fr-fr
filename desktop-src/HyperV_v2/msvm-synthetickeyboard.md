---
description: Représente un périphérique clavier synthétique.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Classe Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543653"
---
# <a name="msvm_synthetickeyboard-class"></a><span data-ttu-id="82639-103">MSVM \_ SyntheticKeyboard, classe</span><span class="sxs-lookup"><span data-stu-id="82639-103">Msvm\_SyntheticKeyboard class</span></span>

<span data-ttu-id="82639-104">Représente un périphérique clavier synthétique.</span><span class="sxs-lookup"><span data-stu-id="82639-104">Represents a synthetic keyboard device.</span></span>

<span data-ttu-id="82639-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="82639-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="82639-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82639-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a><span data-ttu-id="82639-107">Membres</span><span class="sxs-lookup"><span data-stu-id="82639-107">Members</span></span>

<span data-ttu-id="82639-108">La classe **MSVM \_ SyntheticKeyboard** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="82639-108">The **Msvm\_SyntheticKeyboard** class has these types of members:</span></span>

-   [<span data-ttu-id="82639-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="82639-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="82639-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="82639-110">Methods</span></span>

<span data-ttu-id="82639-111">La classe **MSVM \_ SyntheticKeyboard** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="82639-111">The **Msvm\_SyntheticKeyboard** class has these methods.</span></span>



| <span data-ttu-id="82639-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="82639-112">Method</span></span>                                                                  | <span data-ttu-id="82639-113">Description</span><span class="sxs-lookup"><span data-stu-id="82639-113">Description</span></span>                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="82639-114">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="82639-114">**RequestStateChange**</span></span>](msvm-synthetickeyboard-requeststatechange.md) | <span data-ttu-id="82639-115">Demande un changement d’État.</span><span class="sxs-lookup"><span data-stu-id="82639-115">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="82639-116">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="82639-116">**Reset**</span></span>](msvm-synthetickeyboard-reset.md)                           | <span data-ttu-id="82639-117">réinitialise l’appareil.</span><span class="sxs-lookup"><span data-stu-id="82639-117">resets the device.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="82639-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82639-118">Requirements</span></span>



| <span data-ttu-id="82639-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82639-119">Requirement</span></span> | <span data-ttu-id="82639-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="82639-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82639-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82639-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82639-122">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82639-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="82639-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82639-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82639-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82639-124">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="82639-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="82639-125">Namespace</span></span><br/>                | <span data-ttu-id="82639-126">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="82639-126">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="82639-127">MOF</span><span class="sxs-lookup"><span data-stu-id="82639-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82639-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82639-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="82639-129">DLL</span><span class="sxs-lookup"><span data-stu-id="82639-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82639-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="82639-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="82639-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82639-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82639-132">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="82639-132">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

 




