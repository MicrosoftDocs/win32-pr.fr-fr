---
title: Méthode IWMPCdromCollection getByDriveSpecifier
description: La méthode getByDriveSpecifier retourne une interface IWMPCdrom associée à une lettre de lecteur particulière.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- méthode getByDriveSpecifier lecteur Windows Media
- méthode getByDriveSpecifier lecteur Windows Media, interface IWMPCdromCollection
- Interface IWMPCdromCollection lecteur Windows Media, méthode getByDriveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543211"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="d3d3f-106">IWMPCdromCollection :: getByDriveSpecifier, méthode</span><span class="sxs-lookup"><span data-stu-id="d3d3f-106">IWMPCdromCollection::getByDriveSpecifier method</span></span>

<span data-ttu-id="d3d3f-107">La méthode **getByDriveSpecifier** retourne une interface **IWMPCdrom** associée à une lettre de lecteur particulière.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-107">The **getByDriveSpecifier** method returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d3f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3d3f-108">Syntax</span></span>


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a><span data-ttu-id="d3d3f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3d3f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d3f-110">*bstrDriveSpecifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d3d3f-110">*bstrDriveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d3f-111">**System. String** qui est la lettre de lecteur suivie d’un signe deux-points («  : »).</span><span class="sxs-lookup"><span data-stu-id="d3d3f-111">A **System.String** that is the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d3f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3d3f-112">Return value</span></span>

<span data-ttu-id="d3d3f-113">Interface **wmplib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="d3d3f-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3d3f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d3d3f-114">Remarks</span></span>

<span data-ttu-id="d3d3f-115">Les lettres de lecteur doivent être indiquées sous la forme *x*:, où *x* représente la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="d3d3f-116">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d3d3f-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d3d3f-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d3d3f-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="d3d3f-118">Examples</span></span>

<span data-ttu-id="d3d3f-119">L’exemple suivant utilise **getByDriveSpecifier** pour obtenir l’interface **IWMPCdrom** qui correspond à une lettre de lecteur fournie par l’utilisateur dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-119">The following example uses **getByDriveSpecifier** to get the **IWMPCdrom** interface that corresponds to a drive letter provided by the user in a text box.</span></span> <span data-ttu-id="d3d3f-120">La méthode **IWMPCdrom. EJECT** est ensuite appelée pour éjecter le lecteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-120">The **IWMPCdrom.eject** method is then called to eject the specified drive.</span></span> <span data-ttu-id="d3d3f-121">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a><span data-ttu-id="d3d3f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3d3f-122">Requirements</span></span>



| <span data-ttu-id="d3d3f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3d3f-123">Requirement</span></span> | <span data-ttu-id="d3d3f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3d3f-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d3f-125">Version</span><span class="sxs-lookup"><span data-stu-id="d3d3f-125">Version</span></span><br/>   | <span data-ttu-id="d3d3f-126">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d3d3f-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d3d3f-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3d3f-127">Namespace</span></span><br/> | <span data-ttu-id="d3d3f-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d3d3f-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d3d3f-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="d3d3f-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d3d3f-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d3d3f-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d3f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3d3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d3f-132">**Interface IWMPCdrom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d3d3f-132">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d3d3f-133">**IWMPCdrom. EJECT (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d3d3f-133">**IWMPCdrom.eject (VB and C#)**</span></span>](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d3d3f-134">**Interface IWMPCdromCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d3d3f-134">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d3d3f-135">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d3d3f-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d3d3f-136">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="d3d3f-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





