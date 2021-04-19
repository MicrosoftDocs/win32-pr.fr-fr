---
description: La fonction EnumPorts énumère les ports qui sont disponibles pour l’impression sur un serveur spécifié.
ms.assetid: 72ea0e35-bf26-4c12-9451-8f6941990d82
title: EnumPorts, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPorts
- EnumPortsA
- EnumPortsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2f4cceb6b6915f92139d8919b74f62ba4392381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529191"
---
# <a name="enumports-function"></a>EnumPorts fonction)

La fonction **EnumPorts** énumère les ports qui sont disponibles pour l’impression sur un serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnumPorts(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPorts,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur dont vous souhaitez énumérer les ports d’imprimante.

Si *pname* a la **valeur null**, la fonction énumère les ports d’imprimante de l’ordinateur local.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type d’informations retournées dans la mémoire tampon *pPorts* . Si le *niveau* est 1, *pPorts* reçoit un tableau de structures d' [**informations de port \_ \_ 1**](port-info-1.md) . Si le *niveau* est 2, *pPorts* reçoit un tableau de structures d' [**informations de port \_ \_ 2**](port-info-2.md) .

</dd> <dt>

*pPorts* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau de structures d' [**informations de port \_ \_ 1**](port-info-1.md) ou d' [**informations de port \_ \_ 2**](port-info-2.md) . Chaque structure contient des données qui décrivent un port d’imprimante disponible. La mémoire tampon doit être suffisamment grande pour stocker les chaînes pointées par les membres de la structure.

Pour déterminer la taille de mémoire tampon requise, appelez **EnumPorts** avec *cbBuf* défini à zéro. **EnumPorts** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pPorts*.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets copiés dans la mémoire tampon *pPorts* . Si la mémoire tampon est trop petite, la fonction échoue et la variable reçoit le nombre d’octets requis.

</dd> <dt>

*pcReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de structures [**d' \_ informations \_ de port 1**](port-info-1.md) ou d' [**informations de port \_ \_ 2**](port-info-2.md) retournées dans la mémoire tampon *pPorts* . Il s’agit du nombre de ports d’imprimante disponibles sur le serveur spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La fonction **EnumPorts** peut être exécutée même si le serveur spécifié par *pname* n’a pas d’imprimante définie.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **EnumPortsW** (Unicode) et **EnumPortsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**\_Informations sur le port \_ 1**](port-info-1.md)
</dt> <dt>

[**\_Informations sur le port \_ 2**](port-info-2.md)
</dt> </dl>

 

