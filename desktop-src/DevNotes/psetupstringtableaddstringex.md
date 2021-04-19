---
description: Ajoute une chaîne et des données supplémentaires à une table.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532237"
---
# <a name="psetupstringtableaddstringex-function"></a>pSetupStringTableAddStringEx fonction)

\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]

Ajoute une chaîne et des données supplémentaires à une table.

## <a name="syntax"></a>Syntaxe


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*STRINGTABLE* \[ dans\]
</dt> <dd>

Pointeur vers la table de chaînes.

</dd> <dt>

*Chaîne* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne à ajouter à la table.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

La valeur de ce paramètre peut être `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .



| Valeur                                                                                                                                                                                                                                             | Signification                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <dt>**STRTAB \_ 0x001 \_ sensibles**</dt> à la casse <dt></dt> </dl> | La chaîne respecte la casse.<br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <dt>**STRTAB \_ NOUVEAU \_ EXTRADATA**</dt> <dt>0x004</dt> </dl>    | Il y a des données supplémentaires.<br/>      |



 

</dd> <dt>

*ExtraData* \[ dans, facultatif\]
</dt> <dd>

Pointeur facultatif vers un objet de données supplémentaire.

</dd> <dt>

*ExtraDataSize* \[ dans, facultatif\]
</dt> <dd>

Taille des données supplémentaires.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
