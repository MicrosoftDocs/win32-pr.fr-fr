---
description: Rappel qui avertit l’hôte d’informations de mémoire tampon écrites dans un fichier par la demande dans.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IBufferObjectDataCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 41a5017171fee8476033e3c38d050bc38b1642a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392875"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span data-ttu-id="cfb67-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="cfb67-103"><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback::ResultCallback method</span></span>

<span data-ttu-id="cfb67-104">Rappel qui avertit l’hôte d’informations de mémoire tampon écrites dans un fichier par la demande dans.</span><span class="sxs-lookup"><span data-stu-id="cfb67-104">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb67-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfb67-105">Syntax</span></span>

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a><span data-ttu-id="cfb67-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfb67-106">Parameters</span></span>

<span data-ttu-id="cfb67-107">*Fichier* Chaîne COM qui contient le nom du chemin d’accès du fichier dans lequel les résultats sont écrits.</span><span class="sxs-lookup"><span data-stu-id="cfb67-107">*File* A COM string that contains the pathname of the file where results are written.</span></span>

## <a name="return-value"></a><span data-ttu-id="cfb67-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfb67-108">Return value</span></span>

<span data-ttu-id="cfb67-109">Si cette méthode est réussie, elle retourne **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="cfb67-109">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="cfb67-110">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cfb67-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb67-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cfb67-111">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="cfb67-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfb67-112">Header</span></span></p></td><td><span data-ttu-id="cfb67-113">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="cfb67-113">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="cfb67-114"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfb67-114"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="cfb67-115">**IBufferObjectDataCallback**</span><span class="sxs-lookup"><span data-stu-id="cfb67-115">**IBufferObjectDataCallback**</span></span>](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
