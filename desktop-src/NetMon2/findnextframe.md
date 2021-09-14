---
description: Recherche le frame suivant dans le contexte de capture actuel qui correspond au filtre.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: FindNextFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222649"
---
# <a name="findnextframe-function"></a>FindNextFrame fonction)

La fonction **FindNextFrame** recherche le frame suivant dans le contexte de capture actuel qui correspond au filtre.

## <a name="syntax"></a>Syntaxe


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCurrentFrame* 
</dt> <dd>

Handle du frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nom de protocole, tel que TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Adresse de destination.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Adresse source.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Pointeur vers un **mot** qui recevra le décalage de protocole.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Point de départ de la recherche. Par défaut, cette fonction recherche les frames Forward 1 000 à partir du point de départ *OriginalFrameNumber* . Pour modifier la distance de recherche, ajoutez la ligne suivante au fichier Nmapi.ini, situé dans le \\ répertoire Moniteur réseau.

MAXLOOKBACK =<new lookforward distance>

</dd> <dt>

*HighestFrame* 
</dt> <dd>

Numéro de trame le plus élevé dans la capture dans laquelle la recherche est effectuée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un handle vers le frame suivant.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Le filtre de capture est défini principalement par le paramètre *ProtocolName* , qui est la seule entrée de filtre requise ; vous pouvez ajouter des données *DestinationAddress* et *sourceAddress* pour augmenter la vitesse de capture.

Le pointeur *ProtocolOffset* est retourné à l’analyseur appelant, qui ajoute le **mot** au pointeur retourné en verrouillant le frame (avec [ParserTemporaryLockFrame](parsertemporarylockframe.md)) pour obtenir le **LPBYTE** du protocole recherché. Au retour, le HFRAME qui a réussi le filtre est donné à l’analyseur. Si l’analyseur constate que ce frame n’est pas celui qui est recherché, l’analyseur peut remettre le HFRAME à la fonction **FindNextFrame** pour accéder au frame suivant. Les adresses source et de destination ne sont pas requises et peuvent être passées comme **null**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




