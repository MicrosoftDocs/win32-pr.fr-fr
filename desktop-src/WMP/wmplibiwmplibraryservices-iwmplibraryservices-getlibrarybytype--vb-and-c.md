---
title: Méthode IWMPLibraryServices getLibraryByType
description: La méthode getLibraryByType retourne une interface IWMPLibrary qui représente la bibliothèque qui a le type et l’index spécifiés.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- méthode getLibraryByType lecteur Windows Media
- méthode getLibraryByType lecteur Windows Media, interface IWMPLibraryServices
- Interface IWMPLibraryServices lecteur Windows Media, méthode getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544119"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a><span data-ttu-id="d8360-106">IWMPLibraryServices :: getLibraryByType, méthode</span><span class="sxs-lookup"><span data-stu-id="d8360-106">IWMPLibraryServices::getLibraryByType method</span></span>

<span data-ttu-id="d8360-107">La méthode **getLibraryByType** retourne une interface **IWMPLibrary** qui représente la bibliothèque qui a le type et l’index spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d8360-107">The **getLibraryByType** method returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8360-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8360-108">Syntax</span></span>


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a><span data-ttu-id="d8360-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8360-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8360-110">*wmplt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8360-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8360-111">Valeur de l’énumération **wmplib. WMPLibraryType** qui spécifie le type de bibliothèque à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d8360-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d8360-112">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d8360-112">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8360-113">**System. Int32** qui est l’index de la bibliothèque à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d8360-113">A **System.Int32** that is the index of the library to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8360-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8360-114">Return value</span></span>

<span data-ttu-id="d8360-115">Interface **wmplib. IWMPLibrary** pour la bibliothèque qui est retournée.</span><span class="sxs-lookup"><span data-stu-id="d8360-115">A **WMPLib.IWMPLibrary** interface for the library that is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8360-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d8360-116">Remarks</span></span>

<span data-ttu-id="d8360-117">Il n’existe qu’une seule bibliothèque locale, et les bibliothèques de disques sont uniquement disponibles sur les CD et DVD de données contenant du contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="d8360-117">There is only one local library, and disc libraries are available only on data CDs and DVDs that contain media content.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8360-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8360-118">Requirements</span></span>



| <span data-ttu-id="d8360-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8360-119">Requirement</span></span> | <span data-ttu-id="d8360-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8360-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8360-121">Version</span><span class="sxs-lookup"><span data-stu-id="d8360-121">Version</span></span><br/>   | <span data-ttu-id="d8360-122">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="d8360-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="d8360-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d8360-123">Namespace</span></span><br/> | <span data-ttu-id="d8360-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d8360-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d8360-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="d8360-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d8360-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d8360-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8360-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8360-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8360-128">**Interface IWMPLibrary (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d8360-128">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8360-129">**Interface IWMPLibraryServices (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d8360-129">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d8360-130">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="d8360-130">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





