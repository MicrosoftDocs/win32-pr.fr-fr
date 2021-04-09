---
description: Affiche une boîte de dialogue qui contient les informations sur le signataire d’un message signé.
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: CryptUIDlgViewSignerInfo, fonction
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862310"
---
# <a name="cryptuidlgviewsignerinfo-function"></a>CryptUIDlgViewSignerInfo, fonction

\[La fonction **CryptUIDlgViewSignerInfo** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

La fonction **CryptUIDlgViewSignerInfo** affiche une boîte de dialogue qui contient les informations sur le signataire d’un message signé.

> [!Note]  
> Cette fonction n’est pas déclarée dans un fichier d’en-tête publié. Pour utiliser cette structure, déclarez-la dans le format exact indiqué.

## <a name="syntax"></a>Syntaxe


```C++
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pcvsi* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ \_ struct VIEWSIGNERINFO**](cryptui-viewsignerinfo-struct.md) qui contient les informations de signataire à afficher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne une valeur différente de zéro en cas de réussite et zéro en cas d’échec. Pour obtenir des informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Les codes d’erreur possibles retournés par [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) incluent, mais ne sont pas limités à, ce qui suit.



| Code de retour                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Un ou plusieurs arguments ne sont pas valides.<br/>  |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Un échec d’allocation de mémoire s’est produit.<br/> |

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                        |
| Fin de la prise en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                       |
| Bibliothèque<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>      |
| Noms Unicode et ANSI<br/>   | **CryptUIDlgViewSignerInfoW** (Unicode) et **CryptUIDlgViewSignerInfoA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIEWSIGNERINFO, \_ struct**](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
