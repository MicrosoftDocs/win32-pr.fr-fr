---
title: Méthode IConfigAsfWriter GetCurrentProfileId
description: La méthode GetCurrentProfileId récupère l’ID de profil actuel. (Pour les profils Windows Media format 4,0 uniquement.).
ms.assetid: a5162bb1-5fcb-449e-b8d3-624b863e656d
keywords:
- Méthode GetCurrentProfileId format Windows Media
- Méthode GetCurrentProfileId format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetCurrentProfileId
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileId
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416ac2c48f6ec8836a7390f18f38eca3dca35274
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106544154"
---
# <a name="iconfigasfwritergetcurrentprofileid-method"></a><span data-ttu-id="1810a-107">IConfigAsfWriter :: GetCurrentProfileId, méthode</span><span class="sxs-lookup"><span data-stu-id="1810a-107">IConfigAsfWriter::GetCurrentProfileId method</span></span>

<span data-ttu-id="1810a-108">La méthode **GetCurrentProfileId** récupère l’ID de profil actuel.</span><span class="sxs-lookup"><span data-stu-id="1810a-108">The **GetCurrentProfileId** method retrieves the current profile ID.</span></span> <span data-ttu-id="1810a-109">(Pour les profils Windows Media format 4,0 uniquement.)</span><span class="sxs-lookup"><span data-stu-id="1810a-109">(For Windows Media Format 4.0 profiles only.)</span></span>

## <a name="syntax"></a><span data-ttu-id="1810a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1810a-110">Syntax</span></span>


```C++
HRESULT GetCurrentProfileId(
  [out] DWORD *pdwProfileId
);
```



## <a name="parameters"></a><span data-ttu-id="1810a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1810a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1810a-112">*pdwProfileId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1810a-112">*pdwProfileId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1810a-113">Pointeur vers une variable de type **DWORD** qui reçoit l’ID de profil actuel.</span><span class="sxs-lookup"><span data-stu-id="1810a-113">Pointer to a variable of type **DWORD** that receives the current profile ID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1810a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1810a-114">Return value</span></span>

<span data-ttu-id="1810a-115">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1810a-115">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="1810a-116">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1810a-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1810a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1810a-117">Remarks</span></span>

<span data-ttu-id="1810a-118">Cette méthode est désormais obsolète, car elle suppose les profils du kit de développement logiciel (SDK) de format Windows Media version 4,0.</span><span class="sxs-lookup"><span data-stu-id="1810a-118">This method is now obsolete because it assumes version 4.0 Windows Media Format SDK profiles.</span></span> <span data-ttu-id="1810a-119">Utilisez [**IConfigAsfWriter :: GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) ou [**IConfigAsfWriter :: GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) à la place pour identifier correctement un profil pour la version 7,0 et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1810a-119">Use [**IConfigAsfWriter::GetCurrentProfile**](iconfigasfwriter-getcurrentprofile.md) or [**IConfigAsfWriter::GetCurrentProfileGuid**](iconfigasfwriter-getcurrentprofileguid.md) instead to correctly identify a profile for version 7.0 and later.</span></span>

## <a name="see-also"></a><span data-ttu-id="1810a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1810a-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="1810a-121">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1810a-121">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 