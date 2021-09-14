---
description: Définit le filtre ETYPE/SAP de l’objet BLOB.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: SetNPPEtypeSapFilter, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194567"
---
# <a name="setnppetypesapfilter-function"></a>SetNPPEtypeSapFilter fonction)

La fonction **SetNPPEtypeSapFilter** définit le filtre ETYPE/SAP de l’objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB.

</dd> <dt>

*nSaps* \[ dans\]
</dt> <dd>

Nombre de SAP.

</dd> <dt>

*nEtypes* \[ dans\]
</dt> <dd>

Nombre de ETYPE dans la table ETYPE en cours de définition.

</dd> <dt>

*lpSapTable* \[ dans\]
</dt> <dd>

Pointeur vers la table SAP qui est définie.

</dd> <dt>

*lpEtypeTable* \[ dans\]
</dt> <dd>

Pointeur vers la table ETYPE qui est définie.

</dd> <dt>

*FilterFlags* \[ dans\]
</dt> <dd>

Indicateurs de filtre définis.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle d’un objet BLOB d’erreurs qui spécifie à quel endroit de l’objet BLOB d’origine l’erreur (le cas échéant) s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetNPPEtypeSapFilter](getnppetypesapfilter.md)
</dt> </dl>

 

 




