---
title: Méthode IWMPCdromBurn getItemInfo
description: La méthode getItemInfo récupère la valeur de l’attribut spécifié pour le CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, interface IWMPCdromBurn
- Interface IWMPCdromBurn lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528869"
---
# <a name="iwmpcdromburngetiteminfo-method"></a><span data-ttu-id="61dad-106">IWMPCdromBurn :: getItemInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="61dad-106">IWMPCdromBurn::getItemInfo method</span></span>

<span data-ttu-id="61dad-107">La méthode **getItemInfo** récupère la valeur de l’attribut spécifié pour le CD.</span><span class="sxs-lookup"><span data-stu-id="61dad-107">The **getItemInfo** method retrieves the value of the specified attribute for the CD.</span></span>

## <a name="syntax"></a><span data-ttu-id="61dad-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61dad-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="61dad-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61dad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61dad-110">*bstrItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61dad-110">*bstrItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61dad-111">**System. String** qui contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="61dad-111">A **System.String** that contains one of the following values.</span></span>



| <span data-ttu-id="61dad-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="61dad-112">Value</span></span>         | <span data-ttu-id="61dad-113">Description</span><span class="sxs-lookup"><span data-stu-id="61dad-113">Description</span></span>                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61dad-114">AvailableTime</span><span class="sxs-lookup"><span data-stu-id="61dad-114">AvailableTime</span></span> | <span data-ttu-id="61dad-115">Récupère le temps disponible sur le CD, en secondes.</span><span class="sxs-lookup"><span data-stu-id="61dad-115">Retrieves the time available on the CD, in seconds.</span></span>                                          |
| <span data-ttu-id="61dad-116">Vide</span><span class="sxs-lookup"><span data-stu-id="61dad-116">Blank</span></span>         | <span data-ttu-id="61dad-117">Récupère un **System. Boolean** (représenté sous la forme d’une chaîne) indiquant si le CD est vide.</span><span class="sxs-lookup"><span data-stu-id="61dad-117">Retrieves a **System.Boolean** (represented as a string) indicating whether the CD is blank.</span></span> |
| <span data-ttu-id="61dad-118">FreeSpace</span><span class="sxs-lookup"><span data-stu-id="61dad-118">FreeSpace</span></span>     | <span data-ttu-id="61dad-119">Récupère l’espace libre sur le CD, en octets.</span><span class="sxs-lookup"><span data-stu-id="61dad-119">Retrieves the free space on the CD, in bytes.</span></span>                                                |
| <span data-ttu-id="61dad-120">TotalSpace</span><span class="sxs-lookup"><span data-stu-id="61dad-120">TotalSpace</span></span>    | <span data-ttu-id="61dad-121">Récupère l’espace total, en octets, sur le CD.</span><span class="sxs-lookup"><span data-stu-id="61dad-121">Retrieves the total space on the CD, in bytes.</span></span>                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61dad-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61dad-122">Return value</span></span>

<span data-ttu-id="61dad-123">**System. String** qui est la valeur de l’attribut spécifié.</span><span class="sxs-lookup"><span data-stu-id="61dad-123">A **System.String** that is the value of the specified attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="61dad-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61dad-124">Requirements</span></span>



| <span data-ttu-id="61dad-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61dad-125">Requirement</span></span> | <span data-ttu-id="61dad-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="61dad-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61dad-127">Version</span><span class="sxs-lookup"><span data-stu-id="61dad-127">Version</span></span><br/>   | <span data-ttu-id="61dad-128">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="61dad-128">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="61dad-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61dad-129">Namespace</span></span><br/> | <span data-ttu-id="61dad-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="61dad-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="61dad-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="61dad-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="61dad-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="61dad-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61dad-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61dad-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61dad-134">**Interface IWMPCdromBurn (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="61dad-134">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





