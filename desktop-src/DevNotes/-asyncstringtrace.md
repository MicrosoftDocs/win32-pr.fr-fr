---
description: Termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540399"
---
# <a name="asyncstringtrace-function"></a>AsyncStringTrace fonction)

Termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style **sprintf**.

## <a name="syntax"></a>Syntaxe


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Paramètre de trace 32 bits utilisé pour le filtrage au niveau de l’application.

</dd> <dt>

*szFormat* 
</dt> <dd>

Chaîne se terminant par zéro qui décrit le format de la trace.

</dd> <dt>

*repère* 
</dt> <dd>

Marqueur pour les fonctions **vsprintf** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la longueur de l’instruction de trace, en octets.

## <a name="remarks"></a>Notes

Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).

Le type de données de la **\_ liste va** est un type standard utilisé pour stocker les informations requises par les macros End **\_ arg** et **va \_ end** . Pour plus d’informations, consultez [types standard](/cpp/c-runtime-library/standard-types?view=vs-2019).

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

