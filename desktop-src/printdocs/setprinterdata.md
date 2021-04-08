---
description: La fonction SetPrinterData définit les données de configuration d’une imprimante ou d’un serveur d’impression.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: SetPrinterData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864750"
---
# <a name="setprinterdata-function"></a>SetPrinterData fonction)

La fonction **SetPrinterData** définit les données de configuration d’une imprimante ou d’un serveur d’impression.

Pour spécifier la clé de Registre dans laquelle stocker les données, appelez la fonction [**SetPrinterDataEx**](setprinterdataex.md) . L’appel de **SetPrinterData** équivaut à appeler la fonction **SetPrinterDataEx** avec le paramètre *pKeyName* défini sur « PrinterDriverData ».

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante ou le serveur d’impression pour lequel la fonction définit les données de configuration. Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pValueName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null qui identifie les données à définir.

Pour les imprimantes, cette chaîne correspond au nom d’une valeur de Registre sous la clé « PrinterDriverData » de l’imprimante dans le registre.

Pour les serveurs d’impression, cette chaîne est l’une des chaînes prédéfinies énumérées dans la section Notes suivante.

</dd> <dt>

*Type* \[ dans\]
</dt> <dd>

Code qui indique le type de données vers lequel pointe le paramètre *pData* . Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types).

</dd> <dt>

*pData* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’octets qui contient les données de configuration de l’imprimante.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une **erreur de \_ réussite**.

Si la fonction échoue, la valeur de retour est une valeur d’erreur.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Pour récupérer les données de configuration existantes d’une imprimante, appelez la fonction [**GetPrinterDataEx**](getprinterdataex.md) ou [**GetPrinterData**](getprinterdata.md) .

Si *hPrinter* est un handle vers un serveur d’impression, *pValueName* peut spécifier l’une des valeurs prédéfinies suivantes.



| Valeur                                                               | Commentaires                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ autoriser l' \_ utilisateur \_ MANAGEFORMS**                                | Windows XP avec Service Pack 2 (SP2) et versions ultérieures<br/> Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures<br/>                                                                                                    |
| **\_signal sonore SPLREG \_ activé**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ \_ Répertoire de spoule par défaut \_**                               |                                                                                                                                                                                                                                 |
| **\_Journal des événements SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_fenêtre SPLREG NET \_**                                              | Non pris en charge dans Windows Server 2003 et versions ultérieures<br/>                                                                                                                                                                       |
| **\_ \_ \_ \_ valeur par défaut de la priorité du thread du port SPLREG**                         |                                                                                                                                                                                                                                 |
| **\_priorité de \_ thread de port SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **\_ \_ \_ groupes d’isolation du pilote d’impression SPLREG \_**                        | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ temps d’isolement du pilote d’impression SPLREG \_ avant le \_ \_ recyclage**         | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_isolement du \_ pilote d’impression SPLREG \_ \_ nombre maximal d' \_ objets \_ avant le \_ recyclage** | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ \_ délai d’inactivité d’isolation du pilote d’impression \_ SPLREG**                 | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ stratégie d’exécution de \_ l' \_ isolation du pilote d’impression SPLREG**             | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_stratégie de \_ \_ remplacement d’isolation du pilote d’impression \_ SPLREG \_**              | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_ \_ fenêtre contextuelle SPLREG Retry**                                            | En cas de retour réussi, *pData* contient 1 si le serveur est configuré pour réessayer les fenêtres contextuelles pour tous les travaux, ou 0 si le serveur ne réessaye pas les fenêtres publicitaires pour tous les travaux.<br/> Non pris en charge dans Windows Server 2003 et versions ultérieures<br/> |
| **\_ \_ priorité de threads du planificateur SPLREG \_**                             |                                                                                                                                                                                                                                 |
| **\_priorité de thread du planificateur SPLREG \_ \_ \_ par défaut**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 et versions ultérieures<br/>                                                                                                                                                                                        |



 

Les valeurs suivantes de *pValueName* déterminent le comportement d’impression du pool lorsqu’une erreur se produit.



| Valeur                                       | Commentaires                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ erreur de redémarrage du travail SPLREG \_ sur le \_ pool \_**   | La valeur de *pData* indique la durée, en secondes, à laquelle un travail est redémarré sur un autre port après qu’une erreur s’est produite. Ce paramètre est utilisé avec **la \_ tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**.<br/> |
| **\_tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée** | Une valeur différente de zéro dans *pData* indique **que \_ \_ le travail de redémarrage SPLREG sur l' \_ \_ \_ erreur de pool** est activé.<br/>                                                                                            |



 

L’heure spécifiée dans **l' \_ erreur de redémarrage du \_ travail SPLREG \_ sur le \_ pool \_** est une heure minimale. L’heure réelle peut être plus longue, en fonction des paramètres de moniteur de port suivants, qui sont des valeurs de Registre sous cette clé de Registre :

**HKLM \\ System \\ CurrentControlSet \\ Control \\ moniteurs d’impression \\ \\ <  > \\ ports nomdumoniteur**

Appelez la fonction [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) pour définir ces valeurs.



| Paramètre du moniteur de port     | Type de données      | Signification                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **\_valeur DWORD reg** | Si la valeur est différente de zéro, active le moniteur de port pour mettre à jour le spouleur avec l’état du port.<br/>            |
| **StatusUpdateInterval** | **\_valeur DWORD reg** | Spécifie l’intervalle, en minutes, au cours duquel le moniteur de port met à jour le spouleur avec l’état du port.<br/> |



 

Dans Windows 7 et les versions ultérieures de Windows, les travaux d’impression qui sont envoyés à un serveur d’impression sont rendus sur le client par défaut. Le rendu côté client d’un travail d’impression peut être configuré pour chaque imprimante en définissant les valeurs suivantes dans *pValueName*.



| Paramètre                      | Type de données      | Description                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **\_valeur DWORD reg** | La valeur 0, ou si cette valeur n’est pas présente dans le registre, active le rendu par défaut côté client des travaux d’impression.<br/> La valeur 1 désactive le rendu côté client des travaux d’impression.<br/>                                                                                                                                                                                                      |
| **ForceClientSideRendering** | **\_valeur DWORD reg** | La valeur 0, ou si cette valeur n’est pas présente dans le registre, entraîne le rendu des travaux d’impression sur le client. Si un travail d’impression ne peut pas être rendu sur le client, il sera rendu sur le serveur. Si un travail d’impression ne peut pas être rendu sur le serveur, il échoue.<br/> La valeur 1 affiche les travaux d’impression sur le client. Si un travail d’impression ne peut pas être rendu sur le client, l’opération échoue.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **SetPrinterDataW** (Unicode) et **SetPrinterDataA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

