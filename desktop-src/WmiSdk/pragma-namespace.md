---
description: Demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que NamespacePath. Si le commutateur d’espace de noms MOF compiler-n et l' \# espace de noms pragma&\# 32 ; NamespacePath sont utilisés, la commande prend la priorité sur le commutateur.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: espace de noms pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: d3eea58c8e32ab8b1b851205b365b837194d0472a1c39017e2eb69dc3fe70a98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316825"
---
# <a name="pragma-namespace"></a>espace de noms pragma

La commande de préprocesseur d' **espace de noms pragma** demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que *NamespacePath*. Si le commutateur d’espace de noms MOF compiler **-n** et la commande **\# pragma namespace** *NamespacePath* sont utilisés, la commande prend la priorité sur le commutateur.

Les éléments suivants décrivent la syntaxe :


```mof
#pragma namespace ("[Namespace]")
```



L' *\[ espace de noms \]* est l’espace de noms spécifié.

Si vous ne spécifiez pas cette commande ou le commutateur de ligne de commande équivalent, le compilateur MOF utilise par \\ défaut l’espace de noms racine par défaut.

## <a name="remarks"></a>Remarques

Vous pouvez exiger que les applications et les scripts clients utilisent une connexion chiffrée pour l’authentification en ajoutant le qualificateur **RequiresEncryption** au fichier. MOF qui crée l’espace de noms. Vous pouvez également modifier un espace de noms existant en ajoutant cet attribut et recompiler le fichier MOF. Pour plus d’informations sur l’utilisation de **RequiresEncryption**, consultez la page [exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="examples"></a>Exemples

L’exemple suivant montre comment placer des classes ou des instances dans l' \\ espace de noms « test racine ».


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Qualificateurs WMI standard**](standard-wmi-qualifiers.md)
</dt> <dt>

[Commandes de préprocesseur](preprocessor-commands.md)
</dt> </dl>

 

 




