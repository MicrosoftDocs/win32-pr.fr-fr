---
description: La fonction InetGetAutodial retourne les paramètres de numérotation automatique à partir du Registre.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 066a00428993d2a1358740cf69d31094fc18b33192c9accf17ce4550b8473edc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001859"
---
# <a name="inetgetautodial-function"></a>InetGetAutodial fonction)

\[Cette fonction n’est pas prise en charge et peut être modifiée ou indisponible dans les futures versions de Windows. \]

La fonction **InetGetAutodial** retourne les paramètres de numérotation automatique à partir du Registre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpfEnable* \[ à\]
</dt> <dd>

Indique si la numérotation automatique est activée. La valeur **true** lors du retour indique que la numérotation automatique est activée.

</dd> <dt>

*lpszEntryName* \[ à\]
</dt> <dd>

Au retour, contient le nom de l’entrée d’annuaire téléphonique définie pour la numérotation automatique.

</dd> <dt>

*cbEntryNameSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon allouée par l’appelant pour le nom de l’entrée de l’annuaire téléphonique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction peut retourner l’une de ces valeurs.



| Code de retour                                                                                                | Description                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR de \_ réussite**</dt> </dl>              | L’appel a réussi.<br/>                                                                                                                       |
| <dl> <dt>**ERREUR d' \_ arguments incorrects \_**</dt> </dl>       | *lpfEnable* ou *lpszEntryName* contient un pointeur **null** , ou la valeur de *cbEntryNameSize* est égale à zéro.<br/>                                         |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl>  | La mémoire est insuffisante pour allouer les tampons internes.<br/>                                                                                    |
| <dl> <dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt> </dl> | *cbEntryNameSize* n’indique pas que la mémoire tampon vers laquelle pointe *lpszEntryName* est suffisamment grande pour recevoir le nom de l’entrée de l’annuaire téléphonique.<br/> |



 

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Inetcfg.dll</dt> </dl> |



 

 
