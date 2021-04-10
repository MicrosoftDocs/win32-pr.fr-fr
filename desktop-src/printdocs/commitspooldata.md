---
description: La fonction CommitSpoolData informe le spouleur d’impression qu’une quantité de données spécifiée a été écrite dans un fichier spouleur spécifié et qu’elle est prête à être rendue.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: CommitSpoolData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864761"
---
# <a name="commitspooldata-function"></a>CommitSpoolData fonction)

La fonction **CommitSpoolData** informe le spouleur d’impression qu’une quantité de données spécifiée a été écrite dans un fichier spouleur spécifié et qu’elle est prête à être rendue.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
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

Handle du fichier de mise en attente en cours de modification. Lors du premier appel de **CommitSpoolData**, il doit s’agir du même handle que celui retourné par [**GetSpoolFileHandle**](getspoolfilehandle.md). Les appels suivants à **CommitSpoolData** doivent passer le handle retourné par l’appel précédent. Consultez la section Notes.

</dd> <dt>

*cbCommit* 
</dt> <dd>

Nombre d’octets validés dans le spouleur d’impression.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne un handle au fichier de mise en file d’attente.

Si la fonction échoue, elle retourne une \_ valeur de handle non valide \_ .

## <a name="remarks"></a>Notes

Les applications qui envoient un travail d’impression de spouleur peuvent appeler [**GetSpoolFileHandle**](getspoolfilehandle.md) , puis écrire directement les données dans le handle de fichier de mise en file d’attente en appelant [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile). Pour informer le spouleur d’impression que le fichier contient des données qui sont prêtes à être rendues, l’application doit appeler **CommitSpoolData** et fournir le nombre d’octets disponibles.

Si **CommitSpoolData** est appelée plusieurs fois, chaque appel doit utiliser le descripteur de fichier de mise en file d’attente retourné par l’appel précédent. Quand plus aucune donnée n’est écrite dans le fichier de mise en file d’attente, [**CloseSpoolFileHandle**](closespoolfilehandle.md) doit être appelé pour le handle de fichier retourné par le dernier appel à **CommitSpoolData**.

Avant d’appeler **CommitSpoolData**, les applications doivent définir le pointeur de fichier à la position qu’il avait avant d’écrire des données dans le fichier. Dans le processus de rendu des données dans le fichier du spouleur, le spouleur d’impression déplace le pointeur de fichier spool *cbCommit* octets de la valeur actuelle du pointeur de fichier.

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

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 

