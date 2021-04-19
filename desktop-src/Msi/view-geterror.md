---
description: La méthode GetError de l’objet View retourne l’erreur de validation et le nom de la colonne pour laquelle l’erreur s’est produite.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: Vue. GetError, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534970"
---
# <a name="viewgeterror-method"></a><span data-ttu-id="20ff9-103">Vue. GetError, méthode</span><span class="sxs-lookup"><span data-stu-id="20ff9-103">View.GetError method</span></span>

<span data-ttu-id="20ff9-104">La méthode **GetError** de l’objet [**View**](view-object.md) retourne l’erreur de validation et le nom de la colonne pour laquelle l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="20ff9-104">The **GetError** method of the [**View**](view-object.md) object returns the Validation error and the column name for which the error occurred.</span></span> <span data-ttu-id="20ff9-105">Dans Automation, la valeur retournée est une chaîne au format \# \# ColumnName, où \# \# représente un code d’erreur à deux chiffres.</span><span class="sxs-lookup"><span data-stu-id="20ff9-105">In automation, the returned value is a string of the form \#\#ColumnName, where the \#\# represents a 2-digit error code.</span></span> <span data-ttu-id="20ff9-106">Elle retourne la première erreur dans le tableau d’erreurs de la vue ; les appels suivants retournent la valeur suivante dans le tableau d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="20ff9-106">It returns the first error in the view's error array; subsequent calls return the next value in the error array.</span></span> <span data-ttu-id="20ff9-107">Une fois qu’une valeur de « 00 » est retournée, il n’y a plus d’erreurs, et les appels suivants font simplement une nouvelle boucle sur le tableau.</span><span class="sxs-lookup"><span data-stu-id="20ff9-107">Once a value of '00' is returned, no more errors exist, and subsequent calls merely loop through the array again.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ff9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20ff9-108">Syntax</span></span>


```JScript
View.GetError()
```



## <a name="parameters"></a><span data-ttu-id="20ff9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20ff9-109">Parameters</span></span>

<span data-ttu-id="20ff9-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="20ff9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20ff9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20ff9-111">Return value</span></span>

<span data-ttu-id="20ff9-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="20ff9-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ff9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20ff9-113">Requirements</span></span>



| <span data-ttu-id="20ff9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20ff9-114">Requirement</span></span> | <span data-ttu-id="20ff9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="20ff9-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20ff9-116">Version</span><span class="sxs-lookup"><span data-stu-id="20ff9-116">Version</span></span><br/> | <span data-ttu-id="20ff9-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20ff9-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="20ff9-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20ff9-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="20ff9-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="20ff9-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="20ff9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="20ff9-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="20ff9-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20ff9-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="20ff9-122">IID</span><span class="sxs-lookup"><span data-stu-id="20ff9-122">IID</span></span><br/>     | <span data-ttu-id="20ff9-123">L’IID \_ IView est défini en tant que 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="20ff9-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




