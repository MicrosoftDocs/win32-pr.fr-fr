---
description: Fonction de rappel utilisée pour informer l’hôte d’informations sur les fichiers sources associés à la pile des appels.
MS-HAID: vspixengine.ISourceFileInfoCallback\_ResultCallback\_DWORD\_SourceFileInfo\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISourceFileInfoCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AB3249FF-DA67-4902-B75D-4EC3D0F25EE7
api_name:
- ISourceFileInfoCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a60122615cf15e9ed39ae7809e574c4d3d0c1146
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109862"
---
# <a name="span-idvspixengineisourcefileinfocallback_resultcallback_dword_sourcefileinfo_arrspanisourcefileinfocallbackresultcallback-method"></a><span data-ttu-id="5a7a6-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback :: ResultCallback, méthode</span><span class="sxs-lookup"><span data-stu-id="5a7a6-103"><span id="vspixengine.isourcefileinfocallback_resultcallback_dword_sourcefileinfo_arr"></span>ISourceFileInfoCallback::ResultCallback method</span></span>

<span data-ttu-id="5a7a6-104">Fonction de rappel utilisée pour informer l’hôte d’informations sur les fichiers sources associés à la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="5a7a6-104">A callback function used to notify the host of information about source files associated with the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a7a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a7a6-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   SourceFileInfo [] count0_sourceFileInfoBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="5a7a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a7a6-106">Parameters</span></span>

<span data-ttu-id="5a7a6-107">*saut* </span><span class="sxs-lookup"><span data-stu-id="5a7a6-107">*count* </span></span>  
<span data-ttu-id="5a7a6-108">Nombre de fichiers sources retournés.</span><span class="sxs-lookup"><span data-stu-id="5a7a6-108">The number of source files returned.</span></span>

<span data-ttu-id="5a7a6-109">*count0 \_ sourceFileInfoBuffer* </span><span class="sxs-lookup"><span data-stu-id="5a7a6-109">*count0\_sourceFileInfoBuffer* </span></span>  
<span data-ttu-id="5a7a6-110">Fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="5a7a6-110">The source files.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a7a6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a7a6-111">Return value</span></span>

<span data-ttu-id="5a7a6-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5a7a6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a7a6-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a7a6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a7a6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a7a6-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5a7a6-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a7a6-115">Header</span></span></p></td><td><span data-ttu-id="5a7a6-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5a7a6-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="5a7a6-117"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a7a6-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="5a7a6-118">**ISourceFileInfoCallback**</span><span class="sxs-lookup"><span data-stu-id="5a7a6-118">**ISourceFileInfoCallback**</span></span>](/windows/desktop/direct3dtools/isourcefileinfocallback)

 

 
