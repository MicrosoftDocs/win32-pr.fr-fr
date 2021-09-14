---
description: La fonction CreateHandoffTable crée une table de remise qui comprend les informations du jeu de remise stockées dans le fichier INI de l’analyseur.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: CreateHandoffTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222689"
---
# <a name="createhandofftable-function"></a>CreateHandoffTable fonction)

La fonction **CreateHandoffTable** crée une [*table de remise*](h.md) qui comprend les informations du jeu de remise stockées dans le fichier ini de l’analyseur.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CNAME* \[ dans\]
</dt> <dd>

Chaîne qui indique la section du fichier INI où se trouvent les informations sur le jeu de remise.

</dd> <dt>

*Inifile* \[ dans\]
</dt> <dd>

Chaîne qui comprend le nom du fichier INI de l’analyseur.

</dd> <dt>

*htable* \[ à\]
</dt> <dd>

Handle vers une structure **HANDOFFTABLE** créée et gérée par Moniteur réseau.

</dd> <dt>

*nMaxProtocolEntries* \[ dans\]
</dt> <dd>

Nombre qui spécifie le nombre maximal d’entrées que la table de remise peut traiter.

</dd> <dt>

de *base* \[ dans\]
</dt> <dd>

Base numérique des numéros des jeux de remise stockés dans le fichier INI.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est le nombre d’entrées dans la table de remise.

Si la fonction échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

La table de remise créée par Moniteur réseau est basée sur les informations fournies dans le fichier INI de l’analyseur. Le handle retourné à la table de remise peut ensuite être utilisé pour obtenir un handle vers l’un des protocoles inclus dans la table. Pour obtenir un handle de l’un de ces protocoles, appelez [GetProtocolFromTable](getprotocolfromtable.md).

Notez que l’application de l’analyseur n’accède jamais directement à la structure **HANDOFFTABLE** . Cette structure est créée et gérée par Moniteur réseau.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetProtocolFromTable](getprotocolfromtable.md)
</dt> <dt>

[HANDOFFTABLE](handofftable.md)
</dt> </dl>

 

 




