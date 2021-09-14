---
description: La fonction SetJob suspend, reprend, annule ou redémarre un travail d’impression sur une imprimante spécifiée. Vous pouvez également utiliser la fonction SetJob pour définir les paramètres du travail d’impression, tels que la priorité du travail d’impression et le nom du document.
ms.assetid: 21947c69-c517-4962-8eb7-b45ed4211d9a
title: SetJob, fonction (WinSpool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetJob
- SetJobA
- SetJobW
api_type:
- DllExport
api_location:
- WinSpool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 34dfc8c0239a10d7e7f036beed457d57329f4c67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231623"
---
# <a name="setjob-function"></a>SetJob fonction)

La fonction **SetJob** suspend, reprend, annule ou redémarre un travail d’impression sur une imprimante spécifiée. Vous pouvez également utiliser la fonction **SetJob** pour définir les paramètres du travail d’impression, tels que la priorité du travail d’impression et le nom du document.

Vous pouvez utiliser la fonction **SetJob** pour fournir une commande à un travail d’impression ou pour définir des paramètres de travail d’impression, ou pour effectuer les deux dans le même appel. La valeur du paramètre de *commande* n’affecte pas la manière dont la fonction utilise les paramètres *Level* et *pJob* . En outre, vous pouvez utiliser **SetJob** avec les [**informations de travail \_ \_ 3**](job-info-3.md) pour lier ensemble un ensemble de travaux d’impression. Pour plus d'informations, consultez la section Notes.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  JobId,
  _In_ DWORD  Level,
  _In_ LPBYTE pJob,
  _In_ DWORD  Command
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’objet Printer qui vous intéresse. Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*JobID* \[ dans\]
</dt> <dd>

Identificateur qui spécifie le travail d’impression. Vous obtenez un identificateur de travail d’impression en appelant la fonction [**AddJob**](addjob.md) ou la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) .

Si le paramètre *Level* a la valeur 3, le paramètre *JobID* doit correspondre au membre **JobID** de la structure [**Job \_ info \_ 3**](job-info-3.md) pointé par *pJob*

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type de structure d’informations de travail vers lequel pointe le paramètre *pJob* .

**toutes les versions de Windows**: vous pouvez définir le paramètre de *niveau* sur 0, 1 ou 2. Lorsque vous définissez *Level* sur 0, *pJob* doit avoir la **valeur null**. Utilisez ces valeurs lorsque vous ne définissez pas de paramètres de travail d’impression.

Vous pouvez également définir le paramètre de *niveau* sur 3.

à compter de **Windows Vista**: vous pouvez également définir le paramètre de *niveau* sur 4.

</dd> <dt>

*pJob* \[ dans\]
</dt> <dd>

Pointeur vers une structure qui définit les paramètres du travail d’impression.

**toutes les versions de Windows**: *pJob* peut pointer vers une structure [**job information \_ \_ 1**](job-info-1.md) ou [**job \_ info \_ 2**](job-info-2.md) .

*pJob* peut également pointer vers une structure d' [**informations de travail \_ \_ 3**](job-info-3.md) . Vous devez disposer de l’autorisation **\_ \_ administrer** l’accès au travail pour les travaux spécifiés par les membres **JobID** et **NextJobId** de la structure **Job \_ info \_ 3** .

à compter de **Windows Vista**: *pJob* peut également pointer vers une structure d' [**informations de travail \_ \_ 4**](job-info-4.md) .

Si le paramètre *Level* est égal à 0, *pJob* doit avoir la **valeur null**.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Opération de travail d’impression à effectuer. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                            | Signification                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="JOB_CONTROL_CANCEL"></span><span id="job_control_cancel"></span><dl> <dt>**\_annulation du contrôle de travail \_**</dt> </dl>                                    | Ne pas utiliser. Pour supprimer un travail d’impression, utilisez l' **opération de \_ \_ Suppression de contrôle de tâche**.<br/>        |
| <span id="JOB_CONTROL_PAUSE"></span><span id="job_control_pause"></span><dl> <dt>**\_pause du contrôle de travail \_**</dt> </dl>                                       | Suspendez le travail d’impression.<br/>                                                    |
| <span id="JOB_CONTROL_RESTART"></span><span id="job_control_restart"></span><dl> <dt>**redémarrage du contrôle de travail \_ \_**</dt> </dl>                                 | Redémarrez le travail d’impression. Un travail ne peut être redémarré que s’il a été imprimé.<br/>  |
| <span id="JOB_CONTROL_RESUME"></span><span id="job_control_resume"></span><dl> <dt>**\_reprise du contrôle de travail \_**</dt> </dl>                                    | Reprendre un travail d’impression suspendu.<br/>                                              |
| <span id="JOB_CONTROL_DELETE"></span><span id="job_control_delete"></span><dl> <dt>**\_suppression du contrôle de travail \_**</dt> </dl>                                    | Supprimez le travail d’impression.<br/>                                                   |
| <span id="JOB_CONTROL_SENT_TO_PRINTER"></span><span id="job_control_sent_to_printer"></span><dl> <dt>**\_contrôle \_ de travail envoyé à l' \_ \_ imprimante**</dt> </dl>       | Utilisé par les moniteurs de port pour mettre fin au travail d’impression.<br/>                             |
| <span id="JOB_CONTROL_LAST_PAGE_EJECTED"></span><span id="job_control_last_page_ejected"></span><dl> <dt>**\_dernière page du contrôle des travaux \_ \_ \_ éjectée**</dt> </dl> | Utilisé par les moniteurs de langage pour mettre fin au travail d’impression.<br/>                         |
| <span id="JOB_CONTROL_RETAIN"></span><span id="job_control_retain"></span><dl> <dt>**\_conservation du contrôle de travail \_**</dt> </dl>                                    | **Windows Vista et versions ultérieures**: conservez le travail dans la file d’attente après son impression.<br/> |
| <span id="JOB_CONTROL_RELEASE"></span><span id="job_control_release"></span><dl> <dt>**\_version de contrôle du travail \_**</dt> </dl>                                 | **Windows Vista et versions ultérieures**: libérez le travail d’impression.<br/>                     |



 

