---
description: La fonction GetSpoolFileHandle récupère un handle pour le fichier de mise en file d’attente associé au travail actuellement soumis par l’application.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: GetSpoolFileHandle, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035224"
---
# <a name="getspoolfilehandle-function"></a>GetSpoolFileHandle fonction)

La fonction **GetSpoolFileHandle** récupère un handle pour le fichier de mise en file d’attente associé au travail actuellement soumis par l’application.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante sur laquelle le travail a été soumis. Il doit s’agir du même handle que celui utilisé pour envoyer le travail. (Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.)

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne un handle au fichier de mise en file d’attente.

Si la fonction échoue, elle retourne **une \_ \_ valeur de handle non valide**.

## <a name="remarks"></a>Notes

Avec le descripteur du fichier de mise en file d’attente, votre application peut écrire dans le fichier de mise en file d’attente avec des appels à [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) suivis de [**CommitSpoolData**](commitspooldata.md).

Votre application ne doit pas appeler [**ClosePrinter**](closeprinter.md) sur *hPrinter* tant qu’elle n’a pas accédé au fichier spool pour la dernière fois. Ensuite, il doit appeler [**CloseSpoolFileHandle**](closespoolfilehandle.md) suivi de **ClosePrinter**. Toute tentative d’accès au descripteur de fichier de mise en file d’attente après la fermeture du *hPrinter* d’origine échoue, même si le descripteur de fichier lui-même n’a pas été fermé. **CloseSpoolFileHandle** échouera même si **ClosePrinter** est appelé en premier.

Cette fonction échoue si elle est appelée avant la fin de la mise en attente du travail d’impression.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **GetSpoolFileHandleW** (Unicode) et **GetSpoolFileHandleA** (ANSI)<br/>                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> <dt>

[**CommitSpoolData**](commitspooldata.md)
</dt> </dl>

 

