---
UID: ''
title: UnicodeToBytes fonction)
description: Convertit les caractères Unicode en octets GB18030.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 01109763644dc04aeb398e5fc64e221cd5f3d18870df2654fa5348bc163a277c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764724"
---
# <a name="unicodetobytes-function"></a>UnicodeToBytes fonction)

## <a name="description"></a>Description

Action déconseillée. Convertit les caractères Unicode en octets GB18030.

**Remarque**  lors de la conversion de caractères Unicode en octets GB18030, une application à exécuter sur Windows Vista et versions ultérieures doit utiliser la fonction [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>Paramètres

### <a name="lpwidecharstr-in"></a>lpWideCharStr [in]

Pointeur vers la chaîne Unicode à convertir.

### <a name="cchwidechar-in"></a>cchWideChar [in]

Nombre de caractères de la chaîne Unicode à convertir.

### <a name="lpmultibytestr-in"></a>lpMultiByteStr [in]

Pointeur vers la mémoire tampon multioctet cible.
Si *lpMultiByteStr* est égal à 0, le nombre d’octets du résultat GB18030 est retourné et aucune conversion n’est effectuée.

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

Nombre d’octets de la mémoire tampon multioctets cible.
Si *cchMultiByte* est égal à 0, le nombre d’octets du résultat GB18030 est retourné et aucune conversion n’est effectuée.

## <a name="returns"></a>Retours

Retourne le nombre d’octets des caractères multioctets qui sont générés, en cas de réussite.

## <a name="remarks"></a>Remarques

## <a name="see-also"></a>Voir aussi

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
