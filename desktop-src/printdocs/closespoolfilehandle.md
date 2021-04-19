---
description: La fonction CloseSpoolFileHandle ferme un handle vers un fichier de mise en file d’attente associé au travail d’impression actuellement soumis par l’application.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: CloseSpoolFileHandle, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544829"
---
# <a name="closespoolfilehandle-function"></a>CloseSpoolFileHandle fonction)

La fonction **CloseSpoolFileHandle** ferme un handle vers un fichier de mise en file d’attente associé au travail d’impression actuellement soumis par l’application.

## <a name="syntax"></a>Syntaxe


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante sur laquelle le travail a été soumis. Il doit s’agir du même handle que celui utilisé pour obtenir *hSpoolFile* avec [**GetSpoolFileHandle**](getspoolfilehandle.md).

</dd> <dt>

*hSpoolFile* \[ dans\]
</dt> <dd>

Handle du fichier spouleur en cours de fermeture. Si [**CommitSpoolData**](commitspooldata.md) n’a pas été appelé depuis l’appel de [**GetSpoolFileHandle**](getspoolfilehandle.md) , il doit s’agir du même handle que celui retourné par **GetSpoolFileHandle**. Dans le cas contraire, il doit s’agir du handle qui a été retourné par l’appel le plus récent à **CommitSpoolData**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**True**, si elle est réussie, **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Votre application ne doit pas appeler [**ClosePrinter**](closeprinter.md) sur *hPrinter* tant qu’elle n’a pas accédé au fichier spool pour la dernière fois. Ensuite, il doit appeler **CloseSpoolFileHandle** suivi de **ClosePrinter**. Toute tentative d’accès au descripteur de fichier de mise en file d’attente après la fermeture du *hPrinter* d’origine échoue, même si le descripteur de fichier lui-même n’a pas été fermé. **CloseSpoolFileHandle** échoue si **ClosePrinter** est appelé en premier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> </dl>

 

 




