---
description: La fonction GetPrintProcessorDirectory récupère le chemin d’accès au répertoire du processeur d’impression sur le serveur spécifié.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: GetPrintProcessorDirectory, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868537"
---
# <a name="getprintprocessordirectory-function"></a>GetPrintProcessorDirectory fonction)

La fonction **GetPrintProcessorDirectory** récupère le chemin d’accès au répertoire du processeur d’impression sur le serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur. Si ce paramètre a la **valeur null**, un chemin d’accès local est retourné.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Niveau de la structure. Cette valeur doit être 1.

</dd> <dt>

*pPrintProcessorInfo* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le chemin d’accès. Notez que, pour les systèmes d’exploitation antérieurs à Windows Server 2003 SP 1, le chemin d’accès est au format local pour le serveur, et non dans le format à distance réel. Par exemple, le chemin d’accès est spécifié sous la forme « % windir% \\ system32 \\ spool \\ prtprocs \\ % environnement% » au lieu de « \\ \\ nom_serveur \\ Print $ \\ prtprocs \\ % environnement% », même lorsqu’il est appelé pour un serveur distant. Pour les systèmes d’exploitation Windows Server 2003 SP 1 et versions ultérieures, le chemin d’accès distant réel est retourné.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon vers laquelle pointe *pPrintProcessorInfo*.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui spécifie le nombre d’octets copiés si la fonction est réussie, ou le nombre d’octets requis si *cbBuf* est trop petit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **GetPrintProcessorDirectoryW** (Unicode) et **GetPrintProcessorDirectoryA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 




