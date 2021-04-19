---
description: Demande d’envoi de chemins d’accès aux symboles de débogage au moteur local (non distant).
MS-HAID: vspixengine.ISymbolSettings\_UpdateSymbolSettings\_SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISymbolSettings :: UpdateSymbolSettings, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E48E509F-8C33-49D6-B799-B16F70C1AA64
api_name:
- ISymbolSettings.UpdateSymbolSettings
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c60ceacbf8d11f951896979862dad6520c32837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514305"
---
# <a name="span-idvspixengineisymbolsettings_updatesymbolsettings_symbolserverinfospanisymbolsettingsupdatesymbolsettings-method"></a><span data-ttu-id="dd37f-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings :: UpdateSymbolSettings, méthode</span><span class="sxs-lookup"><span data-stu-id="dd37f-103"><span id="vspixengine.isymbolsettings_updatesymbolsettings_symbolserverinfo"></span>ISymbolSettings::UpdateSymbolSettings method</span></span>

<span data-ttu-id="dd37f-104">Demande d’envoi de chemins d’accès aux symboles de débogage au moteur local (non distant).</span><span class="sxs-lookup"><span data-stu-id="dd37f-104">A request to send debug symbol paths to the local (non-remote) engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd37f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd37f-105">Syntax</span></span>


```C++
HRESULT UpdateSymbolSettings(
   SymbolServerInfo symbolServerInfo
);
```

## <a name="parameters"></a><span data-ttu-id="dd37f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd37f-106">Parameters</span></span>

<span data-ttu-id="dd37f-107">*symbolServerInfo* </span><span class="sxs-lookup"><span data-stu-id="dd37f-107">*symbolServerInfo* </span></span>  
<span data-ttu-id="dd37f-108">Déboguer les informations de chemin d’accès du serveur de symboles.</span><span class="sxs-lookup"><span data-stu-id="dd37f-108">Debug symbol server path information.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd37f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd37f-109">Return value</span></span>

<span data-ttu-id="dd37f-110">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dd37f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dd37f-111">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dd37f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd37f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd37f-112">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="dd37f-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd37f-113">Header</span></span></p></td><td><span data-ttu-id="dd37f-114">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="dd37f-114">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="dd37f-115"><span id="see_also"></span>Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd37f-115"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="dd37f-116">**ISymbolSettings**</span><span class="sxs-lookup"><span data-stu-id="dd37f-116">**ISymbolSettings**</span></span>](/windows/desktop/direct3dtools/isymbolsettings)

 

 
