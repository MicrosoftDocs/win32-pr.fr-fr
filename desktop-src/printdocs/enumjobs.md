---
description: La fonction EnumJobs récupère des informations sur un ensemble spécifié de travaux d’impression pour une imprimante spécifiée.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Fonction EnumJobs (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412824"
---
# <a name="enumjobs-function"></a>EnumJobs, fonction

La fonction **EnumJobs** récupère des informations sur un ensemble spécifié de travaux d’impression pour une imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’objet Printer dont les tâches d’impression sont énumérées par la fonction. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*FirstJob* \[ dans\]
</dt> <dd>

Position de base zéro dans la file d’attente à l’impression du premier travail d’impression à énumérer. Par exemple, la valeur 0 spécifie que l’énumération doit commencer au premier travail d’impression dans la file d’attente à l’impression ; la valeur 9 spécifie que l’énumération doit commencer au dixième travail d’impression dans la file d’attente à l’impression.

</dd> <dt>

*Nojobs* \[ dans\]
</dt> <dd>

Nombre total de travaux d’impression à énumérer.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type d’informations retournées dans la mémoire tampon *pJob* .



| Valeur                                                                                                | Signification                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* reçoit un tableau de structures [**Job \_ info \_ 1**](job-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* reçoit un tableau de structures [**Job \_ info \_ 2**](job-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* reçoit un tableau de structures [**Job \_ info \_ 3**](job-info-3.md)<br/> |



 

</dd> <dt>

*pJob* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau d' [**informations sur le travail \_ \_ 1**](job-info-1.md), des [**\_ informations sur le travail \_ 2**](job-info-2.md)ou des structures [**Job \_ info \_ 3**](job-info-3.md) . La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures et toutes les chaînes ou autres données auxquelles les membres de la structure pointent.

Pour déterminer la taille de mémoire tampon requise, appelez **EnumJobs** avec *cbBuf* défini à zéro. Échec de **EnumJobs** , [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur \_ \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon *pJob* .

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets copiés si la fonction est réussie. Si la fonction échoue, la variable reçoit le nombre d’octets requis.

</dd> <dt>

*pcReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d' [**\_ informations sur le travail \_ 1**](job-info-1.md), les [**\_ informations sur le travail \_ 2**](job-info-2.md)ou les structures d' [**informations de travail \_ \_ 3**](job-info-3.md) retournées dans la mémoire tampon *pJob* .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La [**structure \_ informations \_ sur le travail 1**](job-info-1.md) contient des informations générales sur le travail d’impression ; la structure des informations de [**travail \_ \_ 2**](job-info-2.md) présente des informations bien plus détaillées. La structure [**Job \_ info \_ 3**](job-info-3.md) contient des informations sur la façon dont les tâches sont liées.

Pour déterminer le nombre de travaux d’impression dans la file d’attente de l’imprimante, appelez la fonction [**GetPrinter**](getprinter.md) avec le paramètre de *niveau* défini sur 2.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **EnumJobsW** (Unicode) et **EnumJobsA** (ANSI)<br/>                                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Informations sur le travail \_ 1**](job-info-1.md)
</dt> <dt>

[**\_Informations sur le travail \_ 2**](job-info-2.md)
</dt> <dt>

[**\_Informations sur le travail \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