Vous pouvez utiliser le même appel à la fonction **SetJob** pour définir les paramètres du travail d’impression et fournir une commande à un travail d’impression. Par conséquent, la *commande* ne doit pas avoir la valeur 0 si vous définissez des paramètres de travail d’impression, bien que cela puisse être le cas.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Vous pouvez utiliser la fonction **SetJob** pour définir différents paramètres de travail d’impression en fournissant un pointeur vers une structure [**Job information \_ \_ 1**](job-info-1.md), Job info [**\_ \_ 2**](job-info-2.md), [**Job \_ info \_ 3**](job-info-3.md)ou [**Job \_ info \_ 4**](job-info-4.md) qui contient les données nécessaires.

Pour supprimer ou supprimer tous les travaux d’impression pour une imprimante spécifique, appelez la fonction [**SetPrinter**](setprinter.md) avec son paramètre de *commande* défini **sur \_ \_ vidage du contrôle** de l’imprimante.

Les membres suivants d’une structure [**Job information \_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)ou [**Job \_ info \_ 4**](job-info-4.md) sont ignorés lors d’un appel à **SetJob**: **JobID**, **pPrinterName**, **pMachineName**, **pUserName**, **pDrivername**, **Size**, **sent**, **Time** et **TotalPages**.

Vous devez disposer de l’autorisation **\_ \_ administrer** l’accès à l’imprimante pour une imprimante afin de modifier la position d’un travail d’impression dans la file d’attente à l’impression.

Si vous ne souhaitez pas définir la position d’un travail d’impression dans la file d’attente à l’impression, vous devez définir le membre **position** de la structure Job information [**\_ \_ 1**](job-info-1.md), [**Job \_ info \_ 2**](job-info-2.md)ou [**Job \_ info \_ 4**](job-info-4.md) sur **Job \_ position \_ Unspecified**.

Utilisez la fonction **SetJob** avec la structure [**Job \_ info \_ 3**](job-info-3.md) pour lier ensemble un ensemble de travaux d’impression (également appelé chaîne). Cela est utile dans les situations où un document unique est constitué de plusieurs parties que vous souhaitez restituer séparément. Pour imprimer les travaux A, B, C et D dans l’ordre, appelez **SetJob** avec les [**informations de travail \_ \_ 4**](job-info-4.md) pour lier A à b, b à c et c à D.

Si vous liez des travaux d’impression, notez les points suivants :

-   Les travaux peuvent être ajoutés au début ou à la fin d’une chaîne.
-   Tous les travaux de la chaîne doivent avoir le même type de données.
-   La chaîne doit être entièrement liée avant le début de la mise en file d’attente ; sinon, le spouleur peut imprimer et supprimer les travaux mis en attente avant de les lier tous. Il existe deux façons de garder la chaîne imprime prématurément :

    -   Suspendez la première tâche de la chaîne jusqu’à ce que la chaîne soit entièrement liée. L’état suspendu de la première tâche régit l’état de tous les travaux de la chaîne.
    -   Conservez la première tâche incomplète, autrement dit, n’appelez pas [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) ou [**ScheduleJob**](schedulejob.md) pour le premier travail. Toutefois, si l’option « imprimer pendant la mise en file d’attente » est activée (valeur par défaut), cette méthode bloque le port pendant la génération de la chaîne, ce qui empêche également l’impression des travaux non liés.

-   L’application doit gérer le cas où l’utilisateur supprime un travail dans la chaîne avant la fin de l’impression de la chaîne. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne **un \_ paramètre non valide** lorsqu’un JobID n’existe pas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>WinSpool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WinSpool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **SetJobW** (Unicode) et **SetJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**\_Informations sur le travail \_ 1**](job-info-1.md)
</dt> <dt>

[**\_Informations sur le travail \_ 2**](job-info-2.md)
</dt> <dt>

[**\_Informations sur le travail \_ 3**](job-info-3.md)
</dt> <dt>

[**\_Informations sur le travail \_ 4**](job-info-4.md)
</dt> </dl>

 

