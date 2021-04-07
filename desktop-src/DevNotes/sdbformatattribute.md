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
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846901"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




