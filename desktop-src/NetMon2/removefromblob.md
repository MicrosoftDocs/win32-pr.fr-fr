---
description: La fonction RemoveFromBlob supprime tout niveau d’entrée d’objet BLOB (propriétaire, catégorie ou balise).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: RemoveFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 09c9c7f5ada320f33d38cd9e935add7e47721c554fbeed11c35a1b73248d963c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063689"
---
# <a name="removefromblob-function"></a>RemoveFromBlob fonction)

La fonction **RemoveFromBlob** supprime tout niveau d’entrée d’objet BLOB (**propriétaire**, **catégorie** ou **balise**).

## <a name="syntax"></a>Syntaxe


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers l’objet BLOB à partir duquel une entrée est supprimée.

</dd> <dt>

*pOwnerName* \[ dans\]
</dt> <dd>

Pointeur vers le nom du **propriétaire** .

</dd> <dt>

*pCategoryName* \[ dans\]
</dt> <dd>

Pointeur vers le nom de la **catégorie** . Une valeur de paramètre **null** indique que l’appelant tente de supprimer les informations de **propriétaire** données et toutes ses entrées enfants. Notez que si la valeur du paramètre *pCategoryName* est **null**, le paramètre *pTagName* doit également avoir la valeur **null**.

</dd> <dt>

*pTagName* \[ dans\]
</dt> <dd>

Pointeur vers le nom de la **balise** . Une valeur _PTagName_ **null** indique que l’appelant tente de supprimer la **catégorie** donnée et toutes ses entrées enfants. Si la valeur du paramètre n’est pas **null**, l’appelant demande uniquement que les entrées de **balise** spécifiées soient supprimées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




