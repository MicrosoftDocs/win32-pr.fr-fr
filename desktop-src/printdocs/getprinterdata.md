---
description: La fonction GetPrinterData récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: GetPrinterData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518789"
---
# <a name="getprinterdata-function"></a>GetPrinterData fonction)

La fonction **GetPrinterData** récupère les données de configuration pour l’imprimante ou le serveur d’impression spécifié.

Dans Windows 2000 et les versions ultérieures de Windows, l’appel de **GetPrinterData** équivaut à appeler [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) avec le paramètre *pKeyName* défini sur « PrinterDriverData ».

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante ou le serveur d’impression pour lequel la fonction récupère les données de configuration. Utilisez la fonction [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pValueName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne terminée par le caractère null qui identifie les données à récupérer.

Pour les imprimantes, cette chaîne correspond au nom d’une valeur de Registre sous la clé « PrinterDriverData » de l’imprimante dans le registre.

Pour les serveurs d’impression, cette chaîne est l’une des chaînes prédéfinies énumérées dans la section Notes suivante.

</dd> <dt>

*PTYPE* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur qui indique le type de données extraites dans *pData*. La fonction retourne le type spécifié dans l’appel [**SetPrinterData**](setprinterdata.md) ou [**SetPrinterDataEx**](setprinterdataex.md) qui a stocké les données. Affectez la valeur **null** à ce paramètre si vous n’avez pas besoin du type de données.

</dd> <dt>

*pData* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les données de configuration.

</dd> <dt>

*nSize* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle *pData* pointe.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille, en octets, des données de configuration. Si la taille de la mémoire tampon spécifiée par *nSize* est trop petite, la fonction retourne l' **erreur \_ plus de \_ données** et *pcbNeeded* indique la taille de mémoire tampon requise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une **erreur de \_ réussite**. Si la fonction échoue, la valeur de retour est une valeur d’erreur.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

**GetPrinterData** récupère les données de configuration d’imprimante qui ont été définies par la fonction [**SetPrinterDataEx**](setprinterdataex.md) ou [**SetPrinterData**](setprinterdata.md) .

**GetPrinterData** peut déclencher un appel Windows à [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), qui peut écrire dans le registre. Si c’est le cas, des effets secondaires peuvent se produire, tels que le déclenchement d’une mise à jour ou d’une mise à niveau de l’ID d’événement 20 dans le client, si l’imprimante est partagée sur un réseau.

Si *hPrinter* est un handle vers un serveur d’impression, *pValueName* peut spécifier l’une des valeurs prédéfinies suivantes.



| Valeur                                                               | Commentaires                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SPLREG \_ autoriser l' \_ utilisateur \_ MANAGEFORMS**                                | Windows XP avec Service Pack 2 (SP2) et versions ultérieures<br/> Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures<br/>                                                                                                    |
| **\_architecture SPLREG**                                            |                                                                                                                                                                                                                                 |
| **\_signal sonore SPLREG \_ activé**                                           |                                                                                                                                                                                                                                 |
| **SPLREG \_ \_ Répertoire de spoule par défaut \_**                               |                                                                                                                                                                                                                                 |
| **nom de l' \_ ordinateur DNS SPLREG \_ \_**                                      |                                                                                                                                                                                                                                 |
| **SPLREG \_ DS \_ présent**                                             | En cas de retour réussi, *pData* contient 0x0001 si l’ordinateur se trouve sur un domaine DS, sinon, 0.<br/>                                                                                                                         |
| **SPLREG \_ DS \_ présent \_ pour l' \_ utilisateur**                                  | En cas de retour réussi, *pData* contient 0x0001 si l’utilisateur a ouvert une session sur un domaine DS, sinon, 0.<br/>                                                                                                                   |
| **\_Journal des événements SPLREG \_**                                              |                                                                                                                                                                                                                                 |
| **\_version principale de SPLREG \_**                                          |                                                                                                                                                                                                                                 |
| **\_version mineure SPLREG \_**                                          |                                                                                                                                                                                                                                 |
| **\_fenêtre SPLREG NET \_**                                              | Non pris en charge dans Windows Server 2003 et versions ultérieures<br/>                                                                                                                                                                       |
| **SPLREG \_ NET \_ Popup \_ à l' \_ ordinateur**                                | En cas de retour réussi, *pData* contient 1 si les notifications de travaux doivent être envoyées à l’ordinateur client, ou 0 si les notifications de travail doivent être envoyées à l’utilisateur.<br/> Non pris en charge dans Windows Server 2003 et versions ultérieures<br/> |
| **\_version du système d’exploitation SPLREG \_**                                             | Windows XP et versions ultérieures<br/>                                                                                                                                                                                                 |
| **SPLREG \_ se \_ VERSIONEX**                                           |                                                                                                                                                                                                                                 |
| **\_ \_ \_ \_ valeur par défaut de la priorité du thread du port SPLREG**                         |                                                                                                                                                                                                                                 |
| **\_priorité de \_ thread de port SPLREG \_**                                  |                                                                                                                                                                                                                                 |
| **\_ \_ \_ groupes d’isolation du pilote d’impression SPLREG \_**                        | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ temps d’isolement du pilote d’impression SPLREG \_ avant le \_ \_ recyclage**         | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_isolement du \_ pilote d’impression SPLREG \_ \_ nombre maximal d' \_ objets \_ avant le \_ recyclage** | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ \_ délai d’inactivité d’isolation du pilote d’impression \_ SPLREG**                 | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_ \_ \_ stratégie d’exécution de \_ l' \_ isolation du pilote d’impression SPLREG**             | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_stratégie de \_ \_ remplacement d’isolation du pilote d’impression \_ SPLREG \_**              | Windows 7 et ultérieur<br/>                                                                                                                                                                                                  |
| **\_télécopie à distance SPLREG \_**                                             | En cas de retour réussi, *pData* contient 0x0001 si le service de télécopie prend en charge les clients distants, sinon 0.<br/>                                                                                                               |
| **\_ \_ fenêtre contextuelle SPLREG Retry**                                            | En cas de retour réussi, *pData* contient 1 si le serveur est configuré pour réessayer les fenêtres contextuelles pour tous les travaux, ou 0 si le serveur ne réessaye pas les fenêtres publicitaires pour tous les travaux.<br/> Non pris en charge dans Windows Server 2003 et versions ultérieures<br/> |
| **\_ \_ priorité de threads du planificateur SPLREG \_**                             |                                                                                                                                                                                                                                 |
| **\_priorité de thread du planificateur SPLREG \_ \_ \_ par défaut**                    |                                                                                                                                                                                                                                 |
| **SPLREG \_ WEBSHAREMGMT**                                            | Windows Server 2003 et versions ultérieures<br/>                                                                                                                                                                                        |



 

Les valeurs suivantes de *pValueName* indiquent le comportement d’impression du pool lorsqu’une erreur se produit.



| Valeur                                       | Commentaires                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ erreur de redémarrage du travail SPLREG \_ sur le \_ pool \_**   | La valeur de *pData* indique la durée, en secondes, à laquelle un travail est redémarré sur un autre port après qu’une erreur s’est produite. Ce paramètre est utilisé avec **la \_ tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée**.<br/> |
| **\_tâche de redémarrage SPLREG \_ \_ sur le \_ pool \_ activée** | Une valeur différente de zéro dans *pData* indique **que \_ \_ le travail de redémarrage SPLREG sur l' \_ \_ \_ erreur de pool** est activé.<br/>                                                                                            |



 

L’heure spécifiée dans **l' \_ erreur de redémarrage du \_ travail SPLREG \_ sur le \_ pool \_** est une heure minimale. L’heure réelle peut être plus longue, en fonction des paramètres de moniteur de port suivants, qui sont des valeurs de Registre sous cette clé de Registre :

**HKLM \\ System \\ CurrentControlSet \\ Control \\ moniteurs d’impression \\ \\ <  > \\ ports nomdumoniteur**

Appelez la fonction [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) pour interroger ces valeurs.



| Paramètre du moniteur de port     | Type de données      | Signification                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| **StatusUpdateEnabled**  | **\_valeur DWORD reg** | Si la valeur est différente de zéro, active le moniteur de port pour mettre à jour le spouleur avec l’état du port.<br/>            |
| **StatusUpdateInterval** | **\_valeur DWORD reg** | Spécifie l’intervalle, en minutes, au cours duquel le moniteur de port met à jour le spouleur avec l’état du port.<br/> |



 

Dans Windows 7 et les versions ultérieures de Windows, les travaux d’impression qui sont envoyés à un serveur d’impression sont rendus sur le client par défaut. Les valeurs suivantes configurent le rendu côté client d’un travail d’impression et peuvent être lues si vous définissez les valeurs suivantes dans *pValueName*.



| Paramètre                      | Type de données      | Description                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EMFDespoolingSetting**     | **\_valeur DWORD reg** | La valeur 0, ou si cette valeur n’est pas présente dans le registre, active le rendu par défaut côté client des travaux d’impression.<br/> La valeur 1 désactive le rendu côté client des travaux d’impression.<br/>                                                                                                                                                                                                          |
| **ForceClientSideRendering** | **\_valeur DWORD reg** | La valeur 0, ou si cette valeur n’est pas présente dans le registre, entraîne le rendu des travaux d’impression sur le client. Si un travail d’impression ne peut pas être rendu sur le client, il sera rendu sur le serveur. Si un travail d’impression ne peut pas être rendu sur le serveur, il échoue.<br/> La valeur 1 affiche les travaux d’impression sur le client. Si un travail d’impression ne peut pas être rendu sur le client, l’opération échoue.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **GetPrinterDataW** (Unicode) et **GetPrinterDataA** (ANSI)<br/>                                   |



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

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> <dt>

[**PRINTPROCESSOR \_ Cap \_ 1**](printprocessor-caps-1.md)
</dt> </dl>

 

