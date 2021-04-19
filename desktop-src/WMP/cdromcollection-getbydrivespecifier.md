---
title: Méthode CdromCollection. getByDriveSpecifier
description: La méthode getByDriveSpecifier récupère l’objet cdrom associé à une lettre de lecteur particulière.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- méthode getByDriveSpecifier lecteur Windows Media
- méthode getByDriveSpecifier lecteur Windows Media, classe CdromCollection
- Classe CdromCollection lecteur Windows Media, méthode getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544126"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a><span data-ttu-id="77d73-106">Méthode CdromCollection. getByDriveSpecifier</span><span class="sxs-lookup"><span data-stu-id="77d73-106">CdromCollection.getByDriveSpecifier method</span></span>

<span data-ttu-id="77d73-107">La méthode **getByDriveSpecifier** récupère l’objet **cdrom** associé à une lettre de lecteur particulière.</span><span class="sxs-lookup"><span data-stu-id="77d73-107">The **getByDriveSpecifier** method retrieves the **Cdrom** object associated with a particular drive letter.</span></span>

## <a name="syntax"></a><span data-ttu-id="77d73-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77d73-108">Syntax</span></span>


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a><span data-ttu-id="77d73-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77d73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d73-110">*driveSpecifier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77d73-110">*driveSpecifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77d73-111">**Chaîne** contenant la lettre de lecteur suivie d’un signe deux-points («  : »).</span><span class="sxs-lookup"><span data-stu-id="77d73-111">**String** containing the drive letter followed by a colon (":") character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77d73-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77d73-112">Return value</span></span>

<span data-ttu-id="77d73-113">Cette méthode retourne un objet **cdrom** .</span><span class="sxs-lookup"><span data-stu-id="77d73-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="77d73-114">Notes</span><span class="sxs-lookup"><span data-stu-id="77d73-114">Remarks</span></span>

<span data-ttu-id="77d73-115">Les lettres de lecteur doivent être indiquées sous la forme *x*:, où *x* représente la lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="77d73-115">Drive letters must be given in the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="77d73-116">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="77d73-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="77d73-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="77d73-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="77d73-118">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="77d73-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="77d73-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="77d73-119">Examples</span></span>

<span data-ttu-id="77d73-120">L’exemple JScript suivant utilise *CdromCollection*. **getByDriveSpecifier** pour récupérer l’objet **cdrom** qui correspond à une lettre de lecteur fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77d73-120">The following JScript example uses *CdromCollection*.**getByDriveSpecifier** to retrieve the **Cdrom** object that corresponds to a drive letter provided by the user.</span></span> <span data-ttu-id="77d73-121">Un élément de texte HTML a été créé, avec NAME = "MyText", pour l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="77d73-121">An HTML text element was created, with NAME = "MyText", for user input.</span></span> <span data-ttu-id="77d73-122">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="77d73-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a><span data-ttu-id="77d73-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77d73-123">Requirements</span></span>



| <span data-ttu-id="77d73-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77d73-124">Requirement</span></span> | <span data-ttu-id="77d73-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="77d73-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="77d73-126">Version</span><span class="sxs-lookup"><span data-stu-id="77d73-126">Version</span></span><br/> | <span data-ttu-id="77d73-127">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="77d73-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="77d73-128">DLL</span><span class="sxs-lookup"><span data-stu-id="77d73-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="77d73-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77d73-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77d73-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77d73-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d73-131">**Objet cdrom**</span><span class="sxs-lookup"><span data-stu-id="77d73-131">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="77d73-132">**Cdrom. éjecter**</span><span class="sxs-lookup"><span data-stu-id="77d73-132">**Cdrom.eject**</span></span>](cdrom-eject.md)
</dt> <dt>

[<span data-ttu-id="77d73-133">**Objet CdromCollection**</span><span class="sxs-lookup"><span data-stu-id="77d73-133">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="77d73-134">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="77d73-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="77d73-135">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="77d73-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





