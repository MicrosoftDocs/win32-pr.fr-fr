---
description: La fonction SetPort définit l’état associé à un port d’imprimante.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: SetPort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034464"
---
# <a name="setport-function"></a>SetPort fonction)

La fonction **SetPort** définit l’état associé à un port d’imprimante.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du serveur d’impression auquel le port est connecté. Affectez la valeur **null** à ce paramètre si le port se trouve sur l’ordinateur local.

</dd> <dt>

*pPortName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du port d’imprimante.

</dd> <dt>

*dwLevel* \[ dans\]
</dt> <dd>

Spécifie le type de structure vers lequel pointe le paramètre *pPortInfo* .

Cette valeur doit être 3, ce qui correspond à une structure de données de [**port \_ informations \_ 3**](port-info-3.md) .

</dd> <dt>

*pPortInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure d' [**informations de port \_ \_ 3**](port-info-3.md) qui contient les informations d’état de port à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant de la fonction **SetPort** doit s’exécuter en tant qu’administrateur. En outre, si l’appelant est un moniteur de port ou un moniteur de langage, il doit appeler [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour arrêter l’emprunt d’identité avant d’appeler **SetPort**.

Tous les programmes qui appellent **SetPort** doivent disposer d’un accès serveur \_ \_ administrer l’accès au serveur auquel le port est connecté.

Lorsque vous définissez une valeur d’état de port d’imprimante avec la valeur de gravité \_ \_ erreur de type état du port \_ , le spouleur d’impression cesse d’envoyer des travaux au port. Le spouleur d’impression reprend l’envoi des travaux au port lorsque l’état du port est effacé par un autre appel à **SetPort**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **SetPortW** (Unicode) et **SetPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**\_Informations sur le port \_ 3**](port-info-3.md)
</dt> </dl>

 

