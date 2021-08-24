---
description: La fonction BuildINIPath retourne un chemin d’accès complet à un fichier INI qui correspond aux informations que vous entrez.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: BuildINIPath, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b75df338142ab0ec97db3e60cbba1b5f68df3e0e67947d4c13cdccccd409bdf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744690"
---
# <a name="buildinipath-function"></a>BuildINIPath fonction)

La fonction **BuildINIPath** retourne un chemin d’accès complet à un fichier ini qui correspond aux informations que vous entrez.

## <a name="syntax"></a>Syntaxe


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FullPath* 
</dt> <dd>

Mémoire tampon qui reçoit le nom de fichier INI complet.

</dd> <dt>

*IniFileName* 
</dt> <dd>

Nom du fichier INI (nom de fichier complet moins l’extension de nom de fichier).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est un pointeur vers le nom de fichier INI complet.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Remarques

Le chemin d’accès retourné par cette fonction est un chemin d’accès complet à un fichier INI qui correspond aux informations que vous entrez. Par exemple, si vous entrez XNS ou TCP, la fonction génère un chemin d’accès vers Xns.ini ou Tcp.ini, respectivement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




