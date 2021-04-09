---
description: Classe de base abstraite à partir de laquelle toutes les classes de données du fournisseur MCA (machine Check architecture), telles que MSMCAInfo \_ RawMCAData, sont dérivées. Cette classe est disponible uniquement dans les systèmes Windows 64 bits.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: MSMCAInfo, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033970"
---
# <a name="msmcainfo-class"></a><span data-ttu-id="b3a39-104">MSMCAInfo, classe</span><span class="sxs-lookup"><span data-stu-id="b3a39-104">MSMCAInfo class</span></span>

<span data-ttu-id="b3a39-105">La classe **MSMCAInfo** est une classe de base abstraite à partir de laquelle toutes les classes de données du fournisseur MCA (machine Check architecture), telles que [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md), sont dérivées.</span><span class="sxs-lookup"><span data-stu-id="b3a39-105">The **MSMCAInfo** class is an abstract base class from which all Machine Check Architecture (MCA) provider data classes, such as [**MSMCAInfo\_RawMCAData**](msmcainfo-rawmcadata.md), are derived.</span></span> <span data-ttu-id="b3a39-106">Le fournisseur MCA possède également des classes d’événements, dérivées de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="b3a39-106">The MCA provider also has event classes, derived from [**WMIEvent**](wmievent.md).</span></span> <span data-ttu-id="b3a39-107">Cette classe est disponible uniquement dans les systèmes Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b3a39-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="b3a39-108">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b3a39-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b3a39-109">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="b3a39-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3a39-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3a39-110">Syntax</span></span>

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a><span data-ttu-id="b3a39-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b3a39-111">Members</span></span>

<span data-ttu-id="b3a39-112">La classe **MSMCAInfo** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="b3a39-112">The **MSMCAInfo** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3a39-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3a39-113">Requirements</span></span>



| <span data-ttu-id="b3a39-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3a39-114">Requirement</span></span> | <span data-ttu-id="b3a39-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3a39-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3a39-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3a39-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3a39-117">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b3a39-117">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b3a39-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3a39-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3a39-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b3a39-119">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b3a39-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3a39-120">Namespace</span></span><br/>                | <span data-ttu-id="b3a39-121">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="b3a39-121">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="b3a39-122">MOF</span><span class="sxs-lookup"><span data-stu-id="b3a39-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3a39-123"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3a39-123"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3a39-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b3a39-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3a39-125"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3a39-125"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3a39-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3a39-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3a39-127">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="b3a39-127">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="b3a39-128">**\_En-tête MSMCAEvent**</span><span class="sxs-lookup"><span data-stu-id="b3a39-128">**MSMCAEvent\_Header**</span></span>](msmcaevent-header.md)
</dt> <dt>

[<span data-ttu-id="b3a39-129">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="b3a39-129">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

 




