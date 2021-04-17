---
description: Définit l’ordinateur de lecture actuel pour le journal des graphiques spécifié.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2 :: SetPlaybackMachine, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d7366da4aa999828309136900edfe725af4f622
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522716"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span data-ttu-id="57502-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2 :: SetPlaybackMachine, méthode</span><span class="sxs-lookup"><span data-stu-id="57502-103"><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2::SetPlaybackMachine method</span></span>

<span data-ttu-id="57502-104">Définit l’ordinateur de lecture actuel pour le journal des graphiques spécifié.</span><span class="sxs-lookup"><span data-stu-id="57502-104">Sets the current playback machine for the specified graphics log.</span></span>

## <a name="syntax"></a><span data-ttu-id="57502-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57502-105">Syntax</span></span>


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a><span data-ttu-id="57502-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57502-106">Parameters</span></span>

<span data-ttu-id="57502-107">*Relog* </span><span class="sxs-lookup"><span data-stu-id="57502-107">*logFile* </span></span>  
<span data-ttu-id="57502-108">Chaîne COM contianing le nom du journal de graphisme.</span><span class="sxs-lookup"><span data-stu-id="57502-108">A COM string contianing the name of the graphics log.</span></span>

<span data-ttu-id="57502-109">*bUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="57502-109">*bUseAuthentication* </span></span>  
<span data-ttu-id="57502-110">true pour utiliser l’authentification ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="57502-110">true to use authentication; otherwise, false.</span></span>

<span data-ttu-id="57502-111">*usinage* </span><span class="sxs-lookup"><span data-stu-id="57502-111">*machine* </span></span>  
<span data-ttu-id="57502-112">Chaîne COM contenant le nom de l’ordinateur de lecture.</span><span class="sxs-lookup"><span data-stu-id="57502-112">A COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="57502-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57502-113">Return value</span></span>

<span data-ttu-id="57502-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="57502-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57502-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="57502-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="57502-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57502-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="57502-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="57502-117">Header</span></span></p></td><td><span data-ttu-id="57502-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="57502-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="57502-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57502-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="57502-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="57502-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
