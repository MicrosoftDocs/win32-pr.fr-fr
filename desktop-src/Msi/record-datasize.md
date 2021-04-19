---
description: La propriété DataSize de l’objet record est une propriété en lecture seule qui retourne la taille des données pour le champ désigné.
ms.assetid: 6f89321e-bdb2-4c18-bdf8-01dea38b47c9
title: Record. DataSize, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.DataSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 500ee0039f4bfe638f4eca3740669e821c97ca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544446"
---
# <a name="recorddatasize-property"></a><span data-ttu-id="fb53c-103">Record. DataSize, propriété</span><span class="sxs-lookup"><span data-stu-id="fb53c-103">Record.DataSize property</span></span>

<span data-ttu-id="fb53c-104">La propriété **DataSize** de l’objet [**Record**](record-object.md) est une propriété en lecture seule qui retourne la taille des données pour le champ désigné.</span><span class="sxs-lookup"><span data-stu-id="fb53c-104">The **DataSize** property of the [**Record**](record-object.md) object is a read-only property that returns the size of the data for the designated field.</span></span> <span data-ttu-id="fb53c-105">Si les données sont un flux, la longueur du flux en octets est retournée.</span><span class="sxs-lookup"><span data-stu-id="fb53c-105">If the data is a stream, the stream length in bytes is returned.</span></span> <span data-ttu-id="fb53c-106">Si les données sont une chaîne, la longueur de la chaîne sans valeur null est retournée.</span><span class="sxs-lookup"><span data-stu-id="fb53c-106">If the data is a string, the string length without Null is returned.</span></span> <span data-ttu-id="fb53c-107">Si les données sont un entier, la valeur 4 est retournée (indiquant la taille de l’entier).</span><span class="sxs-lookup"><span data-stu-id="fb53c-107">If the data is an integer, the value 4 is returned (indicating the size of the integer).</span></span> <span data-ttu-id="fb53c-108">Si les données ont la valeur null, la valeur 0 est retournée.</span><span class="sxs-lookup"><span data-stu-id="fb53c-108">If the data is Null, 0 is returned.</span></span>

<span data-ttu-id="fb53c-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fb53c-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb53c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb53c-110">Syntax</span></span>


```JScript
propVal = Record.DataSize
```



## <a name="property-value"></a><span data-ttu-id="fb53c-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fb53c-111">Property value</span></span>

<span data-ttu-id="fb53c-112">Numéro de champ obligatoire de la valeur dans l’enregistrement, de base 1.</span><span class="sxs-lookup"><span data-stu-id="fb53c-112">Required field number of the value within the record, 1-based.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb53c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb53c-113">Requirements</span></span>



| <span data-ttu-id="fb53c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb53c-114">Requirement</span></span> | <span data-ttu-id="fb53c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb53c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb53c-116">Version</span><span class="sxs-lookup"><span data-stu-id="fb53c-116">Version</span></span><br/> | <span data-ttu-id="fb53c-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fb53c-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fb53c-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fb53c-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fb53c-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb53c-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fb53c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fb53c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb53c-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb53c-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fb53c-122">IID</span><span class="sxs-lookup"><span data-stu-id="fb53c-122">IID</span></span><br/>     | <span data-ttu-id="fb53c-123">IID \_ iRecord est défini en tant que 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fb53c-123">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



 

 




