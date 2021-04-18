---
description: La méthode Close de l’objet View met fin à l’exécution de la requête et libère les ressources de la base de données.
ms.assetid: 677377be-38be-47c0-9a58-a0d08cc05770
title: View. Close, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Close
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d0a0afbf078879f579eae15a9636a4a270799fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532885"
---
# <a name="viewclose-method"></a><span data-ttu-id="dd0b7-103">View. Close, méthode</span><span class="sxs-lookup"><span data-stu-id="dd0b7-103">View.Close method</span></span>

<span data-ttu-id="dd0b7-104">La méthode **Close** de l’objet [**View**](view-object.md) met fin à l’exécution de la requête et libère les ressources de la base de données.</span><span class="sxs-lookup"><span data-stu-id="dd0b7-104">The **Close** method of the [**View**](view-object.md) object terminates query execution and releases database resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd0b7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd0b7-105">Syntax</span></span>


```JScript
View.Close()
```



## <a name="parameters"></a><span data-ttu-id="dd0b7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd0b7-106">Parameters</span></span>

<span data-ttu-id="dd0b7-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd0b7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd0b7-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd0b7-108">Return value</span></span>

<span data-ttu-id="dd0b7-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dd0b7-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd0b7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="dd0b7-110">Remarks</span></span>

<span data-ttu-id="dd0b7-111">Cette méthode doit être appelée avant que la méthode [**Execute**](view-execute.md) soit appelée à nouveau sur l’objet [**View**](view-object.md) , à moins que toutes les lignes du jeu de résultats aient été obtenues avec la méthode [**Fetch**](view-fetch.md) .</span><span class="sxs-lookup"><span data-stu-id="dd0b7-111">This method must be called before the [**Execute**](view-execute.md) method is called again on the [**View**](view-object.md) object unless all rows of the result set have been obtained with the [**Fetch**](view-fetch.md) method.</span></span> <span data-ttu-id="dd0b7-112">Elle est appelée en interne lorsque la vue est détruite.</span><span class="sxs-lookup"><span data-stu-id="dd0b7-112">It is called internally when the view is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd0b7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd0b7-113">Requirements</span></span>



| <span data-ttu-id="dd0b7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd0b7-114">Requirement</span></span> | <span data-ttu-id="dd0b7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd0b7-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0b7-116">Version</span><span class="sxs-lookup"><span data-stu-id="dd0b7-116">Version</span></span><br/> | <span data-ttu-id="dd0b7-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd0b7-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dd0b7-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd0b7-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dd0b7-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd0b7-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dd0b7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="dd0b7-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd0b7-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd0b7-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dd0b7-122">IID</span><span class="sxs-lookup"><span data-stu-id="dd0b7-122">IID</span></span><br/>     | <span data-ttu-id="dd0b7-123">L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dd0b7-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




