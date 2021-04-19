---
title: Méthode IConfigAsfWriter ConfigureFilterUsingProfileId
description: La méthode ConfigureFilterUsingProfileId configure le filtre pour écrire un fichier ASF avec un index d’identificateur de profil (ID) à partir de la liste des profils système. (Pour les profils Windows Media format 4,0 uniquement.).
ms.assetid: b0375785-83db-4540-aca9-7ba0bb81c1ef
keywords:
- Méthode ConfigureFilterUsingProfileId format Windows Media
- Méthode ConfigureFilterUsingProfileId format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode ConfigureFilterUsingProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0226195d7657667e3947b55546b321edafa7befc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510476"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileid-method"></a><span data-ttu-id="40a55-107">IConfigAsfWriter :: ConfigureFilterUsingProfileId, méthode</span><span class="sxs-lookup"><span data-stu-id="40a55-107">IConfigAsfWriter::ConfigureFilterUsingProfileId method</span></span>

<span data-ttu-id="40a55-108">La méthode **ConfigureFilterUsingProfileId** configure le filtre pour écrire un fichier ASF avec un index d’identificateur de profil (ID) à partir de la liste des profils système.</span><span class="sxs-lookup"><span data-stu-id="40a55-108">The **ConfigureFilterUsingProfileId** method configures the filter to write an ASF file with a profile identifier (ID) index from the system profile list.</span></span> <span data-ttu-id="40a55-109">(Pour les profils Windows Media format 4,0 uniquement.)</span><span class="sxs-lookup"><span data-stu-id="40a55-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="40a55-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40a55-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfileId(
  [in] DWORD dwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="40a55-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40a55-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a55-112">*dwProfileId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40a55-112">*dwProfileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a55-113">ID de profil tel que défini dans la version 4,0 du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="40a55-113">Profile ID as defined in version 4.0 of the Windows Media Format SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a55-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40a55-114">Return value</span></span>

<span data-ttu-id="40a55-115">Retourne l’une des valeurs **HRESULT** suivantes.</span><span class="sxs-lookup"><span data-stu-id="40a55-115">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="40a55-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="40a55-116">Return code</span></span>                                                                                         | <span data-ttu-id="40a55-117">Description</span><span class="sxs-lookup"><span data-stu-id="40a55-117">Description</span></span>                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="40a55-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="40a55-118"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="40a55-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="40a55-119">The method succeeded.</span></span><br/>        |
| <dl> <span data-ttu-id="40a55-120"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="40a55-120"><dt>**E\_FAIL**</dt></span></span> </dl>              | <span data-ttu-id="40a55-121">Le profil n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="40a55-121">The profile is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="40a55-122"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="40a55-122"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="40a55-123">Le graphique de filtre est arrêté.</span><span class="sxs-lookup"><span data-stu-id="40a55-123">The filter graph is stopped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40a55-124">Notes</span><span class="sxs-lookup"><span data-stu-id="40a55-124">Remarks</span></span>

<span data-ttu-id="40a55-125">Cette méthode est désormais obsolète, car elle suppose les profils du kit de développement logiciel (SDK) de format Windows Media version 4,0.</span><span class="sxs-lookup"><span data-stu-id="40a55-125">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="40a55-126">Pour configurer le filtre pour les profils version 7,0 et versions ultérieures, utilisez [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) ou [**IConfigAsfWriter :: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span><span class="sxs-lookup"><span data-stu-id="40a55-126">To configure the filter for version 7.0 and later profiles, use [**IConfigAsfWriter::ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) or [**IConfigAsfWriter::ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="40a55-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40a55-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="40a55-128">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="40a55-128">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

