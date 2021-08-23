---
description: La fonction AddPrinter ajoute une imprimante à la liste des imprimantes prises en charge pour un serveur spécifié.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: AddPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6034c330da19f5982e9bbacbf75cc16f0a7d10dd65f9c8bded2efa5cbda70835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601139"
---
# <a name="addprinter-function"></a>AddPrinter fonction)

La fonction **AddPrinter** ajoute une imprimante à la liste des imprimantes prises en charge pour un serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel l’imprimante doit être installée. Si cette chaîne est **null**, l’imprimante est installée localement.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle *pPrinter* pointe. Cette valeur doit être 2.

</dd> <dt>

*pPrinter* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ informations \_ d’imprimante 2**](printer-info-2.md) qui contient des informations sur l’imprimante. Vous devez spécifier des valeurs **non null** pour les membres **pPrinterName**, **pPortName**, **pDriverName** et **pPrintProcessor** de cette structure avant d’appeler **AddPrinter**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est un handle (pas thread-safe) vers un nouvel objet Printer. Lorsque vous avez terminé avec le descripteur, transmettez-le à la fonction [**ClosePrinter**](closeprinter.md) pour le fermer.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Remarques

N’appelez pas cette méthode dans [**DllMain**](/windows/desktop/Dlls/dllmain).

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Le handle retourné n’est pas thread-safe. Si les appelants doivent l’utiliser simultanément sur plusieurs threads, ils doivent fournir un accès de synchronisation personnalisé au handle d’imprimante à l’aide des [fonctions de synchronisation](/windows/desktop/Sync/synchronization-functions). Pour éviter d’écrire du code personnalisé, l’application peut ouvrir un handle d’imprimante sur chaque thread, si nécessaire.

Voici les membres de la structure [**Printer \_ info \_ 2**](printer-info-2.md) qui peuvent être définis avant l’appel de la fonction **AddPrinter** :

-   **Attributs**
-   **pPrintProcessor**
-   **DefaultPriority**
-   **Priorité**
-   **pComment**
-   **pSecurityDescriptor**
-   **pDatatype**
-   **pSepFile**
-   **pDevMode**
-   **pShareName**
-   **pLocation**
-   **StartTime**
-   **pParameters**
-   **UntilTime**

Les membres **Status**, **cJobs** et **AveragePPM** de la structure [**Printer \_ info \_ 2**](printer-info-2.md) sont réservés pour une utilisation par la fonction [**GetPrinter**](getprinter.md) . Ils ne doivent pas être définis avant d’appeler **AddPrinter**.

Si **pSecurityDescriptor** a la **valeur null**, le système affecte un descripteur de sécurité par défaut à l’imprimante. Le descripteur de sécurité par défaut dispose des autorisations suivantes.



| Valeur                          | Description                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administrateurs et utilisateurs avec pouvoir | Contrôle total sur la file d’attente à l’impression. Cela signifie que les membres de ces groupes peuvent imprimer, gérer la file d’attente (peut supprimer la file d’attente, modifier les paramètres de la file d’attente, y compris le descripteur de sécurité) et gérer les travaux d’impression de tous les utilisateurs (supprimer, suspendre, reprendre, redémarrer les travaux). notez que les utilisateurs avec pouvoir n’existent pas avant Windows XP Professional.<br/> |
| Propriétaire créateur                  | Peut gérer ses propres travaux. Cela signifie que les utilisateurs qui envoient des travaux peuvent gérer (supprimer, suspendre, reprendre, redémarrer) leurs propres travaux.                                                                                                                                                                                                                                  |
| Tout le monde                       | Exécution et contrôle de lecture standard. Cela signifie que les membres du groupe tout le monde peuvent imprimer et lire les propriétés de la file d’attente à l’impression.                                                                                                                                                                                                                     |



 

Une fois qu’une application a créé un objet Printer avec la fonction **AddPrinter** , elle doit utiliser la fonction [**PrinterProperties**](printerproperties.md) pour spécifier les paramètres corrects pour le pilote d’imprimante associé à l’objet Printer.

La fonction **AddPrinter** renvoie une erreur si un objet Printer portant le même nom existe déjà, sauf si cet objet est marqué comme étant en attente de suppression. Dans ce cas, l’imprimante existante n’est pas supprimée et les paramètres de création de **AddPrinter** sont utilisés pour modifier les paramètres d’imprimante existants (comme si l’application avait utilisé la fonction [**SetPrinter**](setprinter.md) ).

Utilisez la fonction [**EnumPrintProcessors**](enumprintprocessors.md) pour énumérer l’ensemble des processeurs d’impression installés sur un serveur. Utilisez la fonction [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) pour énumérer l’ensemble des types de données pris en charge par un processeur d’impression. Utilisez la fonction [**EnumPorts**](enumports.md) pour énumérer l’ensemble des ports disponibles. Utilisez la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) pour énumérer les pilotes d’imprimante installés.

L’appelant de la fonction **AddPrinter** doit disposer d’un accès serveur \_ \_ administrer l’accès au serveur sur lequel l’imprimante doit être créée. Le descripteur retourné par la fonction disposera de l' \_ autorisation d’accès imprimante All \_ et pourra être utilisé pour effectuer des opérations administratives sur l’imprimante.

Si la fonction **DrvPrinterEvent** est passée à l' \_ indicateur \_ d’événement d’imprimante \_ no \_ UI, le pilote ne doit pas utiliser d’appel d’interface utilisateur pendant **DrvPrinterEvent**. Pour effectuer des tâches liées à l’interface utilisateur, le programme d’installation doit utiliser l’entrée **VendorSetup** dans le fichier. inf de l’imprimante ou, pour plug-and-Play appareils, le programme d’installation peut utiliser un co-programme d’installation spécifique à l’appareil. pour plus d’informations sur **VendorSetup**, consultez le kit de développement de pilotes (DDK) Microsoft Windows.

Le pare-feu de connexion Internet (ICF) bloque les ports d’imprimante par défaut, mais une exception pour le partage de fichiers et d’imprimantes est activée lorsque vous exécutez **AddPrinter**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddPrinterW** (Unicode) et **AddPrinterA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> <dt>

[**PrinterProperties**](printerproperties.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> </dl>

 

