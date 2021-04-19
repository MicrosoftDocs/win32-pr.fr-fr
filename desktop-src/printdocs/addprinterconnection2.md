---
description: Ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel et spécifie les détails de connexion.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: AddPrinterConnection2, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520543"
---
# <a name="addprinterconnection2-function"></a>AddPrinterConnection2 fonction)

Ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel et spécifie les détails de connexion.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente dans laquelle la boîte de dialogue s’affiche si le système d’impression doit télécharger un pilote d’imprimante à partir du serveur d’impression pour cette connexion.

</dd> <dt>

*pszName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante se terminant par un caractère null qui spécifie le nom de l’imprimante à laquelle l’utilisateur actuel souhaite se connecter.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Version de la structure vers laquelle pointe *pConnectionInfo*. Actuellement, seul le niveau 1 est défini, de sorte que la valeur de *dwLevel* doit être 1.

</dd> <dt>

*pConnectionInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ informations de connexion d’imprimante \_ \_ 1**](printer-connection-info-1.md) . Pour plus d’informations sur ce paramètre, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Lorsque Windows Vista établit une connexion à une imprimante, il peut être nécessaire de copier les fichiers du pilote d’imprimante à partir du serveur auquel l’imprimante est attachée. Si l’utilisateur n’a pas l’autorisation de copier les fichiers vers l’emplacement approprié, la fonction **AddPrinterConnection2** échoue et [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ accès \_ refusé.

Si les fichiers de pilote d’imprimante doivent être copiés à partir du serveur d’impression mais ne peuvent pas être copiés en mode silencieux en raison des stratégies de groupe en vigueur et de la connexion à l’imprimante, \_ \_ aucune \_ interface utilisateur n’est définie dans *pConnectionInfo->dwFlags*, aucune boîte de dialogue ne s’affiche et l’appel échoue.

Si le pilote d’imprimante locale peut être utilisé pour afficher les travaux d’impression pour cette imprimante et que la version du pilote local ne doit pas correspondre à la version du pilote d’imprimante sur le serveur, définissez \_ incompatibilité de connexion d’imprimante \_ dans *PConnectionInfo->dwFlags* et affectez le pointeur à une variable de chaîne qui contient le chemin d’accès au pilote d’imprimante locale pour *pConnectionInfo->pszDriverName*.

Une connexion d’imprimante établie par l’appel de **AddPrinterConnection2** est énumérée lorsque [**EnumPrinters**](enumprinters.md) est appelé avec *dwType* défini sur la \_ connexion d’enum d’imprimante \_ .

La version ANSI de cette fonction, **AddPrinterConnection2A**, n’est pas prise en charge et retourne une **erreur \_ non \_ prise en charge**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddPrinterConnection2W** (Unicode)<br/>                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> </dl>

 

