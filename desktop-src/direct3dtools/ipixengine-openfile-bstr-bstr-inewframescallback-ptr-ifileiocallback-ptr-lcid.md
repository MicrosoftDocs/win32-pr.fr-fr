---
description: Ouvre un journal de graphisme.
MS-HAID: vspixengine.IPixEngine\_OpenFile\_BSTR\_BSTR\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_LCID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine :: OpenFile, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8E0E1336-9FC7-4C32-AF3C-F3BDF39A36D9
api_name:
- IPixEngine.OpenFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d18b0ff4d6d2301c6d52d2bc855d48a3db124ccb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109059"
---
# <a name="span-idvspixengineipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcidspanipixengineopenfile-method"></a><span data-ttu-id="01666-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine :: OpenFile, méthode</span><span class="sxs-lookup"><span data-stu-id="01666-103"><span id="vspixengine.ipixengine_openfile_bstr_bstr_inewframescallback_ptr_ifileiocallback_ptr_lcid"></span>IPixEngine::OpenFile method</span></span>

<span data-ttu-id="01666-104">Ouvre un journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="01666-104">Opens a graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="01666-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01666-105">Syntax</span></span>


```C++
HRESULT OpenFile(
   BSTR                FileName,
   BSTR                registryBoot,
   INewFramesCallback* callbacks,
   IFileIOCallback*    pFileIOCallback,
   LCID                uiLocale
);
```

## <a name="parameters"></a><span data-ttu-id="01666-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01666-106">Parameters</span></span>

<span data-ttu-id="01666-107">*Extension* </span><span class="sxs-lookup"><span data-stu-id="01666-107">*FileName* </span></span>  
<span data-ttu-id="01666-108">Chaîne COM contenant le nom du journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="01666-108">A COM string containing the name of the graphics log.</span></span>

<span data-ttu-id="01666-109">*registryBoot* </span><span class="sxs-lookup"><span data-stu-id="01666-109">*registryBoot* </span></span>  
<span data-ttu-id="01666-110">Chaîne COM contenant la racine du Registre.</span><span class="sxs-lookup"><span data-stu-id="01666-110">A COM string containing the registry root.</span></span> <span data-ttu-id="01666-111">Le moteur recherche le DIA et d’autres clés de registre.</span><span class="sxs-lookup"><span data-stu-id="01666-111">The engine looks here for DIA and other registry keys.</span></span>

<span data-ttu-id="01666-112">*rappels* </span><span class="sxs-lookup"><span data-stu-id="01666-112">*callbacks* </span></span>  
<span data-ttu-id="01666-113">Adresse d’une fonction utilisée pour informer l’hôte que de nouveaux frames ont été analysés.</span><span class="sxs-lookup"><span data-stu-id="01666-113">The address of a function used to notify the host that new frames have been parsed.</span></span>

<span data-ttu-id="01666-114">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="01666-114">*pFileIOCallback* </span></span>  
<span data-ttu-id="01666-115">Adresse d’une fonction utilisée pour notifier l’hôte des erreurs d’e/s de fichier lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="01666-115">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="01666-116">*uiLocale* </span><span class="sxs-lookup"><span data-stu-id="01666-116">*uiLocale* </span></span>  
<span data-ttu-id="01666-117">ID de paramètres régionaux utilisé pour présenter les messages d’erreur en fonction des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="01666-117">The locale ID used to present error messages according to locale settings.</span></span>

## <a name="return-value"></a><span data-ttu-id="01666-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01666-118">Return value</span></span>

<span data-ttu-id="01666-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01666-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01666-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01666-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01666-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01666-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="01666-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="01666-122">Header</span></span></p></td><td><span data-ttu-id="01666-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="01666-123">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="01666-124"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01666-124"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="01666-125">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="01666-125">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
