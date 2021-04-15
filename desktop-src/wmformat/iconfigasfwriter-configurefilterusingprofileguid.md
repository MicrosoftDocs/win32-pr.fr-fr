---
title: Méthode IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: La méthode ConfigureFilterUsingProfileGuid configure le filtre pour écrire un fichier ASF basé sur le profil prédéfini spécifié. (Déconseillé.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Méthode ConfigureFilterUsingProfileGuid format Windows Media
- Méthode ConfigureFilterUsingProfileGuid format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508073"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a><span data-ttu-id="0086a-107">IConfigAsfWriter :: ConfigureFilterUsingProfileGuid, méthode</span><span class="sxs-lookup"><span data-stu-id="0086a-107">IConfigAsfWriter::ConfigureFilterUsingProfileGuid method</span></span>

<span data-ttu-id="0086a-108">La méthode **ConfigureFilterUsingProfileGuid** configure le filtre pour écrire un fichier ASF basé sur le profil prédéfini spécifié.</span><span class="sxs-lookup"><span data-stu-id="0086a-108">The **ConfigureFilterUsingProfileGuid** method configures the filter to write an ASF file based on the specified predefined profile.</span></span> <span data-ttu-id="0086a-109">(Déconseillée).</span><span class="sxs-lookup"><span data-stu-id="0086a-109">(Deprecated.)</span></span>

## <a name="syntax"></a><span data-ttu-id="0086a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0086a-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a><span data-ttu-id="0086a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0086a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0086a-112">*guidProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0086a-112">*guidProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0086a-113">**GUID** identifiant un profil tel que défini dans le fichier d’en-tête du kit de développement logiciel (SDK) Windows Media format Wmsysprf. h.</span><span class="sxs-lookup"><span data-stu-id="0086a-113">**GUID** identifying a profile as defined in the Windows Media Format SDK header file Wmsysprf.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0086a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0086a-114">Return value</span></span>

<span data-ttu-id="0086a-115">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="0086a-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="0086a-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0086a-116">Return code</span></span>                                                                                         | <span data-ttu-id="0086a-117">Description</span><span class="sxs-lookup"><span data-stu-id="0086a-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="0086a-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0086a-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="0086a-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0086a-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="0086a-120"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0086a-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="0086a-121">Le profil n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0086a-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="0086a-122"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0086a-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="0086a-123">Le graphique de filtre est arrêté.</span><span class="sxs-lookup"><span data-stu-id="0086a-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0086a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="0086a-124">Remarks</span></span>

<span data-ttu-id="0086a-125">À partir du kit de développement logiciel (SDK) Windows Media Format 9 Series, aucun nouveau profil système n’a été défini.</span><span class="sxs-lookup"><span data-stu-id="0086a-125">Beginning with the Windows Media Format 9 Series SDK, no new system profiles have been defined.</span></span> <span data-ttu-id="0086a-126">Seuls les GUID de profil système de version 8 (ou version antérieure) peuvent être utilisés avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0086a-126">Only version 8 (or earlier) system profile GUIDs can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="0086a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0086a-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="0086a-128">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0086a-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

