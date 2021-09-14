---
description: Crée un gestionnaire de flux d’octets pour la source média MP3.
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313842"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>MFCreateMP3ByteStreamPlugin fonction)

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Au lieu de cela, les applications doivent utiliser le programme de [résolution source](source-resolver.md) pour créer la source de média MP3.\]

Crée un gestionnaire de flux d’octets pour la source média MP3.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* \[ dans\]
</dt> <dd>

Identificateur d'interface (IID) de l'interface demandée. Affectez à ce paramètre la valeur **IID \_ IMFByteStreamHandler** pour recevoir un pointeur vers l’interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) .

</dd> <dt>

*ppvHandler* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface. L’appelant doit libérer l’interface.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation associée. Pour appeler cette fonction, vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à mf.dll.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows Vista<br/>                             |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions Media Foundation](media-foundation-functions.md)
</dt> <dt>

[Gestionnaires de schémas et gestionnaires de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Résolveur source](source-resolver.md)
</dt> </dl>

 

 
