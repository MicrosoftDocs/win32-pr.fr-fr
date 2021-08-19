---
description: Récupère une chaîne de message non mise en forme lorsqu’un identificateur de code d’erreur (IDA) est fourni.
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 39bd07b3ac75bed85ff26dd7f014420ebaca8be16d6f0195d40e9161c0905496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955758"
---
# <a name="jeterridarawmessage-function"></a>JetErrIDARawMessage fonction)

Récupère une chaîne de message non mise en forme lorsqu’un identificateur de code d’erreur (IDA) est fourni.

## <a name="syntax"></a>Syntaxe


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Ida* 
</dt> <dd>

Numéro qui mappe à un code d’erreur spécifique et qui est affiché à l’utilisateur.

</dd> <dt>

*pMessage* 
</dt> <dd>

Pointeur vers le message d’erreur.

</dd> <dt>

*cbMessage* 
</dt> <dd>

Nombre d’octets dans le message d’erreur.

</dd> <dt>

*pcbActual* 
</dt> <dd>

Pointeur vers le nombre réel d’octets lus.

</dd> <dt>

*pContextId* 
</dt> <dd>

Pointeur vers l’identificateur de contexte qui est associé au fichier d’aide.

</dd> <dt>

*pwszHelp/fichier* 
</dt> <dd>

Pointeur vers un pointeur vers le fichier qui explique l’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne **Jet \_ errSuccess**; sinon, elle retourne un message sans mise en forme qui indique la raison spécifique de l’échec.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
