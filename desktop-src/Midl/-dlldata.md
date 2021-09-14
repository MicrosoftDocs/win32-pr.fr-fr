---
title: commutateur/dlldata
description: Le commutateur/dlldata est utilisé pour spécifier le nom de fichier du fichier dlldata généré pour une DLL de proxy. Le nom de fichier par défaut dlldata. c est utilisé si le commutateur/dlldata n’est pas spécifié.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- MIDL du commutateur/dlldata
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093938"
---
# <a name="dlldata-switch"></a>commutateur/dlldata

Le commutateur **/dlldata** est utilisé pour spécifier le nom de fichier du fichier dlldata généré pour une dll de proxy. Le nom de fichier par défaut dlldata. c est utilisé si le commutateur **/dlldata** n’est pas spécifié.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*nom de fichier* 
</dt> <dd>

Nom du fichier source C que le compilateur MIDL génère pour la DLL du proxy.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fichier spécifié par le *nom de fichier* doit être lié à la dll du proxy. Le fichier dlldata contient des points d’entrée et des structures de données requis par la fabrique de classe pour la DLL du proxy. Ces structures de données spécifient les interfaces d’objet contenues dans la DLL du proxy. Le fichier dlldata spécifie également l’identificateur de classe de la fabrique de classe pour la DLL du proxy. Il s’agit toujours de l’UUID (IID) de la première interface du premier fichier proxy (par ordre alphabétique).

Le même fichier dlldata doit être spécifié lors de l’appel de MIDL sur tous les fichiers IDL qui seront placés dans une DLL proxy particulière. Le fichier dlldata est créé ou mis à jour lors de chaque compilation MIDL, générant de façon incrémentielle une liste des interfaces qui seront insérées dans la DLL du proxy.

## <a name="examples"></a>Exemples

**MIDL/dlldata données. c**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




