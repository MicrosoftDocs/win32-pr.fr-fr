---
description: La fonction EnumPrinterDataEx énumère tous les noms de valeur et les données pour une imprimante et une clé spécifiées.
ms.assetid: bc5ecc46-24a4-4b54-9431-0eaf6446e2d6
title: EnumPrinterDataEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDataEx
- EnumPrinterDataExA
- EnumPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 517d480d1c831627cadb289c41f99d24b1025ef2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412816"
---
# <a name="enumprinterdataex-function"></a>EnumPrinterDataEx fonction)

La fonction **EnumPrinterDataEx** énumère tous les noms de valeur et les données pour une imprimante et une clé spécifiées.

Les données de l’imprimante sont stockées dans le registre. Lors de l’énumération des données d’imprimante, n’appelez pas les fonctions de Registre susceptibles de modifier les données.

## <a name="syntax"></a>Syntaxe


```C++
DWORD EnumPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _Out_ LPBYTE  pEnumValues,
  _In_  DWORD   cbEnumValues,
  _Out_ LPDWORD pcbEnumValues,
  _Out_ LPDWORD pnEnumValues
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle la fonction récupère les données de configuration. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pKeyName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant les valeurs à énumérer. Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès avec une ou plusieurs sous-clés. **EnumPrinterDataEx** énumère toutes les valeurs de la clé, mais n’énumère pas les valeurs des sous-clés de la clé spécifiée. Utilisez la fonction [**EnumPrinterKey**](enumprinterkey.md) pour énumérer les sous-clés.

Si *pKeyName* a la **valeur null** ou est une chaîne vide, **ENUMPRINTERDATAEX** retourne un paramètre d’erreur \_ non valide \_ .

</dd> <dt>

*pEnumValues* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau de structures de [**\_ \_ valeurs d’enum d’imprimante**](printer-enum-values.md) . Chaque structure contient le nom de la valeur, le type, les données et la taille d’une valeur sous la clé.

</dd> <dt>

*cbEnumValues* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pcbEnumValues*. Si vous affectez à *cbEnumValues* la valeur zéro, le paramètre *pcbEnumValues* retourne la taille de mémoire tampon requise.

</dd> <dt>

*pcbEnumValues* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille, en octets, des données de configuration récupérées. Si la taille de la mémoire tampon spécifiée par *cbEnumValues* est trop petite, la fonction retourne \_ l’erreur plus \_ de données et *pcbEnumValues* indique la taille de mémoire tampon requise.

</dd> <dt>

*pnEnumValues* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de structures [**de \_ \_ valeurs d’enum d’imprimante**](printer-enum-values.md) retournées dans *pEnumValues*.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur système.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

**EnumPrinterDataEx** récupère les données de configuration de l’imprimante définies par les fonctions [**SetPrinterDataEx**](setprinterdataex.md) et [**SetPrinterData**](setprinterdata.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **EnumPrinterDataExW** (Unicode) et **EnumPrinterDataExA** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDataEx**](deleteprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_valeurs d’énumération d’imprimante \_**](printer-enum-values.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




