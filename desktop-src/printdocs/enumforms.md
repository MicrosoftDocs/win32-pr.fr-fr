---
description: La fonction EnumForms énumère les formulaires pris en charge par l’imprimante spécifiée.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: EnumForms, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319097"
---
# <a name="enumforms-function"></a>EnumForms fonction)

La fonction **EnumForms** énumère les formulaires pris en charge par l’imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle les formulaires doivent être énumérés. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Spécifie la version de la structure vers laquelle *pForm* pointe. Cette valeur doit être 1 ou 2.

</dd> <dt>

*pForm* \[ à\]
</dt> <dd>

Pointeur vers une ou plusieurs structures d' [**informations de formulaire \_ \_ 1**](form-info-1.md) ou vers une ou plusieurs structures d' [**informations de formulaire \_ \_ 2**](form-info-2.md) . Toutes les structures ont le même niveau.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Spécifie la taille, en octets, de la mémoire tampon vers laquelle *pForm* pointe.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets copiés dans le tableau vers lequel *pForm* pointe (si l’opération réussit) ou le nombre d’octets requis (en cas d’échec, car *cbBuf* est trop petit).

</dd> <dt>

*pcReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de structures copiées dans le tableau vers lequel *pForm* pointe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Si l’appelant est distant et que le *niveau* est 2, la **valeur StringType** des structures d' [**informations de formulaire \_ \_ 2**](form-info-2.md) retournées est toujours la **chaîne \_ LANGPAIR**.

Dans Windows Vista, les données de formulaire retournées par **EnumForms** sont récupérées à partir d’un cache local lorsque *hPrinter* fait référence à un serveur d’impression distant ou à une imprimante hébergée par un serveur d’impression et qu’il existe au moins une connexion ouverte à une imprimante sur le serveur d’impression distant. Dans toutes les autres configurations, les données du formulaire sont interrogées à partir du serveur d’impression distant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **EnumFormsW** (Unicode) et **EnumFormsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**Informations de formulaire \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




