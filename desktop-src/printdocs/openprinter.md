---
description: La fonction OpenPrinter récupère un handle vers l’imprimante ou le serveur d’impression spécifié ou d’autres types de handles dans le sous-système d’impression.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: OpenPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531981"
---
# <a name="openprinter-function"></a>OpenPrinter fonction)

La fonction **OpenPrinter** récupère un handle vers l’imprimante ou le serveur d’impression spécifié ou d’autres types de handles dans le sous-système d’impression.

## <a name="syntax"></a>Syntaxe


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPrinterName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante ou du serveur d’impression, de l’objet Printer, du XcvMonitor ou du XcvPort.

Pour un objet Printer, utilisez : nom_imprimante, Job xxxx. Pour un XcvMonitor, utilisez : ServerName, XcvMonitor Nomdumoniteur. Pour un XcvPort, utilisez : ServerName, XcvPort PortName.

Si la **valeur est null**, le serveur d’impression local est activé.

</dd> <dt>

*phPrinter* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un handle (non thread-safe) vers l’imprimante ou l’objet serveur d’impression ouvert.

Le paramètre *phPrinter* peut retourner un handle XCV à utiliser avec la fonction XcvData. Pour plus d’informations sur XcvData, consultez le DDK.

</dd> <dt>

*pDefault* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**imprimante \_ par défaut**](printer-defaults.md) . Cette valeur peut être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Un handle obtenu pour une imprimante distante par un appel à **OpenPrinter** pour une imprimante distante accède à l’imprimante via un cache local dans le service spouleur d’impression. Ce cache n’est pas précis en temps réel. Pour obtenir des données précises, remplacez l’appel de OpenPrinter par [**OpenPrinter2**](openprinter2.md) par POptions. dwFlags défini sur Printer \_ option \_ no \_ cache. Notez que seul OpenPrinter2W est fonctionnel. La fonction retourne un handle d’imprimante qui utilise d’autres appels d’API d’impression et contourne le cache local. Cette méthode bloque tout en attendant la communication réseau avec l’imprimante distante, il est donc possible qu’elle ne soit pas renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut rendre l’application sans réponse.

 

> [!Note]  
> Un handle obtenu par un appel à **OpenPrinter** pour une imprimante distante accède à l’imprimante via un cache local dans le service spouleur d’impression. Ce cache est, de par sa conception, non précis en temps réel. Si vous devez obtenir des données précises, remplacez l’appel de **OpenPrinter** par [**OpenPrinter2**](openprinter2.md) par *POptions. dwFlags* défini [**sur \_ Printer option \_ no \_ cache**](printer-options.md). Notez que seul **OpenPrinter2W** est fonctionnel. En procédant ainsi, la fonction retourne un handle d’imprimante qui effectue d’autres appels d’API d’impression pour contourner le cache local. Notez que cette approche sera bloquée en attendant la communication réseau aller-retour à l’imprimante distante, de sorte qu’elle risque de ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et l’implémentation du pilote d’imprimante, facteurs difficiles à prédire lors de l’écriture d’une application. Par conséquent, l’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Le handle pointé par *phPrinter* n’est pas thread-safe. Si les appelants doivent l’utiliser simultanément sur plusieurs threads, ils doivent fournir un accès de synchronisation personnalisé au handle d’imprimante à l’aide des [fonctions de synchronisation](/windows/desktop/Sync/synchronization-functions). Pour éviter d’écrire du code personnalisé, l’application peut ouvrir un handle d’imprimante sur chaque thread, si nécessaire.

Le paramètre *pDefault* vous permet de spécifier les valeurs du type de données et du mode de l’appareil utilisées pour l’impression des documents soumis par la fonction [**StartDocPrinter**](startdocprinter.md) . Toutefois, vous pouvez remplacer ces valeurs à l’aide de la fonction [**SetJob**](setjob.md) après le démarrage d’un document.

Les paramètres [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) définis dans la [**structure \_ par défaut**](printer-defaults.md) de l’imprimante du paramètre *pDefault* ne sont pas utilisés lorsque la valeur du membre *pDatatype* de la structure [**\_ infos doc \_ 1**](doc-info-1.md) qui a été transmise dans le paramètre *pDocInfo* de l’appel [**StartDocPrinter**](startdocprinter.md) est « RAW ». Lorsqu’un document de niveau supérieur (par exemple, un fichier Adobe PDF ou Microsoft Word) ou d’autres données d’imprimante (par exemple, PCL, PS ou HPGL) est envoyé directement à une imprimante avec *pDatatype* défini sur « RAW », le document doit décrire entièrement les paramètres du travail d’impression de style **DEVMODE** dans la langue comprise par le matériel.

Vous pouvez appeler la fonction **OpenPrinter** pour ouvrir un handle sur un serveur d’impression ou pour déterminer les droits d’accès d’un client à un serveur d’impression. Pour ce faire, spécifiez le nom du serveur d’impression dans le paramètre *pPrinterName* , définissez les membres **pDatatype** et **pDevMode** de la structure [**\_ par défaut**](printer-defaults.md) de l’imprimante sur la valeur **null**, puis définissez le membre **desiredAccess** de manière à spécifier une valeur de masque d’accès au serveur, par exemple \_ tous les \_ accès serveur. Lorsque vous avez terminé avec le descripteur, transmettez-le à la fonction [**ClosePrinter**](closeprinter.md) pour le fermer.

Utilisez le membre **desiredAccess** de la [**structure \_ par défaut**](printer-defaults.md) de l’imprimante pour spécifier les droits d’accès dont vous avez besoin pour l’imprimante. Les droits d’accès peuvent être l’un des suivants : (Si *pDefault* a la **valeur null**, les droits d’accès sont Printer \_ utilisation de l’accès \_ .)



| Valeur d’accès souhaitée                        | Signification                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_administration de l’accès aux imprimantes \_                 | Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md).                                                                                                 |
| \_utilisation de l’accès à l’imprimante \_                        | Pour effectuer des opérations d’impression de base.                                                                                                                                                        |
| \_tout \_ accès imprimante                        | Pour effectuer toutes les tâches d’administration et les opérations d’impression de base, à l’exception de la synchronisation (consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).                                     |
| \_gestion de l’accès à l’imprimante \_ \_ limitée            | Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md) et [**SetPrinterData**](setprinterdata.md). Cette valeur est disponible à partir de Windows 8.1. |
| valeurs de sécurité génériques, telles que WRITE \_ DAC | Pour autoriser des droits d’accès de contrôle spécifiques. Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Si un utilisateur n’est pas autorisé à ouvrir l’imprimante ou le serveur d’impression spécifié avec l’accès souhaité, l’appel **OpenPrinter** échoue avec une valeur de retour égale à zéro et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne la valeur erreur \_ accès \_ refusé.

## <a name="examples"></a>Exemples

Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **OpenPrinterW** (Unicode) et **OpenPrinterA** (ANSI)<br/>                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**\_valeurs par défaut de l’imprimante**](printer-defaults.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> </dl>

 

