---
description: Fonction de rappel utilisée pour informer l’hôte des informations de résumé du journal de graphisme.
MS-HAID: vspixengine.ISummaryCallback\_ResultCallback\_DWORD\_SummaryItem\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ISummaryCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07569D26-45A6-41A5-868D-8038BAB9079B
api_name:
- ISummaryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c4ea46550628ec9701ab6b0e6bb3af9ab71a2499
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515329"
---
# <a name="span-idvspixengineisummarycallback_resultcallback_dword_summaryitem_arrspanisummarycallbackresultcallback-method"></a><span id="vspixengine.isummarycallback_resultcallback_dword_summaryitem_arr"></span>ISummaryCallback :: ResultCallback, méthode

Fonction de rappel utilisée pour informer l’hôte des informations de résumé du journal de graphisme.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResultCallback(
   DWORD          count,
   SummaryItem [] count0_summaryItem
);
```

## <a name="parameters"></a>Paramètres

*saut*   
Nombre d’éléments d’informations de résumé retournés.

*count0 \_ summaryItem*   
Éléments d’informations de résumé (paires clé-valeur).

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**ISummaryCallback**](/windows/desktop/direct3dtools/isummarycallback)

 

 
