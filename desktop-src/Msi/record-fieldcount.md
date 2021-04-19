---
description: La propriété FieldCount de l’objet record est une propriété en lecture seule qui retourne le nombre de champs dans l’enregistrement. L’accès en lecture aux champs au-delà de ce nombre retourne des valeurs NULL. L’accès en écriture échoue.
ms.assetid: 50be848a-2d38-4768-aeb4-25cbaedade01
title: Record. FieldCount, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FieldCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 548c1da4c2a0106cbcd667b5ce3c915ec17bf1ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525278"
---
# <a name="recordfieldcount-property"></a><span data-ttu-id="724bf-105">Record. FieldCount, propriété</span><span class="sxs-lookup"><span data-stu-id="724bf-105">Record.FieldCount property</span></span>

<span data-ttu-id="724bf-106">La propriété **FieldCount** de l’objet [**Record**](record-object.md) est une propriété en lecture seule qui retourne le nombre de champs dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="724bf-106">The **FieldCount** property of the [**Record**](record-object.md) object is a read-only property that returns the number of fields in the record.</span></span> <span data-ttu-id="724bf-107">L’accès en lecture aux champs au-delà de ce nombre retourne des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="724bf-107">Read access to fields beyond this count returns Null values.</span></span> <span data-ttu-id="724bf-108">L’accès en écriture échoue.</span><span class="sxs-lookup"><span data-stu-id="724bf-108">Write access fails.</span></span>

<span data-ttu-id="724bf-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="724bf-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="724bf-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="724bf-110">Syntax</span></span>


```JScript
propVal = Record.FieldCount
```



## <a name="property-value"></a><span data-ttu-id="724bf-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="724bf-111">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="724bf-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="724bf-112">Requirements</span></span>



| <span data-ttu-id="724bf-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="724bf-113">Requirement</span></span> | <span data-ttu-id="724bf-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="724bf-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="724bf-115">Version</span><span class="sxs-lookup"><span data-stu-id="724bf-115">Version</span></span><br/> | <span data-ttu-id="724bf-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="724bf-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="724bf-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="724bf-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="724bf-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="724bf-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="724bf-119">DLL</span><span class="sxs-lookup"><span data-stu-id="724bf-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="724bf-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="724bf-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="724bf-121">IID</span><span class="sxs-lookup"><span data-stu-id="724bf-121">IID</span></span><br/>     | <span data-ttu-id="724bf-122">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="724bf-122">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




