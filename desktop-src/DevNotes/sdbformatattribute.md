---
description: Convertit les données d’attribut spécifiées au format XML.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: SdbFormatAttribute fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 44303a568a9f7775893033edc512e8a916004c43207277e308e1d4826d9f9537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161553"
---
# <a name="sdbformatattribute-function"></a>SdbFormatAttribute fonction)

Convertit les données d’attribut spécifiées au format XML.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAttrInfo* \[ dans\]
</dt> <dd>

Structure [**ATTRINFO**](attrinfo.md) .

</dd> <dt>

*pchBuffer* \[ à\]
</dt> <dd>

Mémoire tampon de sortie.

</dd> <dt>

*dwBufferSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon *pchBuffer* , en caractères.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** si la mémoire tampon est insuffisante ou si l’attribut est introuvable.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




