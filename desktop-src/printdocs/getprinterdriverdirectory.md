---
description: La fonction GetPrinterDriverDirectory récupère le chemin d’accès du répertoire du pilote d’imprimante.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: GetPrinterDriverDirectory, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530242"
---
# <a name="getprinterdriverdirectory-function"></a>GetPrinterDriverDirectory fonction)

La fonction **GetPrinterDriverDirectory** récupère le chemin d’accès du répertoire du pilote d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le pilote d’imprimante réside. Si ce paramètre a la **valeur null**, le chemin d’accès au répertoire du pilote local est récupéré.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Niveau de la structure. Cette valeur doit être 1.

</dd> <dt>

*pDriverDirectory* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le chemin d’accès.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon à laquelle *pDriverDirectory* pointe.

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
| Noms Unicode et ANSI<br/>   | **GetPrinterDriverDirectoryW** (Unicode) et **GetPrinterDriverDirectoryA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> </dl>

 

 




