---
description: Supprime un package de pilotes d’imprimante du magasin de pilotes.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: DeletePrinterDriverPackage, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: d7247f4f0ef4d1f77f00664792d0b7b36bc991b19d437017b54db676731ccc70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112549"
---
# <a name="deleteprinterdriverpackage-function"></a>DeletePrinterDriverPackage fonction)

Supprime un package de pilotes d’imprimante du magasin de pilotes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression à partir duquel le package de pilotes est supprimé. Une valeur de pointeur **null** signifie l’ordinateur local.

</dd> <dt>

*pszInfPath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le chemin d’accès au \* fichier. inf du pilote.

</dd> <dt>

*pszEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86). Il peut s’agir de la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

\_OK si l’opération a échoué.

E \_ ACCESSDENIED, si le package a été fourni avec Windows.

\_Code HRESULT (erreur \_ \_ d’impression \_ \_ du package de pilotes en cours d' \_ utilisation), si le package est utilisé.

Sinon, **HRESULT** contient un code d’erreur.

Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Le magasin de pilotes correspond généralement à% windir% \\ INF ou% windir% \\ system32 \\ DriverStore \\ FileRepository.

un package de pilotes fourni avec Windows ne peut pas être supprimé avec cette fonction.

L’utilisateur doit disposer de privilèges d’administration d’imprimante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **DeletePrinterDriverPackageW** (Unicode) et **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

