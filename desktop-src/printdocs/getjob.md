---
description: La fonction GetJob récupère des informations sur un travail d’impression spécifié.
ms.assetid: 57e59f84-d2a0-4722-b0fc-6673f7bb5c57
title: GetJob, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetJob
- GetJobA
- GetJobW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 26665d6141ea36adbe8aeeca0555bc6a5e918cb5213a4fb7a6dbd315eac92a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949080"
---
# <a name="getjob-function"></a>GetJob fonction)

La fonction **GetJob** récupère des informations sur un travail d’impression spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   JobId,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle les données du travail d’impression sont récupérées. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*JobID* \[ dans\]
</dt> <dd>

Identifie le travail d’impression dont les données doivent être récupérées. Utilisez la fonction [**AddJob**](addjob.md) ou la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) pour obtenir un identificateur de travail d’impression.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type d’informations retournées dans la mémoire tampon *pJob* . Si le *niveau* est 1, *pJob* reçoit une structure [**\_ informations sur le travail \_ 1**](job-info-1.md) . Si le *niveau* est 2, *pJob* reçoit une structure d' [**informations de travail \_ \_ 2**](job-info-2.md) .

</dd> <dt>

*pJob* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un [**Job \_ information \_ 1**](job-info-1.md) ou une structure [**Job \_ information \_ 2**](job-info-2.md) contenant des informations sur le travail. La mémoire tampon doit être suffisamment grande pour stocker les chaînes pointées par les membres de la structure.

Pour déterminer la taille de mémoire tampon requise, appelez **GetJob** avec *cbBuf* défini à zéro. **GetJob** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui spécifie le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **GetJobW** (Unicode) et **GetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**\_Informations sur le travail \_ 1**](job-info-1.md)
</dt> <dt>

[**\_Informations sur le travail \_ 2**](job-info-2.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

