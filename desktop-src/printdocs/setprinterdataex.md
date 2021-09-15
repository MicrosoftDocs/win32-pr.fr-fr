---
description: La fonction SetPrinterDataEx définit les données de configuration d’une imprimante ou d’un serveur d’impression. La fonction stocke les données de configuration sous la clé de Registre Printers.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: SetPrinterDataEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525509"
---
# <a name="setprinterdataex-function"></a>SetPrinterDataEx fonction)

La fonction **SetPrinterDataEx** définit les données de configuration d’une imprimante ou d’un serveur d’impression. La fonction stocke les données de configuration sous la clé de registre de l’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante ou le serveur d’impression pour lequel la fonction définit les données de configuration. Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pKeyName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant la valeur à définir. Si la clé ou les sous-clés spécifiées n’existent pas, la fonction les crée.

Pour stocker les données de configuration qui peuvent être publiées dans le service d’annuaire (DS), spécifiez l’une des clés de Registre prédéfinies suivantes.



| Valeur                                                                                                                                                                      | Signification                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <dt>**SPLDS_DRIVER_KEY**</dt> </dl>    | Pilotes d’imprimante Utilisez cette clé pour stocker les propriétés du pilote.<br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <dt>**SPLDS_SPOOLER_KEY**</dt> </dl> | Réservé. Utilisé uniquement par le spouleur d’impression pour stocker les propriétés internes du spouleur.<br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <dt>**SPLDS_USER_KEY**</dt> </dl>          | Les applications utilisent cette clé pour stocker des propriétés d’imprimante telles que des numéros de ressources d’imprimante.<br/> |



 

Les valeurs stockées sous la clé de SPLDS_USER_KEY sont publiées dans le service d’annuaire uniquement s’il existe une propriété correspondante dans le schéma. Un administrateur de domaine doit créer la propriété si elle n’existe pas déjà. Pour publier une propriété définie par l’utilisateur après avoir utilisé **SetPrinterDataEx** pour ajouter ou modifier une valeur, appelez [**SetPrinter**](setprinter.md) avec *Level* = 7 et avec le membre **dwAction** de [**PRINTER_INFO_7**](printer-info-7.md) défini sur **DSPRINT_UPDATE**.

Vous pouvez spécifier d’autres clés pour stocker des données de configuration non-DS. Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès qui a une ou plusieurs sous-clés.

Si *hPrinter* est un handle d’imprimante et que *PKeyName* a la **valeur null** ou est une chaîne vide, **SetPrinterDataEx** retourne **ERROR_INVALID_PARAMETER**.

Si *hPrinter* est un handle vers un serveur d’impression, *pKeyName* est ignoré.

N’utilisez pas **SPLDS_SPOOLER_KEY**. Pour modifier les propriétés de l’imprimante du spouleur, utilisez [**SetPrinter**](setprinter.md) avec *Level* = 2.

</dd> <dt>

*pValueName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null qui identifie les données à définir.

Pour les imprimantes, cette chaîne spécifie le nom d’une valeur sous la clé *pKeyName* .

Pour les serveurs d’impression, cette chaîne est l’une des chaînes prédéfinies énumérées dans la section Notes suivante.

</dd> <dt>

*Type* \[ dans\]
</dt> <dd>

Code indiquant le type de données vers lequel pointe le paramètre *pData* . Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types).

Si *pKeyName* spécifie l’une des clés de service d’annuaire prédéfinies, le *Type* doit être **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** ou **REG_BINARY**. Si **REG_BINARY** est utilisé, *cbData* doit être égal à 1 et le service d’annuaire traite les données comme une valeur booléenne.

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient les données de configuration de l’imprimante.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est **ERROR_SUCCESS**.

Si la fonction échoue, la valeur de retour est une valeur d’erreur.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Pour récupérer les données de configuration existantes d’une imprimante ou d’un spouleur d’impression, appelez la fonction [**GetPrinterDataEx**](getprinterdataex.md) .

L’appel de **SetPrinterDataEx** avec le paramètre *pKeyName* défini sur « PrinterDriverData » équivaut à appeler la fonction [**SetPrinterData**](setprinterdata.md) .

Si *hPrinter* est un handle vers un serveur d’impression, *pValueName* peut spécifier l’une des valeurs prédéfinies suivantes.



