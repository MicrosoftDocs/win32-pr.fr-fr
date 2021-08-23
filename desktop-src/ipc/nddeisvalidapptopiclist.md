---
description: Détermine si une application et une chaîne de rubrique (&\# 0034 ; AppName \| thème&\# 0034 ;) utilise la syntaxe appropriée.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: NDdeIsValidAppTopicList, fonction (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: f7b70d3e33f67c8c0a457f85df91e83e374a3ef4d0f0b1a0af1c5c41ea81c2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611129"
---
# <a name="nddeisvalidapptopiclist-function"></a>NDdeIsValidAppTopicList fonction)

\[Le DDE réseau n’est plus pris en charge. Nddeapi.dll est présent sur Windows Vista, mais tous les appels de fonction renvoient NDDE \_ non \_ implémenté.\]

Détermine si une application et une chaîne de rubrique («*appname* \| *thème*») utilisent la syntaxe appropriée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*targetTopic* \[ dans\]
</dt> <dd>

Pointeur vers l’application et la chaîne de rubrique à valider. Ce paramètre ne peut pas être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la syntaxe du paramètre *targetTopic* est valide, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

Cette fonction est également appelée par [**NDdeShareAdd**](nddeshareadd.md) lors de la création du partage DDE.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Nddeapi. h</dt> </dl>      |
| Bibliothèque<br/>                  | <dl> <dt>Nddeapi. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Noms Unicode et ANSI<br/>   | **NDdeIsValidAppTopicListW** (Unicode) et **NDdeIsValidAppTopicListA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[présentation du échange dynamique de données réseau](network-dynamic-data-exchange.md)
</dt> <dt>

[Fonctions DDE réseau](network-dde-functions.md)
</dt> <dt>

[**NDdeShareAdd**](nddeshareadd.md)
</dt> </dl>

 

 




