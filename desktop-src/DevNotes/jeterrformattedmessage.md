---
description: Récupère un identificateur de code d’erreur (IDA) et crée la dernière chaîne d’affichage lorsqu’une erreur jet et des informations d’erreur étendues sont fournies.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541264"
---
# <a name="jeterrformattedmessage-function"></a>JetErrFormattedMessage fonction)

Récupère un identificateur de code d’erreur (IDA) et crée la dernière chaîne d’affichage lorsqu’une erreur jet et des informations d’erreur étendues sont fournies.

## <a name="syntax"></a>Syntaxe


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
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

Numéro d’erreur jet utilisé pour rechercher et mettre en forme le message d’erreur affichable.

</dd> <dt>

*pExtendedErrorInfo* 
</dt> <dd>

Toutes les informations sur les erreurs jet, y compris le nom de la base de données, le nom de la table et toute information d’erreur mineure.

</dd> <dt>

*pIda* 
</dt> <dd>

Pointeur vers IDA associé au code d’erreur spécifique.

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

Si la fonction est réussie, elle retourne **Jet \_ errSuccess**; sinon, elle retourne un message d’erreur mis en forme qui indique la raison spécifique de l’échec.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjter40.dll</dt> </dl> |



 

 
