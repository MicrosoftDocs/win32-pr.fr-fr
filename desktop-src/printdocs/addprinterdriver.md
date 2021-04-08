---
description: La fonction AddPrinterDriver installe un pilote d’imprimante local ou distant et associe les fichiers de configuration, de données et de pilote.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: AddPrinterDriver, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757858"
---
# <a name="addprinterdriver-function"></a>AddPrinterDriver fonction)

La fonction **AddPrinterDriver** installe un pilote d’imprimante local ou distant et associe les fichiers de configuration, de données et de pilote.

Pour une plus grande flexibilité lors de l’installation ou de la mise à niveau des pilotes d’imprimante, utilisez la fonction [**AddPrinterDriverEx**](addprinterdriverex.md) car elle permet une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers plus récents uniquement et la copie de tous les fichiers (quels que soient les horodatages de fichier).

> [!Note]  
> L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée. Utilisez [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) à la place.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le pilote doit être installé.

Si *pname* a la **valeur null**, le pilote est installé localement.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle *pDriverInfo* pointe.

Cette valeur peut être 2, 3, 4, 6 ou 8.

</dd> <dt>

*pDriverInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure contenant des informations sur le pilote d’imprimante. Cela dépend de la valeur de *Level*.



| Valeur | Structure du lecteur d’imprimante                  |
|-------|------------------------------------------|
| 2     | [**\_Informations sur le pilote \_ 2**](driver-info-2.md) |
| 3     | [**\_Informations sur le pilote \_ 3**](driver-info-3.md) |
| 4     | [**\_Informations sur le pilote \_ 4**](driver-info-4.md) |
| 6     | [**\_Informations sur le pilote \_ 6**](driver-info-6.md) |
| 8     | [**\_Informations sur le pilote \_ 8**](driver-info-8.md) |



 

Si le membre **pEnvironment** de la structure vers laquelle pointe *PDriverInfo* a la **valeur null**, l’environnement actuel de l’appelant/client (et non du serveur/de destination) est utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Avant qu’une application appelle la fonction **AddPrinterDriver** , tous les fichiers requis par le pilote doivent être copiés dans le répertoire du pilote d’imprimante du système. Une application peut récupérer le nom de ce répertoire en appelant la fonction [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .

Une application peut déterminer les pilotes d’imprimante actuellement installés en appelant la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddPrinterDriverW** (Unicode) et **AddPrinterDriverA** (ANSI)<br/>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 2**](driver-info-2.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 3**](driver-info-3.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 4**](driver-info-4.md)
</dt> <dt>

[**\_Informations sur le pilote \_ 6**](driver-info-6.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriverDirectory**](getprinterdriverdirectory.md)
</dt> </dl>

 

