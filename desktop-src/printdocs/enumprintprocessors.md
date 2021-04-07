---
description: La fonction EnumPrintProcessors énumère les processeurs d’impression installés sur le serveur spécifié.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: EnumPrintProcessors, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952337"
---
# <a name="enumprintprocessors-function"></a>EnumPrintProcessors fonction)

La fonction **EnumPrintProcessors** énumère les processeurs d’impression installés sur le serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel résident les processeurs d’impression. Si ce paramètre a la **valeur null**, les processeurs d’impression locaux sont énumérés.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Type d’informations retournées dans la mémoire tampon *pPrintProcessorInfo* . Ce paramètre doit être 1.

</dd> <dt>

*pPrintProcessorInfo* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau de structures [**PRINTPROCESSOR \_ info \_ 1**](printprocessor-info-1.md) . Chaque structure décrit un processeur d’impression disponible. La mémoire tampon doit être suffisamment grande pour recevoir le tableau de structures et toutes les chaînes auxquelles les membres de la structure pointent.

Pour déterminer la taille de mémoire tampon requise, appelez **EnumPrintProcessors** avec *cbBuf* défini à zéro. **EnumPrintProcessors** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pPrintProcessorInfo*.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets copiés dans la mémoire tampon *pPrintProcessorInfo* si la fonction est réussie. Si la mémoire tampon est trop petite, la fonction échoue et la variable reçoit le nombre d’octets requis.

</dd> <dt>

*pcReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de structures retournées dans la mémoire tampon *pPrintProcessorInfo* .

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
| Noms Unicode et ANSI<br/>   | **EnumPrintProcessorsW** (Unicode) et **EnumPrintProcessorsA** (ANSI)<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**\_Informations PRINTPROCESSOR \_ 1**](printprocessor-info-1.md)
</dt> </dl>

 

