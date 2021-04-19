---
description: La \_ classe WMI MethodParameterClass abstraite de base dérive toute classe définie en tant que conteneur de valeurs de paramètre qui seront passées à une méthode.
ms.assetid: 293fa378-432d-4e97-a8ab-8dc4917d5476
ms.tgt_platform: multiple
title: Classe Win32_MethodParameterClass
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MethodParameterClass
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4e791941df681b2e46c4de6f0714b1290baecfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515144"
---
# <a name="win32_methodparameterclass-class"></a><span data-ttu-id="6b795-103">\_Classe MethodParameterClass Win32</span><span class="sxs-lookup"><span data-stu-id="6b795-103">Win32\_MethodParameterClass class</span></span>

<span data-ttu-id="6b795-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MethodParameterClass** abstraite de base dérive toute classe définie en tant que conteneur de valeurs de paramètre qui seront passées à une méthode.</span><span class="sxs-lookup"><span data-stu-id="6b795-104">The **Win32\_MethodParameterClass** abstract, base [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) derives any class defined as a container of parameter values that will be passed to a method.</span></span> <span data-ttu-id="6b795-105">Sans aucune propriété propre, cette classe sert de nœud de classification.</span><span class="sxs-lookup"><span data-stu-id="6b795-105">Having no properties of its own, this class serves as a classification node.</span></span> <span data-ttu-id="6b795-106">Un exemple similaire est [**CIM \_ PhysicalElement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="6b795-106">A similar example is [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span> <span data-ttu-id="6b795-107">La dérivation à partir de **CIM \_ PhysicalElement** indique que la classe décrit une entité physique et non logique.</span><span class="sxs-lookup"><span data-stu-id="6b795-107">Derivation from **CIM\_PhysicalElement** indicates that the class describes a physical rather than logical entity.</span></span> <span data-ttu-id="6b795-108">Dans le cas de **\_ MethodParameterClass Win32**, les classes dérivées de celui-ci sont créées spécifiquement pour passer des paramètres à une méthode.</span><span class="sxs-lookup"><span data-stu-id="6b795-108">In the case of **Win32\_MethodParameterClass**, classes derived from it are created specifically to pass parameters to a method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b795-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b795-109">Syntax</span></span>

## <a name="members"></a><span data-ttu-id="6b795-110">Membres</span><span class="sxs-lookup"><span data-stu-id="6b795-110">Members</span></span>

<span data-ttu-id="6b795-111">La classe **Win32 \_ MethodParameterClass** ne définit aucun membre.</span><span class="sxs-lookup"><span data-stu-id="6b795-111">The **Win32\_MethodParameterClass** class does not define any members.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b795-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b795-112">Requirements</span></span>



| <span data-ttu-id="6b795-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b795-113">Requirement</span></span> | <span data-ttu-id="6b795-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b795-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b795-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b795-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6b795-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b795-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b795-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b795-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6b795-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b795-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b795-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6b795-119">Namespace</span></span><br/>                | <span data-ttu-id="6b795-120">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6b795-120">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b795-121">MOF</span><span class="sxs-lookup"><span data-stu-id="6b795-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b795-122"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b795-122"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b795-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6b795-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b795-124"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b795-124"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b795-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b795-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b795-126">Classes de gestion des services WMI</span><span class="sxs-lookup"><span data-stu-id="6b795-126">WMI Service Management Classes</span></span>](/windows/desktop/CIMWin32Prov/wmi-service-management-classes)
</dt> </dl>

 

