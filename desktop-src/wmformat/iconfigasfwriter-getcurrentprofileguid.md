---
title: Méthode IConfigAsfWriter GetCurrentProfileGuid
description: La méthode GetCurrentProfileGuid récupère le GUID du profil de système Windows Media actuel.
ms.assetid: e7a2ecc0-48d4-446c-852a-0d7677cbbe71
keywords:
- Méthode GetCurrentProfileGuid format Windows Media
- Méthode GetCurrentProfileGuid format Windows Media, interface IConfigAsfWriter
- Interface IConfigAsfWriter Windows Media format, méthode GetCurrentProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.GetCurrentProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49282ed6ea33db8052e167568e5b5fa70cda9e01
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316127"
---
# <a name="iconfigasfwritergetcurrentprofileguid-method"></a><span data-ttu-id="dba82-106">IConfigAsfWriter :: GetCurrentProfileGuid, méthode</span><span class="sxs-lookup"><span data-stu-id="dba82-106">IConfigAsfWriter::GetCurrentProfileGuid method</span></span>

<span data-ttu-id="dba82-107">La méthode **GetCurrentProfileGuid** récupère le GUID du profil de système Windows Media actuel.</span><span class="sxs-lookup"><span data-stu-id="dba82-107">The **GetCurrentProfileGuid** method retrieves the current Windows Media system profile GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="dba82-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dba82-108">Syntax</span></span>


```C++
HRESULT GetCurrentProfileGuid(
  [out] GUID *pProfileGuid
);
```



## <a name="parameters"></a><span data-ttu-id="dba82-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dba82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dba82-110">*pProfileGuid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dba82-110">*pProfileGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dba82-111">Pointeur vers une variable de type **GUID** qui identifie le profil système actuel utilisé par le filtre.</span><span class="sxs-lookup"><span data-stu-id="dba82-111">Pointer to a variable of type **GUID** that identifies the current system profile being used by the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dba82-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dba82-112">Return value</span></span>

<span data-ttu-id="dba82-113">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dba82-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="dba82-114">En cas d’échec, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dba82-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dba82-115">Notes</span><span class="sxs-lookup"><span data-stu-id="dba82-115">Remarks</span></span>

<span data-ttu-id="dba82-116">Cette méthode n’est pas utilisée avec les profils personnalisés (y compris tous les profils qui incluent des flux qui utilisent les codecs Windows Media Audio et vidéo), car tous ces profils sont créés par des applications et n’ont pas d’identificateur GUID.</span><span class="sxs-lookup"><span data-stu-id="dba82-116">This method is not used with custom profiles (including all profiles that include streams that use the Windows Media Audio and Video codecs) because all such profiles are created by applications and have no GUID identifier.</span></span> <span data-ttu-id="dba82-117">Si aucun profil système n’est chargé, *pProfileGuid* prend la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="dba82-117">If no system profile is loaded, *pProfileGuid* will be set to **NULL**.</span></span>

## <a name="see-also"></a><span data-ttu-id="dba82-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dba82-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="dba82-119">[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dba82-119">[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>
</dt> </dl>

 

 