---
description: Fournit la liste de tous les ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: 'IRTC :: QueryStations, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a0cebd789284dd41c293424a70686f30eb4601d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951633"
---
# <a name="irtcquerystations-method"></a>IRTC :: QueryStations, méthode

La méthode **QueryStations** fournit la liste de tous les ordinateurs qui utilisent actuellement Moniteur réseau pour capturer les données réseau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpQueryTable* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**QUERYTABLE**](querytable.md) . En entrée, cette structure doit contenir le nombre maximal d’ordinateurs que vous souhaitez Moniteur réseau retourner et un tableau de structures [**STATIONQUERY**](stationquery.md) .

Lors de la sortie, cette structure retourne le nombre d’ordinateurs qui capturent les données et une structure [**STATIONQUERY**](stationquery.md) pour chaque ordinateur trouvé. N’oubliez pas que cela peut inclure des ordinateurs utilisant des versions de Moniteur réseau qui prédatent la version 2,0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est **NMERR \_ Success**.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt> </dl> | La mémoire requise pour traiter cette requête n’est pas disponible.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode peut être appelée à tout moment après l’appel de la méthode [**CreateNPPInterface**](createnppinterface.md) . Un appel à cette méthode est un appel synchrone, qui peut prendre plusieurs secondes pendant que Moniteur réseau attend que les ordinateurs distants répondent à la requête. Seuls les ordinateurs sur le sous-réseau local peuvent être interrogés.

L’utilisateur doit allouer la mémoire pour la structure [**QUERYTABLE**](querytable.md) et libérer cette mémoire une fois que la table n’est plus nécessaire. Cette exigence comprend la mémoire nécessaire pour le tableau [**STATIONQUERY**](stationquery.md) utilisé dans **QUERYTABLE**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**QUERYTABLE**](querytable.md)
</dt> <dt>

[**STATIONQUERY**](stationquery.md)
</dt> </dl>

 

 




