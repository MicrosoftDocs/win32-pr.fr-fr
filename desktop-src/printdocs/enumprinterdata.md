---
description: La fonction EnumPrinterData énumère les données de configuration d’une imprimante spécifiée.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: EnumPrinterData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a542b6a0432ccf7065d94eeb8ebb3acbd8e2ace22044f2cc8984a1f4b2404299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846079"
---
# <a name="enumprinterdata-function"></a>EnumPrinterData fonction)

La fonction **EnumPrinterData** énumère les données de configuration d’une imprimante spécifiée.

Pour récupérer les données de configuration en un seul appel, utilisez la fonction [**EnumPrinterDataEx**](enumprinterdataex.md) .

## <a name="syntax"></a>Syntaxe


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante dont les données de configuration doivent être obtenues. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Valeur d’index qui spécifie la valeur des données de configuration à récupérer.

Affectez à ce paramètre la valeur zéro pour le premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié. Incrémentez ensuite le paramètre d’une unité pour les appels suivants impliquant la même imprimante, jusqu’à ce que la fonction retourne l’erreur \_ \_ plus d' \_ éléments. Pour plus d’informations, consultez la section Notes suivante.

Si vous utilisez la technique mentionnée dans les descriptions des paramètres *cbValueName* et *cbData* pour obtenir les valeurs de taille de mémoire tampon adéquates, en définissant ces deux paramètres sur zéro dans un premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié, la valeur de *dwIndex* n’a pas d’importance pour cet appel. Affectez à *dwIndex* la valeur zéro dans le prochain appel à **EnumPrinterData** pour démarrer le processus d’énumération réel.

Les valeurs des données de configuration ne sont pas triées. Les nouvelles valeurs comporteront un index arbitraire. Cela signifie que la fonction **EnumPrinterData** peut retourner des valeurs dans n’importe quel ordre.

</dd> <dt>

*pValueName* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le nom de la valeur des données de configuration, y compris un caractère null de fin.

</dd> <dt>

*cbValueName* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pValueName*.

Si vous souhaitez que le système d’exploitation fournisse une taille de mémoire tampon appropriée, définissez à la fois ce paramètre et le paramètre *cbData* sur zéro pour le premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié. Quand la fonction retourne, la variable vers laquelle pointe *pcbValueName* contient une taille de mémoire tampon suffisamment grande pour énumérer correctement tous les noms de valeur de données de configuration de l’imprimante.

</dd> <dt>

*pcbValueName* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets stockés dans la mémoire tampon vers laquelle pointe *pValueName*.

</dd> <dt>

*PTYPE* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un code indiquant le type de données stockées dans la valeur spécifiée. Pour obtenir la liste des codes de type possibles, consultez [types de valeurs de Registre](/windows/desktop/SysInfo/registry-value-types). Le paramètre *PTYPE* peut avoir la **valeur null** si le code de type n’est pas requis.

</dd> <dt>

*pData* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la valeur des données de configuration.

Ce paramètre peut avoir la valeur **null** si la valeur des données de configuration n’est pas requise.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pData*.

Si vous souhaitez que le système d’exploitation fournisse une taille de mémoire tampon appropriée, définissez à la fois ce paramètre et le paramètre *cbValueName* sur zéro pour le premier appel à **EnumPrinterData** pour un handle d’imprimante spécifié. Quand la fonction retourne, la variable vers laquelle pointe *pcbData* contient une taille de mémoire tampon suffisamment grande pour énumérer correctement tous les noms de valeur de données de configuration de l’imprimante.

</dd> <dt>

*pcbData* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets stockés dans la mémoire tampon vers laquelle pointe *pData*.

Ce paramètre peut avoir la **valeur null** si *PData* a la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur système.

La fonction retourne l’erreur \_ aucun \_ autre \_ élément lorsqu’il n’y a plus de valeurs de données de configuration à récupérer pour un handle d’imprimante spécifié.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

**EnumPrinterData** récupère les données de configuration de l’imprimante définies par la fonction [**SetPrinterData**](setprinterdata.md) . Les données de configuration d’une imprimante consistent en un ensemble de valeurs nommées et typées. La fonction **EnumPrinterData** obtient l’une de ces valeurs, son nom et un code de type, chaque fois que vous l’appelez. Appelez la fonction **EnumPrinterData** plusieurs fois de suite pour obtenir toutes les valeurs de données de configuration de l’imprimante.

Les données de configuration de l’imprimante sont stockées dans le registre. Lors de l’énumération des données de configuration de l’imprimante, vous devez éviter d’appeler des fonctions de Registre susceptibles de modifier ces données.

Si vous souhaitez que le système d’exploitation fournisse une taille de mémoire tampon appropriée, appelez d’abord **EnumPrinterData** avec les paramètres *cbValueName* et *cbData* définis sur zéro, comme indiqué plus haut dans la section paramètres. La valeur de *dwIndex* n’a pas d’importance pour cet appel. Quand la fonction retourne, \* *pcbValueName* et \* *pcbData* contiendront des tailles de mémoire tampon suffisamment grandes pour énumérer tous les noms et valeurs de la valeur des données de configuration de l’imprimante. Lors du prochain appel, allouez un nom de valeur et des mémoires tampons de données, définissez *cbValueName* et *cbData* sur les tailles en octets des mémoires tampons allouées, puis définissez *dwIndex* sur zéro. Ensuite, continuez à appeler la fonction **EnumPrinterData** , en incrémentant *dwIndex* à chaque fois, jusqu’à ce que la fonction retourne l’erreur plus \_ aucun \_ \_ élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **EnumPrinterDataW** (Unicode) et **EnumPrinterDataA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterData**](deleteprinterdata.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

