---
description: La fonction AddMonitor installe un moniteur de port local et lie les fichiers de configuration, de données et de surveillance.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: AddMonitor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035226"
---
# <a name="addmonitor-function"></a>AddMonitor fonction)

La fonction **AddMonitor** installe un moniteur de port local et lie les fichiers de configuration, de données et de surveillance.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel l’analyse doit être installée. Pour les systèmes qui prennent uniquement en charge l’installation locale de moniteurs, cette chaîne doit avoir la **valeur null**.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle *pMonitors* pointe. Cette valeur doit être 2.

</dd> <dt>

*pMonitors* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ informations \_ d’analyse 2**](monitor-info-2.md) . Si le membre **pEnvironment** de la structure *pMonitors* est **null**, l’environnement actuel de l’appelant (client), et non de la destination (serveur), est utilisé.

Notez que l’appel échoue si l’environnement ne correspond pas à l’environnement du serveur, autrement dit, vous pouvez uniquement ajouter une analyse écrite pour l’architecture du serveur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Avant qu’une application appelle la fonction **AddMonitor** , tous les fichiers requis par le moniteur doivent être copiés dans le répertoire system32.

Pour déterminer les moniteurs de port actuellement installés, appelez la fonction [**EnumMonitors**](enummonitors.md) .

Pour supprimer un moniteur ajouté par **AddMonitor**, appelez la fonction [**DeleteMonitor**](deletemonitor.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddMonitorW** (Unicode) et **AddMonitorA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeleteMonitor**](deletemonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**\_Informations sur le moniteur \_ 2**](monitor-info-2.md)
</dt> </dl>

 

