---
description: La fonction EnumMonitors récupère des informations sur les moniteurs de port installés sur le serveur spécifié.
ms.assetid: 4d4fbed2-193f-426c-8463-eeb6b1eaf316
title: EnumMonitors, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMonitors
- EnumMonitorsA
- EnumMonitorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 1154cae0864b9d034ff356657d689cd3a768186f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756400"
---
# <a name="enummonitors-function"></a>EnumMonitors fonction)

La fonction **EnumMonitors** récupère des informations sur les moniteurs de port installés sur le serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnumMonitors(
  _In_  LPTSTR  pName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pMonitors,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel les analyses résident. Si ce paramètre a la **valeur null**, les analyses locales sont énumérées.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle pointe *pMonitors*.

Cette valeur peut être 1 ou 2.

</dd> <dt>

*pMonitors* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau de structures. La mémoire tampon doit être suffisamment grande pour stocker les chaînes référencées par les membres de la structure.

Pour déterminer la taille de mémoire tampon requise, appelez **EnumMonitors** avec *cbBuf* défini à zéro. **EnumMonitors** échoue, [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une \_ erreur \_ de mémoire tampon insuffisante et le paramètre *pcbNeeded* retourne la taille, en octets, de la mémoire tampon nécessaire pour contenir le tableau de structures et leurs données.

La mémoire tampon reçoit un tableau de structures [**information d’analyse \_ \_ 1**](monitor-info-1.md) si le *niveau* est 1, ou [**Surveillez les structures \_ info \_ 2**](monitor-info-2.md) si le *niveau* est 2.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pMonitors*.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.

</dd> <dt>

*pcReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de structures retournées dans la mémoire tampon vers laquelle pointe *pMonitors*.

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
| Noms Unicode et ANSI<br/>   | **EnumMonitorsW** (Unicode) et **EnumMonitorsA** (ANSI)<br/>                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**\_Informations sur le moniteur \_ 1**](monitor-info-1.md)
</dt> <dt>

[**\_Informations sur le moniteur \_ 2**](monitor-info-2.md)
</dt> </dl>

 

