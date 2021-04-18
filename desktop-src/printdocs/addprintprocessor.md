---
description: La fonction AddPrintProcessor installe un processeur d’impression sur le serveur spécifié et ajoute le nom du processeur d’impression à la liste des processeurs d’impression pris en charge.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: AddPrintProcessor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536602"
---
# <a name="addprintprocessor-function"></a>AddPrintProcessor fonction)

La fonction **AddPrintProcessor** installe un processeur d’impression sur le serveur spécifié et ajoute le nom du processeur d’impression à la liste des processeurs d’impression pris en charge.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le processeur d’impression doit être installé. Si ce paramètre a la **valeur null**, le processeur d’impression est installé localement.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, l’environnement actuel de l’appelant/client (pas du serveur/de destination) est utilisé.

</dd> <dt>

*pPathName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier qui contient le processeur d’impression. Ce fichier doit se trouver dans le répertoire du processeur d’impression système.

</dd> <dt>

*pPrintProcessorName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Avant d’appeler la fonction **AddPrintProcessor** , une application doit vérifier que le fichier contenant le processeur d’impression est stocké dans le répertoire du processeur d’impression système. Une application peut récupérer le nom du répertoire du processeur d’impression système en appelant la fonction [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) .

Une application peut déterminer le nom de processeurs d’impression existants en appelant la fonction [**EnumPrintProcessors**](enumprintprocessors.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddPrintProcessorW** (Unicode) et **AddPrintProcessorA** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**GetPrintProcessorDirectory**](getprintprocessordirectory.md)
</dt> </dl>

 

