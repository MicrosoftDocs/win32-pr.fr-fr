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
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011567"
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

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un pointeur vers le nom de fichier INI complet.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Le chemin d’accès retourné par cette fonction est un chemin d’accès complet à un fichier INI qui correspond aux informations que vous entrez. Par exemple, si vous entrez XNS ou TCP, la fonction génère un chemin d’accès vers Xns.ini ou Tcp.ini, respectivement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Analyseur. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl>  |



 

 




