---
description: La propriété Environment de l’objet installer est une propriété en lecture-écriture qui est la valeur de chaîne d’une variable d’environnement du processus en cours.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Installer. Environment, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528778"
---
# <a name="installerenvironment-property"></a><span data-ttu-id="7200d-103">Installer. Environment, propriété</span><span class="sxs-lookup"><span data-stu-id="7200d-103">Installer.Environment property</span></span>

<span data-ttu-id="7200d-104">La propriété **Environment** de l’objet [**installer**](installer-object.md) est une propriété en lecture-écriture qui est la valeur de chaîne d’une variable d’environnement du processus en cours.</span><span class="sxs-lookup"><span data-stu-id="7200d-104">The **Environment** property of the [**Installer**](installer-object.md) object is a read-write property that is the string value for an environment variable of the current process.</span></span>

<span data-ttu-id="7200d-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7200d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7200d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7200d-106">Syntax</span></span>


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a><span data-ttu-id="7200d-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7200d-107">Property value</span></span>

<span data-ttu-id="7200d-108">Nom de la variable d’environnement à lire ou à écrire.</span><span class="sxs-lookup"><span data-stu-id="7200d-108">The name of the environment variable to be read or written.</span></span> <span data-ttu-id="7200d-109">Cela ne tient pas compte de la casse.</span><span class="sxs-lookup"><span data-stu-id="7200d-109">This is case-insensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="7200d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7200d-110">Remarks</span></span>

<span data-ttu-id="7200d-111">La définition d’une variable d’environnement avec la propriété d' **environnement** affecte uniquement la session active.</span><span class="sxs-lookup"><span data-stu-id="7200d-111">Setting an environment variable with the **Environment** property only affects the active session.</span></span> <span data-ttu-id="7200d-112">Pour apporter des modifications persistantes à une variable d’environnement, utilisez la [table d’environnement](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="7200d-112">To make persistent changes to an environment variable, use the [Environment table](environment-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7200d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7200d-113">Requirements</span></span>



| <span data-ttu-id="7200d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7200d-114">Requirement</span></span> | <span data-ttu-id="7200d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7200d-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7200d-116">Version</span><span class="sxs-lookup"><span data-stu-id="7200d-116">Version</span></span><br/> | <span data-ttu-id="7200d-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7200d-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7200d-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7200d-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7200d-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="7200d-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7200d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7200d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="7200d-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7200d-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7200d-122">IID</span><span class="sxs-lookup"><span data-stu-id="7200d-122">IID</span></span><br/>     | <span data-ttu-id="7200d-123">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7200d-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




