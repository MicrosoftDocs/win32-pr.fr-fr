---
description: Enregistre le journal de graphisme à l’emplacement spécifié.
MS-HAID: vspixengine.IPixEngine\_SaveFile\_BSTR\_IFileIOCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine :: SaveFile, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A80498F4-C8F5-4AC0-92C5-A90EB2A090B7
api_name:
- IPixEngine.SaveFile
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f7e1bed8765ca64123ccf13cbc3ee5f0d989b115
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522724"
---
# <a name="span-idvspixengineipixengine_savefile_bstr_ifileiocallback_ptrspanipixenginesavefile-method"></a><span data-ttu-id="88268-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine :: SaveFile, méthode</span><span class="sxs-lookup"><span data-stu-id="88268-103"><span id="vspixengine.ipixengine_savefile_bstr_ifileiocallback_ptr"></span>IPixEngine::SaveFile method</span></span>

<span data-ttu-id="88268-104">Enregistre le journal de graphisme à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="88268-104">Saves the graphics log to the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="88268-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88268-105">Syntax</span></span>


```C++
HRESULT SaveFile(
   BSTR             FileName,
   IFileIOCallback* pFileIOCallback
);
```

## <a name="parameters"></a><span data-ttu-id="88268-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88268-106">Parameters</span></span>

<span data-ttu-id="88268-107">*Extension* </span><span class="sxs-lookup"><span data-stu-id="88268-107">*FileName* </span></span>  
<span data-ttu-id="88268-108">Chaîne COM contenant le nom du chemin d’accès du journal de graphisme enregistré.</span><span class="sxs-lookup"><span data-stu-id="88268-108">A COM string containing the pathname of the saved graphics log.</span></span>

<span data-ttu-id="88268-109">*pFileIOCallback* </span><span class="sxs-lookup"><span data-stu-id="88268-109">*pFileIOCallback* </span></span>  
<span data-ttu-id="88268-110">Adresse d’un importation utilisé pour notifier l’hôte des erreurs d’e/s de fichier lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="88268-110">The address of a functon used to notify the host of file IO errors during save.</span></span>

## <a name="return-value"></a><span data-ttu-id="88268-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="88268-111">Return value</span></span>

<span data-ttu-id="88268-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="88268-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88268-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88268-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="88268-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88268-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="88268-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="88268-115">Header</span></span></p></td><td><span data-ttu-id="88268-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="88268-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="88268-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88268-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="88268-118">**IPixEngine**</span><span class="sxs-lookup"><span data-stu-id="88268-118">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
