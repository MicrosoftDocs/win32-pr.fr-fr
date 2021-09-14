---
description: La fonction GetNPPEtypeSapFilter récupère le filtre ETYPE/SAP à partir d’un objet BLOB donné.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: GetNPPEtypeSapFilter, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121406"
---
# <a name="getnppetypesapfilter-function"></a>GetNPPEtypeSapFilter fonction)

La fonction **GetNPPEtypeSapFilter** récupère le filtre ETYPE/SAP à partir d’un objet BLOB donné.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB.

</dd> <dt>

*pnSaps* \[ à\]
</dt> <dd>

Pointeur vers le nombre de protocoles renvoyés dans la table SAP.

</dd> <dt>

*pnEtypes* \[ à\]
</dt> <dd>

Pointeur vers le nombre retourné de ETYPE dans la table ETYPE.

</dd> <dt>

*ppSapTable* \[ à\]
</dt> <dd>

Pointeur vers la table SAP retournée.

</dd> <dt>

*ppEtypeTable* \[ à\]
</dt> <dd>

Pointeur vers la table ETYPE retournée.

</dd> <dt>

*pFilterFlags* \[ à\]
</dt> <dd>

Pointeur vers les indicateurs de filtre retournés.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle vers un objet BLOB d’erreur, qui spécifie l’emplacement dans l’objet BLOB d’origine où l’erreur (le cas échéant) s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

## <a name="remarks"></a>Notes

Les informations ETYPE/SAP sont stockées dans la catégorie de **configuration** de la section **propriétaire** NPP.

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

[SetNPPEtypeSapFilter](setnppetypesapfilter.md)
</dt> </dl>

 

 




