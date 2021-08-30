---
description: Rappel qui avertit l’hôte des informations de maillage des étapes de pipeline retournées par la requête dans.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPipeLineStagesCallback :: MeshDataVertCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e51321373de80a4e90835a46c53e895bff7114df
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625945"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback :: MeshDataVertCallback, méthode

Rappel qui avertit l’hôte des informations de maillage des étapes de pipeline retournées par la requête dans.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a>Paramètres

*numVertices*   
Nombre de vertex dans les résultats.

*numBufferLayoutEntries*   
Nombre d’entrées de disposition de mémoire tampon dans les résultats.

*\_entrées count1*   
La disposition de la mémoire tampon entière. Ils décrivent la signature de sortie du nuanceur.

*progrès*   
Taille (Stride) d’un bloc de sortie entier.

*numVBBytes*   
Taille de la mémoire tampon de vertex, en octets.

*count4 \_ pVBData*   
Mémoire tampon de vertex.

*numIBBytes*   
Taille de la mémoire tampon d’index en octets.

*count6 \_ pIBData*   
Mémoire tampon d’index.

*indexSize*   
Taille de chaque index, en octets.

*IBOffset*   
Offset dans la mémoire tampon d’index qui spécifie où les index doivent commencer à être utilisés.

*baseVertex*   
Offset dans la mémoire tampon de vertex qui spécifie l’emplacement où les vertex doivent commencer à être utilisés.

*minVertex*   

*IBIndexesVB*   
true lorsque la mémoire tampon d’index est utilisée ; Sinon, false.

*numIndices*   
Nombre d’index utilisés.

*topologie*   
Topolology du nuanceur. Ce n’est pas nécessairement le même que la topologie de l’appel de dessin associé.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
