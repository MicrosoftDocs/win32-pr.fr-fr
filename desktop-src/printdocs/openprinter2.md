---
description: Récupère un handle vers l’imprimante, le serveur d’impression ou d’autres types de handles spécifiés dans le sous-système d’impression, tout en définissant certaines options d’imprimante.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: OpenPrinter2, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 132e7225850899cb33ff815c2fce309fd70a9d288839da2bbf20a6e9f8aafc50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776499"
---
# <a name="openprinter2-function"></a>OpenPrinter2 fonction)

Récupère un handle vers l’imprimante, le serveur d’impression ou d’autres types de handles spécifiés dans le sous-système d’impression, tout en définissant certaines options d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPrinterName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante se terminant par un caractère null qui spécifie le nom de l’imprimante ou du serveur d’impression, l’objet Printer, XcvMonitor ou XcvPort.

Pour un objet Printer, utilisez : nom_imprimante, Job xxxx. Pour un XcvMonitor, utilisez : ServerName, XcvMonitor Nomdumoniteur. Pour un XcvPort, utilisez : ServerName, XcvPort PortName.

**Windows Vista :** Si la **valeur est null**, le serveur d’impression local est activé.

</dd> <dt>

*phPrinter* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un handle vers l’imprimante ouverte ou l’objet serveur d’impression.

</dd> <dt>

*pDefault* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**imprimante \_ par défaut**](printer-defaults.md) . Cette valeur peut être **null**.

</dd> <dt>

*pOptions* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ options d’imprimante**](printer-options.md) . Cette valeur peut être **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La version ANSI de cette fonction n’est pas implémentée et retourne une erreur \_ non \_ prise en charge.

Le paramètre *pDefault* vous permet de spécifier les valeurs du type de données et du mode de l’appareil utilisées pour l’impression des documents soumis par la fonction [**StartDocPrinter**](startdocprinter.md) . Toutefois, vous pouvez remplacer ces valeurs à l’aide de la fonction [**SetJob**](setjob.md) après le démarrage d’un document.

Vous pouvez appeler la fonction **OpenPrinter2** pour ouvrir un handle sur un serveur d’impression ou pour déterminer les droits d’accès client à un serveur d’impression. Pour ce faire, spécifiez le nom du serveur d’impression dans le paramètre *pPrinterName* , définissez les membres **pDatatype** et **pDevMode** de la structure [**\_ par défaut**](printer-defaults.md) de l’imprimante sur la valeur **null**, puis définissez le membre **desiredAccess** de manière à spécifier une valeur de masque d’accès au serveur, par exemple \_ tous les \_ accès serveur. Lorsque vous avez terminé avec le descripteur, transmettez-le à la fonction [**ClosePrinter**](closeprinter.md) pour le fermer.

Utilisez le membre **desiredAccess** de la [**structure \_ par défaut**](printer-defaults.md) de l’imprimante pour spécifier les droits d’accès nécessaires. Les droits d’accès peuvent être l’un des suivants :



| Valeur d’accès souhaitée                        | Signification                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_administration de l’accès aux imprimantes \_                 | Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md).                                                                                                 |
| \_utilisation de l’accès à l’imprimante \_                        | Pour effectuer des opérations d’impression de base.                                                                                                                                                        |
| \_tout \_ accès imprimante                        | Pour effectuer toutes les tâches d’administration et les opérations d’impression de base, à l’exception de SYNCHRONISEr. Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).                                         |
| \_gestion de l’accès à l’imprimante \_ \_ limitée            | Pour effectuer des tâches d’administration, telles que celles fournies par [**SetPrinter**](setprinter.md) et [**SetPrinterData**](setprinterdata.md). Cette valeur est disponible à partir de Windows 8.1. |
| valeurs de sécurité génériques, telles que WRITE \_ DAC | Pour autoriser des droits d’accès de contrôle spécifiques. Consultez [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights).                                                                                      |



 

Si un utilisateur n’a pas l’autorisation d’ouvrir une imprimante ou un serveur d’impression spécifié avec l’accès souhaité, l’appel **OpenPrinter2** échoue et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne la valeur erreur \_ accès \_ refusé.

Quand *pPrinterName* est une imprimante locale, **OpenPrinter2** ignore toutes les valeurs de l' **dwFlags** que la structure des [**\_ options**](printer-options.md) de l’imprimante a référencées à l’aide de *pOptions*, à l’exception de l’option Printer \_ modification du \_ client \_ . Si ce dernier est passé, **OpenPrinter2** retourne l’erreur \_ accès \_ refusé. En conséquence, lors de l’ouverture d’une imprimante locale, **OpenPrinter2** n’offre aucun avantage sur [**OpenPrinter**](openprinter.md).

**Windows Vista :** Les données d’imprimante retournées par **OpenPrinter2** sont extraites d’un cache local, sauf si l' **option d’imprimante aucun indicateur de \_ \_ \_ cache** n’est définie dans le champ **dwFlags** de la structure d' [**\_ options d’imprimante**](printer-options.md) référencée par *pOptions*.

## <a name="examples"></a>Exemples

Dans cet exemple, **OpenPrinter2** échoue lorsque la \_ gestion de l’accès à \_ \_ l’imprimante limitée est transmise à la structure [**\_ par défaut**](printer-defaults.md) de l’imprimante et que l’utilisateur ne dispose pas de l’autorisation appropriée.


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



Pour obtenir un exemple de programme qui montre comment utiliser cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **OpenPrinter2W** (Unicode) et **OpenPrinter2A** (ANSI)<br/>                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**\_valeurs par défaut de l’imprimante**](printer-defaults.md)
</dt> <dt>

[**OPTIONS de l’imprimante \_**](printer-options.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

