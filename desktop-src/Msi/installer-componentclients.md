---
description: La propriété ComponentClients en lecture seule retourne un objet StringList énumérant l’ensemble des clients d’un composant spécifié.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer. ComponentClients, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528759"
---
# <a name="installercomponentclients-property"></a><span data-ttu-id="70333-103">Installer. ComponentClients, propriété</span><span class="sxs-lookup"><span data-stu-id="70333-103">Installer.ComponentClients property</span></span>

<span data-ttu-id="70333-104">La propriété **ComponentClients** en lecture seule retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des clients d’un composant spécifié.</span><span class="sxs-lookup"><span data-stu-id="70333-104">The read-only **ComponentClients** property returns a [**StringList**](stringlist-object.md) object enumerating the set of clients of a specified component.</span></span>

<span data-ttu-id="70333-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="70333-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70333-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70333-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a><span data-ttu-id="70333-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="70333-107">Property value</span></span>

<span data-ttu-id="70333-108">GUID de chaîne qui représente le code de composant du composant.</span><span class="sxs-lookup"><span data-stu-id="70333-108">A string GUID that represents the component code of the component.</span></span> <span data-ttu-id="70333-109">Les codes des composants sont spécifiés dans la colonne ComponentId de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="70333-109">The component codes are specified in the ComponentId column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70333-110">Notes</span><span class="sxs-lookup"><span data-stu-id="70333-110">Remarks</span></span>

<span data-ttu-id="70333-111">Pour énumérer les clients du composant, une application peut itérer au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each.</span><span class="sxs-lookup"><span data-stu-id="70333-111">To enumerate the component clients, an application may iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="70333-112">Étant donné que les clients ne sont pas triés, les nouveaux composants possèdent un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="70333-112">Because clients are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="70333-113">Cela signifie que la fonction peut retourner des clients dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="70333-113">This means that the function may return clients in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="70333-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70333-114">Requirements</span></span>



| <span data-ttu-id="70333-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70333-115">Requirement</span></span> | <span data-ttu-id="70333-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="70333-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70333-117">Version</span><span class="sxs-lookup"><span data-stu-id="70333-117">Version</span></span><br/> | <span data-ttu-id="70333-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70333-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="70333-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="70333-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="70333-120">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="70333-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="70333-121">DLL</span><span class="sxs-lookup"><span data-stu-id="70333-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="70333-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70333-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="70333-123">IID</span><span class="sxs-lookup"><span data-stu-id="70333-123">IID</span></span><br/>     | <span data-ttu-id="70333-124">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="70333-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="70333-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70333-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70333-126">**MsiEnumClients**</span><span class="sxs-lookup"><span data-stu-id="70333-126">**MsiEnumClients**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




