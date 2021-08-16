---
description: La fonction GetCaptureCommentFromFilename extrait le commentaire de capture à partir d’un fichier de capture.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: GetCaptureCommentFromFilename, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1b92b81fa00834c3a4038a6a6bb9f295246a7c0b217c99779a5d2c569dbbf982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366810"
---
# <a name="getcapturecommentfromfilename-function"></a>GetCaptureCommentFromFilename fonction)

La fonction **GetCaptureCommentFromFilename** extrait le commentaire de capture à partir d’un [*fichier de capture*](c.md).

## <a name="syntax"></a>Syntaxe


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpFilename* \[ dans\]
</dt> <dd>

Pointeur vers le nom du fichier de capture.

</dd> <dt>

*lpComment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne pré-allouée pour le commentaire.

</dd> <dt>

*BufferSize* \[ dans\]
</dt> <dd>

Taille de la chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (autrement dit, si le commentaire est trouvé et copié, ou s’il n’y a aucun commentaire dans le fichier de capture), la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est un code d’erreur.



| Code de retour                                                                                                 | Description                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_erreur de \_ lecture du fichier NMERR \_**</dt> </dl>     | Impossible de lire le commentaire de capture.<br/>                               |
| <dl> <dt>**\_format de \_ fichier non valide NMERR \_**</dt> </dl> | La trame de commentaire n’est pas un format de fichier valide.<br/>                     |
| <dl> <dt>**\_fichier NMERR \_ \_ introuvable**</dt> </dl>      | Impossible de trouver le fichier spécifié par le paramètre *lpFilename* .<br/> |
| <dl> <dt>**\_paramètre NMERR non valide \_**</dt> </dl>    | L’un des paramètres est spécifié de manière incorrecte.<br/>                   |



 

## <a name="remarks"></a>Remarques

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureCommentFromFilename** .

Pour récupérer le commentaire d’une capture en temps réel, appelez la fonction [GetCaptureComment](getcapturecomment.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




