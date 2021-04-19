---
title: Méthode IConfigAsfWriter GetCurrentProfile
description: La méthode GetCurrentProfile récupère le profil défini par l’application.
ms.assetid: 7f6e7085-982b-4234-b890-950efdcdb559
keywords:
- Méthode GetCurrentProfile format Windows Media
- Méthode GetCurrentProfile format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetCurrentProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88931d83674ffa84288b4bec10e3c9dba15c812a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511694"
---
# <a name="iconfigasfwritergetcurrentprofile-method"></a><span data-ttu-id="f1e71-106">IConfigAsfWriter :: GetCurrentProfile, méthode</span><span class="sxs-lookup"><span data-stu-id="f1e71-106">IConfigAsfWriter::GetCurrentProfile method</span></span>

<span data-ttu-id="f1e71-107">La méthode **GetCurrentProfile** récupère le profil défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="f1e71-107">The **GetCurrentProfile** method retrieves the application-defined profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e71-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1e71-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfile(
  [out] IWMProfile **ppProfile
);
```



## <a name="parameters"></a><span data-ttu-id="f1e71-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1e71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1e71-110">*ppProfile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f1e71-110">*ppProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1e71-111">Adresse d’un pointeur qui reçoit l’interface [**IWMProfile**](iwmprofile.md) du profil défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="f1e71-111">Address of a pointer that receives the [**IWMProfile**](iwmprofile.md) interface of the application-defined profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1e71-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1e71-112">Return value</span></span>

<span data-ttu-id="f1e71-113">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f1e71-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f1e71-114">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1e71-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1e71-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f1e71-115">Remarks</span></span>

<span data-ttu-id="f1e71-116">Si la méthode est réussie, le pointeur **IWMProfile** retourné a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="f1e71-116">If the method succeeds, the **IWMProfile** pointer that it returns has an outstanding reference count.</span></span> <span data-ttu-id="f1e71-117">Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="f1e71-117">Be sure to release the interface when you are finished using it.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1e71-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1e71-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1e71-119">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1e71-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 