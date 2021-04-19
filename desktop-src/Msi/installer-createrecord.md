---
description: La méthode CreateRecord de l’objet installer retourne un nouvel objet enregistrement avec le nombre demandé de champs.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Installer. CreateRecord, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528843"
---
# <a name="installercreaterecord-method"></a><span data-ttu-id="9f068-103">Installer. CreateRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="9f068-103">Installer.CreateRecord method</span></span>

<span data-ttu-id="9f068-104">La méthode **CreateRecord** de l’objet [**installer**](installer-object.md) retourne un nouvel objet [**enregistrement**](record-object.md) avec le nombre demandé de champs.</span><span class="sxs-lookup"><span data-stu-id="9f068-104">The **CreateRecord** method of the [**Installer**](installer-object.md) object returns a new [**Record**](record-object.md) object with the requested number of fields.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f068-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f068-105">Syntax</span></span>


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a><span data-ttu-id="9f068-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f068-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f068-107">*count*</span><span class="sxs-lookup"><span data-stu-id="9f068-107">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="9f068-108">Nombre de champs requis, qui peut être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="9f068-108">Required number of fields, which may be 0.</span></span> <span data-ttu-id="9f068-109">Le nombre maximal de champs dans un enregistrement est limité à 65535.</span><span class="sxs-lookup"><span data-stu-id="9f068-109">The maximum number of fields in a record is limited to 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f068-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f068-110">Return value</span></span>

<span data-ttu-id="9f068-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9f068-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f068-112">Notes</span><span class="sxs-lookup"><span data-stu-id="9f068-112">Remarks</span></span>

<span data-ttu-id="9f068-113">Le champ 0, et non l’un des champs dans *Count*, est normalement utilisé pour les éléments orientés enregistrement, tels que les chaînes de format ou les codes d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9f068-113">Field 0, not one of the fields in *count*, is normally used for record-oriented items such as format strings or execution op-codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f068-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f068-114">Requirements</span></span>



| <span data-ttu-id="9f068-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f068-115">Requirement</span></span> | <span data-ttu-id="9f068-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f068-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f068-117">Version</span><span class="sxs-lookup"><span data-stu-id="9f068-117">Version</span></span><br/> | <span data-ttu-id="9f068-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f068-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9f068-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9f068-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9f068-120">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="9f068-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9f068-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9f068-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="9f068-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f068-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9f068-123">IID</span><span class="sxs-lookup"><span data-stu-id="9f068-123">IID</span></span><br/>     | <span data-ttu-id="9f068-124">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9f068-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




