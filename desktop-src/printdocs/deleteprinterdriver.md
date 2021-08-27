---
description: La fonction DeletePrinterDriver supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: DeletePrinterDriver, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d878bb848eebed7eaccd904d4cdfd035d5056ee32eaa67eac5064dd5cf4e1e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060029"
---
# <a name="deleteprinterdriver-function"></a>DeletePrinterDriver fonction)

La fonction **DeletePrinterDriver** supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur.

Pour supprimer les fichiers associés au pilote en plus de supprimer le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge pour un serveur, utilisez la fonction [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .

**DeletePrinterDriver** supprime un pilote uniquement si aucune version du pilote n’est utilisée pour l’environnement spécifié. [**DeletePrinterDriverEx**](deleteprinterdriverex.md) peut supprimer des versions spécifiques du pilote.

## <a name="syntax"></a>Syntaxe


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur à partir duquel le pilote doit être supprimé. Si ce paramètre a la **valeur null**, le nom du pilote d’imprimante est supprimé localement.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le pilote doit être supprimé (par exemple, Windows x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, le nom du pilote est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (et non de l’application de destination et du serveur d’impression).

</dd> <dt>

*pDriverName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote qui doit être supprimé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

La fonction **DeletePrinterDriver** ne supprime pas les fichiers associés, elle supprime simplement le nom du pilote de la liste retournée par la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Avant d’appeler **DeletePrinterDriver**, vous devez supprimer tous les objets d’imprimante qui utilisent le pilote d’imprimante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **DeletePrinterDriverW** (Unicode) et **DeletePrinterDriverA** (ANSI)<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

