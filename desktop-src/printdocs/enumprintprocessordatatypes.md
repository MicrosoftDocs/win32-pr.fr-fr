---
description: La fonction EnumPrintProcessorDatatypes énumère les types de données pris en charge par un processeur d’impression spécifié.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: EnumPrintProcessorDatatypes, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b6985181abca6fa6116fe39ab02ff5b60431bd44d771fedbcad179ba9e949a9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091989"
---
# <a name="enumprintprocessordatatypes-function"></a>EnumPrintProcessorDatatypes fonction)

La fonction **EnumPrintProcessorDatatypes** énumère les types de données pris en charge par un processeur d’impression spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le processeur d’impression réside. Si ce paramètre a la **valeur null**, les types de données du processeur d’impression local sont énumérés.

</dd> <dt>

*pPrintProcessorName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression dont les types de données sont énumérés.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type d’informations retournées dans la mémoire tampon *pDatatypes* . Ce paramètre doit être 1.

</dd> <dt>

*pDatatypes* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau de structures d' [**informations de types de données \_ \_ 1**](datatypes-info-1.md) . Chaque structure décrit un type de données disponible. La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures et toutes les chaînes ou autres données auxquelles les membres de la structure pointent.

Pour déterminer la taille de mémoire tampon requise, appelez **EnumPrintProcessorDatatypes** avec *cbBuf* défini à zéro. **EnumPrintProcessorDatatypes** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pDatatypes*.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets copiés dans la mémoire tampon *pDatatypes* si la fonction est réussie. Si la mémoire tampon est trop petite, la fonction échoue et la variable reçoit le nombre d’octets requis.

</dd> <dt>

*pcReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de structures retournées dans la mémoire tampon *pDatatypes* . Il s’agit du nombre de types de données pris en charge.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

v

à partir de Windows Vista, les informations de type de données des serveurs d’impression distants sont récupérées à partir d’un cache local.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **EnumPrintProcessorDatatypesW** (Unicode) et **EnumPrintProcessorDatatypesA** (ANSI)<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Informations de type de données \_ \_ 1**](datatypes-info-1.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

