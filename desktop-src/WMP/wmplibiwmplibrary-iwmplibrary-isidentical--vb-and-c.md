---
title: Méthode IWMPLibrary isIdentical
description: La méthode isIdentical retourne une valeur qui indique si l’objet fourni est le même que celui en cours.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- méthode isIdentical lecteur Windows Media
- méthode isIdentical lecteur Windows Media, interface IWMPLibrary
- Interface IWMPLibrary lecteur Windows Media, méthode isIdentical
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535374"
---
# <a name="iwmplibraryisidentical-method"></a><span data-ttu-id="4cace-106">IWMPLibrary :: isIdentical, méthode</span><span class="sxs-lookup"><span data-stu-id="4cace-106">IWMPLibrary::isIdentical method</span></span>

<span data-ttu-id="4cace-107">La méthode **isIdentical** retourne une valeur qui indique si l’objet fourni est le même que celui en cours.</span><span class="sxs-lookup"><span data-stu-id="4cace-107">The **isIdentical** method returns a value that indicates whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cace-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cace-108">Syntax</span></span>


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a><span data-ttu-id="4cace-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4cace-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cace-110">*pIWMPLibrary* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4cace-110">*pIWMPLibrary* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4cace-111">Interface **wmplib. IWMPLibrary** qui représente l’objet à comparer avec l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="4cace-111">A **WMPLib.IWMPLibrary** interface that represents the object to compare with current one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cace-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4cace-112">Return value</span></span>

<span data-ttu-id="4cace-113">**System. Boolean** qui est le résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="4cace-113">A **System.Boolean** that is the result of the comparison.</span></span> <span data-ttu-id="4cace-114">La valeur **true** indique que les objets sont identiques.</span><span class="sxs-lookup"><span data-stu-id="4cace-114">The value **true** indicates that the objects are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cace-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cace-115">Requirements</span></span>



| <span data-ttu-id="4cace-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cace-116">Requirement</span></span> | <span data-ttu-id="4cace-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cace-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cace-118">Version</span><span class="sxs-lookup"><span data-stu-id="4cace-118">Version</span></span><br/>   | <span data-ttu-id="4cace-119">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="4cace-119">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="4cace-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4cace-120">Namespace</span></span><br/> | <span data-ttu-id="4cace-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4cace-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4cace-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="4cace-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4cace-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4cace-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cace-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cace-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cace-125">**Interface IWMPLibrary (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4cace-125">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