| Valeur                                                               | Commentaires                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_ALLOW_USER_MANAGEFORMS**                                | Windows XP avec Service Pack 2 (SP2) et versions ultérieures<br/> Windows Serveur 2003 avec Service Pack 1 (SP1) et versions ultérieures<br/>                                                                                                    |
| **SPLREG_BEEP_ENABLED**                                           |                                                                                                                                                                                                                                 |
| **SPLREG_DEFAULT_SPOOL_DIRECTORY**                               |                                                                                                                                                                                                                                 |
| **SPLREG_EVENT_LOG**                                              |                                                                                                                                                                                                                                 |
| **SPLREG_NET_POPUP**                                              | non pris en charge dans Windows Server 2003 et versions ultérieures<br/>                                                                                                                                                                       |
| **SPLREG_PORT_THREAD_PRIORITY_DEFAULT**                         |                                                                                                                                                                                                                                 |
| **SPLREG_PORT_THREAD_PRIORITY**                                  |                                                                                                                                                                                                                                 |
| **SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**                        | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**         | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE** | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**                 | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**             | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**              | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **SPLREG_RETRY_POPUP**                                            | En cas de retour réussi, *pData* contient 1 si le serveur est configuré pour réessayer les fenêtres contextuelles pour tous les travaux, ou 0 si le serveur ne réessaye pas les fenêtres publicitaires pour tous les travaux.<br/> non pris en charge dans Windows Server 2003 et versions ultérieures<br/> |
| **SPLREG_SCHEDULER_THREAD_PRIORITY**                             |                                                                                                                                                                                                                                 |
| **SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**                    |                                                                                                                                                                                                                                 |
| **SPLREG_WEBSHAREMGMT**                                            | Windows Serveur 2003 et versions ultérieures<br/>                                                                                                                                                                                        |



 

Le passage de l’une des valeurs prédéfinies suivantes comme *pValueName* définit le comportement d’impression du pool lorsqu’une erreur se produit.



| Valeur                                       | Commentaires                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG_RESTART_JOB_ON_POOL_ERROR**   | La valeur de *pData* indique la durée, en secondes, à laquelle un travail est redémarré sur un autre port après qu’une erreur s’est produite. Ce paramètre est utilisé avec **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.<br/> |
| **SPLREG_RESTART_JOB_ON_POOL_ENABLED** | Une valeur différente de zéro dans *pData* indique que **SPLREG_RESTART_JOB_ON_POOL_ERROR** est activé.<br/>                                                                                            |



 

L’heure spécifiée dans **SPLREG_RESTART_JOB_ON_POOL_ERROR** est une durée minimale. L’heure réelle peut être plus longue, en fonction des paramètres de moniteur de port suivants, qui sont des valeurs de Registre sous cette clé de Registre :

**HKLM \\ System \\ CurrentControlSet \\ Control \\ moniteurs d’impression \\ \\ <  > \\ ports nomdumoniteur**

Appelez la fonction [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) pour définir ces valeurs.



| Paramètre du moniteur de port     | Type de données      | Signification                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **REG_DWORD** | Si la valeur est différente de zéro, active le moniteur de port pour mettre à jour le spouleur avec l’état du port.<br/>            |
| **StatusUpdateInterval** | **REG_DWORD** | Spécifie l’intervalle, en minutes, au cours duquel le moniteur de port met à jour le spouleur avec l’état du port.<br/> |



 

Pour vous assurer que le spouleur redirige les travaux vers la prochaine imprimante disponible dans le pool (lorsque le travail d’impression n’est pas imprimé dans le délai défini), le moniteur de port doit prendre en charge SNMP et les ports réseau du pool doivent être configurés comme « État SNMP activé ». Le moniteur de port qui prend en charge SNMP est le moniteur de port TCP/IP standard.

dans Windows 7 et les versions ultérieures de Windows, les travaux d’impression qui sont envoyés à un serveur d’impression sont rendus sur le client par défaut. Le rendu côté client des travaux d’impression peut être configuré en définissant *pKeyName* sur « PrinterDriverData » et *pValueName* sur la valeur de paramètre dans le tableau suivant.



| Paramètre                      | Type de données      | Description                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **REG_DWORD** | La valeur 0, ou si cette valeur n’est pas présente dans le registre, active le rendu par défaut côté client des travaux d’impression.<br/> La valeur 1 désactive le rendu côté client des travaux d’impression.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **REG_DWORD** | La valeur 0, ou si cette valeur n’est pas présente dans le registre, entraîne le rendu des travaux d’impression sur le client. Si un travail d’impression ne peut pas être rendu sur le client, il sera rendu sur le serveur. Si un travail d’impression ne peut pas être rendu sur le serveur, il échoue.<br/> La valeur 1 affiche les travaux d’impression sur le client. Si un travail d’impression ne peut pas être rendu sur le client, l’opération échoue.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **SetPrinterDataExW** (Unicode) et **SetPrinterDataExA** (ANSI)<br/>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**PRINTER_INFO_7**](printer-info-7.md)
</dt> </dl>

 

