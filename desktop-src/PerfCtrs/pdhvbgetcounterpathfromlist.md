---
description: La fonction PdhVbGetCounterPathFromList copie le chemin d’accès du compteur référencé par le paramètre d’index à partir d’une liste de chemins de compteurs créée par l’utilisateur à partir de l’appel le plus récent à la fonction PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416659"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>PdhVbGetCounterPathFromList fonction)

La fonction **PdhVbGetCounterPathFromList** copie le chemin d’accès du compteur référencé par le paramètre d' *index* à partir d’une liste de chemins de compteurs créée par l’utilisateur à partir de l’appel le plus récent à la fonction [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

> [!IMPORTANT]
> La fonction décrite dans cette rubrique peut être modifiée ou non disponible à l’avenir. Au lieu de cela, Microsoft vous recommande d’utiliser les fonctions décrites dans [fonctions des compteurs de performances](performance-counters-functions.md).

Function PdhVbGetCounterPathFromList ( \_ index ByVal comme long, \_ ByVal buffer sous forme de chaîne, \_ ByVal BufferLength As long \_ ) As long

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Index du chemin d’accès du compteur à récupérer. Il doit s’agir d’une valeur supérieure ou égale à 1 et inférieure ou égale à la valeur retournée par la fonction [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

</dd> <dt>

*Buffer* 
</dt> <dd>

Chaîne dimensionnée et initialisée qui recevra le chemin d’accès du compteur qui correspond à la valeur du paramètre d’index.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Nombre maximal de caractères qui peuvent être contenus dans la chaîne référencée par la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La fonction retourne le nombre de caractères copiés dans la mémoire tampon.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| Bibliothèque<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




