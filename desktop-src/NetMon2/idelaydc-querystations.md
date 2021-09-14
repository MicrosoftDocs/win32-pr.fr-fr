---
description: La méthode QueryStations fournit la liste de tous les ordinateurs qui utilisent actuellement Moniteur réseau pour capturer des données.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: 'IDelaydC :: QueryStations, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5a45f5046dbd2e5714424baf42621e0c1d5539ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121369"
---
# <a name="idelaydcquerystations-method"></a>IDelaydC :: QueryStations, méthode

La méthode **QueryStations** fournit la liste de tous les ordinateurs qui utilisent actuellement Moniteur réseau pour capturer des données.

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

Pointeur vers une structure [QUERYTABLE](querytable.md) . En entrée, cette structure doit contenir le nombre maximal d’ordinateurs que vous souhaitez Moniteur réseau retourner et un tableau de structures [STATIONQUERY](stationquery.md) .

Lors de la sortie, cette structure retourne le nombre d’ordinateurs qui capturent des données et une structure [STATIONQUERY](stationquery.md) pour chaque ordinateur trouvé. Notez que cette liste peut inclure des ordinateurs utilisant des versions de Moniteur réseau qui prédatent la version 2,0.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est le code d’erreur suivant :



| Code de retour                                                                                           | Description                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt> </dl> | Aucune mémoire n’était disponible pour traiter cette requête.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode peut être appelée à tout moment après l’appel de [CreateNPPInterface](createnppinterface.md) . Un appel à cette méthode est un appel synchrone, qui peut prendre plusieurs secondes pour s’exécuter Moniteur réseau attend que les ordinateurs distants répondent à la requête. Seuls les ordinateurs sur le sous-réseau local peuvent être interrogés.

Il vous incombe d’allouer la mémoire pour la structure [QUERYTABLE](querytable.md) et de libérer de la mémoire une fois que la table n’est plus nécessaire. Cette exigence comprend la mémoire nécessaire pour le tableau [STATIONQUERY](stationquery.md) utilisé dans QUERYTABLE.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[QUERYTABLE](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




