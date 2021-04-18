---
description: Récupère un identificateur de code d’erreur (IDA) et une chaîne de message non mise en forme lorsqu’une erreur jet est fournie.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532735"
---
# <a name="jeterrrawmessage-function"></a>JetErrRawMessage fonction)

Récupère un identificateur de code d’erreur (IDA) et une chaîne de message non mise en forme lorsqu’une erreur jet est fournie.

## <a name="syntax"></a>Syntaxe


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Raise* 
</dt> <dd>

Erreur Jet qui correspond aux informations obtenues.

</dd> <dt>

*pIda* 
</dt> <dd>

Pointeur vers IDA.

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

Pointe vers un pointeur vers le fichier qui explique l’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne **Jet \_ errSuccess**; sinon, elle retourne un message d’erreur non mis en forme qui indique la raison spécifique de l’échec.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
