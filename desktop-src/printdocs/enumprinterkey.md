---
description: La fonction EnumPrinterKey énumère les sous-clés d’une clé spécifiée pour une imprimante spécifiée.
ms.assetid: 721b1d23-a594-4439-b8f9-9b11be5fe874
title: EnumPrinterKey, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterKey
- EnumPrinterKeyA
- EnumPrinterKeyW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c3666cce36884a331085d074df44e05b5bcfd0422433ce24bdbf3dbc385d7f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471783"
---
# <a name="enumprinterkey-function"></a>EnumPrinterKey fonction)

La fonction **EnumPrinterKey** énumère les sous-clés d’une clé spécifiée pour une imprimante spécifiée.

Les données de l’imprimante sont stockées dans le registre. Lors de l’énumération des données d’imprimante, n’appelez pas les fonctions de Registre susceptibles de modifier les données.

## <a name="syntax"></a>Syntaxe


```C++
DWORD EnumPrinterKey(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPTSTR  pSubkey,
  _In_  DWORD   cbSubkey,
  _Out_ LPDWORD pcbSubkey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle la fonction énumère les sous-clés. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pKeyName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant les sous-clés à énumérer. Utilisez la barre oblique inverse « \\ » comme séparateur pour spécifier un chemin d’accès avec une ou plusieurs sous-clés. **EnumPrinterKey** énumère toutes les sous-clés de la clé, mais n’énumère pas les sous-clés de ces sous-clés.

Si *pKeyName* est une chaîne vide (""), **EnumPrinterKey** énumère la clé de niveau supérieur pour l’imprimante. Si *pKeyName* a la **valeur null**, **ENUMPRINTERKEY** retourne un paramètre d’erreur \_ non valide \_ .

</dd> <dt>

*pSubkey* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau de noms de sous-clés se terminant par null. Le tableau se termine par deux caractères null.

</dd> <dt>

*cbSubkey* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pSubkey*. Si vous affectez à *cbSubkey* la valeur zéro, le paramètre *pcbSubkey* retourne la taille de mémoire tampon requise.

</dd> <dt>

*pcbSubkey* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets récupérés dans la mémoire tampon *pSubkey* . Si la taille de la mémoire tampon spécifiée par *cbSubkey* est trop petite, la fonction retourne \_ l’erreur plus \_ de données et *pcbSubkey* indique la taille de mémoire tampon requise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur système. Si *pKeyName* n’existe pas, la valeur de retour est \_ fichier d’erreurs \_ \_ introuvable.

## <a name="remarks"></a>Remarques

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
| Noms Unicode et ANSI<br/>   | **EnumPrinterKeyW** (Unicode) et **EnumPrinterKeyA** (ANSI)<br/>                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




