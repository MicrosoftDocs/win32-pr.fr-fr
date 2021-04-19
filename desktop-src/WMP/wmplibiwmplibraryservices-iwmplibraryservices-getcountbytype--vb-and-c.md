---
title: Méthode IWMPLibraryServices getCountByType
description: La méthode getCountByType retourne le nombre de bibliothèques disponibles d’un type spécifié.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- méthode getCountByType lecteur Windows Media
- méthode getCountByType lecteur Windows Media, interface IWMPLibraryServices
- Interface IWMPLibraryServices lecteur Windows Media, méthode getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543187"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a><span data-ttu-id="8e8f9-106">IWMPLibraryServices :: getCountByType, méthode</span><span class="sxs-lookup"><span data-stu-id="8e8f9-106">IWMPLibraryServices::getCountByType method</span></span>

<span data-ttu-id="8e8f9-107">La méthode **getCountByType** retourne le nombre de bibliothèques disponibles d’un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e8f9-107">The **getCountByType** method returns the count of available libraries of a specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e8f9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e8f9-108">Syntax</span></span>


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a><span data-ttu-id="8e8f9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e8f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e8f9-110">*wmplt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8e8f9-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8f9-111">Valeur de l’énumération **wmplib. WMPLibraryType** qui spécifie le type de bibliothèque à compter.</span><span class="sxs-lookup"><span data-stu-id="8e8f9-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e8f9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e8f9-112">Return value</span></span>

<span data-ttu-id="8e8f9-113">**System. Int32** qui est le nombre de bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="8e8f9-113">A **System.Int32** that is the library count.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8f9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e8f9-114">Requirements</span></span>



| <span data-ttu-id="8e8f9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e8f9-115">Requirement</span></span> | <span data-ttu-id="8e8f9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e8f9-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8f9-117">Version</span><span class="sxs-lookup"><span data-stu-id="8e8f9-117">Version</span></span><br/>   | <span data-ttu-id="8e8f9-118">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="8e8f9-118">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="8e8f9-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8e8f9-119">Namespace</span></span><br/> | <span data-ttu-id="8e8f9-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8e8f9-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8e8f9-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="8e8f9-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8e8f9-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8e8f9-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8f9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e8f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e8f9-124">**Interface IWMPLibraryServices (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8e8f9-124">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e8f9-125">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="8e8f9-125">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





