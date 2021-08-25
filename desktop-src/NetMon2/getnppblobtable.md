---
description: La fonction GetNPPBlobTable récupère une table d’objets BLOB NPP qui représente les cartes réseau du Registre sur l’ordinateur local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: GetNPPBlobTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 49920df1be929eb9b35781aeabdcdf47167e82a94066e2d3237207dd00b08f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910699"
---
# <a name="getnppblobtable-function"></a>GetNPPBlobTable fonction)

La fonction **GetNPPBlobTable** récupère une table d’objets BLOB NPP qui représente les cartes réseau du Registre sur l’ordinateur local.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFilterBlob* \[ dans\]
</dt> <dd>

Handle vers un objet BLOB de filtre qui limite les objets BLOB NPP renvoyés dans la table.

</dd> <dt>

*ppBlobTable* \[ à\]
</dt> <dd>

Pointeur vers une structure de [ \_ table d’objets BLOB](blob-table.md) qui contient au moins un pointeur d’objet BLOB.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                | Description                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ aucune \_ \_ dll NPP**</dt> </dl>         | Aucune dll n’a été trouvée dans le répertoire NPP.<br/>                    |
| <dl> <dt>**NMERR \_ aucune \_ \_ dll NPP \_ valide**</dt> </dl> | Aucune des dll du répertoire NPP n’était des dll NPP valides.<br/>  |
| <dl> <dt>**NMERR \_ aucun \_ \_ NPPS correspondant**</dt> </dl>   | Les objets BLOB NPP ont été découverts, mais aucun n’a passé le test de filtre.<br/> |
| <dl> <dt>**NMERR \_ hors \_ \_ Mémo**</dt> </dl>       | Moniteur réseau n’a pas pu allouer de mémoire.<br/>            |



 

## <a name="remarks"></a>Remarques

L’objet BLOB nommé par *hFilterBlob* peut également être un objet BLOB spécial.

Si vous affectez la **valeur true** à l’indicateur dans l’objet blob de filtres, la table d’objets BLOB retournée peut également inclure des objets BLOB spéciaux.

Si l’objet BLOB nommé par *hFilterBlob* est un objet BLOB spécial, l’interface utilisateur de moniteur réseau tente de la traiter. Par exemple, supposons qu’un appel précédent retourne un objet BLOB spécial du NPP distant. L’application insère la balise requise, le nom de l’ordinateur \_ . Le Finder transmet ensuite cet objet BLOB au NPP distant, qui retourne ensuite une table des objets BLOB NPP associés au nom de l’ordinateur.

Pour détruire tous les objets BLOB retournés et la table BLOB, l’appelant est chargé d’appeler la fonction **DestroyBlob** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




