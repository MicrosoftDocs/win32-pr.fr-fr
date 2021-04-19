---
description: Rappel qui avertit l’hôte des informations de maillage écrites par la requête associée.
MS-HAID: vspixengine.IPipeLineStagesCallback3\_MeshFileReadyCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback3 :: MeshFileReadyCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: BD4719A5-AC07-446A-A7CA-5978F869F66E
api_name:
- IPipeLineStagesCallback3.MeshFileReadyCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7974a9f04acf8e620d792b377fa482dab6de71dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515127"
---
# <a name="span-idvspixengineipipelinestagescallback3_meshfilereadycallback_bstrspanipipelinestagescallback3meshfilereadycallback-method"></a><span id="vspixengine.ipipelinestagescallback3_meshfilereadycallback_bstr"></span>IPipeLineStagesCallback3 :: MeshFileReadyCallback, méthode

Rappel qui avertit l’hôte des informations de maillage écrites par la requête associée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MeshFileReadyCallback(
   BSTR meshFilename
);
```

## <a name="parameters"></a>Paramètres

*meshFilename*   
Chaîne COM contenant le nom du chemin d’accès du fichier dans lequel les données de maillage sont écrites.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPipeLineStagesCallback3**](/windows/desktop/direct3dtools/ipipelinestagescallback3)

 

 
