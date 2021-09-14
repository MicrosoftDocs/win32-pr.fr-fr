---
description: La fonction FindPreviousFrame recherche le frame précédent dans le contexte de capture actuel qui correspond au filtre.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: FindPreviousFrame, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011564"
---
# <a name="findpreviousframe-function"></a>FindPreviousFrame fonction)

La fonction **FindPreviousFrame** recherche le frame précédent dans le contexte de capture actuel qui correspond au filtre.

## <a name="syntax"></a>Syntaxe


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCurrentFrame* 
</dt> <dd>

Handle vers le frame.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nom de protocole, tel que TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Adresse de destination du frame recherché.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Adresse source du frame recherché.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Pointeur vers un **mot** qui reçoit le décalage de protocole.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Point de départ de la recherche. Par défaut, cette fonction effectue une recherche vers l’arrière 1 000 frames à partir du point de départ *OriginalFrameNumber* . Vous pouvez modifier la distance de recherche en ajoutant cette ligne au fichier Nmapi.ini, qui se trouve dans le \\ répertoire Moniteur réseau.

MAXLOOKBACK =<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

Numéro de trame le plus bas dans la capture dans laquelle la recherche est effectuée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un handle vers le frame précédent.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Le filtre de capture est défini principalement par *ProtocolName*, qui est la seule entrée de filtre requise ; vous pouvez ajouter des informations *DestinationAddress* et *sourceAddress* pour augmenter la vitesse de capture.

*ProtocolOffset* est retourné à l’analyseur appelant, ce qui ajoute ce **DWORD** au pointeur retourné par le verrouillage du frame (avec [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) pour obtenir le LPBYTE du protocole recherché. Au retour, le HFRAME qui a réussi le filtre est donné à l’analyseur. Si l’analyseur constate que le frame n’est pas celui qui est recherché, l’analyseur peut remettre ce HFRAME à la fonction **FindPreviousFrame** pour récupérer le frame suivant. Les adresses source et de destination, qui ne sont pas nécessaires, peuvent être transmises en tant que **valeurs NULL**. En cas d’utilisation, ces adresses peuvent être de type adresse \_ \_ IP, et ainsi de suite, pas seulement des types Mac.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




