---
title: commutateur/h
description: L’option/h est fonctionnellement équivalente à l’option/Header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h Switch MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093934"
---
# <a name="h-switch"></a>commutateur/h

L’option **/h** est fonctionnellement équivalente à l’option [**/header**](-header.md) .

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*extension* 
</dt> <dd>

Spécifie un nom de fichier d’en-tête qui remplace le nom du fichier d’en-tête par défaut. Les noms de fichiers peuvent être mis en guillemets explicitement à l’aide de guillemets doubles (") pour empêcher l’interpréteur de commandes d’interpréter des caractères spéciaux.

</dd> </dl>

## <a name="remarks"></a>Notes

Le commutateur **/h** spécifie *filename* comme nom pour un fichier d’en-tête qui contient toutes les définitions contenues dans le fichier IDL, sans la syntaxe IDL. Ce fichier peut être utilisé en tant que fichier d’en-tête C ou C++.

## <a name="examples"></a>Exemples

**MIDL/h tlibhead. h nom_fichier. idl**

**MIDL/h « MIDL. h » NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> </dl>

 

 




