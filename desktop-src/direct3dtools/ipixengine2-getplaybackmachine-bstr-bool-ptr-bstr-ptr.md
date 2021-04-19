---
description: Obtient des informations sur l’ordinateur de lecture en cours.
MS-HAID: vspixengine.IPixEngine2\_GetPlaybackMachine\_BSTR\_BOOL\_ptr\_BSTR\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2 :: GetPlaybackMachine, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D6C3C391-F039-4A5A-AA88-87A3624ECAD2
api_name:
- IPixEngine2.GetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c572d1a87fb537fd53a7f3e8f8048d1046980b20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515913"
---
# <a name="span-idvspixengineipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptrspanipixengine2getplaybackmachine-method"></a><span data-ttu-id="6fd5d-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2 :: GetPlaybackMachine, méthode</span><span class="sxs-lookup"><span data-stu-id="6fd5d-103"><span id="vspixengine.ipixengine2_getplaybackmachine_bstr_bool_ptr_bstr_ptr"></span>IPixEngine2::GetPlaybackMachine method</span></span>

<span data-ttu-id="6fd5d-104">Obtient des informations sur l’ordinateur de lecture en cours.</span><span class="sxs-lookup"><span data-stu-id="6fd5d-104">Gets information about the current playback machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fd5d-105">Syntax</span></span>


```C++
HRESULT GetPlaybackMachine(
   BSTR   logFile,
   BOOL * pUseAuthentication,
   BSTR * pMachine
);
```

## <a name="parameters"></a><span data-ttu-id="6fd5d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fd5d-106">Parameters</span></span>

<span data-ttu-id="6fd5d-107">*Relog* </span><span class="sxs-lookup"><span data-stu-id="6fd5d-107">*logFile* </span></span>  
<span data-ttu-id="6fd5d-108">Chaîne COM contenant le nom du journal des graphiques associé.</span><span class="sxs-lookup"><span data-stu-id="6fd5d-108">A COM string containing the name of the associated graphics log.</span></span>

<span data-ttu-id="6fd5d-109">*pUseAuthentication* </span><span class="sxs-lookup"><span data-stu-id="6fd5d-109">*pUseAuthentication* </span></span>  
<span data-ttu-id="6fd5d-110">Au retour, true si la connexion utilise l’authentification ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="6fd5d-110">On return, true if the connection uses authentication; otherwise, false.</span></span>

<span data-ttu-id="6fd5d-111">*pMachine* </span><span class="sxs-lookup"><span data-stu-id="6fd5d-111">*pMachine* </span></span>  
<span data-ttu-id="6fd5d-112">Au retour, chaîne COM contenant le nom de l’ordinateur de lecture.</span><span class="sxs-lookup"><span data-stu-id="6fd5d-112">On return, a COM string containing the name of the playback machine.</span></span>

## <a name="return-value"></a><span data-ttu-id="6fd5d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fd5d-113">Return value</span></span>

<span data-ttu-id="6fd5d-114">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6fd5d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6fd5d-115">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6fd5d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd5d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fd5d-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6fd5d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fd5d-117">Header</span></span></p></td><td><span data-ttu-id="6fd5d-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6fd5d-118">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="6fd5d-119"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fd5d-119"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="6fd5d-120">**IPixEngine2**</span><span class="sxs-lookup"><span data-stu-id="6fd5d-120">**IPixEngine2**</span></span>](/windows/desktop/direct3dtools/ipixengine2)

 

 
