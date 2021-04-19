---
title: Méthode IConfigAsfWriter ConfigureFilterUsingProfile
description: La méthode ConfigureFilterUsingProfile est la méthode recommandée pour définir un profil. Il configure le filtre pour écrire un fichier ASF basé sur le profil défini par l’application spécifié.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Méthode ConfigureFilterUsingProfile format Windows Media
- Méthode ConfigureFilterUsingProfile format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513732"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a><span data-ttu-id="22eae-107">IConfigAsfWriter :: ConfigureFilterUsingProfile, méthode</span><span class="sxs-lookup"><span data-stu-id="22eae-107">IConfigAsfWriter::ConfigureFilterUsingProfile method</span></span>

<span data-ttu-id="22eae-108">La méthode **ConfigureFilterUsingProfile** est la méthode recommandée pour définir un profil.</span><span class="sxs-lookup"><span data-stu-id="22eae-108">The **ConfigureFilterUsingProfile** method is the recommended way to set a profile.</span></span> <span data-ttu-id="22eae-109">Il configure le filtre pour écrire un fichier ASF basé sur le profil défini par l’application spécifié.</span><span class="sxs-lookup"><span data-stu-id="22eae-109">It configures the filter to write an ASF file based on the specified application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="22eae-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22eae-110">Syntax</span></span>


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a><span data-ttu-id="22eae-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22eae-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22eae-112">*pProfile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22eae-112">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22eae-113">Pointeur vers l’interface [**IWMProfile**](iwmprofile.md) sur le profil défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="22eae-113">Pointer to the [**IWMProfile**](iwmprofile.md) interface on the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22eae-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22eae-114">Return value</span></span>

<span data-ttu-id="22eae-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22eae-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22eae-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="22eae-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22eae-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="22eae-117">Return code</span></span>                                                                                         | <span data-ttu-id="22eae-118">Description</span><span class="sxs-lookup"><span data-stu-id="22eae-118">Description</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="22eae-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22eae-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="22eae-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="22eae-120">The method succeeded.</span></span><br/>                              |
| <dl> <span data-ttu-id="22eae-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="22eae-121"><dt>**E\_POINTER**</dt></span></span> </dl>           | <span data-ttu-id="22eae-122">Le pointeur d’interface **IWMProfile** n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="22eae-122">The **IWMProfile** interface pointer is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="22eae-123"><dt>**VFW \_ E \_ état incorrect \_**</dt></span><span class="sxs-lookup"><span data-stu-id="22eae-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl> | <span data-ttu-id="22eae-124">Le graphique est arrêté.</span><span class="sxs-lookup"><span data-stu-id="22eae-124">The graph is stopped.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="22eae-125">Notes</span><span class="sxs-lookup"><span data-stu-id="22eae-125">Remarks</span></span>

<span data-ttu-id="22eae-126">En cas de réussite, cette méthode entraîne l’envoi d’un événement **\_ \_ Changed Graph** à l’application.</span><span class="sxs-lookup"><span data-stu-id="22eae-126">If successful, this method will cause an **EC\_GRAPH\_CHANGED** event to be sent to the application.</span></span> <span data-ttu-id="22eae-127">Utilisez cette méthode pour configurer l’enregistreur avec un profil Windows Media 9 de la série personnalisé que vous avez créé (ou chargé à partir d’un fichier. prx existant) à l’aide des méthodes du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22eae-127">Use this method to configure the writer with a custom Windows Media 9 Series profile you have created (or loaded from an existing .prx file) using the methods of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="22eae-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22eae-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="22eae-129">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22eae-129">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

